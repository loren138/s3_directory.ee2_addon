## S3 Directory

This simple fieldtype allows you to select an existing file from an Amazon S3 bucket, and then output useful info about it. This is not for uploading, editing, or deleting files in your S3 buckets. It's essentially a simple file browser.

### Template Tags

`{my_field}` or `{my_feld:url}` - the full URL to your file. Note that your file must have public-readable permissions for this URL to be useful. Add `ssl="y"` to obtain an SSL-hosted URL.

`{my_field:name}` - the name of your file.

`{my_field:size}` - your file's size in bytes.

`{my_field:human_size}` - human-readable file size, in KB, MB, GB, or TB respectively.

`{my_field:date}` and `{my_field:gmt_date}` - the last-modified date of your file. Accepts a standard EE `format` parameter for date formatting.

This fieldtype uses Donovan Schönknecht's [Amazon S3 PHP Class](https://github.com/tpyo/amazon-s3-php-class/).

### Change Log
__v1.0.1__
* Feature: Allow Cloudfront URLs
