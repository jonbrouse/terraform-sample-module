# VPC Module

This module is called within the `infrastructure` repository to create a new AWS VPC.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| availability_zones | The AWS availability zones in which subnets will be created | string | `<list>` | no |
| aws_account | The name of the AWS account in which the VPC is being created | string | - | yes |
| aws_region | The name of the AWS region in which the VPC will be created | string | - | yes |
| aws_region_shortnames |  | string | `<map>` | no |
| enable_dns_hostnames | True to enable DNS hostnames in the VPC | string | `true` | no |
| enable_dns_support | True to enable private DNS within the VPC | string | `true` | no |
| environment_name | Name of the enviornment the VPC belongs to | string | - | yes |
| map_public_ip_on_launch | True to auto-assign a public IP on launch | string | `true` | no |
| private_propagating_vgws | A list of VGWs the private route table should propagate. | string | `<list>` | no |
| private_subnets |  | string | `<list>` | no |
| public_propagating_vgws | A list of VGWs the public route table should propagate. | string | `<list>` | no |
| public_subnets |  | string | `<list>` | no |
| vpc_cidr | Define the VPC CIDR block | string | - | yes |
| vpc_name | The desired name of the VPC being created | string | - | yes |

## Outputs

| Name | Description |
|------|-------------|
| aws_region_shortname | The AWS region's shortname used when naming resources. i.e. "use1" |
| flow_log_cloudwatch_log_group_arn |  |
| flow_log_cloudwatch_log_group_name |  |
| internet_gateway_id |  |
| nat_eips |  |
| private_route_table_ids |  |
| private_subnet_cidr_blocks |  |
| private_subnet_ids |  |
| public_route_table_ids |  |
| public_subnet_cidr_blocks |  |
| public_subnet_ids |  |
| vpc_cidr_block |  |
| vpc_id |  |

To instantiate the module, create a root module with the following files:
