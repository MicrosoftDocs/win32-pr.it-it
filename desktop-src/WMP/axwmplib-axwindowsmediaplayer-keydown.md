---
title: Evento KeyDown dell'oggetto AxWindowsMediaPlayer
description: L'evento KeyDown si verifica quando viene premuto un tasto. | Evento KeyDown dell'oggetto AxWindowsMediaPlayer
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Evento KeyDown dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331890"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="203d3-105">Evento KeyDown dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="203d3-105">KeyDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="203d3-106">L'evento KeyDown si verifica quando viene premuto un tasto.</span><span class="sxs-lookup"><span data-stu-id="203d3-106">The KeyDown event occurs when a key is pressed.</span></span>

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a><span data-ttu-id="203d3-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="203d3-107">Event Data</span></span>

<span data-ttu-id="203d3-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_KeyDownEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="203d3-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEventHandler**.</span></span> <span data-ttu-id="203d3-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="203d3-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="203d3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="203d3-110">Property</span></span>    | <span data-ttu-id="203d3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="203d3-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="203d3-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="203d3-112">nKeyCode</span></span>    | <span data-ttu-id="203d3-113">System. Int16Specifies in cui viene premuto il tasto fisico.</span><span class="sxs-lookup"><span data-stu-id="203d3-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="203d3-114">Per i valori possibili, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="203d3-114">For possible values, see Remarks.</span></span><br/>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="203d3-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="203d3-115">nShiftState</span></span> | <span data-ttu-id="203d3-116">System. Int16a bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="203d3-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="203d3-117">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="203d3-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="203d3-118">L'argomento Shift indica lo stato di queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="203d3-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="203d3-119">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="203d3-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="203d3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="203d3-120">Remarks</span></span>

<span data-ttu-id="203d3-121">La proprietà **nKeyCode** specifica una chiave fisica.</span><span class="sxs-lookup"><span data-stu-id="203d3-121">The **nKeyCode** property specifies a physical key.</span></span> <span data-ttu-id="203d3-122">Nelle tabelle seguenti vengono illustrati i valori possibili per le chiavi principali in una tastiera standard.</span><span class="sxs-lookup"><span data-stu-id="203d3-122">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="203d3-123">Valori per le chiavi principali.</span><span class="sxs-lookup"><span data-stu-id="203d3-123">Values for the main keys.</span></span>



| <span data-ttu-id="203d3-124">Chiave</span><span class="sxs-lookup"><span data-stu-id="203d3-124">Key</span></span>                     | <span data-ttu-id="203d3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="203d3-125">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="203d3-126">A-Z</span><span class="sxs-lookup"><span data-stu-id="203d3-126">A-Z</span></span>                     | <span data-ttu-id="203d3-127">65-90</span><span class="sxs-lookup"><span data-stu-id="203d3-127">65-90</span></span>   |
| <span data-ttu-id="203d3-128">0-9</span><span class="sxs-lookup"><span data-stu-id="203d3-128">0-9</span></span>                     | <span data-ttu-id="203d3-129">48-56</span><span class="sxs-lookup"><span data-stu-id="203d3-129">48-56</span></span>   |
| <span data-ttu-id="203d3-130">F1-F12</span><span class="sxs-lookup"><span data-stu-id="203d3-130">F1-F12</span></span>                  | <span data-ttu-id="203d3-131">112-123</span><span class="sxs-lookup"><span data-stu-id="203d3-131">112-123</span></span> |
| <span data-ttu-id="203d3-132">ESC</span><span class="sxs-lookup"><span data-stu-id="203d3-132">ESC</span></span>                     | <span data-ttu-id="203d3-133">27</span><span class="sxs-lookup"><span data-stu-id="203d3-133">27</span></span>      |
| <span data-ttu-id="203d3-134">TAB</span><span class="sxs-lookup"><span data-stu-id="203d3-134">TAB</span></span>                     | <span data-ttu-id="203d3-135">9</span><span class="sxs-lookup"><span data-stu-id="203d3-135">9</span></span>       |
| <span data-ttu-id="203d3-136">Bloc Maiusc</span><span class="sxs-lookup"><span data-stu-id="203d3-136">CAPS LOCK</span></span>               | <span data-ttu-id="203d3-137">20</span><span class="sxs-lookup"><span data-stu-id="203d3-137">20</span></span>      |
| <span data-ttu-id="203d3-138">Maiusc (a sinistra o a destra)</span><span class="sxs-lookup"><span data-stu-id="203d3-138">SHIFT (left or right)</span></span>   | <span data-ttu-id="203d3-139">16</span><span class="sxs-lookup"><span data-stu-id="203d3-139">16</span></span>      |
| <span data-ttu-id="203d3-140">CTRL (a sinistra o a destra)</span><span class="sxs-lookup"><span data-stu-id="203d3-140">CTRL (left or right)</span></span>    | <span data-ttu-id="203d3-141">17</span><span class="sxs-lookup"><span data-stu-id="203d3-141">17</span></span>      |
| <span data-ttu-id="203d3-142">ALT (a sinistra o a destra)</span><span class="sxs-lookup"><span data-stu-id="203d3-142">ALT (left or right)</span></span>     | <span data-ttu-id="203d3-143">18</span><span class="sxs-lookup"><span data-stu-id="203d3-143">18</span></span>      |
| <span data-ttu-id="203d3-144">SPACE</span><span class="sxs-lookup"><span data-stu-id="203d3-144">SPACE</span></span>                   | <span data-ttu-id="203d3-145">32</span><span class="sxs-lookup"><span data-stu-id="203d3-145">32</span></span>      |
| <span data-ttu-id="203d3-146">BACKSPACE</span><span class="sxs-lookup"><span data-stu-id="203d3-146">BACKSPACE</span></span>               | <span data-ttu-id="203d3-147">8</span><span class="sxs-lookup"><span data-stu-id="203d3-147">8</span></span>       |
| <span data-ttu-id="203d3-148">INVIO</span><span class="sxs-lookup"><span data-stu-id="203d3-148">ENTER</span></span>                   | <span data-ttu-id="203d3-149">13</span><span class="sxs-lookup"><span data-stu-id="203d3-149">13</span></span>      |
| <span data-ttu-id="203d3-150">Tasto logo Windows, a sinistra</span><span class="sxs-lookup"><span data-stu-id="203d3-150">Windows logo key, left</span></span>  | <span data-ttu-id="203d3-151">91</span><span class="sxs-lookup"><span data-stu-id="203d3-151">91</span></span>      |
| <span data-ttu-id="203d3-152">Tasto logo Windows, a destra</span><span class="sxs-lookup"><span data-stu-id="203d3-152">Windows logo key, right</span></span> | <span data-ttu-id="203d3-153">92</span><span class="sxs-lookup"><span data-stu-id="203d3-153">92</span></span>      |
| <span data-ttu-id="203d3-154">Chiave applicazione</span><span class="sxs-lookup"><span data-stu-id="203d3-154">Application key</span></span>         | <span data-ttu-id="203d3-155">93</span><span class="sxs-lookup"><span data-stu-id="203d3-155">93</span></span>      |



 

