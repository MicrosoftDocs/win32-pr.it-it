---
title: Evento MediaCollectionAttributeStringChanged dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaCollectionAttributeStringChanged si verifica quando viene modificato un valore di attributo nella libreria. | Evento MediaCollectionAttributeStringChanged dell'oggetto AxWindowsMediaPlayer
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- Evento MediaCollectionAttributeStringChanged dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b83d8036ca0dca7f79e2a9ba721830447f9c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331878"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="43134-105">Evento MediaCollectionAttributeStringChanged dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="43134-105">MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="43134-106">L'evento MediaCollectionAttributeStringChanged si verifica quando viene modificato un valore di attributo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="43134-106">The MediaCollectionAttributeStringChanged event occurs when an attribute value in the library is changed.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a><span data-ttu-id="43134-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="43134-107">Event Data</span></span>

<span data-ttu-id="43134-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaCollectionAttributeStringChangedEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="43134-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEventHandler**.</span></span> <span data-ttu-id="43134-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="43134-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="43134-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43134-110">Property</span></span>         | <span data-ttu-id="43134-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43134-111">Description</span></span>                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43134-112">bstrAttribName</span><span class="sxs-lookup"><span data-stu-id="43134-112">bstrAttribName</span></span>   | <span data-ttu-id="43134-113">System. StringSpecifies il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="43134-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="43134-114">Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="43134-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="43134-115">bstrOldAttribVal</span><span class="sxs-lookup"><span data-stu-id="43134-115">bstrOldAttribVal</span></span> | <span data-ttu-id="43134-116">System. StringSpecifies il valore precedente dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="43134-116">System.StringSpecifies the old value of the attribute.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="43134-117">bstrNewAttribVal</span><span class="sxs-lookup"><span data-stu-id="43134-117">bstrNewAttribVal</span></span> | <span data-ttu-id="43134-118">System. StringSpecifies il nuovo valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="43134-118">System.StringSpecifies the new value of the attribute.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="43134-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="43134-119">Remarks</span></span>

<span data-ttu-id="43134-120">Quando un utente modifica i metadati della libreria, l'insieme di supporti viene aggiornato e questo evento viene generato per ogni attributo modificato.</span><span class="sxs-lookup"><span data-stu-id="43134-120">When a user modifies library metadata, the media collection is updated and this event fires for each attribute changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="43134-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43134-121">Requirements</span></span>



| <span data-ttu-id="43134-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="43134-122">Requirement</span></span> | <span data-ttu-id="43134-123">Valore</span><span class="sxs-lookup"><span data-stu-id="43134-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43134-124">Versione</span><span class="sxs-lookup"><span data-stu-id="43134-124">Version</span></span><br/>   | <span data-ttu-id="43134-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="43134-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="43134-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43134-126">Namespace</span></span><br/> | <span data-ttu-id="43134-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="43134-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="43134-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="43134-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="43134-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="43134-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43134-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43134-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43134-131">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="43134-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="43134-132">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="43134-132">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="43134-133">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="43134-133">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





