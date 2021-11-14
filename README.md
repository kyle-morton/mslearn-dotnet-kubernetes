### KM Useful Kubernetes Commands
-  kubectl apply -f backend-deploy.yml (KB creates a new pod instance using the yml file. NOTE: Kubernetes is resilient and keeps the pod state exactly as it is in the yml file - if a pod fails, it will create a new one to takes it's place).

- kubectl get pods (displays all pod instances running [all your running containers] including those that spinning up or terminating)

- kubectl scale --replicas=5 deployment/pizzabackend (KB will create more pods of the given pod. NOTE: We're calling out the deployment/ name instead of just pizzabackend)

- kubectl delete pod pizzafrontend-7644df9875-8qnsn (deletes a given pod instance. NOTE: this must match the name given under 'kubetcl get pods' command)

- kubectl get deployments --all-namespaces (gets names of all deployed containers. NOTE: These are the deployments themselves which is what you'll need to delete if you want to delete the pod and have it NOT restart)

- kubectl delete -n default deployment pizzabackend (fully deletes the deployment so it will not be restarted)

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# Legal Notices

Microsoft and any contributors grant you a license to the Microsoft documentation and other content
in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode),
see the [LICENSE](LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the
[LICENSE-CODE](LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation
may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries.
The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks.
Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all other rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.
