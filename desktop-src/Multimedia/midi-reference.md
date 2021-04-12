---
title: Riferimento MIDI
description: Riferimento MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Multimedia di Windows, Musical Instrument Digital Interface (MIDI)
- Multimedia, Musical Instrument Digital Interface (MIDI)
- audio multimediale, MIDI (Musical Instrument Digital Interface)
- audio, Musical Instrument Digital Interface (MIDI)
- Windows Multimedia, riferimento MIDI
- Multimedia, riferimento MIDI
- audio multimediale, riferimento MIDI
- audio, riferimento MIDI
- MIDI (Musical Instrument Digital Interface), riferimento
- MIDI (Musical Instrument Digital Interface), riferimento
- informazioni di riferimento su MIDI, informazioni
- Riferimento MIDI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398971"
---
# <a name="midi-reference"></a><span data-ttu-id="30bed-115">Riferimento MIDI</span><span class="sxs-lookup"><span data-stu-id="30bed-115">MIDI Reference</span></span>

<span data-ttu-id="30bed-116">Questa sezione descrive le funzioni, le macro, i messaggi e le strutture associati al MIDI (Musical Instrument Digital Interface).</span><span class="sxs-lookup"><span data-stu-id="30bed-116">This section describes the functions, macros, messages, and structures associated with the Musical Instrument Digital Interface (MIDI).</span></span> <span data-ttu-id="30bed-117">Questi elementi vengono raggruppati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="30bed-117">These elements are grouped as follows.</span></span>

## <a name="allocating-and-managing-buffers"></a><span data-ttu-id="30bed-118">Allocazione e gestione dei buffer</span><span class="sxs-lookup"><span data-stu-id="30bed-118">Allocating and Managing Buffers</span></span>

