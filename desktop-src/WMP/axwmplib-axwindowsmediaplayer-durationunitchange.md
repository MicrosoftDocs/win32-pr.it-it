---
title: Evento DurationUnitChange dell'oggetto AxWindowsMediaPlayer
description: L'evento DurationUnitChange è riservato per un utilizzo futuro.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Evento DurationUnitChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f90aa052c61893d83683d10f482cd05841a49fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324401"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3bb2e-104">Evento DurationUnitChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="3bb2e-104">DurationUnitChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3bb2e-105">L'evento DurationUnitChange è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="3bb2e-105">The DurationUnitChange event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a><span data-ttu-id="3bb2e-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="3bb2e-106">Event Data</span></span>

<span data-ttu-id="3bb2e-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_DurationUnitChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="3bb2e-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEventHandler**.</span></span> <span data-ttu-id="3bb2e-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="3bb2e-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="3bb2e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3bb2e-109">Property</span></span>        | <span data-ttu-id="3bb2e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bb2e-110">Description</span></span>                               |
|-----------------|-------------------------------------------|
| <span data-ttu-id="3bb2e-111">newDurationUnit</span><span class="sxs-lookup"><span data-stu-id="3bb2e-111">newDurationUnit</span></span> | <span data-ttu-id="3bb2e-112">**System. Int32** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="3bb2e-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3bb2e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bb2e-113">Remarks</span></span>

<span data-ttu-id="3bb2e-114">Questo evento è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="3bb2e-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb2e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bb2e-115">Requirements</span></span>



| <span data-ttu-id="3bb2e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bb2e-116">Requirement</span></span> | <span data-ttu-id="3bb2e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3bb2e-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb2e-118">Versione</span><span class="sxs-lookup"><span data-stu-id="3bb2e-118">Version</span></span><br/>   | <span data-ttu-id="3bb2e-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3bb2e-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3bb2e-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3bb2e-120">Namespace</span></span><br/> | <span data-ttu-id="3bb2e-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3bb2e-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3bb2e-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="3bb2e-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3bb2e-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3bb2e-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bb2e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bb2e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb2e-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3bb2e-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





