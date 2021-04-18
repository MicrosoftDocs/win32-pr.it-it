---
title: Metodo IWMPPlaylistCollection importPlaylist
description: Il metodo importPlaylist aggiunge una playlist statica alla libreria. | Metodo IWMPPlaylistCollection importPlaylist
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- Metodo importPlaylist Windows Media Player
- Metodo importPlaylist Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player, metodo importPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324715"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a><span data-ttu-id="4e7d5-107">Metodo IWMPPlaylistCollection:: importPlaylist</span><span class="sxs-lookup"><span data-stu-id="4e7d5-107">IWMPPlaylistCollection::importPlaylist method</span></span>

<span data-ttu-id="4e7d5-108">Il metodo **importPlaylist** aggiunge una playlist statica alla libreria.</span><span class="sxs-lookup"><span data-stu-id="4e7d5-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e7d5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e7d5-109">Syntax</span></span>


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a><span data-ttu-id="4e7d5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e7d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e7d5-111">*pItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e7d5-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7d5-112">Interfaccia **wmplib. IWMPPlaylist** per la playlist che verrà aggiunta da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4e7d5-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e7d5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e7d5-113">Return value</span></span>

<span data-ttu-id="4e7d5-114">Interfaccia **wmplib. IWMPPlaylist** per la playlist aggiunta.</span><span class="sxs-lookup"><span data-stu-id="4e7d5-114">A **WMPLib.IWMPPlaylist** interface for the added playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e7d5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e7d5-115">Remarks</span></span>

<span data-ttu-id="4e7d5-116">Le playlist che non contengono elementi multimediali non possono essere aggiunte alla libreria utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4e7d5-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="4e7d5-117">Per creare una playlist vuota nella libreria, usare il metodo **nuova playlist** .</span><span class="sxs-lookup"><span data-stu-id="4e7d5-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="4e7d5-118">È quindi possibile compilare la playlist risultante con elementi multimediali usando **IWMPPlaylist. appendItem** o **IWMPPlaylist. InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="4e7d5-118">You can then fill the resulting playlist with media items by using **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="4e7d5-119">Se si passa questo metodo una playlist automatica, la query viene eseguita una volta e il risultato viene aggiunto alla libreria come playlist statica.</span><span class="sxs-lookup"><span data-stu-id="4e7d5-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="4e7d5-120">Per aggiungere una playlist automatica alla libreria e mantenerne il comportamento automatico, usare **IWMPMediaCollection. Add**.</span><span class="sxs-lookup"><span data-stu-id="4e7d5-120">To add an auto playlist to the library and preserve its automatic behavior, use **IWMPMediaCollection.add**.</span></span> <span data-ttu-id="4e7d5-121">Per altre informazioni, vedere [playlist statiche e automatiche](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="4e7d5-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="4e7d5-122">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="4e7d5-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="4e7d5-123">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4e7d5-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e7d5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e7d5-124">Requirements</span></span>



| <span data-ttu-id="4e7d5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e7d5-125">Requirement</span></span> | <span data-ttu-id="4e7d5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4e7d5-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7d5-127">Versione</span><span class="sxs-lookup"><span data-stu-id="4e7d5-127">Version</span></span><br/>   | <span data-ttu-id="4e7d5-128">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="4e7d5-128">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="4e7d5-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e7d5-129">Namespace</span></span><br/> | <span data-ttu-id="4e7d5-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4e7d5-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4e7d5-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="4e7d5-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4e7d5-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4e7d5-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e7d5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e7d5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7d5-134">**IWMPMediaCollection. Add (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4e7d5-134">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4e7d5-135">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4e7d5-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4e7d5-136">**IWMPPlaylist. appendItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4e7d5-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4e7d5-137">**IWMPPlaylist. insertItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4e7d5-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4e7d5-138">**Interfaccia IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4e7d5-138">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4e7d5-139">**IWMPPlaylistCollection. nuova playlist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4e7d5-139">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





