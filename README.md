# This with Nginx

### Command Thin

__Start__
```
thin start -C config/thin.yml
```
__Restart__
```
thin restart -C config/thin.yml
```
__Stop__
```
thin stop -C config/thin.yml
```

### Rails Init to Deploy

__bundle__
```
bundle install --deployment --without development test
```
__secret key__
```
echo "export SECRET_KEY_BASE=$(rails secret RAILS_ENV=production)" >> ~/.bashrc
```
__precompile assets__
```
rails assets:precompile RAILS_ENV=production
```
