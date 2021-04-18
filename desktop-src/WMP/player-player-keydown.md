---
title: Evento Player. KeyDown
description: L'evento KeyDown si verifica quando viene premuto un tasto. | Evento Player. KeyDown
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Media Player di Windows evento KeyDown
- KeyDown Event Windows Media Player, classe Player
- Classe Player Windows Media Player, evento KeyDown
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331859"
---
# <a name="playerkeydown-event"></a><span data-ttu-id="60416-107">Evento Player. KeyDown</span><span class="sxs-lookup"><span data-stu-id="60416-107">Player.KeyDown event</span></span>

<span data-ttu-id="60416-108">L'evento **KeyDown** si verifica quando viene premuto un tasto.</span><span class="sxs-lookup"><span data-stu-id="60416-108">The **KeyDown** event occurs when a key is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="60416-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60416-109">Syntax</span></span>


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="60416-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="60416-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60416-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="60416-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="60416-112">**Numero** (**int**) che specifica quale tasto fisico è premuto.</span><span class="sxs-lookup"><span data-stu-id="60416-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="60416-113">Per i valori possibili, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="60416-113">For possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="60416-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="60416-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="60416-115">**Number** (**int**) che specifica un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto Ctrl (bit 1) e il tasto Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="60416-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="60416-116">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="60416-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="60416-117">L'argomento Shift indica lo stato di queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="60416-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="60416-118">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="60416-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60416-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60416-119">Return value</span></span>

<span data-ttu-id="60416-120">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="60416-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60416-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="60416-121">Remarks</span></span>

<span data-ttu-id="60416-122">L'argomento *nKeyCode* specifica una chiave fisica.</span><span class="sxs-lookup"><span data-stu-id="60416-122">The *nKeyCode* argument specifies a physical key.</span></span> <span data-ttu-id="60416-123">Nelle tabelle seguenti vengono illustrati i valori possibili per le chiavi principali in una tastiera standard.</span><span class="sxs-lookup"><span data-stu-id="60416-123">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="60416-124">Valori per le chiavi principali.</span><span class="sxs-lookup"><span data-stu-id="60416-124">Values for the main keys.</span></span>



| <span data-ttu-id="60416-125">Chiave</span><span class="sxs-lookup"><span data-stu-id="60416-125">Key</span></span>                     | <span data-ttu-id="60416-126">Valore</span><span class="sxs-lookup"><span data-stu-id="60416-126">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="60416-127">A-Z</span><span class="sxs-lookup"><span data-stu-id="60416-127">A-Z</span></span>                     | <span data-ttu-id="60416-128">65-90</span><span class="sxs-lookup"><span data-stu-id="60416-128">65-90</span></span>   |
| <span data-ttu-id="60416-129">0-9</span><span class="sxs-lookup"><span data-stu-id="60416-129">0-9</span></span>                     | <span data-ttu-id="60416-130">48-56</span><span class="sxs-lookup"><span data-stu-id="60416-130">48-56</span></span>   |
| <span data-ttu-id="60416-131">F1-F12</span><span class="sxs-lookup"><span data-stu-id="60416-131">F1-F12</span></span>                  | <span data-ttu-id="60416-132">112-123</span><span class="sxs-lookup"><span data-stu-id="60416-132">112-123</span></span> |
| <span data-ttu-id="60416-133">ESC</span><span class="sxs-lookup"><span data-stu-id="60416-133">ESC</span></span>                     | <span data-ttu-id="60416-134">27</span><span class="sxs-lookup"><span data-stu-id="60416-134">27</span></span>      |
| <span data-ttu-id="60416-135">TAB</span><span class="sxs-lookup"><span data-stu-id="60416-135">TAB</span></span>                     | <span data-ttu-id="60416-136">9</span><span class="sxs-lookup"><span data-stu-id="60416-136">9</span></span>       |
| <span data-ttu-id="60416-137">Bloc Maiusc</span><span class="sxs-lookup"><span data-stu-id="60416-137">CAPS LOCK</span></span>               | <span data-ttu-id="60416-138">20</span><span class="sxs-lookup"><span data-stu-id="60416-138">20</span></span>      |
| <span data-ttu-id="60416-139">Maiusc (a sinistra o a destra)</span><span class="sxs-lookup"><span data-stu-id="60416-139">SHIFT (left or right)</span></span>   | <span data-ttu-id="60416-140">16</span><span class="sxs-lookup"><span data-stu-id="60416-140">16</span></span>      |
| <span data-ttu-id="60416-141">CTRL (a sinistra o a destra)</span><span class="sxs-lookup"><span data-stu-id="60416-141">CTRL (left or right)</span></span>    | <span data-ttu-id="60416-142">17</span><span class="sxs-lookup"><span data-stu-id="60416-142">17</span></span>      |
| <span data-ttu-id="60416-143">ALT (a sinistra o a destra)</span><span class="sxs-lookup"><span data-stu-id="60416-143">ALT (left or right)</span></span>     | <span data-ttu-id="60416-144">18</span><span class="sxs-lookup"><span data-stu-id="60416-144">18</span></span>      |
| <span data-ttu-id="60416-145">SPACE</span><span class="sxs-lookup"><span data-stu-id="60416-145">SPACE</span></span>                   | <span data-ttu-id="60416-146">32</span><span class="sxs-lookup"><span data-stu-id="60416-146">32</span></span>      |
| <span data-ttu-id="60416-147">BACKSPACE</span><span class="sxs-lookup"><span data-stu-id="60416-147">BACKSPACE</span></span>               | <span data-ttu-id="60416-148">8</span><span class="sxs-lookup"><span data-stu-id="60416-148">8</span></span>       |
| <span data-ttu-id="60416-149">INVIO</span><span class="sxs-lookup"><span data-stu-id="60416-149">ENTER</span></span>                   | <span data-ttu-id="60416-150">13</span><span class="sxs-lookup"><span data-stu-id="60416-150">13</span></span>      |
| <span data-ttu-id="60416-151">Tasto logo Windows, a sinistra</span><span class="sxs-lookup"><span data-stu-id="60416-151">Windows logo key, left</span></span>  | <span data-ttu-id="60416-152">91</span><span class="sxs-lookup"><span data-stu-id="60416-152">91</span></span>      |
| <span data-ttu-id="60416-153">Tasto logo Windows, a destra</span><span class="sxs-lookup"><span data-stu-id="60416-153">Windows logo key, right</span></span> | <span data-ttu-id="60416-154">92</span><span class="sxs-lookup"><span data-stu-id="60416-154">92</span></span>      |
| <span data-ttu-id="60416-155">Chiave applicazione</span><span class="sxs-lookup"><span data-stu-id="60416-155">Application key</span></span>         | <span data-ttu-id="60416-156">93</span><span class="sxs-lookup"><span data-stu-id="60416-156">93</span></span>      |



 

