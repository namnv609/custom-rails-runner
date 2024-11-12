# Custom Rails Runner

Supports showing ActiveRecord logs and sandbox mode.

# Usage

* Copy the script to `<path/to/rails/project>/bin` (e.g., `/home/acme/rails-prj/bin/runner`).
* Update the path to the Rails runner in the shebang (first line of the script). E.g., `#!/usr/bin/env /home/acme/rails-prj/bin/rails runner`.
* Run with `bin/runner <path to Ruby script>`.

## Options

By default, the script will show ActiveRecord logs and enable sandbox mode. You can disable this by adding an option when running the script or by adding an option to the first line of the script.

### CLI options

* `-a`: Turn off ActiveRecord logs. E.g., `bin/runner path/to/script.rb -a`.
* `-s`: Disable sandbox mode. E.g., `bin/runner path/to/script.rb -s`.

You can combine turning off logs and disabling sandbox mode by passing both options, like `-as`.

### Inline script

You can also turn off logs and disable sandbox mode by adding options to the first two lines of the script like this:

```rb
# no-ar-log
# no-sandbox

def greeting(name)
  puts "Hello, #{name}"
end
```
