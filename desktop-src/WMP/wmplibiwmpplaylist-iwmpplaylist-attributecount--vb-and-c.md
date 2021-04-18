---
title: Proprietà attributeCount di IWMPPlaylist
description: La proprietà attributeCount ottiene il numero di attributi associati a una playlist.
ms.assetid: 0713ec4e-7e06-4ad2-8f7c-17ed5a92d5ee
keywords:
- Finestra delle proprietà di attributeCount Media Player
- Proprietà di attributeCount Media Player Windows, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, proprietà attributeCount
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4107eb1ad302415715b573b55d2dee1d7155128d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330978"
---
# <a name="iwmpplaylistattributecount-property"></a><span data-ttu-id="a6f7e-106">Proprietà IWMPPlaylist:: attributeCount</span><span class="sxs-lookup"><span data-stu-id="a6f7e-106">IWMPPlaylist::attributeCount property</span></span>

<span data-ttu-id="a6f7e-107">La proprietà **attributeCount** ottiene il numero di attributi associati a una playlist.</span><span class="sxs-lookup"><span data-stu-id="a6f7e-107">The **attributeCount** property gets the number of attributes associated with a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6f7e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6f7e-108">Syntax</span></span>


```CSharp
public System.Int32 attributeCount {get; set;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="a6f7e-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a6f7e-109">Property value</span></span>

<span data-ttu-id="a6f7e-110">**System. Int32** che rappresenta il numero di attributi associati alla playlist.</span><span class="sxs-lookup"><span data-stu-id="a6f7e-110">A **System.Int32** that is the number of attributes associated with the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f7e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6f7e-111">Remarks</span></span>

<span data-ttu-id="a6f7e-112">Poiché le playlist possono provenire da molte origini diverse, possono avere set di attributi diversi.</span><span class="sxs-lookup"><span data-stu-id="a6f7e-112">Because playlists can come from many different sources, they can have several different sets of attributes.</span></span> <span data-ttu-id="a6f7e-113">Questa proprietà ottiene il numero totale di attributi associati a una playlist specifica in modo che gli altri membri dell'interfaccia **IWMPPlaylist** possano accedervi.</span><span class="sxs-lookup"><span data-stu-id="a6f7e-113">This property gets the total number of attributes associated with a particular playlist so that other members of the **IWMPPlaylist** interface can access them.</span></span>

<span data-ttu-id="a6f7e-114">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="a6f7e-114">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="a6f7e-115">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a6f7e-115">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="a6f7e-116">Per ulteriori informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a6f7e-116">For more information about attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a6f7e-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a6f7e-117">Examples</span></span>

<span data-ttu-id="a6f7e-118">Nell'esempio seguente viene illustrato il modo in cui vengono utilizzate le varie proprietà e i metodi delle interfacce **IWMPPlaylist** e **IWMPMedia** compilando un controllo TreeView con nodi per la playlist corrente, gli attributi della playlist, gli elementi multimediali nella playlist e gli attributi degli elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="a6f7e-118">The following example illustrates how various properties and methods of the **IWMPPlaylist** and **IWMPMedia** interfaces are used by filling a treeview control with nodes for the current playlist, playlist attributes, media items in the playlist, and media item attributes.</span></span> <span data-ttu-id="a6f7e-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="a6f7e-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
WMPLib.IWMPPlaylist playlist = player.currentPlaylist;
WMPLib.IWMPMedia media;
string name;

// Demonstrates setItemInfo()
playlist.setItemInfo("custom playlist attribute", "changed");
playlist.get_Item(0).setItemInfo("new custom attribute", "5");

// Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
System.Windows.Forms.TreeNode playlistRootNode = new System.Windows.Forms.TreeNode("Playlist Attributes");

for (int i = 0; i < playlist.attributeCount; ++i)
{
    // Add a tree node for each playlist attribute.
    string attribute = playlist.get_attributeName(i);
    playlistRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(attribute));

    // Add a subnode for the item info for that attribute.
    string info = playlist.getItemInfo(attribute);
    playlistRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(info));
}

// Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode);

// Add nodes for each media item and subnodes for each attribute of that item.
System.Windows.Forms.TreeNode mediaRootNode = new System.Windows.Forms.TreeNode("Media Items in the Playlist");
for(int i = 0; i < playlist.count; i++)
{
    // Get the media item
    media = playlist.get_Item(i);

    // Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(media.name));

    // Add a child node for each attribute of the media item
    for(int j = 0; j < media.attributeCount; j++)
    {
        name = media.getAttributeName(j);
        mediaRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(name + ": " + media.getItemInfo(name)));
    }
}

// Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode);
```


```VB

Dim playlist As WMPLib.IWMPPlaylist = player.currentPlaylist
Dim Media As WMPLib.IWMPMedia
Dim name As String

&#39; Demonstrates setItemInfo()
playlist.setItemInfo(&quot;custom playlist attribute&quot;, &quot;changed&quot;)
playlist.Item(0).setItemInfo(&quot;new custom attribute&quot;, &quot;5&quot;)

&#39; Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
Dim playlistRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Playlist Attributes&quot;)

For i As Integer = 0 To (playlist.attributeCount - 1) Step 1

    &#39; Add a tree node for each playlist attribute.
    Dim attribute As String = playlist.attributeName(i)
    playlistRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(attribute))

    &#39; Add a subnode for the item info for that attribute.
    Dim info As String = playlist.getItemInfo(attribute)
    playlistRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(info))

Next i

&#39; Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode)

&#39; Add nodes for each media item and subnodes for each attribute of that item.
Dim mediaRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Media Items in the Playlist&quot;)

For i As Integer = 0 To (playlist.count - 1) Step 1

    &#39; Get the media item
    Media = playlist.Item(i)

    &#39; Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(Media.name))

    &#39; Add a child node for each attribute of the media item
    For j As Integer = 0 To (Media.attributeCount - 1) Step 1

        name = Media.getAttributeName(j)
        mediaRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(name + &quot;: &quot; + Media.getItemInfo(name)))

    Next j

Next i

&#39; Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode)
```





## <a name="requirements"></a><span data-ttu-id="a6f7e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6f7e-120">Requirements</span></span>



| <span data-ttu-id="a6f7e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6f7e-121">Requirement</span></span> | <span data-ttu-id="a6f7e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a6f7e-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f7e-123">Versione</span><span class="sxs-lookup"><span data-stu-id="a6f7e-123">Version</span></span><br/>   | <span data-ttu-id="a6f7e-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a6f7e-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a6f7e-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6f7e-125">Namespace</span></span><br/> | <span data-ttu-id="a6f7e-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a6f7e-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a6f7e-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="a6f7e-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a6f7e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a6f7e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f7e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6f7e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f7e-130">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a6f7e-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





