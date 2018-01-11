# CS-SDL Interface (CS-SE-SD)
## Purpose
You can use the CS-SDL interface to perform interactive scheduling for orders and field service planning with an external scheduling system. In the SAP System, the data is saved in the order and can be used by the application components Plant Maintenance (PM) and Customer Service (CS). The additional functions in comparison to the capacity planning function in the SAP System depend on the respective scheduling system.

## Implementation Considerations
If the scheduling functions in the SAP System are not sufficient for your field services planning, the CS-SDL interface enables you to use an external scheduling system.

You can implement the CS-SDL interface in the following ways:

You use a partner solution. A prerequisite for this is that you have performed all the necessary Customizing settings .

You program your own solution.

SAP delivers function modules that you can use for a scheduling agreement dialog for determining dates.

The function module PM_ORDER_EXTERN_SCHED_DIALOG delivers the dialog and calls up the interface PM_ORDER_EXTERN_SCHED_APPOINT . This results in the scheduling data being copied from the external scheduling system during order scheduling.

## Note
You will find more information on certified products in SAPNet under  Customers & Partners  Partners    Complementary Software Program. 

The implementation of external systems is not supported by SAP consultants, and the technical prerequisites for the external product must be agreed upon with competent consultants for the external system.

## Features
The following scenarios are supported with this component:

## Finite scheduling

You have a work center with five capacities of 40 hours per week each in your company. The external scheduling system checks the dates and schedules on the basis of capacity and not on the basis of individual technicians.

## Field service planning

The external system performs checks and schedules on the basis of individual technicians.

If you use the external scheduling system for finite scheduling, the SAP System frontend is sufficient. If you want to use field service planning in the form of a planning board, you require the external scheduling system as an additional frontend.

## Constraints
The following functions are not supported:

Time dependency or operational constraints (obligatory/optional/start/end)

## SAP planning board

Changes to the order data in the external scheduling system are not updated in the SAP System.