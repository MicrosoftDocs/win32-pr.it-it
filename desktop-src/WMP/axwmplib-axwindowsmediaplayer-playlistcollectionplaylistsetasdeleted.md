---
title: Evento PlaylistCollectionPlaylistSetAsDeleted dell'oggetto AxWindowsMediaPlayer
description: L'evento PlaylistCollectionPlaylistSetAsDeleted è riservato per un utilizzo futuro.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Evento PlaylistCollectionPlaylistSetAsDeleted dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332301"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a7e5a-104">Evento PlaylistCollectionPlaylistSetAsDeleted dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a7e5a-104">PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a7e5a-105">L'evento PlaylistCollectionPlaylistSetAsDeleted è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="a7e5a-105">The PlaylistCollectionPlaylistSetAsDeleted event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a><span data-ttu-id="a7e5a-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="a7e5a-106">Event Data</span></span>

<span data-ttu-id="a7e5a-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_PlaylistCollectionPlaylistSetAsDeletedEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="a7e5a-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span></span> <span data-ttu-id="a7e5a-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="a7e5a-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="a7e5a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7e5a-109">Property</span></span>         | <span data-ttu-id="a7e5a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7e5a-110">Description</span></span>                                 |
|------------------|---------------------------------------------|
| <span data-ttu-id="a7e5a-111">bstrPlaylistName</span><span class="sxs-lookup"><span data-stu-id="a7e5a-111">bstrPlaylistName</span></span> | <span data-ttu-id="a7e5a-112">**System. String** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="a7e5a-112">**System.String** Not supported.</span></span><br/>  |
| <span data-ttu-id="a7e5a-113">varfIsDeleted</span><span class="sxs-lookup"><span data-stu-id="a7e5a-113">varfIsDeleted</span></span>    | <span data-ttu-id="a7e5a-114">**System. Boolean** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="a7e5a-114">**System.Boolean** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7e5a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7e5a-115">Remarks</span></span>

<span data-ttu-id="a7e5a-116">Questo evento è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="a7e5a-116">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7e5a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7e5a-117">Requirements</span></span>



| <span data-ttu-id="a7e5a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7e5a-118">Requirement</span></span> | <span data-ttu-id="a7e5a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a7e5a-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e5a-120">Versione</span><span class="sxs-lookup"><span data-stu-id="a7e5a-120">Version</span></span><br/>   | <span data-ttu-id="a7e5a-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a7e5a-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a7e5a-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7e5a-122">Namespace</span></span><br/> | <span data-ttu-id="a7e5a-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a7e5a-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a7e5a-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="a7e5a-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a7e5a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a7e5a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7e5a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7e5a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e5a-127">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a7e5a-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





