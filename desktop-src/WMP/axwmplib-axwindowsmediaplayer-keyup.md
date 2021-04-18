---
title: Evento KeyUp dell'oggetto AxWindowsMediaPlayer
description: L'evento KeyUp si verifica quando viene rilasciato un tasto. | Evento KeyUp dell'oggetto AxWindowsMediaPlayer
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- Evento KeyUp dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509f520ff7624b0b29302d7bf5cd825cd45b4254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330014"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e57ce-105">Evento KeyUp dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="e57ce-105">KeyUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e57ce-106">L'evento KeyUp si verifica quando viene rilasciato un tasto.</span><span class="sxs-lookup"><span data-stu-id="e57ce-106">The KeyUp event occurs when a key is released.</span></span>

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a><span data-ttu-id="e57ce-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="e57ce-107">Event Data</span></span>

<span data-ttu-id="e57ce-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_KeyUpEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="e57ce-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEventHandler**.</span></span> <span data-ttu-id="e57ce-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="e57ce-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="e57ce-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e57ce-110">Property</span></span>    | <span data-ttu-id="e57ce-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e57ce-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e57ce-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="e57ce-112">nKeyCode</span></span>    | <span data-ttu-id="e57ce-113">System. Int16Specifies in cui viene premuto il tasto fisico.</span><span class="sxs-lookup"><span data-stu-id="e57ce-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="e57ce-114">Per i valori possibili, vedere la sezione Osservazioni dell'evento KeyDown.</span><span class="sxs-lookup"><span data-stu-id="e57ce-114">For possible values, see the Remarks section of the KeyDown event.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="e57ce-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="e57ce-115">nShiftState</span></span> | <span data-ttu-id="e57ce-116">System. Int16a bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="e57ce-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="e57ce-117">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="e57ce-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="e57ce-118">L'argomento Shift indica lo stato di queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="e57ce-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="e57ce-119">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="e57ce-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e57ce-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e57ce-120">Requirements</span></span>



| <span data-ttu-id="e57ce-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e57ce-121">Requirement</span></span> | <span data-ttu-id="e57ce-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e57ce-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e57ce-123">Versione</span><span class="sxs-lookup"><span data-stu-id="e57ce-123">Version</span></span><br/>   | <span data-ttu-id="e57ce-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e57ce-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e57ce-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e57ce-125">Namespace</span></span><br/> | <span data-ttu-id="e57ce-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="e57ce-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e57ce-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="e57ce-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e57ce-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e57ce-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e57ce-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e57ce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e57ce-130">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e57ce-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





