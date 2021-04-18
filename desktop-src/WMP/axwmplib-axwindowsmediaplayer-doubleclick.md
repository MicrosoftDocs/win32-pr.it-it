---
title: Evento DoubleClick dell'oggetto AxWindowsMediaPlayer
description: L'evento DoubleClick si verifica quando l'utente fa doppio clic con un pulsante del mouse su un controllo Media Player di Windows.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Evento DoubleClick dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327628"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="cdd37-104">Evento DoubleClick dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="cdd37-104">DoubleClick Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="cdd37-105">L'evento DoubleClick si verifica quando l'utente fa doppio clic con un pulsante del mouse su un controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="cdd37-105">The DoubleClick event occurs when the user double-clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a><span data-ttu-id="cdd37-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="cdd37-106">Event Data</span></span>

<span data-ttu-id="cdd37-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_DoubleClickEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="cdd37-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEventHandler**.</span></span> <span data-ttu-id="cdd37-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="cdd37-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="cdd37-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cdd37-109">Property</span></span>    | <span data-ttu-id="cdd37-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdd37-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd37-111">Npulsante</span><span class="sxs-lookup"><span data-stu-id="cdd37-111">nButton</span></span>     | <span data-ttu-id="cdd37-112">System. Int16a bit con bit corrispondente al pulsante sinistro (bit 0), pulsante destro (bit 1) e pulsante centrale (bit 2).</span><span class="sxs-lookup"><span data-stu-id="cdd37-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="cdd37-113">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="cdd37-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="cdd37-114">Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.</span><span class="sxs-lookup"><span data-stu-id="cdd37-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="cdd37-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="cdd37-115">nShiftState</span></span> | <span data-ttu-id="cdd37-116">System. Int16a bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="cdd37-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="cdd37-117">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="cdd37-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="cdd37-118">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="cdd37-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="cdd37-119">fX</span><span class="sxs-lookup"><span data-stu-id="cdd37-119">fX</span></span>          | <span data-ttu-id="cdd37-120">System. Int32The: coordinata x del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="cdd37-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd37-121">fY</span><span class="sxs-lookup"><span data-stu-id="cdd37-121">fY</span></span>          | <span data-ttu-id="cdd37-122">Coordinata y di System. Int32The del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="cdd37-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="cdd37-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdd37-123">Requirements</span></span>



| <span data-ttu-id="cdd37-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdd37-124">Requirement</span></span> | <span data-ttu-id="cdd37-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cdd37-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd37-126">Versione</span><span class="sxs-lookup"><span data-stu-id="cdd37-126">Version</span></span><br/>   | <span data-ttu-id="cdd37-127">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cdd37-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cdd37-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cdd37-128">Namespace</span></span><br/> | <span data-ttu-id="cdd37-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="cdd37-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cdd37-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="cdd37-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cdd37-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd37-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd37-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdd37-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd37-133">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cdd37-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





