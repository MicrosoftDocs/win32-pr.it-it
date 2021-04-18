---
title: Evento MediaCollectionAttributeStringAdded dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaCollectionAttributeStringAdded si verifica quando un valore di attributo viene aggiunto alla libreria. | Evento MediaCollectionAttributeStringAdded dell'oggetto AxWindowsMediaPlayer
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- Evento MediaCollectionAttributeStringAdded dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325003"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="49970-105">Evento MediaCollectionAttributeStringAdded dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="49970-105">MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="49970-106">L'evento MediaCollectionAttributeStringAdded si verifica quando un valore di attributo viene aggiunto alla libreria.</span><span class="sxs-lookup"><span data-stu-id="49970-106">The MediaCollectionAttributeStringAdded event occurs when an attribute value is added to the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a><span data-ttu-id="49970-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="49970-107">Event Data</span></span>

<span data-ttu-id="49970-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaCollectionAttributeStringAddedEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="49970-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEventHandler**.</span></span> <span data-ttu-id="49970-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="49970-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="49970-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="49970-110">Property</span></span>           | <span data-ttu-id="49970-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49970-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49970-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="49970-112">**bstrAttribName**</span></span> | <span data-ttu-id="49970-113">System. StringSpecifies il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="49970-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="49970-114">Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="49970-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="49970-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="49970-115">bstrAttribVal</span></span>      | <span data-ttu-id="49970-116">System. StringSpecifies il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="49970-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="49970-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="49970-117">Remarks</span></span>

<span data-ttu-id="49970-118">Quando un elemento multimediale viene aggiunto alla libreria, i relativi metadati vengono aggiunti alla raccolta di supporti e questo evento viene generato per ogni attributo aggiunto.</span><span class="sxs-lookup"><span data-stu-id="49970-118">When a media item is added to the library, its metadata is added to the media collection and this event is fired for each attribute added.</span></span>

## <a name="requirements"></a><span data-ttu-id="49970-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49970-119">Requirements</span></span>



| <span data-ttu-id="49970-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="49970-120">Requirement</span></span> | <span data-ttu-id="49970-121">Valore</span><span class="sxs-lookup"><span data-stu-id="49970-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49970-122">Versione</span><span class="sxs-lookup"><span data-stu-id="49970-122">Version</span></span><br/>   | <span data-ttu-id="49970-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="49970-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="49970-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49970-124">Namespace</span></span><br/> | <span data-ttu-id="49970-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="49970-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="49970-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="49970-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="49970-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="49970-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49970-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49970-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49970-129">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49970-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49970-130">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49970-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49970-131">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49970-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





