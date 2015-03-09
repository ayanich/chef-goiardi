# goiardi-cookbook

Installs and configures [Goiardi](http://goiardi.gl).

## Supported Platforms

* Ubuntu 12.04
* Ubuntu 14.04

## Attributes

<table>
  <tr>
    <td><tt>['goiardi']['version']</tt></td>
    <td>String</td>
    <td>Goiardi version to install</td>
    <td><tt>0.9.0</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['os']</tt></td>
    <td>String</td>
    <td>Target OS (used to build download URL)</td>
    <td><tt>node['os'].downcase</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['arch']</tt></td>
    <td>String</td>
    <td>Target arch (used to build download URL)</td>
    <td><tt>amd64</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['bin']</tt></td>
    <td>String</td>
    <td>Goiardi binary download URL</td>
    <td><tt>https://github.com/ctdk/goiardi/releases ...</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['confdir']</tt></td>
    <td>String</td>
    <td>Goiardi configuration directory</td>
    <td><tt>/etc/goiardi</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['config']</tt></td>
    <td>String</td>
    <td>Goiardi configuration file</td>
    <td><tt>/etc/goiardi/goiardi.conf</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['rundir']</tt></td>
    <td>String</td>
    <td>Goiardi state directory</td>
    <td><tt>/var/run/goiardi</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['lfsdir']</tt></td>
    <td>String</td>
    <td>Goiardi upload directory</td>
    <td><tt>/var/run/goiardi/file_checksums</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['ipaddress']</tt></td>
    <td>String</td>
    <td>Address to listen on</td>
    <td><tt>0.0.0.0</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['port']</tt></td>
    <td>String</td>
    <td>Port to listen on</td>
    <td><tt>4545</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['hostname']</tt></td>
    <td>String</td>
    <td>Hostname to use in served URLs</td>
    <td><tt>node['hostname']</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['freezeint']</tt></td>
    <td>String</td>
    <td>Interval in seconds to freeze in-memory data structures to disk</td>
    <td><tt>10</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['objsize']</tt></td>
    <td>String</td>
    <td>Maximum object size in bytes for the file store</td>
    <td><tt>10485760</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['jsonsize']</tt></td>
    <td>String</td>
    <td>Maximum size for a JSON request from the client</td>
    <td><tt>1000000</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['logfile']</tt></td>
    <td>String</td>
    <td>Optional file to log to</td>
    <td><tt>nil</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['syslog']</tt></td>
    <td>Boolean</td>
    <td>Optional syslog support</td>
    <td><tt>true</tt></td>
  </tr>
  <tr>
    <td><tt>['goiardi']['loglevel']</tt></td>
    <td>String</td>
    <td>Control log verbosity</td>
    <td><tt>critical</tt></td>
  </tr>
</table>

## Usage

### goiardi::default

Include `goiardi` in your node's `run_list`:

```json
{
  "run_list": [
    "recipe[goiardi::default]"
  ]
}
```

## License and Authors

Author:: Matt Whiteley (<mwhiteley@fastly.com>)
