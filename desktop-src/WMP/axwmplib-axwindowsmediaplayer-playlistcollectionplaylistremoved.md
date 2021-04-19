---
title: Evento PlaylistCollectionPlaylistRemoved dell'oggetto AxWindowsMediaPlayer
description: L'evento PlaylistCollectionPlaylistRemoved si verifica quando una playlist viene rimossa dalla raccolta di playlist. | Evento PlaylistCollectionPlaylistRemoved dell'oggetto AxWindowsMediaPlayer
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- Evento PlaylistCollectionPlaylistRemoved dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332305"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a1424-105">Evento PlaylistCollectionPlaylistRemoved dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a1424-105">PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a1424-106">L'evento PlaylistCollectionPlaylistRemoved si verifica quando una playlist viene rimossa dalla raccolta di playlist.</span><span class="sxs-lookup"><span data-stu-id="a1424-106">The PlaylistCollectionPlaylistRemoved event occurs when a playlist is removed from the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a><span data-ttu-id="a1424-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="a1424-107">Event Data</span></span>

<span data-ttu-id="a1424-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_PlaylistCollectionPlaylistRemovedEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="a1424-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEventHandler**.</span></span> <span data-ttu-id="a1424-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="a1424-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="a1424-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a1424-110">Property</span></span>             | <span data-ttu-id="a1424-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1424-111">Description</span></span>                                                                  |
|----------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a1424-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="a1424-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="a1424-113">System. StringSpecifies il nome della playlist che è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="a1424-113">System.StringSpecifies the name of the playlist that was removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a1424-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1424-114">Requirements</span></span>



| <span data-ttu-id="a1424-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1424-115">Requirement</span></span> | <span data-ttu-id="a1424-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a1424-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1424-117">Versione</span><span class="sxs-lookup"><span data-stu-id="a1424-117">Version</span></span><br/>   | <span data-ttu-id="a1424-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a1424-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a1424-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a1424-119">Namespace</span></span><br/> | <span data-ttu-id="a1424-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a1424-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a1424-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="a1424-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a1424-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a1424-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1424-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1424-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1424-124">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a1424-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a1424-125">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a1424-125">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





