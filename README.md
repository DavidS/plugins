## Puppet Plugins
This is a community curated list of plugins and tools for Puppet. Tools and
plugins are defined in `_data/plugins.json`. Tools without plugins are going to
be listed in the table under the `Tools` header. Tools with plugins will have
their own header and table listing the plugins defined for that tool.

### `plugins.json` format
There's a single hash in `plugins.json` with a `tools` key. The `tools` array
contains definitions for different `tools` that may or may not have plugins. A
tool that doesn't have any plugins will be listed in the table under the Tools
header while a tool that does have plugins will have its own header and a table
listing all plugins in the tool's `plugins` array.

#### Tool Schema:
| Key            | Value Data Type | Required or Optional |
| -------------- | --------------- | -------------------- |
| `name`         | String          | Required             |
| `display_name` | String          | Required             |
| `url`          | String          | Required             |
| `description`  | String          | Required             |
| `plugins`      | Array           | Optional             |

#### Plugin Schema:
| Key            | Value Data Type | Required or Optional |
| -------------- | --------------- | -------------------- |
| `name`         | String          | Required             |
| `url`          | String          | Required             |
| `description`  | String          | Required             |

### What's a tool vs. a plugin?
The difference can be kind of fluid, so I figured it would be helpful to define
plugin and tool.

A *plugin* cannot generally be used independent of another tool. Plugins add
functionality to another tool. An example of a plugin is `beaker-libvirt`
because it enables libvirt as a hypervisor in Beaker.

A *tool* can generally be used independent of another specific tool or it is a
tool that has plugins itself. An example of a tool is `rspec-puppet` because it
has plugins. Another example of a tool is `modulesync` because it can be used
independent of another tool.
