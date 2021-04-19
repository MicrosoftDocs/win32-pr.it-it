---
title: IWMPPlaylist. Item (VB e C)
description: La proprietà Item (il \_ metodo Get Item in C \) ottiene un'interfaccia per l'elemento multimediale in corrispondenza dell'indice specificato.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- IWMPPlaylist. Item (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324222"
---
# <a name="iwmpplaylistitem-vb-and-c"></a><span data-ttu-id="d0146-104">IWMPPlaylist. Item (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="d0146-104">IWMPPlaylist.Item (VB and C#)</span></span>

<span data-ttu-id="d0146-105">La proprietà **Item** (il metodo **get \_ Item** in C#) ottiene un'interfaccia per l'elemento multimediale in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="d0146-105">The **Item** property (the **get\_Item** method in C#) gets an interface to the media item at the specified index.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a><span data-ttu-id="d0146-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0146-106">Parameters</span></span>

<span data-ttu-id="d0146-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="d0146-107">*lIndex*</span></span>

<span data-ttu-id="d0146-108">**System. Int32** che rappresenta l'indice dell'elemento multimediale nella playlist.</span><span class="sxs-lookup"><span data-stu-id="d0146-108">A **System.Int32** that is the index of the media item in the playlist.</span></span>

## <a name="property-value"></a><span data-ttu-id="d0146-109">Valore della proprietà</span><span class="sxs-lookup"><span data-stu-id="d0146-109">Property Value</span></span>

<span data-ttu-id="d0146-110">Interfaccia **wmplib. IWMPMedia** che fornisce l'accesso all'elemento multimediale in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="d0146-110">An **WMPLib.IWMPMedia** interface that provides access to the media item at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0146-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0146-111">Remarks</span></span>

<span data-ttu-id="d0146-112">**IWMPPlaylist. Item** è una proprietà di sola lettura in Visual Basic che accetta un parametro, mentre in C# viene chiamato il metodo **IWMPPlaylist. Get \_ Item** .</span><span class="sxs-lookup"><span data-stu-id="d0146-112">**IWMPPlaylist.Item** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_Item** method.</span></span>

## <a name="examples"></a><span data-ttu-id="d0146-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="d0146-113">Examples</span></span>

<span data-ttu-id="d0146-114">Nell'esempio seguente viene usata la proprietà **Item** (il metodo **get \_ Item** in C#) per recuperare un elemento multimediale da una playlist basata sulla selezione di un utente.</span><span class="sxs-lookup"><span data-stu-id="d0146-114">The following example uses the **Item** property (the **get\_Item** method in C#) to retrieve a media item from a playlist based on a user selection.</span></span> <span data-ttu-id="d0146-115">Una casella di riepilogo è stata creata con il nome Weblist e riempita con i titoli dalla playlist denominata audioPlaylist.</span><span class="sxs-lookup"><span data-stu-id="d0146-115">A list box was created with the name weblist, and filled with the titles from the playlist called audioPlaylist.</span></span> <span data-ttu-id="d0146-116">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="d0146-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d0146-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0146-117">Requirements</span></span>



| <span data-ttu-id="d0146-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0146-118">Requirement</span></span> | <span data-ttu-id="d0146-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d0146-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0146-120">Versione</span><span class="sxs-lookup"><span data-stu-id="d0146-120">Version</span></span><br/>   | <span data-ttu-id="d0146-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d0146-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d0146-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d0146-122">Namespace</span></span><br/> | <span data-ttu-id="d0146-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d0146-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d0146-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="d0146-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d0146-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d0146-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0146-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0146-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0146-127">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d0146-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0146-128">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d0146-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0146-129">**IWMPPlaylist. insertItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d0146-129">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0146-130">**IWMPPlaylist. removeItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d0146-130">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0146-131">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d0146-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0146-132">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d0146-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





