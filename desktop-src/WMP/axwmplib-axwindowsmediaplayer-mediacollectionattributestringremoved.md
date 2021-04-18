---
title: Evento MediaCollectionAttributeStringRemoved dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaCollectionAttributeStringRemoved si verifica quando viene rimosso un valore di attributo dalla libreria. | Evento MediaCollectionAttributeStringRemoved dell'oggetto AxWindowsMediaPlayer
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Evento MediaCollectionAttributeStringRemoved dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324749"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8e8c5-105">Evento MediaCollectionAttributeStringRemoved dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="8e8c5-105">MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8e8c5-106">L'evento MediaCollectionAttributeStringRemoved si verifica quando viene rimosso un valore di attributo dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="8e8c5-106">The MediaCollectionAttributeStringRemoved event occurs when an attribute value is removed from the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a><span data-ttu-id="8e8c5-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="8e8c5-107">Event Data</span></span>

<span data-ttu-id="8e8c5-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaCollectionAttributeStringRemovedEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="8e8c5-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEventHandler**.</span></span> <span data-ttu-id="8e8c5-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="8e8c5-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="8e8c5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e8c5-110">Property</span></span>           | <span data-ttu-id="8e8c5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e8c5-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8c5-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="8e8c5-112">**bstrAttribName**</span></span> | <span data-ttu-id="8e8c5-113">System. StringSpecifies il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="8e8c5-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="8e8c5-114">Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8e8c5-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="8e8c5-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="8e8c5-115">bstrAttribVal</span></span>      | <span data-ttu-id="8e8c5-116">System. StringSpecifies il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="8e8c5-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="8e8c5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e8c5-117">Remarks</span></span>

<span data-ttu-id="8e8c5-118">Quando un elemento multimediale viene rimosso dalla libreria, i relativi metadati vengono rimossi da **mediacollection** e questo evento viene generato per ogni attributo rimosso.</span><span class="sxs-lookup"><span data-stu-id="8e8c5-118">When a media item is removed from the library, its metadata is removed from the **MediaCollection** and this event is fired for each attribute removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e8c5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e8c5-119">Requirements</span></span>



| <span data-ttu-id="8e8c5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e8c5-120">Requirement</span></span> | <span data-ttu-id="8e8c5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8e8c5-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8c5-122">Versione</span><span class="sxs-lookup"><span data-stu-id="8e8c5-122">Version</span></span><br/>   | <span data-ttu-id="8e8c5-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8e8c5-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8e8c5-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8e8c5-124">Namespace</span></span><br/> | <span data-ttu-id="8e8c5-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8e8c5-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8e8c5-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="8e8c5-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8e8c5-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8e8c5-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e8c5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e8c5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e8c5-129">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8e8c5-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e8c5-130">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8e8c5-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e8c5-131">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8e8c5-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





