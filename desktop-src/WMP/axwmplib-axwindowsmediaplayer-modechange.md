---
title: Evento ModeChange dell'oggetto AxWindowsMediaPlayer
description: L'evento ModeChange si verifica quando viene modificata una modalità di Windows Media Player. | Evento ModeChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Evento ModeChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330012"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4489d-105">Evento ModeChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4489d-105">ModeChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4489d-106">L'evento ModeChange si verifica quando viene modificata una modalità di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4489d-106">The ModeChange event occurs when a mode of Windows Media Player is changed.</span></span>

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a><span data-ttu-id="4489d-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="4489d-107">Event Data</span></span>

<span data-ttu-id="4489d-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_ModeChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="4489d-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEventHandler**.</span></span> <span data-ttu-id="4489d-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="4489d-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4489d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4489d-110">Property</span></span> | <span data-ttu-id="4489d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4489d-111">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4489d-112">modeName</span><span class="sxs-lookup"><span data-stu-id="4489d-112">modeName</span></span> | <span data-ttu-id="4489d-113">System. StringIndicates la modalità modificata.</span><span class="sxs-lookup"><span data-stu-id="4489d-113">System.StringIndicates the mode that was changed.</span></span> <span data-ttu-id="4489d-114">Per i valori possibili, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4489d-114">For possible values, see Remarks.</span></span><br/> |
| <span data-ttu-id="4489d-115">newValue</span><span class="sxs-lookup"><span data-stu-id="4489d-115">newValue</span></span> | <span data-ttu-id="4489d-116">System. BooleanIndicates il nuovo stato della modalità specificata.</span><span class="sxs-lookup"><span data-stu-id="4489d-116">System.BooleanIndicates the new state of the specified mode.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="4489d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4489d-117">Remarks</span></span>

<span data-ttu-id="4489d-118">Nella tabella seguente sono riportati i valori possibili per la proprietà modeName.</span><span class="sxs-lookup"><span data-stu-id="4489d-118">The following table shows the possible values for the modeName property.</span></span>



| <span data-ttu-id="4489d-119">string</span><span class="sxs-lookup"><span data-stu-id="4489d-119">String</span></span>  | <span data-ttu-id="4489d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4489d-120">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="4489d-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="4489d-121">shuffle</span></span> | <span data-ttu-id="4489d-122">Le tracce vengono riprodotte in ordine casuale.</span><span class="sxs-lookup"><span data-stu-id="4489d-122">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="4489d-123">loop</span><span class="sxs-lookup"><span data-stu-id="4489d-123">loop</span></span>    | <span data-ttu-id="4489d-124">L'intera sequenza di tracce viene riprodotta ripetutamente.</span><span class="sxs-lookup"><span data-stu-id="4489d-124">The entire sequence of tracks is played repeatedly.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="4489d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4489d-125">Requirements</span></span>



| <span data-ttu-id="4489d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4489d-126">Requirement</span></span> | <span data-ttu-id="4489d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4489d-127">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4489d-128">Versione</span><span class="sxs-lookup"><span data-stu-id="4489d-128">Version</span></span><br/>   | <span data-ttu-id="4489d-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="4489d-129">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4489d-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4489d-130">Namespace</span></span><br/> | <span data-ttu-id="4489d-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4489d-131">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4489d-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="4489d-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4489d-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4489d-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4489d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4489d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4489d-135">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4489d-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4489d-136">**IWMPSettings. getMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4489d-136">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4489d-137">**IWMPSettings. semode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4489d-137">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





