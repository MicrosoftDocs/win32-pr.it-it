---
title: Evento MediaCollectionMediaAdded dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaCollectionMediaAdded si verifica quando un elemento multimediale viene aggiunto alla libreria locale. | Evento MediaCollectionMediaAdded dell'oggetto AxWindowsMediaPlayer
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- Evento MediaCollectionMediaAdded dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb839fccf9a5048b5647480eca36fcfcaeb904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331871"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="54a9f-105">Evento MediaCollectionMediaAdded dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="54a9f-105">MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="54a9f-106">L'evento MediaCollectionMediaAdded si verifica quando un elemento multimediale viene aggiunto alla libreria locale.</span><span class="sxs-lookup"><span data-stu-id="54a9f-106">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a><span data-ttu-id="54a9f-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="54a9f-107">Event Data</span></span>

<span data-ttu-id="54a9f-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaCollectionMediaAddedEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="54a9f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEventHandler**.</span></span> <span data-ttu-id="54a9f-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="54a9f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="54a9f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54a9f-110">Property</span></span> | <span data-ttu-id="54a9f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54a9f-111">Description</span></span>                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a9f-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="54a9f-112">pMedia</span></span>   | <span data-ttu-id="54a9f-113">Elemento multimediale System. ObjectThe aggiunto alla libreria locale.</span><span class="sxs-lookup"><span data-stu-id="54a9f-113">System.ObjectThe media item added to the local library.</span></span> <span data-ttu-id="54a9f-114">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPMedia per accedervi.</span><span class="sxs-lookup"><span data-stu-id="54a9f-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54a9f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="54a9f-115">Remarks</span></span>

<span data-ttu-id="54a9f-116">Questo evento si verifica solo per la libreria locale.</span><span class="sxs-lookup"><span data-stu-id="54a9f-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="54a9f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54a9f-117">Requirements</span></span>



| <span data-ttu-id="54a9f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="54a9f-118">Requirement</span></span> | <span data-ttu-id="54a9f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="54a9f-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a9f-120">Versione</span><span class="sxs-lookup"><span data-stu-id="54a9f-120">Version</span></span><br/>   | <span data-ttu-id="54a9f-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="54a9f-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="54a9f-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="54a9f-122">Namespace</span></span><br/> | <span data-ttu-id="54a9f-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="54a9f-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="54a9f-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="54a9f-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="54a9f-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="54a9f-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54a9f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54a9f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a9f-127">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="54a9f-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="54a9f-128">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="54a9f-128">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="54a9f-129">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="54a9f-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="54a9f-130">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="54a9f-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





