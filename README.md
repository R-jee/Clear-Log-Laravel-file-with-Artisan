# Clear-Log-Laravel-file-with-Artisan

**Here's a reusable artisan command that will save you time and effort :)**

```
  Artisan::command('logs:clear', function() {

      exec('rm -f ' . storage_path('logs/*.log'));

      exec('rm -f ' . base_path('*.log'));

      $this->comment('Logs have been cleared!');

  })->describe('Clear log files');
```
- Drop this in **routes/console.php** then just **run php artisan logs:clear**