<span data-ttu-id="203d3-156">Valori per le chiavi del tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="203d3-156">Values for the number pad keys.</span></span>



| <span data-ttu-id="203d3-157">Chiave</span><span class="sxs-lookup"><span data-stu-id="203d3-157">Key</span></span>               | <span data-ttu-id="203d3-158">Valore</span><span class="sxs-lookup"><span data-stu-id="203d3-158">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="203d3-159">0-9</span><span class="sxs-lookup"><span data-stu-id="203d3-159">0-9</span></span>               | <span data-ttu-id="203d3-160">96-105</span><span class="sxs-lookup"><span data-stu-id="203d3-160">96-105</span></span> |
| <span data-ttu-id="203d3-161">BLOC NUM</span><span class="sxs-lookup"><span data-stu-id="203d3-161">NUM LOCK</span></span>          | <span data-ttu-id="203d3-162">144</span><span class="sxs-lookup"><span data-stu-id="203d3-162">144</span></span>    |
| <span data-ttu-id="203d3-163">Divisione (/)</span><span class="sxs-lookup"><span data-stu-id="203d3-163">DIVIDE (/)</span></span>        | <span data-ttu-id="203d3-164">111</span><span class="sxs-lookup"><span data-stu-id="203d3-164">111</span></span>    |
| <span data-ttu-id="203d3-165">MULTIPLY ( \* )</span><span class="sxs-lookup"><span data-stu-id="203d3-165">MULTIPLY (\*)</span></span>     | <span data-ttu-id="203d3-166">106</span><span class="sxs-lookup"><span data-stu-id="203d3-166">106</span></span>    |
| <span data-ttu-id="203d3-167">SOTTRAzione (-)</span><span class="sxs-lookup"><span data-stu-id="203d3-167">SUBTRACT (-)</span></span>      | <span data-ttu-id="203d3-168">109</span><span class="sxs-lookup"><span data-stu-id="203d3-168">109</span></span>    |
| <span data-ttu-id="203d3-169">AGGIUNGI (+)</span><span class="sxs-lookup"><span data-stu-id="203d3-169">ADD (+)</span></span>           | <span data-ttu-id="203d3-170">107</span><span class="sxs-lookup"><span data-stu-id="203d3-170">107</span></span>    |
| <span data-ttu-id="203d3-171">SEPARATOre (invio)</span><span class="sxs-lookup"><span data-stu-id="203d3-171">SEPARATOR (Enter)</span></span> | <span data-ttu-id="203d3-172">108</span><span class="sxs-lookup"><span data-stu-id="203d3-172">108</span></span>    |
| <span data-ttu-id="203d3-173">DECIMALE (.)</span><span class="sxs-lookup"><span data-stu-id="203d3-173">DECIMAL (.)</span></span>       | <span data-ttu-id="203d3-174">110</span><span class="sxs-lookup"><span data-stu-id="203d3-174">110</span></span>    |



 

