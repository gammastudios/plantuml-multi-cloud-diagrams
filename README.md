# plantuml-multi-cloud-diagrams
PlantUML template library to render Multi-Cloud [C4 diagrams](https://c4model.com/) using major public cloud provider icons (AWS, Azure and GCP).

## Usage
Add the following `include` statements after the `@startuml` label:

    !define C4Puml https://raw.githubusercontent.com/RicardoNiepel/C4-PlantUML/master
    !define GCPPuml https://raw.githubusercontent.com/gamma-data/GCP-C4-PlantUML/master/templates
    !define AzurePuml https://raw.githubusercontent.com/RicardoNiepel/Azure-PlantUML/master/dist
    !define AWSPuml https://raw.githubusercontent.com/awslabs/aws-icons-for-plantuml/main/dist

    !includeurl C4Puml/C4_Context.puml
    !includeurl C4Puml/C4_Component.puml
    !includeurl C4Puml/C4_Container.puml
    !includeurl GCPPuml/GCPCommon.puml
    !includeurl AzurePuml/AzureCommon.puml
    !includeurl AWSPuml/AWSCommon.puml

Then add references to the required services from different providers...    

    ' GCP Resources
    !includeurl GCPPuml/Networking/CloudVPN.puml
    !includeurl GCPPuml/DataAnalytics/BigQuery.puml
    !includeurl GCPPuml/Compute/ComputeEngine.puml

    ' Azure Resources
    !includeurl AzurePuml/Networking/AzureDNS.puml
    !includeurl AzurePuml/Networking/AzureVPNGateway.puml
    !includeurl AzurePuml/Compute/AzureVirtualMachine.puml
## Multi Cloud C4 Example
![Example Multi Cloud Component Diagram](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/gamma-data/GCP-C4-PlantUML/master/examples/gcp-C4-example.puml)
