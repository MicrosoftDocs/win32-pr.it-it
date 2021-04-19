---
title: Evento Click dell'oggetto AxWindowsMediaPlayer
description: L'evento click si verifica quando l'utente fa clic con un pulsante del mouse su un controllo Media Player di Windows.
ms.assetid: 41a719a2-103a-46b5-806d-5c21c4a09e00
keywords:
- Evento Click dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- Click Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d316e5dc4c12e75d75dd0b292c1df6db974bc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323913"
---
# <a name="click-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9489d-104">Evento Click dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="9489d-104">Click Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9489d-105">L'evento click si verifica quando l'utente fa clic con un pulsante del mouse su un controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="9489d-105">The Click event occurs when the user clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_OnClick(
  object  sender,
  _WMPOCXEvents_ClickEvent e
);

[Visual Basic]
Private Sub player_OnClick(  
  sender As Object,
  e As WMPOCXEvents_ClickEvent
) Handles player.ClickEvent
```

## <a name="event-data"></a><span data-ttu-id="9489d-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="9489d-106">Event Data</span></span>

<span data-ttu-id="9489d-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_ClickEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="9489d-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ClickEventHandler**.</span></span> <span data-ttu-id="9489d-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ ClickEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="9489d-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="9489d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9489d-109">Property</span></span>    | <span data-ttu-id="9489d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9489d-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9489d-111">Npulsante</span><span class="sxs-lookup"><span data-stu-id="9489d-111">nButton</span></span>     | <span data-ttu-id="9489d-112">System. Int16a bit con bit corrispondente al pulsante sinistro (bit 0), pulsante destro (bit 1) e pulsante centrale (bit 2).</span><span class="sxs-lookup"><span data-stu-id="9489d-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="9489d-113">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="9489d-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="9489d-114">Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.</span><span class="sxs-lookup"><span data-stu-id="9489d-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="9489d-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="9489d-115">nShiftState</span></span> | <span data-ttu-id="9489d-116">System. Int16a bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="9489d-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="9489d-117">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="9489d-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="9489d-118">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="9489d-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="9489d-119">fX</span><span class="sxs-lookup"><span data-stu-id="9489d-119">fX</span></span>          | <span data-ttu-id="9489d-120">System. Int32The: coordinata x del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="9489d-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="9489d-121">fY</span><span class="sxs-lookup"><span data-stu-id="9489d-121">fY</span></span>          | <span data-ttu-id="9489d-122">Coordinata y di System. Int32The del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="9489d-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="9489d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9489d-123">Requirements</span></span>



| <span data-ttu-id="9489d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9489d-124">Requirement</span></span> | <span data-ttu-id="9489d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9489d-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9489d-126">Versione</span><span class="sxs-lookup"><span data-stu-id="9489d-126">Version</span></span><br/>   | <span data-ttu-id="9489d-127">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9489d-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9489d-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9489d-128">Namespace</span></span><br/> | <span data-ttu-id="9489d-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9489d-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9489d-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="9489d-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9489d-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9489d-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9489d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9489d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9489d-133">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9489d-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