<span data-ttu-id="203d3-175">Valori per i tasti di navigazione.</span><span class="sxs-lookup"><span data-stu-id="203d3-175">Values for the navigation keys.</span></span>



| <span data-ttu-id="203d3-176">Chiave</span><span class="sxs-lookup"><span data-stu-id="203d3-176">Key</span></span>         | <span data-ttu-id="203d3-177">Valore</span><span class="sxs-lookup"><span data-stu-id="203d3-177">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="203d3-178">INSERT</span><span class="sxs-lookup"><span data-stu-id="203d3-178">INSERT</span></span>      | <span data-ttu-id="203d3-179">45</span><span class="sxs-lookup"><span data-stu-id="203d3-179">45</span></span>    |
| <span data-ttu-id="203d3-180">DELETE</span><span class="sxs-lookup"><span data-stu-id="203d3-180">DELETE</span></span>      | <span data-ttu-id="203d3-181">46</span><span class="sxs-lookup"><span data-stu-id="203d3-181">46</span></span>    |
| <span data-ttu-id="203d3-182">HOME</span><span class="sxs-lookup"><span data-stu-id="203d3-182">HOME</span></span>        | <span data-ttu-id="203d3-183">36</span><span class="sxs-lookup"><span data-stu-id="203d3-183">36</span></span>    |
| <span data-ttu-id="203d3-184">FINE</span><span class="sxs-lookup"><span data-stu-id="203d3-184">END</span></span>         | <span data-ttu-id="203d3-185">35</span><span class="sxs-lookup"><span data-stu-id="203d3-185">35</span></span>    |
| <span data-ttu-id="203d3-186">PGSU</span><span class="sxs-lookup"><span data-stu-id="203d3-186">PAGE UP</span></span>     | <span data-ttu-id="203d3-187">33</span><span class="sxs-lookup"><span data-stu-id="203d3-187">33</span></span>    |
| <span data-ttu-id="203d3-188">PGGIÙ</span><span class="sxs-lookup"><span data-stu-id="203d3-188">PAGE DOWN</span></span>   | <span data-ttu-id="203d3-189">34</span><span class="sxs-lookup"><span data-stu-id="203d3-189">34</span></span>    |
| <span data-ttu-id="203d3-190">FRECCIA SU</span><span class="sxs-lookup"><span data-stu-id="203d3-190">UP ARROW</span></span>    | <span data-ttu-id="203d3-191">38</span><span class="sxs-lookup"><span data-stu-id="203d3-191">38</span></span>    |
| <span data-ttu-id="203d3-192">Freccia GIÙ</span><span class="sxs-lookup"><span data-stu-id="203d3-192">DOWN ARROW</span></span>  | <span data-ttu-id="203d3-193">40</span><span class="sxs-lookup"><span data-stu-id="203d3-193">40</span></span>    |
| <span data-ttu-id="203d3-194">FRECCIA SINISTRA</span><span class="sxs-lookup"><span data-stu-id="203d3-194">LEFT ARROW</span></span>  | <span data-ttu-id="203d3-195">37</span><span class="sxs-lookup"><span data-stu-id="203d3-195">37</span></span>    |
| <span data-ttu-id="203d3-196">FRECCIA DESTRA</span><span class="sxs-lookup"><span data-stu-id="203d3-196">RIGHT ARROW</span></span> | <span data-ttu-id="203d3-197">39</span><span class="sxs-lookup"><span data-stu-id="203d3-197">39</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="203d3-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="203d3-198">Requirements</span></span>



| <span data-ttu-id="203d3-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="203d3-199">Requirement</span></span> | <span data-ttu-id="203d3-200">Valore</span><span class="sxs-lookup"><span data-stu-id="203d3-200">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="203d3-201">Versione</span><span class="sxs-lookup"><span data-stu-id="203d3-201">Version</span></span><br/>   | <span data-ttu-id="203d3-202">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="203d3-202">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="203d3-203">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="203d3-203">Namespace</span></span><br/> | <span data-ttu-id="203d3-204">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="203d3-204">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="203d3-205">Assembly</span><span class="sxs-lookup"><span data-stu-id="203d3-205">Assembly</span></span><br/>  | <dl> <span data-ttu-id="203d3-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="203d3-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="203d3-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="203d3-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203d3-208">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="203d3-208">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





