# nat_ctl
nat_ctl is a tool designed for simplifing the job of nat and port forwarding when using iptables. This tools is designed for proxmox, it does not rely on iptables daemon for reloading the rules. Therefore, you need to add post-up and post-down manually after your network interfaces configuration in order to make the rules always loaded.

## Usage
	
	nat_ctl load
	nat_ctl unload
	nat_ctl reload
	nat_ctl list
	nat_ctl list_nat
	nat_ctl list_forward
	nat_ctl add_nat <subnet> <out_interface>
	nat_ctl del_nat <subnet> <out_interface>
	nat_ctl add_forward <in_interface> <proto> <port> <to_port>
	nat_ctl del_forward <in_interface> <proto> <port> <to_port>

## Example
	nat_ctl add_nat 10.10.10.0/24 eth0
	nat_ctl add_forward eth0 tcp 80 10.10.10.1:80

## License

Copyright year [guyusoftware]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

[guyusoftware]: https://www.guyusoftware.com/