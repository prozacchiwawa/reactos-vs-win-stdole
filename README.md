This is a comparison of the reatos stdole*.tlb vs the ones in windows 10.

Look in stdole2.diff and stdole32.diff to see the differences.

I generated these files using tlbimp and il disassembler.

for each tlb i generated a .net assembly to bind to it and then
used the il disassembler's dump tree view item to output the
assembly bindings in a readable way.

Summary:

reactos' stdole2 is missing these classes:

 - FontEvents_Event
 - FontEvents_EventProvider
 - FontEvents_FontChangedEventHandler

Other differences:

 - GUID is missing one constructor

stdole32 are the same.
