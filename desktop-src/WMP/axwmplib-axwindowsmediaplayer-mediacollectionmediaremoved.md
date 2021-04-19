---
title: Evento MediaCollectionMediaRemoved dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaCollectionMediaRemoved si verifica quando un elemento multimediale viene rimosso dalla libreria locale. | Evento MediaCollectionMediaRemoved dell'oggetto AxWindowsMediaPlayer
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- Evento MediaCollectionMediaRemoved dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331870"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="75ffb-105">Evento MediaCollectionMediaRemoved dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="75ffb-105">MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="75ffb-106">L'evento MediaCollectionMediaRemoved si verifica quando un elemento multimediale viene rimosso dalla libreria locale.</span><span class="sxs-lookup"><span data-stu-id="75ffb-106">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a><span data-ttu-id="75ffb-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="75ffb-107">Event Data</span></span>

<span data-ttu-id="75ffb-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaCollectionMediaRemovedEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="75ffb-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEventHandler**.</span></span> <span data-ttu-id="75ffb-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="75ffb-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="75ffb-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="75ffb-110">Property</span></span> | <span data-ttu-id="75ffb-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75ffb-111">Description</span></span>                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ffb-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="75ffb-112">pMedia</span></span>   | <span data-ttu-id="75ffb-113">Elemento multimediale System. ObjectThe rimosso dalla libreria locale.</span><span class="sxs-lookup"><span data-stu-id="75ffb-113">System.ObjectThe media item removed from the local library.</span></span> <span data-ttu-id="75ffb-114">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPMedia per accedervi.</span><span class="sxs-lookup"><span data-stu-id="75ffb-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75ffb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="75ffb-115">Remarks</span></span>

<span data-ttu-id="75ffb-116">Questo evento si verifica solo per la libreria locale.</span><span class="sxs-lookup"><span data-stu-id="75ffb-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="75ffb-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75ffb-117">Requirements</span></span>



| <span data-ttu-id="75ffb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ffb-118">Requirement</span></span> | <span data-ttu-id="75ffb-119">Valore</span><span class="sxs-lookup"><span data-stu-id="75ffb-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ffb-120">Versione</span><span class="sxs-lookup"><span data-stu-id="75ffb-120">Version</span></span><br/>   | <span data-ttu-id="75ffb-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="75ffb-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="75ffb-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="75ffb-122">Namespace</span></span><br/> | <span data-ttu-id="75ffb-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="75ffb-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="75ffb-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="75ffb-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="75ffb-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="75ffb-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ffb-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75ffb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ffb-127">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="75ffb-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="75ffb-128">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="75ffb-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





