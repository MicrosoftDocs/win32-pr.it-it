---
title: Evento CdromBurnMediaError dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromBurnMediaError si verifica quando si verifica un errore durante la masterizzazione di un singolo elemento multimediale in un CD.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Evento CdromBurnMediaError dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fac8902fe8700171d2c909e8140c74c8cc3c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323925"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d8e2d-104">Evento CdromBurnMediaError dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d8e2d-104">CdromBurnMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d8e2d-105">L'evento CdromBurnMediaError si verifica quando si verifica un errore durante la masterizzazione di un singolo elemento multimediale in un CD.</span><span class="sxs-lookup"><span data-stu-id="d8e2d-105">The CdromBurnMediaError event occurs when an error happens while burning an individual media item to a CD.</span></span>

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a><span data-ttu-id="d8e2d-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="d8e2d-106">Event Data</span></span>

<span data-ttu-id="d8e2d-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CdromBurnMediaErrorEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="d8e2d-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEventHandler**.</span></span> <span data-ttu-id="d8e2d-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="d8e2d-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="d8e2d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d8e2d-109">Property</span></span>   | <span data-ttu-id="d8e2d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8e2d-110">Description</span></span>                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e2d-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="d8e2d-111">pCdromBurn</span></span> | <span data-ttu-id="d8e2d-112">Interfaccia WMPLib. IWMPCdromBurnThe che rappresenta l'operazione di masterizzazione che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="d8e2d-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/>               |
| <span data-ttu-id="d8e2d-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="d8e2d-113">pMedia</span></span>     | <span data-ttu-id="d8e2d-114">Elemento multimediale System. ObjectThe che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="d8e2d-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="d8e2d-115">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPMedia per accedervi.</span><span class="sxs-lookup"><span data-stu-id="d8e2d-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d8e2d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8e2d-116">Remarks</span></span>

<span data-ttu-id="d8e2d-117">Per acquisire gli errori generici, gestire AxWMPLib. \_ \_Evento CdromBurnError WMPOCXEvents.</span><span class="sxs-lookup"><span data-stu-id="d8e2d-117">To capture generic errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e2d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8e2d-118">Requirements</span></span>



| <span data-ttu-id="d8e2d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8e2d-119">Requirement</span></span> | <span data-ttu-id="d8e2d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d8e2d-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e2d-121">Versione</span><span class="sxs-lookup"><span data-stu-id="d8e2d-121">Version</span></span><br/>   | <span data-ttu-id="d8e2d-122">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="d8e2d-122">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="d8e2d-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d8e2d-123">Namespace</span></span><br/> | <span data-ttu-id="d8e2d-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d8e2d-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d8e2d-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="d8e2d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d8e2d-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d8e2d-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8e2d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8e2d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e2d-128">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d8e2d-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8e2d-129">**Evento AxWindowsMediaPlayer. CdromBurnError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d8e2d-129">**AxWindowsMediaPlayer.CdromBurnError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[<span data-ttu-id="d8e2d-130">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d8e2d-130">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8e2d-131">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d8e2d-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





