## Network > Colocation Gateway > Console User Guide

This guide describes how to use the **Colocation Gateway** service from the console.

## Colocation Gateway

### Create a Colocation Gateway

To create a **colocation gateway**, use the following steps:

> [Note] Only VPCs pre-registered in NHN Cloud Zone can communicate with the on-premises network. For VPCs that are required to communicate with the on-premises network, make sure that you contact through [1:1 inquiry](https://www.toast.com/kr/support/inquiry) of the NHN Cloud Customer Center before creating a colocation gateway.<br>
> [Caution] If you create a colocation gateway by selecting a VPC that is not pre-registered in the NHN Cloud Zone, communication with the on-premises network is not possible, and only communication with other VPCs connected to the same NHN Cloud Zone is available.

1. Go to **Network > Colocation Gateway**.
2. If you click **Create Colocation Gateway**, the screen for creation appears.
3. Enter the **Name** to use for the **colocation gateway**.
4. Choose a **VPC**.<br>
   The selected VPC is connected to the NHN Cloud Zone.<br>
   A VPC can be connected to only one NHN Cloud Zone.
5. Select **NHN Cloud Zone**.
6. Click **Confirm**.

### View a Colocation Gateway

You can view the created colocation gateway on the **Network > Colocation Gateway** page. If you select a colocation gateway, the colocation gateway information appears at the bottom.

### Modify a Colocation Gateway

A colocation gateway can be modified as follows. You can only change **Name** and **Description**.

1. Go to **Network > Colocation Gateway**.
2. Click **Change Colocation Gateway** and change items on the change screen.

### Delete a Colocation Gateway

To delete a colocation gateway, select the colocation gateway you want to delete in the **Network > Colocation Gateway** page and click the Delete Colocation Gateway button.

## Use a Colocation Gateway

Communication between VPCs connected to the same NHN Cloud Zone is routed by the NHN Cloud Zone by the longest prefix matching rule using the CIDR value configured in the VPC when creating a colocation gateway. When CIDRs are overlapped, only one random VPC among the overlapped targets is used for communication.

### Configure a Route for a Colocation Gateway

1. Go to **Network > VPC > Routing**.
2. Choose the **Routing Table** for the **VPC** where you created the **colocation gateway**.
3. Select the **Route** tab from the **Routing Table** information displayed at the bottom.
4. Click **Create Route** to display the creation screen.
5. Enter the **Target CIDR**.<br>
   On-premises network CIDR or CIDR of another VPC connected to the same NHN Cloud Zone
6. Under **Gateway**, select **TRANSIT_GATEWAY** from the **Select Gateway** list.<br>
   > [Note] The TRANSIT_GATEWAY item can be created using Create Colocation Gateway.
