# Migrating from Previous Versions

Microgateway consists of main two distributions.

- Microgateway Toolkit : Used to build the Microgateway project and generate the Microgateway executable.
- Microgateway Runtime : Run the Microgateway executable built with the toolkit applying the requried configurations.

Each Microgateway version has it's own toolkit and runtime. And the Migrogateway executable which is built from specific toolkit version is specific only to that Microgateway version.

If you want to use the same Microgateway project (built from an older Microgateway toolkit version) with Microgateway 3.2.0, follow the steps below.

1. Build the initial Microgateway Project by using the Microgateway Toolkit 3.2.0.
2. Copy the configuration from `<OLD_MGW_RUNTIME_HOME>/conf/micro-gw.conf` and apply them in `<MGW_3.2.0_RUNTIME_HOME>/conf/micro-gw.conf` file. Refer to the [micro-gw.conf](/reference/configurations/micro-gw.conf/) and do any changes to the old configurations.
3. If you use API Manager along with Microgateway for key validation, throttling etc, follow the [Configuration for WSO2 API Manager](/install-and-setup/configuration-for-wso2-api-manager/) document and do the relevant configuration in Microgateway 3.2.0 runtime.

    !!! note
        If you have implemented any custom ballerina extensions for Microgateway previously, you will have to re-write them with the ballerina version 1.2.7.
