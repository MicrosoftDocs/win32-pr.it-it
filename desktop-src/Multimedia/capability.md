---
title: comando Capability
description: Il comando Capability richiede informazioni su una particolare funzionalità di un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- funzionalità di Windows Multimedia Command
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475707"
---
# <a name="capability-command"></a><span data-ttu-id="da3cd-105">comando Capability</span><span class="sxs-lookup"><span data-stu-id="da3cd-105">capability command</span></span>

<span data-ttu-id="da3cd-106">Il comando Capability richiede informazioni su una particolare funzionalità di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da3cd-106">The capability command requests information about a particular capability of a device.</span></span> <span data-ttu-id="da3cd-107">Tutti i dispositivi MCI riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="da3cd-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="da3cd-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="da3cd-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="da3cd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="da3cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da3cd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="da3cd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="da3cd-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="da3cd-111">Identifier of an MCI device.</span></span> <span data-ttu-id="da3cd-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="da3cd-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="da3cd-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="da3cd-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="da3cd-114">Flag che identifica una funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da3cd-114">Flag that identifies a device capability.</span></span> <span data-ttu-id="da3cd-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Capability** e i flag utilizzati da ogni tipo:</span><span class="sxs-lookup"><span data-stu-id="da3cd-115">The following table lists device types that recognize the **capability** command and the flags used by each type:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da3cd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="da3cd-116">Value</span></span></th>
<th><span data-ttu-id="da3cd-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="da3cd-117">Type</span></span></th>
<th><span data-ttu-id="da3cd-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="da3cd-118">Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="da3cd-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="da3cd-119">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="da3cd-120">può espulsione</span><span class="sxs-lookup"><span data-stu-id="da3cd-120">can eject</span></span></li>
<li><span data-ttu-id="da3cd-121">può riprodurre</span><span class="sxs-lookup"><span data-stu-id="da3cd-121">can play</span></span></li>
<li><span data-ttu-id="da3cd-122">può registrare</span><span class="sxs-lookup"><span data-stu-id="da3cd-122">can record</span></span></li>
<li><span data-ttu-id="da3cd-123">consente di salvare</span><span class="sxs-lookup"><span data-stu-id="da3cd-123">can save</span></span></li>
<li><span data-ttu-id="da3cd-124">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="da3cd-124">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="da3cd-125">tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="da3cd-125">device type</span></span></li>
<li><span data-ttu-id="da3cd-126">con audio</span><span class="sxs-lookup"><span data-stu-id="da3cd-126">has audio</span></span></li>
<li><span data-ttu-id="da3cd-127">con video</span><span class="sxs-lookup"><span data-stu-id="da3cd-127">has video</span></span></li>
<li><span data-ttu-id="da3cd-128">Usa file</span><span class="sxs-lookup"><span data-stu-id="da3cd-128">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-129">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="da3cd-129">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="da3cd-130">può espulsione</span><span class="sxs-lookup"><span data-stu-id="da3cd-130">can eject</span></span></li>
<li><span data-ttu-id="da3cd-131">può bloccare</span><span class="sxs-lookup"><span data-stu-id="da3cd-131">can freeze</span></span></li>
<li><span data-ttu-id="da3cd-132">può bloccare</span><span class="sxs-lookup"><span data-stu-id="da3cd-132">can lock</span></span></li>
<li><span data-ttu-id="da3cd-133">può riprodurre</span><span class="sxs-lookup"><span data-stu-id="da3cd-133">can play</span></span></li>
<li><span data-ttu-id="da3cd-134">può registrare</span><span class="sxs-lookup"><span data-stu-id="da3cd-134">can record</span></span></li>
<li><span data-ttu-id="da3cd-135">può invertire</span><span class="sxs-lookup"><span data-stu-id="da3cd-135">can reverse</span></span></li>
<li><span data-ttu-id="da3cd-136">consente di salvare</span><span class="sxs-lookup"><span data-stu-id="da3cd-136">can save</span></span></li>
<li><span data-ttu-id="da3cd-137">può estendersi</span><span class="sxs-lookup"><span data-stu-id="da3cd-137">can stretch</span></span></li>
<li><span data-ttu-id="da3cd-138">è possibile estendere l'input</span><span class="sxs-lookup"><span data-stu-id="da3cd-138">can stretch input</span></span></li>
<li><span data-ttu-id="da3cd-139">è possibile eseguire il test</span><span class="sxs-lookup"><span data-stu-id="da3cd-139">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="da3cd-140">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="da3cd-140">compound device</span></span></li>
<li><span data-ttu-id="da3cd-141">tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="da3cd-141">device type</span></span></li>
<li><span data-ttu-id="da3cd-142">con audio</span><span class="sxs-lookup"><span data-stu-id="da3cd-142">has audio</span></span></li>
<li><span data-ttu-id="da3cd-143">ha ancora</span><span class="sxs-lookup"><span data-stu-id="da3cd-143">has still</span></span></li>
<li><span data-ttu-id="da3cd-144">con video</span><span class="sxs-lookup"><span data-stu-id="da3cd-144">has video</span></span></li>
<li><span data-ttu-id="da3cd-145">velocità di riproduzione massima</span><span class="sxs-lookup"><span data-stu-id="da3cd-145">maximum play rate</span></span></li>
<li><span data-ttu-id="da3cd-146">velocità di riproduzione minima</span><span class="sxs-lookup"><span data-stu-id="da3cd-146">minimum play rate</span></span></li>
<li><span data-ttu-id="da3cd-147">Usa file</span><span class="sxs-lookup"><span data-stu-id="da3cd-147">uses files</span></span></li>
<li><span data-ttu-id="da3cd-148">USA tavolozze</span><span class="sxs-lookup"><span data-stu-id="da3cd-148">uses palettes</span></span></li>
<li><span data-ttu-id="da3cd-149">windows</span><span class="sxs-lookup"><span data-stu-id="da3cd-149">windows</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-150">overlay</span><span class="sxs-lookup"><span data-stu-id="da3cd-150">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="da3cd-151">può espulsione</span><span class="sxs-lookup"><span data-stu-id="da3cd-151">can eject</span></span></li>
<li><span data-ttu-id="da3cd-152">può bloccare</span><span class="sxs-lookup"><span data-stu-id="da3cd-152">can freeze</span></span></li>
<li><span data-ttu-id="da3cd-153">può riprodurre</span><span class="sxs-lookup"><span data-stu-id="da3cd-153">can play</span></span></li>
<li><span data-ttu-id="da3cd-154">può registrare</span><span class="sxs-lookup"><span data-stu-id="da3cd-154">can record</span></span></li>
<li><span data-ttu-id="da3cd-155">consente di salvare</span><span class="sxs-lookup"><span data-stu-id="da3cd-155">can save</span></span></li>
<li><span data-ttu-id="da3cd-156">può estendersi</span><span class="sxs-lookup"><span data-stu-id="da3cd-156">can stretch</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="da3cd-157">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="da3cd-157">compound device</span></span></li>
<li><span data-ttu-id="da3cd-158">tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="da3cd-158">device type</span></span></li>
<li><span data-ttu-id="da3cd-159">con audio</span><span class="sxs-lookup"><span data-stu-id="da3cd-159">has audio</span></span></li>
<li><span data-ttu-id="da3cd-160">con video</span><span class="sxs-lookup"><span data-stu-id="da3cd-160">has video</span></span></li>
<li><span data-ttu-id="da3cd-161">Usa file</span><span class="sxs-lookup"><span data-stu-id="da3cd-161">uses files</span></span></li>
<li><span data-ttu-id="da3cd-162">windows</span><span class="sxs-lookup"><span data-stu-id="da3cd-162">windows</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-163">sequencer</span><span class="sxs-lookup"><span data-stu-id="da3cd-163">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="da3cd-164">può espulsione</span><span class="sxs-lookup"><span data-stu-id="da3cd-164">can eject</span></span></li>
<li><span data-ttu-id="da3cd-165">può riprodurre</span><span class="sxs-lookup"><span data-stu-id="da3cd-165">can play</span></span></li>
<li><span data-ttu-id="da3cd-166">può registrare</span><span class="sxs-lookup"><span data-stu-id="da3cd-166">can record</span></span></li>
<li><span data-ttu-id="da3cd-167">consente di salvare</span><span class="sxs-lookup"><span data-stu-id="da3cd-167">can save</span></span></li>
<li><span data-ttu-id="da3cd-168">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="da3cd-168">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="da3cd-169">tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="da3cd-169">device type</span></span></li>
<li><span data-ttu-id="da3cd-170">con audio</span><span class="sxs-lookup"><span data-stu-id="da3cd-170">has audio</span></span></li>
<li><span data-ttu-id="da3cd-171">con video</span><span class="sxs-lookup"><span data-stu-id="da3cd-171">has video</span></span></li>
<li><span data-ttu-id="da3cd-172">Usa file</span><span class="sxs-lookup"><span data-stu-id="da3cd-172">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-173">VCR</span><span class="sxs-lookup"><span data-stu-id="da3cd-173">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="da3cd-174">può rilevare la lunghezza</span><span class="sxs-lookup"><span data-stu-id="da3cd-174">can detect length</span></span></li>
<li><span data-ttu-id="da3cd-175">può espulsione</span><span class="sxs-lookup"><span data-stu-id="da3cd-175">can eject</span></span></li>
<li><span data-ttu-id="da3cd-176">può bloccare</span><span class="sxs-lookup"><span data-stu-id="da3cd-176">can freeze</span></span></li>
<li><span data-ttu-id="da3cd-177">consente di monitorare le origini</span><span class="sxs-lookup"><span data-stu-id="da3cd-177">can monitor sources</span></span></li>
<li><span data-ttu-id="da3cd-178">può riprodurre</span><span class="sxs-lookup"><span data-stu-id="da3cd-178">can play</span></span></li>
<li><span data-ttu-id="da3cd-179">è possibile preroll</span><span class="sxs-lookup"><span data-stu-id="da3cd-179">can preroll</span></span></li>
<li><span data-ttu-id="da3cd-180">anteprima</span><span class="sxs-lookup"><span data-stu-id="da3cd-180">can preview</span></span></li>
<li><span data-ttu-id="da3cd-181">può registrare</span><span class="sxs-lookup"><span data-stu-id="da3cd-181">can record</span></span></li>
<li><span data-ttu-id="da3cd-182">può invertire</span><span class="sxs-lookup"><span data-stu-id="da3cd-182">can reverse</span></span></li>
<li><span data-ttu-id="da3cd-183">consente di salvare</span><span class="sxs-lookup"><span data-stu-id="da3cd-183">can save</span></span></li>
<li><span data-ttu-id="da3cd-184">è possibile eseguire il test</span><span class="sxs-lookup"><span data-stu-id="da3cd-184">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="da3cd-185">frequenza di incremento Clock</span><span class="sxs-lookup"><span data-stu-id="da3cd-185">clock increment rate</span></span></li>
<li><span data-ttu-id="da3cd-186">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="da3cd-186">compound device</span></span></li>
<li><span data-ttu-id="da3cd-187">tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="da3cd-187">device type</span></span></li>
<li><span data-ttu-id="da3cd-188">con audio</span><span class="sxs-lookup"><span data-stu-id="da3cd-188">has audio</span></span></li>
<li><span data-ttu-id="da3cd-189">con clock</span><span class="sxs-lookup"><span data-stu-id="da3cd-189">has clock</span></span></li>
<li><span data-ttu-id="da3cd-190">con timecode</span><span class="sxs-lookup"><span data-stu-id="da3cd-190">has timecode</span></span></li>
<li><span data-ttu-id="da3cd-191">con video</span><span class="sxs-lookup"><span data-stu-id="da3cd-191">has video</span></span></li>
<li><span data-ttu-id="da3cd-192">numero di contrassegni</span><span class="sxs-lookup"><span data-stu-id="da3cd-192">number of marks</span></span></li>
<li><span data-ttu-id="da3cd-193">accuratezza ricerca</span><span class="sxs-lookup"><span data-stu-id="da3cd-193">seek accuracy</span></span></li>
<li><span data-ttu-id="da3cd-194">Usa file</span><span class="sxs-lookup"><span data-stu-id="da3cd-194">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-195">videodisco</span><span class="sxs-lookup"><span data-stu-id="da3cd-195">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="da3cd-196">può espulsione</span><span class="sxs-lookup"><span data-stu-id="da3cd-196">can eject</span></span></li>
<li><span data-ttu-id="da3cd-197">può riprodurre</span><span class="sxs-lookup"><span data-stu-id="da3cd-197">can play</span></span></li>
<li><span data-ttu-id="da3cd-198">può registrare</span><span class="sxs-lookup"><span data-stu-id="da3cd-198">can record</span></span></li>
<li><span data-ttu-id="da3cd-199">può invertire</span><span class="sxs-lookup"><span data-stu-id="da3cd-199">can reverse</span></span></li>
<li><span data-ttu-id="da3cd-200">consente di salvare</span><span class="sxs-lookup"><span data-stu-id="da3cd-200">can save</span></span></li>
<li><span data-ttu-id="da3cd-201">CAV</span><span class="sxs-lookup"><span data-stu-id="da3cd-201">CAV</span></span></li>
<li><span data-ttu-id="da3cd-202">CLV</span><span class="sxs-lookup"><span data-stu-id="da3cd-202">CLV</span></span></li>
<li><span data-ttu-id="da3cd-203">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="da3cd-203">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="da3cd-204">tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="da3cd-204">device type</span></span></li>
<li><span data-ttu-id="da3cd-205">velocità di riproduzione veloce</span><span class="sxs-lookup"><span data-stu-id="da3cd-205">fast play rate</span></span></li>
<li><span data-ttu-id="da3cd-206">con audio</span><span class="sxs-lookup"><span data-stu-id="da3cd-206">has audio</span></span></li>
<li><span data-ttu-id="da3cd-207">con video</span><span class="sxs-lookup"><span data-stu-id="da3cd-207">has video</span></span></li>
<li><span data-ttu-id="da3cd-208">frequenza di riproduzione normale</span><span class="sxs-lookup"><span data-stu-id="da3cd-208">normal play rate</span></span></li>
<li><span data-ttu-id="da3cd-209">velocità di riproduzione lenta</span><span class="sxs-lookup"><span data-stu-id="da3cd-209">slow play rate</span></span></li>
<li><span data-ttu-id="da3cd-210">Usa file</span><span class="sxs-lookup"><span data-stu-id="da3cd-210">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-211">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="da3cd-211">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="da3cd-212">può espulsione</span><span class="sxs-lookup"><span data-stu-id="da3cd-212">can eject</span></span></li>
<li><span data-ttu-id="da3cd-213">può riprodurre</span><span class="sxs-lookup"><span data-stu-id="da3cd-213">can play</span></span></li>
<li><span data-ttu-id="da3cd-214">può registrare</span><span class="sxs-lookup"><span data-stu-id="da3cd-214">can record</span></span></li>
<li><span data-ttu-id="da3cd-215">consente di salvare</span><span class="sxs-lookup"><span data-stu-id="da3cd-215">can save</span></span></li>
<li><span data-ttu-id="da3cd-216">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="da3cd-216">compound device</span></span></li>
<li><span data-ttu-id="da3cd-217">tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="da3cd-217">device type</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="da3cd-218">con audio</span><span class="sxs-lookup"><span data-stu-id="da3cd-218">has audio</span></span></li>
<li><span data-ttu-id="da3cd-219">con video</span><span class="sxs-lookup"><span data-stu-id="da3cd-219">has video</span></span></li>
<li><span data-ttu-id="da3cd-220">input</span><span class="sxs-lookup"><span data-stu-id="da3cd-220">inputs</span></span></li>
<li><span data-ttu-id="da3cd-221">outputs</span><span class="sxs-lookup"><span data-stu-id="da3cd-221">outputs</span></span></li>
<li><span data-ttu-id="da3cd-222">Usa file</span><span class="sxs-lookup"><span data-stu-id="da3cd-222">uses files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="da3cd-223">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro *lpszRequest* e i relativi significati:</span><span class="sxs-lookup"><span data-stu-id="da3cd-223">The following table lists the flags that can be specified in the *lpszRequest* parameter and their meanings:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da3cd-224">Flags</span><span class="sxs-lookup"><span data-stu-id="da3cd-224">Flags</span></span></th>
<th><span data-ttu-id="da3cd-225">Significato</span><span class="sxs-lookup"><span data-stu-id="da3cd-225">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="da3cd-226">può rilevare la lunghezza</span><span class="sxs-lookup"><span data-stu-id="da3cd-226">can detect length</span></span></td>
<td><span data-ttu-id="da3cd-227">Restituisce <strong>true</strong> se il dispositivo è in grado di rilevare la lunghezza del supporto.</span><span class="sxs-lookup"><span data-stu-id="da3cd-227">Returns <strong>TRUE</strong> if the device can detect the length of the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-228">può espulsione</span><span class="sxs-lookup"><span data-stu-id="da3cd-228">can eject</span></span></td>
<td><span data-ttu-id="da3cd-229">Restituisce <strong>true</strong> se il dispositivo può espellere il supporto.</span><span class="sxs-lookup"><span data-stu-id="da3cd-229">Returns <strong>TRUE</strong> if the device can eject the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-230">può bloccare</span><span class="sxs-lookup"><span data-stu-id="da3cd-230">can freeze</span></span></td>
<td><span data-ttu-id="da3cd-231">Restituisce <strong>true</strong> se il dispositivo può bloccare i dati nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="da3cd-231">Returns <strong>TRUE</strong> if the device can freeze data in the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-232">può bloccare</span><span class="sxs-lookup"><span data-stu-id="da3cd-232">can lock</span></span></td>
<td><span data-ttu-id="da3cd-233">Restituisce <strong>true</strong> se il dispositivo può bloccare i dati.</span><span class="sxs-lookup"><span data-stu-id="da3cd-233">Returns <strong>TRUE</strong> if the device can lock data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-234">consente di monitorare le origini</span><span class="sxs-lookup"><span data-stu-id="da3cd-234">can monitor sources</span></span></td>
<td><span data-ttu-id="da3cd-235">Restituisce <strong>true</strong> se il dispositivo può passare un input (origine) all'output monitorato, indipendentemente dalla selezione di input corrente.</span><span class="sxs-lookup"><span data-stu-id="da3cd-235">Returns <strong>TRUE</strong> if the device can pass an input (source) to the monitored output, independent of the current input selection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-236">può riprodurre</span><span class="sxs-lookup"><span data-stu-id="da3cd-236">can play</span></span></td>
<td><span data-ttu-id="da3cd-237">Restituisce <strong>true</strong> se il dispositivo è in grado di riprodurre.</span><span class="sxs-lookup"><span data-stu-id="da3cd-237">Returns <strong>TRUE</strong> if the device can play.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-238">è possibile preroll</span><span class="sxs-lookup"><span data-stu-id="da3cd-238">can preroll</span></span></td>
<td><span data-ttu-id="da3cd-239">Restituisce <strong>true</strong> se il dispositivo supporta il &quot; flag preroll &quot; con il comando <a href="cue.md">cue</a> .</span><span class="sxs-lookup"><span data-stu-id="da3cd-239">Returns <strong>TRUE</strong> if the device supports the &quot;preroll&quot; flag with the <a href="cue.md">cue</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-240">anteprima</span><span class="sxs-lookup"><span data-stu-id="da3cd-240">can preview</span></span></td>
<td><span data-ttu-id="da3cd-241">Restituisce <strong>true</strong> se il dispositivo supporta le anteprime.</span><span class="sxs-lookup"><span data-stu-id="da3cd-241">Returns <strong>TRUE</strong> if the device supports previews.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-242">può registrare</span><span class="sxs-lookup"><span data-stu-id="da3cd-242">can record</span></span></td>
<td><span data-ttu-id="da3cd-243">Restituisce <strong>true</strong> se il dispositivo supporta la registrazione.</span><span class="sxs-lookup"><span data-stu-id="da3cd-243">Returns <strong>TRUE</strong> if the device supports recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-244">può invertire</span><span class="sxs-lookup"><span data-stu-id="da3cd-244">can reverse</span></span></td>
<td><span data-ttu-id="da3cd-245">Restituisce <strong>true</strong> se il dispositivo può essere riprodotto in senso inverso.</span><span class="sxs-lookup"><span data-stu-id="da3cd-245">Returns <strong>TRUE</strong> if the device can play in reverse.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-246">consente di salvare</span><span class="sxs-lookup"><span data-stu-id="da3cd-246">can save</span></span></td>
<td><span data-ttu-id="da3cd-247">Restituisce <strong>true</strong> se il dispositivo è in grado di salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="da3cd-247">Returns <strong>TRUE</strong> if the device can save data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-248">può estendersi</span><span class="sxs-lookup"><span data-stu-id="da3cd-248">can stretch</span></span></td>
<td><span data-ttu-id="da3cd-249">Restituisce <strong>true</strong> se il dispositivo può estendere i frame per riempire un rettangolo di visualizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="da3cd-249">Returns <strong>TRUE</strong> if the device can stretch frames to fill a given display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-250">è possibile estendere l'input</span><span class="sxs-lookup"><span data-stu-id="da3cd-250">can stretch input</span></span></td>
<td><span data-ttu-id="da3cd-251">Restituisce <strong>true</strong> se il dispositivo può ridimensionare un'immagine nel processo di digitalizzazione nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="da3cd-251">Returns <strong>TRUE</strong> if the device can resize an image in the process of digitizing it into the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-252">è possibile eseguire il test</span><span class="sxs-lookup"><span data-stu-id="da3cd-252">can test</span></span></td>
<td><span data-ttu-id="da3cd-253">Restituisce <strong>true</strong> se il dispositivo riconosce la parola chiave di test.</span><span class="sxs-lookup"><span data-stu-id="da3cd-253">Returns <strong>TRUE</strong> if the device recognizes the test keyword.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-254">CAV</span><span class="sxs-lookup"><span data-stu-id="da3cd-254">cav</span></span></td>
<td><span data-ttu-id="da3cd-255">In combinazione con altri elementi, questo flag specifica che le informazioni restituite si applicano al formato CAV videodischi.</span><span class="sxs-lookup"><span data-stu-id="da3cd-255">When combined with other items, this flag specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="da3cd-256">Si tratta dell'impostazione predefinita se non viene inserito alcun videodisco.</span><span class="sxs-lookup"><span data-stu-id="da3cd-256">This is the default if no videodisc is inserted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-257">frequenza di incremento Clock</span><span class="sxs-lookup"><span data-stu-id="da3cd-257">clock increment rate</span></span></td>
<td><span data-ttu-id="da3cd-258">Restituisce il numero di suddivisioni supportate dal clock esterno al secondo.</span><span class="sxs-lookup"><span data-stu-id="da3cd-258">Returns the number of subdivisions the external clock supports per second.</span></span> <span data-ttu-id="da3cd-259">Se il clock esterno è un clock in millisecondi, il valore restituito è 1000.</span><span class="sxs-lookup"><span data-stu-id="da3cd-259">If the external clock is a millisecond clock, the return value is 1000.</span></span> <span data-ttu-id="da3cd-260">Se il valore restituito è 0, non è supportato alcun clock.</span><span class="sxs-lookup"><span data-stu-id="da3cd-260">If the return value is 0, no clock is supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-261">clv</span><span class="sxs-lookup"><span data-stu-id="da3cd-261">clv</span></span></td>
<td><span data-ttu-id="da3cd-262">In combinazione con altri elementi, questo flag specifica che le informazioni restituite si applicano al formato CLV videodischi.</span><span class="sxs-lookup"><span data-stu-id="da3cd-262">When combined with other items, this flag specifies that the return information applies to CLV format videodiscs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-263">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="da3cd-263">compound device</span></span></td>
<td><span data-ttu-id="da3cd-264">Restituisce <strong>true</strong> se il dispositivo supporta il nome di un elemento (filename).</span><span class="sxs-lookup"><span data-stu-id="da3cd-264">Returns <strong>TRUE</strong> if the device supports an element name (filename).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-265">tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="da3cd-265">device type</span></span></td>
<td><span data-ttu-id="da3cd-266">Restituisce un nome di tipo di dispositivo, che può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="da3cd-266">Returns a device type name, which can be one of the following:</span></span>
<ul>
<li><span data-ttu-id="da3cd-267">cdaudio</span><span class="sxs-lookup"><span data-stu-id="da3cd-267">cdaudio</span></span></li>
<li><span data-ttu-id="da3cd-268">dat</span><span class="sxs-lookup"><span data-stu-id="da3cd-268">dat</span></span></li>
<li><span data-ttu-id="da3cd-269">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="da3cd-269">digitalvideo</span></span></li>
<li><span data-ttu-id="da3cd-270">altro</span><span class="sxs-lookup"><span data-stu-id="da3cd-270">other</span></span></li>
<li><span data-ttu-id="da3cd-271">overlay</span><span class="sxs-lookup"><span data-stu-id="da3cd-271">overlay</span></span></li>
<li><span data-ttu-id="da3cd-272">scanner</span><span class="sxs-lookup"><span data-stu-id="da3cd-272">scanner</span></span></li>
<li><span data-ttu-id="da3cd-273">sequencer</span><span class="sxs-lookup"><span data-stu-id="da3cd-273">sequencer</span></span></li>
<li><span data-ttu-id="da3cd-274">VCR</span><span class="sxs-lookup"><span data-stu-id="da3cd-274">vcr</span></span></li>
<li><span data-ttu-id="da3cd-275">videodisco</span><span class="sxs-lookup"><span data-stu-id="da3cd-275">videodisc</span></span></li>
<li><span data-ttu-id="da3cd-276">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="da3cd-276">waveaudio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-277">velocità di riproduzione veloce</span><span class="sxs-lookup"><span data-stu-id="da3cd-277">fast play rate</span></span></td>
<td><span data-ttu-id="da3cd-278">Restituisce la velocità di riproduzione rapida in frame al secondo oppure zero se il dispositivo non può essere riprodotto velocemente.</span><span class="sxs-lookup"><span data-stu-id="da3cd-278">Returns the fast play rate in frames per second, or zero if the device cannot play fast.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-279">con audio</span><span class="sxs-lookup"><span data-stu-id="da3cd-279">has audio</span></span></td>
<td><span data-ttu-id="da3cd-280">Restituisce <strong>true</strong> se il dispositivo supporta la riproduzione audio.</span><span class="sxs-lookup"><span data-stu-id="da3cd-280">Returns <strong>TRUE</strong> if the device supports audio playback.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-281">con clock</span><span class="sxs-lookup"><span data-stu-id="da3cd-281">has clock</span></span></td>
<td><span data-ttu-id="da3cd-282">Restituisce <strong>true</strong> se il dispositivo ha un clock.</span><span class="sxs-lookup"><span data-stu-id="da3cd-282">Returns <strong>TRUE</strong> if the device has a clock.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-283">ha ancora</span><span class="sxs-lookup"><span data-stu-id="da3cd-283">has still</span></span></td>
<td><span data-ttu-id="da3cd-284">Restituisce <strong>true</strong> se il dispositivo considera i file con una singola immagine in modo più efficiente rispetto ai file video di movimento.</span><span class="sxs-lookup"><span data-stu-id="da3cd-284">Returns <strong>TRUE</strong> if the device treats files with a single image more efficiently than motion video files.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-285">con timecode</span><span class="sxs-lookup"><span data-stu-id="da3cd-285">has timecode</span></span></td>
<td><span data-ttu-id="da3cd-286">Restituisce <strong>true</strong> se il dispositivo è in grado di supportare il codice temporale o se è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="da3cd-286">Returns <strong>TRUE</strong> if the device is capable of supporting timecode, or if it is unknown.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-287">con video</span><span class="sxs-lookup"><span data-stu-id="da3cd-287">has video</span></span></td>
<td><span data-ttu-id="da3cd-288">Restituisce <strong>true</strong> se il dispositivo supporta il video.</span><span class="sxs-lookup"><span data-stu-id="da3cd-288">Returns <strong>TRUE</strong> if the device supports video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-289">input</span><span class="sxs-lookup"><span data-stu-id="da3cd-289">inputs</span></span></td>
<td><span data-ttu-id="da3cd-290">Restituisce il numero totale di dispositivi di input.</span><span class="sxs-lookup"><span data-stu-id="da3cd-290">Returns the total number of input devices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-291">velocità di riproduzione massima</span><span class="sxs-lookup"><span data-stu-id="da3cd-291">maximum play rate</span></span></td>
<td><span data-ttu-id="da3cd-292">Restituisce la velocità di riproduzione massima, in frame al secondo, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da3cd-292">Returns the maximum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-293">velocità di riproduzione minima</span><span class="sxs-lookup"><span data-stu-id="da3cd-293">minimum play rate</span></span></td>
<td><span data-ttu-id="da3cd-294">Restituisce la velocità di riproduzione minima, in frame al secondo, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da3cd-294">Returns the minimum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-295">frequenza di riproduzione normale</span><span class="sxs-lookup"><span data-stu-id="da3cd-295">normal play rate</span></span></td>
<td><span data-ttu-id="da3cd-296">Restituisce la frequenza di riproduzione normale, in frame al secondo, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da3cd-296">Returns the normal play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-297">numero di contrassegni</span><span class="sxs-lookup"><span data-stu-id="da3cd-297">number of marks</span></span></td>
<td><span data-ttu-id="da3cd-298">Restituisce il numero massimo di contrassegni che è possibile utilizzare. zero indica che i contrassegni non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="da3cd-298">Returns the maximum number of marks that can be used; zero indicates that marks are unsupported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-299">outputs</span><span class="sxs-lookup"><span data-stu-id="da3cd-299">outputs</span></span></td>
<td><span data-ttu-id="da3cd-300">Restituisce il numero totale di dispositivi di output.</span><span class="sxs-lookup"><span data-stu-id="da3cd-300">Returns the total number of output devices.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-301">accuratezza ricerca</span><span class="sxs-lookup"><span data-stu-id="da3cd-301">seek accuracy</span></span></td>
<td><span data-ttu-id="da3cd-302">Restituisce l'accuratezza prevista di una ricerca nei frame; 0 indica che il dispositivo è accurato per il frame, 1 indica che il dispositivo è previsto che si trovi all'interno di un frame della posizione di ricerca indicata e così via.</span><span class="sxs-lookup"><span data-stu-id="da3cd-302">Returns the expected accuracy of a search in frames; 0 indicates that the device is frame accurate, 1 indicates that the device expects to be within one frame of the indicated seek position, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-303">velocità di riproduzione lenta</span><span class="sxs-lookup"><span data-stu-id="da3cd-303">slow play rate</span></span></td>
<td><span data-ttu-id="da3cd-304">Restituisce la velocità di riproduzione lenta in frame al secondo oppure zero se il dispositivo non può essere riprodotto lentamente.</span><span class="sxs-lookup"><span data-stu-id="da3cd-304">Returns the slow play rate in frames per second, or zero if the device cannot play slowly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-305">Usa file</span><span class="sxs-lookup"><span data-stu-id="da3cd-305">uses files</span></span></td>
<td><span data-ttu-id="da3cd-306">Restituisce <strong>true</strong> se l'archivio dati utilizzato da un dispositivo composto è un file.</span><span class="sxs-lookup"><span data-stu-id="da3cd-306">Returns <strong>TRUE</strong> if the data storage used by a compound device is a file.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da3cd-307">USA tavolozze</span><span class="sxs-lookup"><span data-stu-id="da3cd-307">uses palettes</span></span></td>
<td><span data-ttu-id="da3cd-308">Restituisce <strong>true</strong> se il dispositivo utilizza tavolozze.</span><span class="sxs-lookup"><span data-stu-id="da3cd-308">Returns <strong>TRUE</strong> if the device uses palettes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da3cd-309">windows</span><span class="sxs-lookup"><span data-stu-id="da3cd-309">windows</span></span></td>
<td><span data-ttu-id="da3cd-310">Restituisce il numero di finestre di visualizzazione simultanee che il dispositivo può supportare.</span><span class="sxs-lookup"><span data-stu-id="da3cd-310">Returns the number of simultaneous display windows the device can support.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="da3cd-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="da3cd-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="da3cd-312">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="da3cd-312">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="da3cd-313">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="da3cd-313">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="da3cd-314">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="da3cd-314">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da3cd-315">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da3cd-315">Return Value</span></span>

