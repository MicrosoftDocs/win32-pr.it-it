---
title: Evento PositionChange dell'oggetto AxWindowsMediaPlayer
description: L'evento PositionChange si verifica quando la posizione di riproduzione corrente all'interno dell'elemento multimediale è stata modificata.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Evento PositionChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326226"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="2a7ae-104">Evento PositionChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="2a7ae-104">PositionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="2a7ae-105">L'evento PositionChange si verifica quando la posizione di riproduzione corrente all'interno dell'elemento multimediale è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-105">The PositionChange event occurs when the current playback position within the media item has been changed.</span></span>

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a><span data-ttu-id="2a7ae-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="2a7ae-106">Event Data</span></span>

<span data-ttu-id="2a7ae-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_PositionChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEventHandler**.</span></span> <span data-ttu-id="2a7ae-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="2a7ae-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a7ae-109">Property</span></span>    | <span data-ttu-id="2a7ae-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a7ae-110">Description</span></span>                                         |
|-------------|-----------------------------------------------------|
| <span data-ttu-id="2a7ae-111">oldPosition</span><span class="sxs-lookup"><span data-stu-id="2a7ae-111">oldPosition</span></span> | <span data-ttu-id="2a7ae-112">System. DoubleSpecifies la posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-112">System.DoubleSpecifies the old position.</span></span><br/> |
| <span data-ttu-id="2a7ae-113">newPosition</span><span class="sxs-lookup"><span data-stu-id="2a7ae-113">newPosition</span></span> | <span data-ttu-id="2a7ae-114">System. DoubleSpecifies la nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-114">System.DoubleSpecifies the new position.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2a7ae-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a7ae-115">Remarks</span></span>

<span data-ttu-id="2a7ae-116">Questo evento non viene generato periodicamente durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-116">This event is not raised routinely during playback.</span></span> <span data-ttu-id="2a7ae-117">Si verifica solo quando un elemento modifica attivamente la posizione corrente dell'elemento multimediale in riproduzione, ad esempio quando l'utente sposta l'handle di ricerca o quando viene eseguito il codice che specifica un valore per IWMPControls. **currentPosition**.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-117">It only occurs when something actively changes the current position of the playing media item, such as when the user moves the seek handle or when code is executed that specifies a value for IWMPControls.**currentPosition**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a7ae-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a7ae-118">Requirements</span></span>



| <span data-ttu-id="2a7ae-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a7ae-119">Requirement</span></span> | <span data-ttu-id="2a7ae-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2a7ae-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7ae-121">Versione</span><span class="sxs-lookup"><span data-stu-id="2a7ae-121">Version</span></span><br/>   | <span data-ttu-id="2a7ae-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2a7ae-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2a7ae-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2a7ae-123">Namespace</span></span><br/> | <span data-ttu-id="2a7ae-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2a7ae-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2a7ae-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="2a7ae-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2a7ae-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2a7ae-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a7ae-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a7ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a7ae-128">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2a7ae-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2a7ae-129">**IWMPControls. currentPosition (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2a7ae-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





