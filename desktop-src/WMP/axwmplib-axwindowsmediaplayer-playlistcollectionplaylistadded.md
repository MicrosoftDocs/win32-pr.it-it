---
title: Evento PlaylistCollectionPlaylistAdded dell'oggetto AxWindowsMediaPlayer
description: L'evento PlaylistCollectionPlaylistAdded si verifica quando viene aggiunta una playlist alla raccolta playlist. | Evento PlaylistCollectionPlaylistAdded dell'oggetto AxWindowsMediaPlayer
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- Evento PlaylistCollectionPlaylistAdded dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332307"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="cb759-105">Evento PlaylistCollectionPlaylistAdded dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="cb759-105">PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="cb759-106">L'evento PlaylistCollectionPlaylistAdded si verifica quando viene aggiunta una playlist alla raccolta playlist.</span><span class="sxs-lookup"><span data-stu-id="cb759-106">The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a><span data-ttu-id="cb759-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="cb759-107">Event Data</span></span>

<span data-ttu-id="cb759-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_PlaylistCollectionPlaylistAddedEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="cb759-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEventHandler**.</span></span> <span data-ttu-id="cb759-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="cb759-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="cb759-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cb759-110">Property</span></span>             | <span data-ttu-id="cb759-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb759-111">Description</span></span>                                                                |
|----------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="cb759-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="cb759-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="cb759-113">System. StringSpecifies il nome della playlist aggiunta.</span><span class="sxs-lookup"><span data-stu-id="cb759-113">System.StringSpecifies the name of the playlist that was added.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb759-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb759-114">Remarks</span></span>

<span data-ttu-id="cb759-115">Il nome della playlist aggiunta può essere usato per recuperare la playlist corrispondente usando IWMPPlaylistCollection. metodo **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="cb759-115">The name of the playlist that was added can be used to retrieve the corresponding playlist by using the IWMPPlaylistCollection.**getByName** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb759-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb759-116">Requirements</span></span>



| <span data-ttu-id="cb759-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb759-117">Requirement</span></span> | <span data-ttu-id="cb759-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cb759-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb759-119">Versione</span><span class="sxs-lookup"><span data-stu-id="cb759-119">Version</span></span><br/>   | <span data-ttu-id="cb759-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cb759-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cb759-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cb759-121">Namespace</span></span><br/> | <span data-ttu-id="cb759-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="cb759-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cb759-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="cb759-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cb759-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cb759-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb759-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb759-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb759-126">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cb759-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb759-127">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cb759-127">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





