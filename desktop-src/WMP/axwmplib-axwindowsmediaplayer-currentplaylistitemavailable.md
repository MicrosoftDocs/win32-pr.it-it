---
title: Evento CurrentPlaylistItemAvailable dell'oggetto AxWindowsMediaPlayer
description: L'evento CurrentPlaylistItemAvailable si verifica quando la playlist corrente diventa disponibile. | Evento CurrentPlaylistItemAvailable dell'oggetto AxWindowsMediaPlayer
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Evento CurrentPlaylistItemAvailable dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324106"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="fef96-105">Evento CurrentPlaylistItemAvailable dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="fef96-105">CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="fef96-106">L'evento CurrentPlaylistItemAvailable si verifica quando la playlist corrente diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="fef96-106">The CurrentPlaylistItemAvailable event occurs when the current playlist becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="fef96-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="fef96-107">Event Data</span></span>

<span data-ttu-id="fef96-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CurrentPlaylistItemAvailableEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="fef96-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEventHandler**.</span></span> <span data-ttu-id="fef96-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="fef96-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="fef96-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fef96-110">Property</span></span>         | <span data-ttu-id="fef96-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fef96-111">Description</span></span>                                                    |
|------------------|----------------------------------------------------------------|
| <span data-ttu-id="fef96-112">**bstrItemName**</span><span class="sxs-lookup"><span data-stu-id="fef96-112">**bstrItemName**</span></span> | <span data-ttu-id="fef96-113">System. StringThe nome dell'elemento della playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="fef96-113">System.StringThe name of the current playlist item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fef96-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fef96-114">Remarks</span></span>

<span data-ttu-id="fef96-115">Il nome della playlist corrente può essere usato per recuperare l'interfaccia **IWMPPlaylist** corrispondente dall'interfaccia IWMPPlaylistArray restituita dal metodo IWMPPlaylistCollection. GetByName.</span><span class="sxs-lookup"><span data-stu-id="fef96-115">The name of the current playlist can be used to retrieve the corresponding **IWMPPlaylist** interface from the IWMPPlaylistArray interface that is returned from the IWMPPlaylistCollection.getByName method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fef96-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fef96-116">Requirements</span></span>



| <span data-ttu-id="fef96-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fef96-117">Requirement</span></span> | <span data-ttu-id="fef96-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fef96-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef96-119">Versione</span><span class="sxs-lookup"><span data-stu-id="fef96-119">Version</span></span><br/>   | <span data-ttu-id="fef96-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="fef96-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="fef96-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fef96-121">Namespace</span></span><br/> | <span data-ttu-id="fef96-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="fef96-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="fef96-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="fef96-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fef96-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fef96-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef96-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fef96-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef96-126">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fef96-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fef96-127">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fef96-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fef96-128">**Interfaccia IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fef96-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fef96-129">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fef96-129">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





