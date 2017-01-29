# Giver

1.  Allow a list if items to be given.  The '~' delimited list can be defined within a BTN notecard.
2.  Allow the folder name to be defined.  The folder name can be defined within the BTN notecard.
3.  Display a dialog with seated AV names for nPose menu user to select from to become the receiver of these items..  If there are no seated AV's, then the menu toucher becomes the receiver of these items.
4.  Optional provide a notecard with the list of items to be given.  LL has a limit to the length of the text that can be sent via link message so a long list will not all be sent.  The optional notecard will key off the giver script to read that notecard to get the list thus getting around the LL limit.
    a.  The name of the notecard containing the list of items must be the same name as the folder that the receiver AV will be getting.
    b.  If the optional notecard is used, the list of items within the BTN notecard are not included (no '~' delimited list).
5.  The Giver plugin will announce in local to the receiver who sent the items and the name of the folder where these items can be found in their inventory.

The Giver plugin is set up to handle giving only a couple items via a tilde delimited list or an entire list from a notecard of items from contents of the prim this script is in.  If there are sitters the menu user will be given a menu of sitter names to pick from to receive the items to be given, and if there are no sitters, the menu user will be the receiver (give to self).

In either case (short list or long list from notecard), create a notecard with a name that will be used in the nPose menu.  The contents (syntax) of this notecard will vary depending upong short list or long list.

Give from short list:
The syntax for giving a short list of item is as follows:    
`LINKMSG|1334|[FolderName],[item1~item2~itemN]|%AVKEY%`    
FolderName will be the folder passed to the receiver and will contain the items.  The receiver will receive a message in local to let them know this folder name to help them find the items.

Give from long list (a notecard):    
`LINKMSG|1334|[FolderName]|%AVKEY%`   
Here the FolderName will serve two purposes.  As in the short list this becomes the folder name the receiver will get.  It also tells nPose to look for the notecard in it's contents with the matching name.  This notecard in contents should contain the list of items to be given.  The items should be listed as one item per line within that notecard.  The receiver will receive a message in local to let them know this folder name to help them find the items.