<span data-ttu-id="60416-157">Valori per le chiavi del tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="60416-157">Values for the number pad keys.</span></span>



| <span data-ttu-id="60416-158">Chiave</span><span class="sxs-lookup"><span data-stu-id="60416-158">Key</span></span>               | <span data-ttu-id="60416-159">Valore</span><span class="sxs-lookup"><span data-stu-id="60416-159">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="60416-160">0-9</span><span class="sxs-lookup"><span data-stu-id="60416-160">0-9</span></span>               | <span data-ttu-id="60416-161">96-105</span><span class="sxs-lookup"><span data-stu-id="60416-161">96-105</span></span> |
| <span data-ttu-id="60416-162">BLOC NUM</span><span class="sxs-lookup"><span data-stu-id="60416-162">NUM LOCK</span></span>          | <span data-ttu-id="60416-163">144</span><span class="sxs-lookup"><span data-stu-id="60416-163">144</span></span>    |
| <span data-ttu-id="60416-164">Divisione (/)</span><span class="sxs-lookup"><span data-stu-id="60416-164">DIVIDE (/)</span></span>        | <span data-ttu-id="60416-165">111</span><span class="sxs-lookup"><span data-stu-id="60416-165">111</span></span>    |
| <span data-ttu-id="60416-166">MULTIPLY ( \* )</span><span class="sxs-lookup"><span data-stu-id="60416-166">MULTIPLY (\*)</span></span>     | <span data-ttu-id="60416-167">106</span><span class="sxs-lookup"><span data-stu-id="60416-167">106</span></span>    |
| <span data-ttu-id="60416-168">SOTTRAzione (-)</span><span class="sxs-lookup"><span data-stu-id="60416-168">SUBTRACT (-)</span></span>      | <span data-ttu-id="60416-169">109</span><span class="sxs-lookup"><span data-stu-id="60416-169">109</span></span>    |
| <span data-ttu-id="60416-170">AGGIUNGI (+)</span><span class="sxs-lookup"><span data-stu-id="60416-170">ADD (+)</span></span>           | <span data-ttu-id="60416-171">107</span><span class="sxs-lookup"><span data-stu-id="60416-171">107</span></span>    |
| <span data-ttu-id="60416-172">SEPARATOre (invio)</span><span class="sxs-lookup"><span data-stu-id="60416-172">SEPARATOR (Enter)</span></span> | <span data-ttu-id="60416-173">108</span><span class="sxs-lookup"><span data-stu-id="60416-173">108</span></span>    |
| <span data-ttu-id="60416-174">DECIMALE (.)</span><span class="sxs-lookup"><span data-stu-id="60416-174">DECIMAL (.)</span></span>       | <span data-ttu-id="60416-175">110</span><span class="sxs-lookup"><span data-stu-id="60416-175">110</span></span>    |



 

