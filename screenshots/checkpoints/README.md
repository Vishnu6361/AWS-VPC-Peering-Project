# Milestone Verification Checkpoint Screenshots

When performing live verification in AWS Management Console, save your screenshots to this folder using the exact filenames below. The report generator script (`report_generator/generate_report.py`) reads these files to compile your submission report (`Vishnu_C_N_EWB_VPC_Peering.pdf`).

| Filename | Description / Console Location |
|---|---|
| `01_key_pair_created.png` | EC2 Key Pairs console showing `ewb-lab` created. |
| `02_vpc_a_created.png` | VPC console showing `ewb-vpc-a` with CIDR `10.10.0.0/16`. |
| `03_subnets_vpc_a.png` | Subnets console showing `ewb-a-public` (`10.10.1.0/24`) and `ewb-a-private` (`10.10.2.0/24`). |
| `04_igw_attached.png` | Internet Gateways console showing `ewb-igw-a` attached to `ewb-vpc-a`. |
| `05_route_table_vpc_a_public.png` | Route Tables console showing `ewb-rt-a-public` with route `0.0.0.0/0 -> ewb-igw-a`. |
| `06_route_table_vpc_a_private.png` | Route Tables console showing `ewb-rt-a-private` associated with `ewb-a-private`. |
| `07_vpc_b_created.png` | VPC console showing `ewb-vpc-b` (`10.20.0.0/16`) and `ewb-b-private` (`10.20.1.0/24`). |
| `08_route_table_vpc_b_private.png` | Route Tables console showing `ewb-rt-b-private` associated with `ewb-b-private`. |
| `09_security_group_bastion.png` | Security Groups console showing `ewb-sg-bastion` allowing SSH port 22 from Admin `/32`. |
| `10_security_group_app_a.png` | Security Groups console showing `ewb-sg-app-a` with SSH from Bastion (`10.10.1.10/32`) and ICMP from App-B (`10.20.1.10/32`). |
| `11_security_group_app_b.png` | Security Groups console showing `ewb-sg-app-b` with SSH from Bastion (`10.10.1.10/32`) and ICMP from App-A (`10.10.2.10/32`). |
| `12_ec2_instances_running.png` | EC2 Instances console showing all 3 instances (`ewb-bastion`, `ewb-app-a`, `ewb-app-b`) running and passing status checks. |
| `13_bastion_public_ip.png` | EC2 instance details showing `ewb-bastion` assigned a public IPv4, and zero public IP on private workloads. |
| `14_vpc_peering_active.png` | Peering Connections console showing `ewb-a-b-peer` in **Active** status. |
| `15_peering_routes_configured.png` | Route Tables console showing static peering routes (`10.20.0.0/16 -> pcx` in VPC A, `10.10.0.0/16 -> pcx` in VPC B). |
| `16_controlled_failure_icmp_rule_deleted.png` | Security group console showing ICMP Echo rule deleted from `ewb-sg-app-b` (proving firewall enforcement). |
| `17_peering_deletion.png` | VPC Peering console showing `ewb-a-b-peer` deleted and routes purged. |
| `18_ec2_instances_terminated.png` | EC2 Instances console showing all 3 instances terminated. |

