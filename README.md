# Bashed Lemon

A bash + lemonbar setup for printing useful information about system activity. Created for personal use.

## Dependencies

Here are listed the most notable direct dependencies for the current setup, which might not be available by default on all expected systems or their version number is an expected concern. Dependencies that are NOT module specific have been **bolded**.

- **Bash (4.0 or greater)**
- **lemonbar-xft**
- **Font Awesome 5 font**
- **Hack font**
- acpi
- amixer
- bspc
- mpc
- xrandr
- xset

## Development

### Global variables

User configuration file and module files are sourced to the main file during execution. Global variables should be avoided where possible and described naming conventions should followed when they are necessary. Module specific global variables should also be prefixed with the module name, e.g. in case of module "foo" and a necessary misc global variable "bar" the name would be `GLOBAL_foo_bar`.

**Global variable name prefixes**

- **DEFAULT\_** - define default settings
- **GLOBAL\_** - misc global variables
- **MODULES\_** - define modules to be used
- **USER\_** - overwrite default settings, read from user configuration file

**Module (bash function) name prefixes**

- **mod\_** - can be called in a main module loop
- **submod\_** - should only be called by a corresponding module

