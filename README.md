# Giver

The Giver plugin is set up to handle giving only a couple items via a tilde delimited list or an entire list from a notecard of items from contents of the prim this script is in.  If there are sitters the menu user will be given a menu of sitter names to pick from to receive the items to be given, and if there are no sitters, the menu user will be the receiver (give to self).

In either case (short list or long list from notecard), create a notecard with a name that will be used in the nPose menu.  The contents (syntax) of this notecard contents will vary depending upon short list or long list.

Give from short list:
The syntax for giving a short list of item is as follows:    
`LINKMSG|1334|[FolderName],[item1~item2~itemN]|%AVKEY%`    
FolderName will be the folder passed to the receiver and will contain the items.  The receiver will receive a message in local to let them know this folder name to help them find the items.

Give from long list (a notecard):    
`LINKMSG|1334|[FolderName]|%AVKEY%`   
Here the FolderName will serve two purposes.  As in the short list this becomes the folder name the receiver will get.  It also tells nPose to look for the notecard in it's contents with the matching name.  This notecard in contents should contain the list of items to be given.  The items should be listed as one item per line within that notecard.  The receiver will receive a message in local to let them know this folder name to help them find the items.
