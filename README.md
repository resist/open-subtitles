This is a temporary fork of [kickasssubtitles/open-subtitles](https://github.com/kickasssubtitles/open-subtitles) to allow the legacy [sorfi.org](https://sorfi.org) to run in a modern environment (Symfony ^8.0, PHP ^8.4). Original README below.

---

# PHP client for OpenSubtitles API

## Usage

```php
$client = KickAssSubtitles\OpenSubtitles\OpenSubtitlesClient::create([
    'username'  => 'USERNAME',
    'password'  => 'PASSWORD',
    'useragent' => 'USERAGENT',
]);

$response = $client->searchSubtitles([
    [
        'sublanguageid' => 'pol',
        'moviehash' => '163ce22b6261f50a',
        'moviebytesize' => '2094235131',
    ]
]);

var_dump($response->toArray());
```