<span data-ttu-id="da3cd-316">Restituisce le informazioni nel parametro *lpszReturnString* della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="da3cd-316">Returns information in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="da3cd-317">Le informazioni dipendono dal tipo di richiesta.</span><span class="sxs-lookup"><span data-stu-id="da3cd-317">The information is dependent on the request type.</span></span>

## <a name="examples"></a><span data-ttu-id="da3cd-318">Esempio</span><span class="sxs-lookup"><span data-stu-id="da3cd-318">Examples</span></span>

<span data-ttu-id="da3cd-319">Il comando seguente restituisce il tipo di dispositivo del dispositivo "audio".</span><span class="sxs-lookup"><span data-stu-id="da3cd-319">The following command returns the device type of the "mysound" device.</span></span>

``` syntax
capability mysound device type
```

## <a name="requirements"></a><span data-ttu-id="da3cd-320">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da3cd-320">Requirements</span></span>



| <span data-ttu-id="da3cd-321">Requisito</span><span class="sxs-lookup"><span data-stu-id="da3cd-321">Requirement</span></span> | <span data-ttu-id="da3cd-322">Valore</span><span class="sxs-lookup"><span data-stu-id="da3cd-322">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="da3cd-323">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da3cd-323">Minimum supported client</span></span><br/> | <span data-ttu-id="da3cd-324">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da3cd-324">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="da3cd-325">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da3cd-325">Minimum supported server</span></span><br/> | <span data-ttu-id="da3cd-326">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da3cd-326">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="da3cd-327">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da3cd-327">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da3cd-328">MCI</span><span class="sxs-lookup"><span data-stu-id="da3cd-328">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="da3cd-329">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="da3cd-329">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="da3cd-330">segnale</span><span class="sxs-lookup"><span data-stu-id="da3cd-330">cue</span></span>](cue.md)
</dt> </dl>

 

