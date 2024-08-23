# Must Use Plugins Base

**Plugin Name:** Must Use Plugins Base  
**Description:** A container plugin for all must-use plugins.  
**Requires at least:** WordPress 6.0  
**Requires PHP:** 7.0  
**Version:** 0.1.0  
**Author:** WordPress Villain  
**License:** GPL-2.0-or-later  
**License URI:** [https://www.gnu.org/licenses/gpl-2.0.html](https://www.gnu.org/licenses/gpl-2.0.html)  
**Text Domain:** mu-plugins-base  

## Overview

The Must Use Plugins Base is a foundational plugin designed to manage and load multiple must-use (MU) plugins in your WordPress environment. It acts as a container for various MU plugins, ensuring they are loaded automatically without requiring activation in the WordPress admin.

## Installation

1. **Download and Upload:**
   - Download the `mu-plugins-base` plugin files.
   - unzip if downloaded as zip
   - Upload the plugin files excluding dolder to your WordPress `wp-content/mu-plugins/` directory.

2. **Loading Plugins:**
   - Inside the `mu-plugins-base.php` file, you can require any additional MU plugins using the `require` statement.
   - Example:
     ```php
     require WPMU_PLUGIN_DIR . '/my-plugin/my-plugin.php';
     ```

3. **Example Usage:**
   - By default, the plugin is set to load a `line-block` plugin:
     ```php
     require WPMU_PLUGIN_DIR . '/line-block/line-block.php';
     ```
    **NB** if the plugin is missing comment this line out

## Usage

- **Adding MU Plugins:**  
  To add more MU plugins, simply add additional `require` statements within the `mu-plugins-base.php` file, pointing to the desired plugin's main file.

- **Managing MU Plugins:**  
  Since MU plugins are automatically loaded by WordPress, they do not appear in the standard plugins list and cannot be deactivated from the admin panel. You can manage these plugins by editing the `mu-plugins-base.php` file.

## Contributing

If you'd like to contribute to the development of the Must Use Plugins Base plugin, feel free to fork the repository, make your changes, and submit a pull request.

## License

This plugin is licensed under the GPL-2.0-or-later license. See the [LICENSE](https://www.gnu.org/licenses/gpl-2.0.html) file for more details.