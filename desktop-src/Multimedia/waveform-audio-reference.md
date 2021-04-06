---
title: Riferimento onda audio
description: Questa sezione elenca le funzioni, le strutture e i messaggi associati all'audio della forma d'onda, documentati in riferimenti multimediali. Questi elementi vengono raggruppati come indicato di seguito.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Multimedia di Windows, informazioni di riferimento su audio Waveform
- informazioni di riferimento su Multimedia, onda audio
- audio multimediale, riferimento alla forma d'onda
- audio, riferimento alla forma d'onda
- Multimedia di Windows, audio Waveform
- Multimedia, audio Waveform
- audio multimediale, forma d'onda
- audio, forma d'onda
- audio Waveform, riferimento
- Guida di riferimento all'audio della forma d'onda, informazioni
- informazioni di riferimento su wavefore audio, about
- riferimento audio per la forma d'onda, dispositivi ausiliari
- informazioni di riferimento per audio wavefore, dispositivi ausiliari
- riferimento audio Waveform, riproduzione
- informazioni di riferimento sull'audio wavefore, riproduzione
- riferimento audio per la forma d'onda, errori
- informazioni di riferimento sull'audio wavefore, errori
- riferimento audio per la forma d'onda, apertura
- informazioni di riferimento sull'audio wavefore, apertura
- riferimento audio per la forma d'onda, chiusura
- informazioni di riferimento per wavefore audio, chiusura
- riferimento audio Waveform, pitch
- informazioni di riferimento su wavefore audio, pitch
- riferimento audio Waveform, volume
- informazioni di riferimento sull'audio wavefore, volume
- riferimento audio Waveform, messaggi
- informazioni di riferimento sull'audio wavefore, messaggi
- riferimento audio Waveform, posizione corrente
- informazioni di riferimento sull'audio wavefore, posizione corrente
- riferimento audio per la forma d'onda, registrazione
- informazioni di riferimento sull'audio di wavefore, registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046654"
---
# <a name="waveform-audio-reference"></a><span data-ttu-id="38a8a-135">Riferimento onda audio</span><span class="sxs-lookup"><span data-stu-id="38a8a-135">Waveform Audio Reference</span></span>

<span data-ttu-id="38a8a-136">Questa sezione elenca le funzioni, le strutture e i messaggi associati all'audio della forma d'onda, documentati in [riferimenti multimediali](multimedia-reference.md).</span><span class="sxs-lookup"><span data-stu-id="38a8a-136">This section lists the functions, structures, and messages associated with waveform audio, which are documented under [Multimedia Reference](multimedia-reference.md).</span></span> <span data-ttu-id="38a8a-137">Questi elementi vengono raggruppati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="38a8a-137">These elements are grouped as follows.</span></span>

## <a name="auxiliary-devices"></a><span data-ttu-id="38a8a-138">Dispositivi ausiliari</span><span class="sxs-lookup"><span data-stu-id="38a8a-138">Auxiliary Devices</span></span>