-   [<span data-ttu-id="30bed-119">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="30bed-119">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [<span data-ttu-id="30bed-120">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="30bed-120">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [<span data-ttu-id="30bed-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="30bed-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [<span data-ttu-id="30bed-122">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="30bed-122">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [<span data-ttu-id="30bed-123">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="30bed-123">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [<span data-ttu-id="30bed-124">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="30bed-124">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a><span data-ttu-id="30bed-125">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="30bed-125">Callback Functions</span></span>

-   <span data-ttu-id="30bed-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="30bed-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span></span>
-   <span data-ttu-id="30bed-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="30bed-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="30bed-128">Funzionalità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="30bed-128">Device Capabilities</span></span>

-   [<span data-ttu-id="30bed-129">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="30bed-129">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [<span data-ttu-id="30bed-130">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="30bed-130">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [<span data-ttu-id="30bed-131">**midiInGetID**</span><span class="sxs-lookup"><span data-stu-id="30bed-131">**midiInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [<span data-ttu-id="30bed-132">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="30bed-132">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [<span data-ttu-id="30bed-133">**MIDIOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="30bed-133">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [<span data-ttu-id="30bed-134">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="30bed-134">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [<span data-ttu-id="30bed-135">**midiOutGetID**</span><span class="sxs-lookup"><span data-stu-id="30bed-135">**midiOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [<span data-ttu-id="30bed-136">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="30bed-136">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [<span data-ttu-id="30bed-137">**MIDISTRMBUFFVER**</span><span class="sxs-lookup"><span data-stu-id="30bed-137">**MIDISTRMBUFFVER**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a><span data-ttu-id="30bed-138">Errore di elaborazione</span><span class="sxs-lookup"><span data-stu-id="30bed-138">Error Processing</span></span>

-   [<span data-ttu-id="30bed-139">**midiInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="30bed-139">**midiInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [<span data-ttu-id="30bed-140">**midiOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="30bed-140">**midiOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [<span data-ttu-id="30bed-141">**\_errore MIM**</span><span class="sxs-lookup"><span data-stu-id="30bed-141">**MIM\_ERROR**</span></span>](mim-error.md)
-   [<span data-ttu-id="30bed-142">**\_LONGERROR MIM**</span><span class="sxs-lookup"><span data-stu-id="30bed-142">**MIM\_LONGERROR**</span></span>](mim-longerror.md)
-   [<span data-ttu-id="30bed-143">**\_errore MIM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="30bed-143">**MM\_MIM\_ERROR**</span></span>](mm-mim-error.md)
-   [<span data-ttu-id="30bed-144">**\_LONGERROR MIM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="30bed-144">**MM\_MIM\_LONGERROR**</span></span>](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a><span data-ttu-id="30bed-145">Gestione dei flussi MIDI</span><span class="sxs-lookup"><span data-stu-id="30bed-145">Managing MIDI Streams</span></span>

-   [<span data-ttu-id="30bed-146">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="30bed-146">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [<span data-ttu-id="30bed-147">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="30bed-147">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [<span data-ttu-id="30bed-148">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="30bed-148">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="30bed-149">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="30bed-149">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="30bed-150">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="30bed-150">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [<span data-ttu-id="30bed-151">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="30bed-151">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [<span data-ttu-id="30bed-152">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="30bed-152">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="30bed-153">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="30bed-153">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a><span data-ttu-id="30bed-154">Apertura e chiusura di dispositivi</span><span class="sxs-lookup"><span data-stu-id="30bed-154">Opening and Closing Devices</span></span>

-   [<span data-ttu-id="30bed-155">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="30bed-155">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [<span data-ttu-id="30bed-156">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="30bed-156">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [<span data-ttu-id="30bed-157">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="30bed-157">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [<span data-ttu-id="30bed-158">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="30bed-158">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [<span data-ttu-id="30bed-159">**\_chiusura MIM**</span><span class="sxs-lookup"><span data-stu-id="30bed-159">**MIM\_CLOSE**</span></span>](mim-close.md)
-   [<span data-ttu-id="30bed-160">**MIM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="30bed-160">**MIM\_OPEN**</span></span>](mim-open.md)
-   [<span data-ttu-id="30bed-161">**MM \_ di \_ chiusura MIM**</span><span class="sxs-lookup"><span data-stu-id="30bed-161">**MM\_MIM\_CLOSE**</span></span>](mm-mim-close.md)
-   [<span data-ttu-id="30bed-162">**\_apertura MIM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="30bed-162">**MM\_MIM\_OPEN**</span></span>](mm-mim-open.md)
-   [<span data-ttu-id="30bed-163">**MM \_ \_ chiusura MOM**</span><span class="sxs-lookup"><span data-stu-id="30bed-163">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md)
-   [<span data-ttu-id="30bed-164">**MM- \_ MOM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="30bed-164">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)
-   [<span data-ttu-id="30bed-165">**\_chiusura MOM**</span><span class="sxs-lookup"><span data-stu-id="30bed-165">**MOM\_CLOSE**</span></span>](mom-close.md)
-   [<span data-ttu-id="30bed-166">**MOM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="30bed-166">**MOM\_OPEN**</span></span>](mom-open.md)

## <a name="output-devices"></a><span data-ttu-id="30bed-167">Dispositivi di output</span><span class="sxs-lookup"><span data-stu-id="30bed-167">Output Devices</span></span>

-   [<span data-ttu-id="30bed-168">Matrice di matrici</span><span class="sxs-lookup"><span data-stu-id="30bed-168">KEYARRAY</span></span>](keyarray.md)
-   [<span data-ttu-id="30bed-169">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="30bed-169">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [<span data-ttu-id="30bed-170">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="30bed-170">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [<span data-ttu-id="30bed-171">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="30bed-171">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [<span data-ttu-id="30bed-172">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="30bed-172">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [<span data-ttu-id="30bed-173">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="30bed-173">PATCHARRAY</span></span>](patcharray.md)

## <a name="playing-a-message-or-messages"></a><span data-ttu-id="30bed-174">Riproduzione di un messaggio o di messaggi</span><span class="sxs-lookup"><span data-stu-id="30bed-174">Playing a Message or Messages</span></span>

-   [<span data-ttu-id="30bed-175">**\_EVENTPARM MEVT**</span><span class="sxs-lookup"><span data-stu-id="30bed-175">**MEVT\_EVENTPARM**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [<span data-ttu-id="30bed-176">**MEVT \_ eventType**</span><span class="sxs-lookup"><span data-stu-id="30bed-176">**MEVT\_EVENTTYPE**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [<span data-ttu-id="30bed-177">**MIDIEVENT**</span><span class="sxs-lookup"><span data-stu-id="30bed-177">**MIDIEVENT**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [<span data-ttu-id="30bed-178">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="30bed-178">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [<span data-ttu-id="30bed-179">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="30bed-179">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [<span data-ttu-id="30bed-180">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="30bed-180">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [<span data-ttu-id="30bed-181">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="30bed-181">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="30bed-182">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="30bed-182">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="30bed-183">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="30bed-183">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="30bed-184">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="30bed-184">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [<span data-ttu-id="30bed-185">**MM \_ MOM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="30bed-185">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)
-   [<span data-ttu-id="30bed-186">**MM \_ \_ POSITIONCB MOM**</span><span class="sxs-lookup"><span data-stu-id="30bed-186">**MM\_MOM\_POSITIONCB**</span></span>](mm-mom-positioncb.md)
-   [<span data-ttu-id="30bed-187">**MOM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="30bed-187">**MOM\_DONE**</span></span>](mom-done.md)
-   [<span data-ttu-id="30bed-188">**\_POSITIONCB MOM**</span><span class="sxs-lookup"><span data-stu-id="30bed-188">**MOM\_POSITIONCB**</span></span>](mom-positioncb.md)

## <a name="recording"></a><span data-ttu-id="30bed-189">Registrazione</span><span class="sxs-lookup"><span data-stu-id="30bed-189">Recording</span></span>

-   [<span data-ttu-id="30bed-190">**midiConnect**</span><span class="sxs-lookup"><span data-stu-id="30bed-190">**midiConnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [<span data-ttu-id="30bed-191">**midiDisconnect**</span><span class="sxs-lookup"><span data-stu-id="30bed-191">**midiDisconnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [<span data-ttu-id="30bed-192">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="30bed-192">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [<span data-ttu-id="30bed-193">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="30bed-193">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [<span data-ttu-id="30bed-194">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="30bed-194">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [<span data-ttu-id="30bed-195">**MIDIPROPTEMPO**</span><span class="sxs-lookup"><span data-stu-id="30bed-195">**MIDIPROPTEMPO**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [<span data-ttu-id="30bed-196">**MIDIPROPTIMEDIV**</span><span class="sxs-lookup"><span data-stu-id="30bed-196">**MIDIPROPTIMEDIV**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [<span data-ttu-id="30bed-197">**\_dati MIM**</span><span class="sxs-lookup"><span data-stu-id="30bed-197">**MIM\_DATA**</span></span>](mim-data.md)
-   [<span data-ttu-id="30bed-198">**\_LONGDATA MIM**</span><span class="sxs-lookup"><span data-stu-id="30bed-198">**MIM\_LONGDATA**</span></span>](mim-longdata.md)
-   [<span data-ttu-id="30bed-199">**\_MOREDATA MIM**</span><span class="sxs-lookup"><span data-stu-id="30bed-199">**MIM\_MOREDATA**</span></span>](mim-moredata.md)
-   [<span data-ttu-id="30bed-200">**\_dati MIM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="30bed-200">**MM\_MIM\_DATA**</span></span>](mm-mim-data.md)
-   [<span data-ttu-id="30bed-201">**\_MOREDATA MIM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="30bed-201">**MM\_MIM\_MOREDATA**</span></span>](mm-mim-moredata.md)
-   [<span data-ttu-id="30bed-202">**\_LONGDATA MIM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="30bed-202">**MM\_MIM\_LONGDATA**</span></span>](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a><span data-ttu-id="30bed-203">Invio di messaggi ai dispositivi</span><span class="sxs-lookup"><span data-stu-id="30bed-203">Sending Messages to Devices</span></span>

-   [<span data-ttu-id="30bed-204">**midiInMessage**</span><span class="sxs-lookup"><span data-stu-id="30bed-204">**midiInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [<span data-ttu-id="30bed-205">**midiOutMessage**</span><span class="sxs-lookup"><span data-stu-id="30bed-205">**midiOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a><span data-ttu-id="30bed-206">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30bed-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30bed-207">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="30bed-207">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 