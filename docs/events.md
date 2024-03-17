# Events

### BeforeInitialization

> Min\FileManager\Events\BeforeInitialization

Example:

```php
\Event::listen('Min\FileManager\Events\BeforeInitialization',
    function ($event) {

    }
);
```

### DiskSelected

> Min\FileManager\Events\DiskSelected

Example:

```php
\Event::listen('Min\FileManager\Events\DiskSelected',
    function ($event) {
        \Log::info('DiskSelected:', [$event->disk()]);
    }
);
```

### FilesUploading

> Min\FileManager\Events\FilesUploading

```php
\Event::listen('Min\FileManager\Events\FilesUploading',
    function ($event) {
        \Log::info('FilesUploading:', [
            $event->disk(),
            $event->path(),
            $event->files(),
            $event->overwrite(),
        ]);
    }
);
```

### FilesUploaded

> Min\FileManager\Events\FilesUploaded

```php
\Event::listen('Min\FileManager\Events\FilesUploaded',
    function ($event) {
        \Log::info('FilesUploaded:', [
            $event->disk(),
            $event->path(),
            $event->files(),
            $event->overwrite(),
        ]);
    }
);
```

### Deleting

> Min\FileManager\Events\Deleting

```php
\Event::listen('Min\FileManager\Events\Deleting',
    function ($event) {
        \Log::info('Deleting:', [
            $event->disk(),
            $event->items(),
        ]);
    }
);
```

### Deleted

> Min\FileManager\Events\Deleted

```php
\Event::listen('Min\FileManager\Events\Deleted',
    function ($event) {
        \Log::info('Deleted:', [
            $event->disk(),
            $event->items(),
        ]);
    }
);
```

### Paste

> Min\FileManager\Events\Paste

```php
\Event::listen('Min\FileManager\Events\Paste',
    function ($event) {
        \Log::info('Paste:', [
            $event->disk(),
            $event->path(),
            $event->clipboard(),
        ]);
    }
);
```

### Rename

> Min\FileManager\Events\Rename

```php
\Event::listen('Min\FileManager\Events\Rename',
    function ($event) {
        \Log::info('Rename:', [
            $event->disk(),
            $event->newName(),
            $event->oldName(),
            $event->type(), // 'file' or 'dir'
        ]);
    }
);
```

### Download

> Min\FileManager\Events\Download

```php
\Event::listen('Min\FileManager\Events\Download',
    function ($event) {
        \Log::info('Download:', [
            $event->disk(),
            $event->path(),
        ]);
    }
);
```

_When using a text editor, the file you are editing is also downloaded! And this event is triggered!_

### DirectoryCreating

> Min\FileManager\Events\DirectoryCreating

```php
\Event::listen('Min\FileManager\Events\DirectoryCreating',
    function ($event) {
        \Log::info('DirectoryCreating:', [
            $event->disk(),
            $event->path(),
            $event->name(),
        ]);
    }
);
```

### DirectoryCreated

> Min\FileManager\Events\DirectoryCreated

```php
\Event::listen('Min\FileManager\Events\DirectoryCreated',
    function ($event) {
        \Log::info('DirectoryCreated:', [
            $event->disk(),
            $event->path(),
            $event->name(),
        ]);
    }
);
```

### FileCreating

> Min\FileManager\Events\FileCreating

```php
\Event::listen('Min\FileManager\Events\FileCreating',
    function ($event) {
        \Log::info('FileCreating:', [
            $event->disk(),
            $event->path(),
            $event->name(),
        ]);
    }
);
```

### FileCreated

> Min\FileManager\Events\FileCreated

```php
\Event::listen('Min\FileManager\Events\FileCreated',
    function ($event) {
        \Log::info('FileCreated:', [
            $event->disk(),
            $event->path(),
            $event->name(),
        ]);
    }
);
```

### FileUpdate

> Min\FileManager\Events\FileUpdate

```php
\Event::listen('Min\FileManager\Events\FileUpdate',
    function ($event) {
        \Log::info('FileUpdate:', [
            $event->disk(),
            $event->path(),
        ]);
    }
);
```

### Zip

> Min\FileManager\Events\Zip

```php
\Event::listen('Min\FileManager\Events\Zip',
    function ($event) {
        \Log::info('Zip:', [
            $event->disk(),
            $event->path(),
            $event->name(),
            $event->elements(),
        ]);
    }
);
```

### ZipCreated

> Min\FileManager\Events\ZipCreated

```php
\Event::listen('Min\FileManager\Events\ZipCreated',
    function ($event) {
        \Log::info('ZipCreated:', [
            $event->disk(),
            $event->path(),
            $event->name(),
            $event->elements(),
        ]);
    }
);
```

### ZipFailed

> Min\FileManager\Events\ZipCreated

```php
\Event::listen('Min\FileManager\Events\ZipFailed',
    function ($event) {
        \Log::info('ZipFailed:', [
            $event->disk(),
            $event->path(),
            $event->name(),
            $event->elements(),
        ]);
    }
);
```

### Unzip

> Min\FileManager\Events\Unzip

```php
\Event::listen('Min\FileManager\Events\Unzip',
    function ($event) {
        \Log::info('Unzip:', [
            $event->disk(),
            $event->path(),
            $event->folder(),
        ]);
    }
);
```

### UnzipCreated

> Min\FileManager\Events\UnzipCreated

```php
\Event::listen('Min\FileManager\Events\UnzipCreated',
    function ($event) {
        \Log::info('UnzipCreated:', [
            $event->disk(),
            $event->path(),
            $event->folder(),
        ]);
    }
);
```

### UnzipFailed

> Min\FileManager\Events\UnzipFailed

```php
\Event::listen('Min\FileManager\Events\UnzipFailed',
    function ($event) {
        \Log::info('UnzipFailed:', [
            $event->disk(),
            $event->path(),
            $event->folder(),
        ]);
    }
);
```
