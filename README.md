<img width="1440" alt="image" src="https://github.com/user-attachments/assets/3e7e643f-e8e5-448b-b395-68c87cfaec03" />
<img width="1360" alt="image" src="https://github.com/user-attachments/assets/4d32db9c-b0a2-4071-97f4-257306236587" />
<img width="1375" alt="image" src="https://github.com/user-attachments/assets/e66d5319-8132-4231-8b30-89233f65b218" />

<img width="997" alt="image" src="https://github.com/user-attachments/assets/ec49d4b7-1aad-4dcb-80ca-5310a570833a" />
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/2b70285b-5413-4071-9525-ce3a29b4f88e" />
<img width="370" alt="image" src="https://github.com/user-attachments/assets/cadd84d7-5448-4731-b440-bd36edfd9a27" />


Past the folder in your production repo, and update the config_sync_directory and add DRUPAL_ENV to see if it's a production env or dev.
```php
$settings['config_sync_directory'] = 'sites/default/files/config_mXIfz1dmgBfSa28m8yZ5UXMHVvNI36a1ocM3TqL_jUqSTouexaeTh4yADe-BsVMLigTq8OyMmg/sync';

if (getenv('DRUPAL_ENV') === 'production') {
  $config['config_split.config_split.development_configuration']['status'] = FALSE;
}
```