-   [<span data-ttu-id="38a8a-139">**AUXCAPS**</span><span class="sxs-lookup"><span data-stu-id="38a8a-139">**AUXCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [<span data-ttu-id="38a8a-140">**auxGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="38a8a-140">**auxGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [<span data-ttu-id="38a8a-141">**auxGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="38a8a-141">**auxGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [<span data-ttu-id="38a8a-142">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="38a8a-142">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [<span data-ttu-id="38a8a-143">**auxOutMessage**</span><span class="sxs-lookup"><span data-stu-id="38a8a-143">**auxOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [<span data-ttu-id="38a8a-144">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="38a8a-144">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a><span data-ttu-id="38a8a-145">Facile riproduzione</span><span class="sxs-lookup"><span data-stu-id="38a8a-145">Easy Playback</span></span>

-   <span data-ttu-id="38a8a-146">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38a8a-146">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>
-   <span data-ttu-id="38a8a-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38a8a-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>

## <a name="errors"></a><span data-ttu-id="38a8a-148">Errors</span><span class="sxs-lookup"><span data-stu-id="38a8a-148">Errors</span></span>

-   [<span data-ttu-id="38a8a-149">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="38a8a-149">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [<span data-ttu-id="38a8a-150">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="38a8a-150">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a><span data-ttu-id="38a8a-151">Apertura e chiusura</span><span class="sxs-lookup"><span data-stu-id="38a8a-151">Opening and Closing</span></span>

-   [<span data-ttu-id="38a8a-152">**PCMWAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="38a8a-152">**PCMWAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [<span data-ttu-id="38a8a-153">**\_Wim \_ chiusura di mm**</span><span class="sxs-lookup"><span data-stu-id="38a8a-153">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md)
-   [<span data-ttu-id="38a8a-154">**\_Wim \_ aperto mm**</span><span class="sxs-lookup"><span data-stu-id="38a8a-154">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)
-   [<span data-ttu-id="38a8a-155">**MM \_ WOM \_ Close**</span><span class="sxs-lookup"><span data-stu-id="38a8a-155">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md)
-   [<span data-ttu-id="38a8a-156">**MM \_ WOM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="38a8a-156">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)
-   [<span data-ttu-id="38a8a-157">**WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="38a8a-157">**WAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [<span data-ttu-id="38a8a-158">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="38a8a-158">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [<span data-ttu-id="38a8a-159">**waveInClose**</span><span class="sxs-lookup"><span data-stu-id="38a8a-159">**waveInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   <span data-ttu-id="38a8a-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38a8a-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span></span>
-   [<span data-ttu-id="38a8a-161">**waveInOpen**</span><span class="sxs-lookup"><span data-stu-id="38a8a-161">**waveInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [<span data-ttu-id="38a8a-162">**waveOutClose**</span><span class="sxs-lookup"><span data-stu-id="38a8a-162">**waveOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   <span data-ttu-id="38a8a-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38a8a-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span></span>
-   [<span data-ttu-id="38a8a-164">**waveOutOpen**</span><span class="sxs-lookup"><span data-stu-id="38a8a-164">**waveOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [<span data-ttu-id="38a8a-165">**chiusura di WIM \_**</span><span class="sxs-lookup"><span data-stu-id="38a8a-165">**WIM\_CLOSE**</span></span>](wim-close.md)
-   [<span data-ttu-id="38a8a-166">**WIM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="38a8a-166">**WIM\_OPEN**</span></span>](wim-open.md)
-   [<span data-ttu-id="38a8a-167">**chiusura di WOM \_**</span><span class="sxs-lookup"><span data-stu-id="38a8a-167">**WOM\_CLOSE**</span></span>](wom-close.md)
-   [<span data-ttu-id="38a8a-168">**WOM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="38a8a-168">**WOM\_OPEN**</span></span>](wom-open.md)

## <a name="pitch"></a><span data-ttu-id="38a8a-169">Tonalità</span><span class="sxs-lookup"><span data-stu-id="38a8a-169">Pitch</span></span>

-   [<span data-ttu-id="38a8a-170">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="38a8a-170">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [<span data-ttu-id="38a8a-171">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="38a8a-171">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a><span data-ttu-id="38a8a-172">Velocità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="38a8a-172">Playback Rate</span></span>

-   [<span data-ttu-id="38a8a-173">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="38a8a-173">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [<span data-ttu-id="38a8a-174">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="38a8a-174">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a><span data-ttu-id="38a8a-175">Stato riproduzione</span><span class="sxs-lookup"><span data-stu-id="38a8a-175">Playback Progress</span></span>

-   [<span data-ttu-id="38a8a-176">**MM \_ WOM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="38a8a-176">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="38a8a-177">**waveOutBreakLoop**</span><span class="sxs-lookup"><span data-stu-id="38a8a-177">**waveOutBreakLoop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [<span data-ttu-id="38a8a-178">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="38a8a-178">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [<span data-ttu-id="38a8a-179">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="38a8a-179">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [<span data-ttu-id="38a8a-180">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="38a8a-180">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [<span data-ttu-id="38a8a-181">**WOM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="38a8a-181">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="playing"></a><span data-ttu-id="38a8a-182">Playing</span><span class="sxs-lookup"><span data-stu-id="38a8a-182">Playing</span></span>

-   [<span data-ttu-id="38a8a-183">**MM \_ WOM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="38a8a-183">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="38a8a-184">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="38a8a-184">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [<span data-ttu-id="38a8a-185">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="38a8a-185">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [<span data-ttu-id="38a8a-186">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="38a8a-186">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [<span data-ttu-id="38a8a-187">**waveOutWrite**</span><span class="sxs-lookup"><span data-stu-id="38a8a-187">**waveOutWrite**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [<span data-ttu-id="38a8a-188">**WOM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="38a8a-188">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="querying-a-device"></a><span data-ttu-id="38a8a-189">Esecuzione di query su un dispositivo</span><span class="sxs-lookup"><span data-stu-id="38a8a-189">Querying a Device</span></span>

-   [<span data-ttu-id="38a8a-190">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="38a8a-190">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [<span data-ttu-id="38a8a-191">**waveInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="38a8a-191">**waveInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [<span data-ttu-id="38a8a-192">**waveInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="38a8a-192">**waveInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [<span data-ttu-id="38a8a-193">**WAVEOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="38a8a-193">**WAVEOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [<span data-ttu-id="38a8a-194">**waveOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="38a8a-194">**waveOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [<span data-ttu-id="38a8a-195">**waveOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="38a8a-195">**waveOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a><span data-ttu-id="38a8a-196">Registrazione</span><span class="sxs-lookup"><span data-stu-id="38a8a-196">Recording</span></span>

-   [<span data-ttu-id="38a8a-197">**\_dati WIM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="38a8a-197">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)
-   [<span data-ttu-id="38a8a-198">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="38a8a-198">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [<span data-ttu-id="38a8a-199">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="38a8a-199">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [<span data-ttu-id="38a8a-200">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="38a8a-200">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [<span data-ttu-id="38a8a-201">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="38a8a-201">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [<span data-ttu-id="38a8a-202">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="38a8a-202">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [<span data-ttu-id="38a8a-203">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="38a8a-203">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [<span data-ttu-id="38a8a-204">**\_dati WIM**</span><span class="sxs-lookup"><span data-stu-id="38a8a-204">**WIM\_DATA**</span></span>](wim-data.md)

## <a name="retrieving-device-identifiers"></a><span data-ttu-id="38a8a-205">Recupero degli identificatori del dispositivo</span><span class="sxs-lookup"><span data-stu-id="38a8a-205">Retrieving Device Identifiers</span></span>

-   [<span data-ttu-id="38a8a-206">**waveInGetID**</span><span class="sxs-lookup"><span data-stu-id="38a8a-206">**waveInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [<span data-ttu-id="38a8a-207">**waveOutGetID**</span><span class="sxs-lookup"><span data-stu-id="38a8a-207">**waveOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a><span data-ttu-id="38a8a-208">Recupero della posizione corrente</span><span class="sxs-lookup"><span data-stu-id="38a8a-208">Retrieving the Current Position</span></span>

-   [<span data-ttu-id="38a8a-209">**waveInGetPosition**</span><span class="sxs-lookup"><span data-stu-id="38a8a-209">**waveInGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [<span data-ttu-id="38a8a-210">**waveOutGetPosition**</span><span class="sxs-lookup"><span data-stu-id="38a8a-210">**waveOutGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a><span data-ttu-id="38a8a-211">Invio di messaggi personalizzati</span><span class="sxs-lookup"><span data-stu-id="38a8a-211">Sending Custom Messages</span></span>

-   [<span data-ttu-id="38a8a-212">**waveInMessage**</span><span class="sxs-lookup"><span data-stu-id="38a8a-212">**waveInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [<span data-ttu-id="38a8a-213">**waveOutMessage**</span><span class="sxs-lookup"><span data-stu-id="38a8a-213">**waveOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a><span data-ttu-id="38a8a-214">Volume</span><span class="sxs-lookup"><span data-stu-id="38a8a-214">Volume</span></span>

-   [<span data-ttu-id="38a8a-215">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="38a8a-215">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [<span data-ttu-id="38a8a-216">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="38a8a-216">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a><span data-ttu-id="38a8a-217">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38a8a-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38a8a-218">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="38a8a-218">Waveform Audio</span></span>](waveform-audio.md)
</dt> </dl>

 

 