This project aims to develop a FIX service in WCF.NET that leverages a RabbitMQ broker.

There will be two WCF services:
  1. FIX Server Service
    * This will connect to remote FIX hosts
      * Fix-In as well as out
    * Will rely upon QuickFix
  1. FIX Client Abstract Service
    * RabbitMQ will route orders, lists and reports from a FIX Server Service to a FIX Client Service
      * Example usages are a trade blotter or a trading algorithm

The idea is that FIX messages will come into the FIX Server and be routed to a FIX client by a RabbitMQ broker.