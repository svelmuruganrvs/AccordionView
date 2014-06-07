AccordionView
=============

Very simple accordion view in Cocoa Touch.

Usage
-----
    AccordionView *accordion = [[AccordionView alloc] initWithFrame:CGRectMake(0, 0, 320, 420)];
    
    accordion.sapceBetween_AccordionView=10; // This is an optional int value that makes the accordion tap sapace.If this is not seted there will not be the space between the accordion.
    
    [self addSubview:accordion];

    // Only height is taken into account, so other parameters are just dummy
    UIButton *header1 = [[UIButton alloc] initWithFrame:CGRectMake(0, 0, 0, 30)];
    [header1 setTitle:@"First row" forState:UIControlStateNormal];

    UIView *view1 = [[UIView alloc] initWithFrame:CGRectMake(0, 0, 0, 200)];
    // ... add subviews to view1

    [accordion addHeader:header1 withView:view1];

    // ... add more panels

    [accordion setNeedsLayout];

    // Set this if you want to allow multiple selection
    [accordion setAllowsMultipleSelection:YES];

    // Set this to NO if you want to have at least one open section at all times
    [accordion setAllowsEmptySelection:YES];

    // Remove section at index 1
    [accordion removeHeaderAtIndex:1];

Todo
----
* Horizontal view

LICENCE
-------

Copyright (C) 2011-2014 Wojtek Siudzinski <admin@suda.pl>, [Appsome](http://appsome.co)

Licensed under the Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0
