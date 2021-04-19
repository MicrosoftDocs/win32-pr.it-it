---
title: Evento MouseUp dell'oggetto AxWindowsMediaPlayer
description: L'evento MouseUp si verifica quando l'utente rilascia un pulsante del mouse. | Evento MouseUp dell'oggetto AxWindowsMediaPlayer
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- Evento MouseUp dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- MouseUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2bf9c209b4fa263eb0a6cbcba2a32b0b1c46fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329444"
---
# <a name="mouseup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="171fd-105">Evento MouseUp dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="171fd-105">MouseUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="171fd-106">L'evento MouseUp si verifica quando l'utente rilascia un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="171fd-106">The MouseUp event occurs when the user releases a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseUpEvent(
  object sender,
  _WMPOCXEvents_MouseUpEvent e
)

[Visual Basic]
Private Sub player_MouseUpEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseUpEvent
) Handles player.MouseUpEvent
```

## <a name="event-data"></a><span data-ttu-id="171fd-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="171fd-107">Event Data</span></span>

<span data-ttu-id="171fd-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MouseUpEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="171fd-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEventHandler**.</span></span> <span data-ttu-id="171fd-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseUpEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="171fd-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="171fd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="171fd-110">Property</span></span>    | <span data-ttu-id="171fd-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="171fd-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="171fd-112">Npulsante</span><span class="sxs-lookup"><span data-stu-id="171fd-112">nButton</span></span>     | <span data-ttu-id="171fd-113">System. Int16a bit con bit corrispondente al pulsante sinistro (bit 0), pulsante destro (bit 1) e pulsante centrale (bit 2).</span><span class="sxs-lookup"><span data-stu-id="171fd-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="171fd-114">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="171fd-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="171fd-115">Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.</span><span class="sxs-lookup"><span data-stu-id="171fd-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="171fd-116">nShiftState</span><span class="sxs-lookup"><span data-stu-id="171fd-116">nShiftState</span></span> | <span data-ttu-id="171fd-117">System. Int16a bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="171fd-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="171fd-118">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="171fd-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="171fd-119">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="171fd-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="171fd-120">fX</span><span class="sxs-lookup"><span data-stu-id="171fd-120">fX</span></span>          | <span data-ttu-id="171fd-121">System. Int32The: coordinata x del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="171fd-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="171fd-122">fY</span><span class="sxs-lookup"><span data-stu-id="171fd-122">fY</span></span>          | <span data-ttu-id="171fd-123">Coordinata y di System. Int32The del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="171fd-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="171fd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="171fd-124">Requirements</span></span>



| <span data-ttu-id="171fd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="171fd-125">Requirement</span></span> | <span data-ttu-id="171fd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="171fd-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="171fd-127">Versione</span><span class="sxs-lookup"><span data-stu-id="171fd-127">Version</span></span><br/>   | <span data-ttu-id="171fd-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="171fd-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="171fd-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="171fd-129">Namespace</span></span><br/> | <span data-ttu-id="171fd-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="171fd-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="171fd-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="171fd-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="171fd-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="171fd-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="171fd-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="171fd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="171fd-134">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="171fd-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





