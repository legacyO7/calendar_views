# DayView

A highly customisable library for displaying a day view. It works for single or for multiple days.

## Components

Component is an object that builds **items** that are then displayed inside a **DayView**.

If this package is used correctly, every component should have access (via Inherited Widgets) 
to all Properties and a Positioning assistant.

Some components are already provided by this library,
but you are free to create your own by extending or implementing the **Component** class.
 
DayView inherits components from a **ComponentsProvider**, it then calls their buildItems method and 
places the built Positioned Widgets as children of a Stack.  
Components are built in an order as provided by a **ComponentsProvider**, 
thus component items that are built later might cover previously built items.

List of already made components:
* EventViewComponent (for displaying events)
* SupportLineComponent: (for displaying lines that indicate some time eg. a line for every hour)
    * IntervalSupportLineComponent
    * CustomSupportLineComponent
* TimeIndicationComponent: (for displaying a time indicators)
    * IntervalTimeIndicationComponent
    * CustomTimeIndicationComponent
    
## PositioningAssistant

PositioningAssistant is an utility object that provided information about different areas inside a **DayView**.

PositioningAssistant is generated (using **PositioningAssistantGenerator**) automatically 
by placing a **DayView**, every component can access it via PositioningAssistantProvider (InheritedWidget).

For every area the following information is available:
* // TODO

Areas:
* // TODO

## Properties

Property is a collection of information that is useful when creating components and their items.

Properties are accessed via Inherited widgets (usually named as "*propertyName*Property"), 
if library is used correctly every **Component** should have access to all properties.

List of properties and their providers:
* Days (DaysProvider)
* Dimensions (DimensionsProvider)
* Restrictions (RestrictionsProvider)
* SizeConstraints (SizeConstraintsProvider)

## DayView

Widget for displaying a DayView.

The following properties and utilities are automatically generated by a DayView:
* Days
* SizeConstraints
* PositioningAssistant

## DayViewResources

Helper widget that provides some essential properties and utilities 
that can be accessed by child widgets.

Provided items:
* Restrictions
* Dimensions
* PositioningAssistantGenerator
* Components
