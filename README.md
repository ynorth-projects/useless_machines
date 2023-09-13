![An animation of a "useless machine" turning itself off.](https://media.tenor.com/ZHRdOnvwCHgAAAAC/funny.gif)

# useless_machines
Modules that turn themselves off.

> A useless machine or useless box is a device whose only function is to turn itself off.
>
> -- [Wikipedia](https://en.wikipedia.org/wiki/Useless_machine)

These modules exist solely to replace modules that have been [accidentally removed from your Drupal site](https://www.drupal.org/docs/updating-drupal/troubleshooting-database-updates#s-manually-removing-a-missing-theme-or-module). Upon `updb` they disable themselves, automagically removing the missing module from your configuration.

## But... no... 😢

### I still want to use a few of these modules

If you are using a package that requires `useless_machines` (like [YMCA Website Services](https://github.com/YCloudYUSA/yusaopeny/blob/main/composer.json#L159)) but you still need one of these modules:

- fork this repo
- remove the line of any module you want to use from the `conflict` section in `composer.json`
- remove the corresponding directory
- swap out your fork by adding a new [repository](https://getcomposer.org/doc/04-schema.md#repositories) entry in your root `composer.json` and following these steps for [patching and forking](https://www.lullabot.com/articles/patch-less-composer-workflow-drupal-using-forks#:~:text=The%20Steps%20for%20Patching%20and%20Forking).

### I don't want any of these useless machines 

Fret not, we've got [a branch for you](https://github.com/YCloudYUSA/useless_machines/tree/allow-contrib). 

```
composer require ycloudyusa/useless_machines:"dev-allow-contrib as dev-main"
```
