# Day 3: Work with configuration & features

### Practice Configuration Sync

<img width="1431" alt="image" src="https://github.com/user-attachments/assets/fd68bede-078a-4a38-887d-6cafbfa9459b" /><img width="1440" alt="image" src="https://github.com/user-attachments/assets/3e7e643f-e8e5-448b-b395-68c87cfaec03" />
<img width="1360" alt="image" src="https://github.com/user-attachments/assets/4d32db9c-b0a2-4071-97f4-257306236587" />
<img width="1375" alt="image" src="https://github.com/user-attachments/assets/e66d5319-8132-4231-8b30-89233f65b218" />

<img width="997" alt="image" src="https://github.com/user-attachments/assets/ec49d4b7-1aad-4dcb-80ca-5310a570833a" />
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/2b70285b-5413-4071-9525-ce3a29b4f88e" />
<img width="370" alt="image" src="https://github.com/user-attachments/assets/cadd84d7-5448-4731-b440-bd36edfd9a27" />


Past the folder in your production repo, and update the config_sync_directory and add DRUPAL_ENV to see if it's a production env or dev. then add in your settings.php :

```php
$settings['config_sync_directory'] = 'sites/default/files/config_mXIfz1dmgBfSa28m8yZ5UXMHVvNI36a1ocM3TqL_jUqSTouexaeTh4yADe-BsVMLigTq8OyMmg/sync';

if (getenv('DRUPAL_ENV') === 'production') {
  $config['config_split.config_split.development_configuration']['status'] = FALSE;
}
```

---

### Practice Features

i added a new feature called Blog :

<img width="1438" alt="image" src="https://github.com/user-attachments/assets/93fc9ec8-5e21-493a-8814-1ecdaa350bce" />

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/8ca45714-56eb-46e3-ad36-b2cf68619b32" />

<img width="433" alt="image" src="https://github.com/user-attachments/assets/cb0fb203-bdf7-4052-a946-2b86c09cb470" />

```bash
./vendor/bin/drush en blog
```

<img width="868" alt="image" src="https://github.com/user-attachments/assets/36a51617-7cca-4459-81db-0fd3880d7af2" />

Blog content type is added successfully :

<img width="1439" alt="image" src="https://github.com/user-attachments/assets/0efa4034-c938-44ef-b777-983715b6eddd" />


- **Was their any conflicts that needed to be resolved ?**

I changed the content type name in production, then added a new field, Subtitle, to the content type in development. I copied the feature back to production (the feature detected that something had changed).

<img width="1431" alt="image" src="https://github.com/user-attachments/assets/654754f0-3571-4655-93fc-73abbbb76071" />


<img width="1351" alt="image" src="https://github.com/user-attachments/assets/9fa9d40e-c478-4d1e-b710-d25f7ed36f6f" />


✅ I didn’t encounter any issues. When I uninstalled and reinstalled the Blog module, it renamed the content type back to Blog and added the new Subtitle field.

<img width="1435" alt="image" src="https://github.com/user-attachments/assets/95e1aedb-9479-4394-9873-2e8f3b836033" />