<span data-ttu-id="60416-176">Valori per i tasti di navigazione.</span><span class="sxs-lookup"><span data-stu-id="60416-176">Values for the navigation keys.</span></span>



| <span data-ttu-id="60416-177">Chiave</span><span class="sxs-lookup"><span data-stu-id="60416-177">Key</span></span>         | <span data-ttu-id="60416-178">Valore</span><span class="sxs-lookup"><span data-stu-id="60416-178">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="60416-179">INSERT</span><span class="sxs-lookup"><span data-stu-id="60416-179">INSERT</span></span>      | <span data-ttu-id="60416-180">45</span><span class="sxs-lookup"><span data-stu-id="60416-180">45</span></span>    |
| <span data-ttu-id="60416-181">DELETE</span><span class="sxs-lookup"><span data-stu-id="60416-181">DELETE</span></span>      | <span data-ttu-id="60416-182">46</span><span class="sxs-lookup"><span data-stu-id="60416-182">46</span></span>    |
| <span data-ttu-id="60416-183">HOME</span><span class="sxs-lookup"><span data-stu-id="60416-183">HOME</span></span>        | <span data-ttu-id="60416-184">36</span><span class="sxs-lookup"><span data-stu-id="60416-184">36</span></span>    |
| <span data-ttu-id="60416-185">FINE</span><span class="sxs-lookup"><span data-stu-id="60416-185">END</span></span>         | <span data-ttu-id="60416-186">35</span><span class="sxs-lookup"><span data-stu-id="60416-186">35</span></span>    |
| <span data-ttu-id="60416-187">PGSU</span><span class="sxs-lookup"><span data-stu-id="60416-187">PAGE UP</span></span>     | <span data-ttu-id="60416-188">33</span><span class="sxs-lookup"><span data-stu-id="60416-188">33</span></span>    |
| <span data-ttu-id="60416-189">PGGIÙ</span><span class="sxs-lookup"><span data-stu-id="60416-189">PAGE DOWN</span></span>   | <span data-ttu-id="60416-190">34</span><span class="sxs-lookup"><span data-stu-id="60416-190">34</span></span>    |
| <span data-ttu-id="60416-191">FRECCIA SU</span><span class="sxs-lookup"><span data-stu-id="60416-191">UP ARROW</span></span>    | <span data-ttu-id="60416-192">38</span><span class="sxs-lookup"><span data-stu-id="60416-192">38</span></span>    |
| <span data-ttu-id="60416-193">Freccia GIÙ</span><span class="sxs-lookup"><span data-stu-id="60416-193">DOWN ARROW</span></span>  | <span data-ttu-id="60416-194">40</span><span class="sxs-lookup"><span data-stu-id="60416-194">40</span></span>    |
| <span data-ttu-id="60416-195">FRECCIA SINISTRA</span><span class="sxs-lookup"><span data-stu-id="60416-195">LEFT ARROW</span></span>  | <span data-ttu-id="60416-196">37</span><span class="sxs-lookup"><span data-stu-id="60416-196">37</span></span>    |
| <span data-ttu-id="60416-197">FRECCIA DESTRA</span><span class="sxs-lookup"><span data-stu-id="60416-197">RIGHT ARROW</span></span> | <span data-ttu-id="60416-198">39</span><span class="sxs-lookup"><span data-stu-id="60416-198">39</span></span>    |



 

<span data-ttu-id="60416-199">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="60416-199">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="60416-200">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="60416-200">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="60416-201">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="60416-201">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="60416-202">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60416-202">Requirements</span></span>



| <span data-ttu-id="60416-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="60416-203">Requirement</span></span> | <span data-ttu-id="60416-204">Valore</span><span class="sxs-lookup"><span data-stu-id="60416-204">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60416-205">Versione</span><span class="sxs-lookup"><span data-stu-id="60416-205">Version</span></span><br/> | <span data-ttu-id="60416-206">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="60416-206">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="60416-207">DLL</span><span class="sxs-lookup"><span data-stu-id="60416-207">DLL</span></span><br/>     | <dl> <span data-ttu-id="60416-208"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60416-208"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60416-209">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60416-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60416-210">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="60416-210">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





