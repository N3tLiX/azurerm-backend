# azurerm-backend

Create an Azure Storage Account to store the Terraform stage file (tfstage).

## Usage AzuerCLI
```sh
$ # Export the Azure Subscription Login data (Linux/MacOS)
$ export ARM_SUBSCRIPTION_ID=""
$ export ARM_CLIENT_ID=""
$ export ARM_CLIENT_SECRET=""
$ export ARM_TENANT_ID=""
$ # Export the Backend Storage Variables (Linux/MacOs)
$ # Create the Storage Backend
$ az login --service-principal --username $ARM_CLIENT_ID --password $ARM_CLIENT_SECRET --tenant $ARM_TENANT_ID
$ az account set --subscription $ARM_SUBSCRIPTION_ID
$ source azurerm.sh \
    TF_STATE_BLOB_ACCOUNT_RESOURCE_GROUP="" \
    TF_STATE_BLOB_ACCOUT_LOCATION="" \
    TF_STATE_BLOB_ACCOUNT_NAME="" \
    TF_STATE_BLOB_ACCOUNT_SKU="" \
    TF_STATE_BLOB_CONTAINER_NAME="" \
    TF_STATE_BLOB_FILE=""
```

Find an example, and more documentation at https://github.com/n3tlix/examples
## Authors

Originally created by [Patrick Hayo](http://github.com/adminph-de)

## License

[MIT](LICENSE)