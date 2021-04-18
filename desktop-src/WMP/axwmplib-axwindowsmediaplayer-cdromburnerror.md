---
title: Evento CdromBurnError dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromBurnError si verifica quando si verifica un errore generico durante un'operazione di masterizzazione del CD.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Evento CdromBurnError dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323927"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d22bb-104">Evento CdromBurnError dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d22bb-104">CdromBurnError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d22bb-105">L'evento CdromBurnError si verifica quando si verifica un errore generico durante un'operazione di masterizzazione del CD.</span><span class="sxs-lookup"><span data-stu-id="d22bb-105">The CdromBurnError event occurs when a generic error happens during a CD burning operation.</span></span>

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a><span data-ttu-id="d22bb-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="d22bb-106">Event Data</span></span>

<span data-ttu-id="d22bb-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CdromBurnErrorEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="d22bb-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEventHandler**.</span></span> <span data-ttu-id="d22bb-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="d22bb-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="d22bb-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d22bb-109">Property</span></span>   | <span data-ttu-id="d22bb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d22bb-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d22bb-111">hrError</span><span class="sxs-lookup"><span data-stu-id="d22bb-111">hrError</span></span>    | <span data-ttu-id="d22bb-112">**System. Int32** Errore che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="d22bb-112">**System.Int32** The error that raised the event.</span></span><br/>                                               |
| <span data-ttu-id="d22bb-113">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="d22bb-113">pCdromBurn</span></span> | <span data-ttu-id="d22bb-114">Interfaccia WMPLib. IWMPCdromBurnThe che rappresenta l'operazione di masterizzazione che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="d22bb-114">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d22bb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d22bb-115">Remarks</span></span>

<span data-ttu-id="d22bb-116">Per acquisire gli errori specifici del supporto, gestire AxWMPLib. \_ \_Evento CdromBurnMediaError WMPOCXEvents.</span><span class="sxs-lookup"><span data-stu-id="d22bb-116">To capture media specific errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="d22bb-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d22bb-117">Requirements</span></span>



| <span data-ttu-id="d22bb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d22bb-118">Requirement</span></span> | <span data-ttu-id="d22bb-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d22bb-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d22bb-120">Versione</span><span class="sxs-lookup"><span data-stu-id="d22bb-120">Version</span></span><br/>   | <span data-ttu-id="d22bb-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="d22bb-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="d22bb-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d22bb-122">Namespace</span></span><br/> | <span data-ttu-id="d22bb-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d22bb-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d22bb-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="d22bb-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d22bb-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d22bb-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d22bb-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d22bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22bb-127">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d22bb-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d22bb-128">**Evento AxWindowsMediaPlayer. CdromBurnMediaError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d22bb-128">**AxWindowsMediaPlayer.CdromBurnMediaError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[<span data-ttu-id="d22bb-129">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d22bb-129">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





