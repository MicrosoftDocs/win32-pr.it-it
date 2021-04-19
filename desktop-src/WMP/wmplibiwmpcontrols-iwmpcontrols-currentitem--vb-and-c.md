---
title: Proprietà currentItem di IWMPControls
description: La proprietà currentItem Ottiene o imposta l'elemento multimediale corrente in una playlist.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- Finestra delle proprietà di currentItem Media Player
- Proprietà di currentItem Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, proprietà currentItem
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332490"
---
# <a name="iwmpcontrolscurrentitem-property"></a><span data-ttu-id="e2b4d-106">Proprietà IWMPControls:: currentItem</span><span class="sxs-lookup"><span data-stu-id="e2b4d-106">IWMPControls::currentItem property</span></span>

<span data-ttu-id="e2b4d-107">La proprietà **CurrentItem** Ottiene o imposta l'elemento multimediale corrente in una playlist.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-107">The **currentItem** property gets or sets the current media item in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b4d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2b4d-108">Syntax</span></span>


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="e2b4d-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e2b4d-109">Property value</span></span>

<span data-ttu-id="e2b4d-110">Interfaccia **wmplib. IWMPMedia** che rappresenta l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-110">A **WMPLib.IWMPMedia** interface that represents the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2b4d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2b4d-111">Remarks</span></span>

<span data-ttu-id="e2b4d-112">Questa proprietà funziona solo con gli elementi nella playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-112">This property works only with items in the current playlist.</span></span> <span data-ttu-id="e2b4d-113">L'impostazione di **CurrentItem** sull'interfaccia di un elemento multimediale salvato non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-113">Setting **currentItem** to the interface of a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="e2b4d-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="e2b4d-114">Examples</span></span>

<span data-ttu-id="e2b4d-115">Nell'esempio seguente viene usato **CurrentItem** per impostare l'elemento multimediale corrente del lettore su un elemento selezionato da una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-115">The following example uses **currentItem** to set the player's current media item to an item selected from a list box.</span></span> <span data-ttu-id="e2b4d-116">La casella di riepilogo è stata compilata con tutti gli elementi nella playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-116">The list box has been filled with all of the items in the current playlist.</span></span> <span data-ttu-id="e2b4d-117">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e2b4d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2b4d-118">Requirements</span></span>



| <span data-ttu-id="e2b4d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2b4d-119">Requirement</span></span> | <span data-ttu-id="e2b4d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e2b4d-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b4d-121">Versione</span><span class="sxs-lookup"><span data-stu-id="e2b4d-121">Version</span></span><br/>   | <span data-ttu-id="e2b4d-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e2b4d-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e2b4d-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e2b4d-123">Namespace</span></span><br/> | <span data-ttu-id="e2b4d-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e2b4d-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e2b4d-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="e2b4d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e2b4d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e2b4d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b4d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2b4d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b4d-128">**IWMPControlsInterface (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e2b4d-128">**IWMPControlsInterface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e2b4d-129">**IWMPMediaInterface (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e2b4d-129">**IWMPMediaInterface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e2b4d-130">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e2b4d-130">**IWMPPlaylistCollection.getByName(VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





