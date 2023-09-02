# Denodo
Technical document to use and manage Denodo


# How to set limit retruned row

You can set the limit of rows return by using Resource Manager. You first need to set the plan by speciiying the outcome of the plan. Let's say 100K row return. Then you specify the rule to match the plan. 

To forbid query to run after office hours on certain application.

`user_agent='reports application' AND gethour(CURRENT_TIMESTAMP) >= 8 AND gethour(CURRENT_TIMESTAMP) < 23`

User_agent field can be setup in the upstream application by using the connection string of the JDBC or ODBC. For detail refer to the link 
[Setting up User Agent](https://community.denodo.com/docs/html/browse/7.0/vdp/administration/monitoring_the_virtual_dataport_server/monitoring_with_a_java_management_extensions_jmx_agent/setting_the_user_agent_of_an_application#setting-the-user-agent-of-an-application)
You can specify the condition programmatically by evaluate the fields. Refer to [here](https://community.denodo.com/docs/html/browse/7.0/vdp/administration/appendix/resource_manager_available_fields_to_evaluate_a_rule/resource_manager_available_fields_to_evaluate_a_rule#resource-manager-available-fields-to-evaluate-a-rule) for avaialbe field to evaluate.
