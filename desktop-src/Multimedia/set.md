---
title: imposta comando
description: Il comando set stabilisce le impostazioni di controllo per il dispositivo. CD audio, Digital-video, MIDI sequencer, VCR, videodisco, video-overlay e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- impostazione del comando Windows Multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "106320056"
---
# <a name="set-command"></a><span data-ttu-id="3de1e-105">imposta comando</span><span class="sxs-lookup"><span data-stu-id="3de1e-105">set command</span></span>

> [!NOTE]
> <span data-ttu-id="3de1e-106">Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="3de1e-107">All'interno di questo documento sono presenti riferimenti alla parola "slave".</span><span class="sxs-lookup"><span data-stu-id="3de1e-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="3de1e-108">La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="3de1e-109">Questo testo viene usato in quanto è attualmente il testo usato nei comandi.</span><span class="sxs-lookup"><span data-stu-id="3de1e-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="3de1e-110">Per coerenza, questo documento contiene questa parola.</span><span class="sxs-lookup"><span data-stu-id="3de1e-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="3de1e-111">Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo da essere in allineamento.</span><span class="sxs-lookup"><span data-stu-id="3de1e-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>


<span data-ttu-id="3de1e-112">Il comando set stabilisce le impostazioni di controllo per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3de1e-112">The set command establishes control settings for the device.</span></span> <span data-ttu-id="3de1e-113">CD audio, Digital-video, MIDI sequencer, VCR, videodisco, video-overlay e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="3de1e-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="3de1e-114">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3de1e-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="3de1e-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="3de1e-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de1e-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3de1e-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3de1e-117">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="3de1e-117">Identifier of an MCI device.</span></span> <span data-ttu-id="3de1e-118">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="3de1e-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3de1e-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span><span class="sxs-lookup"><span data-stu-id="3de1e-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span></span>
</dt> <dd>

<span data-ttu-id="3de1e-120">Flag per la definizione delle impostazioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="3de1e-120">Flag for establishing control settings.</span></span> <span data-ttu-id="3de1e-121">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **set** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="3de1e-121">The following table lists device types that recognize the **set** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3de1e-122">Tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="3de1e-122">Device Type</span></span></th>
<th><span data-ttu-id="3de1e-123">Flag di comando</span><span class="sxs-lookup"><span data-stu-id="3de1e-123">Command Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3de1e-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="3de1e-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="3de1e-125">audio tutto disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-125">audio all off</span></span></li>
<li><span data-ttu-id="3de1e-126">audio tutto su</span><span class="sxs-lookup"><span data-stu-id="3de1e-126">audio all on</span></span></li>
<li><span data-ttu-id="3de1e-127">Audio interrotto</span><span class="sxs-lookup"><span data-stu-id="3de1e-127">audio left off</span></span></li>
<li><span data-ttu-id="3de1e-128">audio lasciato acceso</span><span class="sxs-lookup"><span data-stu-id="3de1e-128">audio left on</span></span></li>
<li><span data-ttu-id="3de1e-129">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-129">audio right off</span></span></li>
<li><span data-ttu-id="3de1e-130">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-130">audio right on</span></span></li>
<li><span data-ttu-id="3de1e-131">sportello chiuso</span><span class="sxs-lookup"><span data-stu-id="3de1e-131">door closed</span></span></li>
<li><span data-ttu-id="3de1e-132">sportello aperto</span><span class="sxs-lookup"><span data-stu-id="3de1e-132">door open</span></span></li>
<li><span data-ttu-id="3de1e-133">millisecondi formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-133">time format milliseconds</span></span></li>
<li><span data-ttu-id="3de1e-134">formato ora MSF</span><span class="sxs-lookup"><span data-stu-id="3de1e-134">time format msf</span></span></li>
<li><span data-ttu-id="3de1e-135">formato ora TMSF</span><span class="sxs-lookup"><span data-stu-id="3de1e-135">time format tmsf</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-136">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="3de1e-136">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="3de1e-137">audio tutto disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-137">audio all off</span></span></li>
<li><span data-ttu-id="3de1e-138">audio tutto su</span><span class="sxs-lookup"><span data-stu-id="3de1e-138">audio all on</span></span></li>
<li><span data-ttu-id="3de1e-139">Audio interrotto</span><span class="sxs-lookup"><span data-stu-id="3de1e-139">audio left off</span></span></li>
<li><span data-ttu-id="3de1e-140">audio lasciato acceso</span><span class="sxs-lookup"><span data-stu-id="3de1e-140">audio left on</span></span></li>
<li><span data-ttu-id="3de1e-141">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-141">audio right off</span></span></li>
<li><span data-ttu-id="3de1e-142">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-142">audio right on</span></span></li>
<li><span data-ttu-id="3de1e-143">sportello chiuso</span><span class="sxs-lookup"><span data-stu-id="3de1e-143">door closed</span></span></li>
<li><span data-ttu-id="3de1e-144">sportello aperto</span><span class="sxs-lookup"><span data-stu-id="3de1e-144">door open</span></span></li>
<li><span data-ttu-id="3de1e-145"><em>formato</em> formato file</span><span class="sxs-lookup"><span data-stu-id="3de1e-145">file format <em>format</em></span></span></li>
<li><span data-ttu-id="3de1e-146">Cerca esattamente in</span><span class="sxs-lookup"><span data-stu-id="3de1e-146">seek exactly on</span></span></li>
<li><span data-ttu-id="3de1e-147">Cerca esattamente fuori</span><span class="sxs-lookup"><span data-stu-id="3de1e-147">seek exactly off</span></span></li>
<li><span data-ttu-id="3de1e-148"><em>fattore</em> di velocità</span><span class="sxs-lookup"><span data-stu-id="3de1e-148">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="3de1e-149"><em>formato</em> file ancora</span><span class="sxs-lookup"><span data-stu-id="3de1e-149">still file format <em>format</em></span></span></li>
<li><span data-ttu-id="3de1e-150">frame formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-150">time format frames</span></span></li>
<li><span data-ttu-id="3de1e-151">millisecondi formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-151">time format milliseconds</span></span></li>
<li><span data-ttu-id="3de1e-152">video disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-152">video off</span></span></li>
<li><span data-ttu-id="3de1e-153">video su</span><span class="sxs-lookup"><span data-stu-id="3de1e-153">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-154">overlay</span><span class="sxs-lookup"><span data-stu-id="3de1e-154">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="3de1e-155">audio tutto disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-155">audio all off</span></span></li>
<li><span data-ttu-id="3de1e-156">audio tutto su</span><span class="sxs-lookup"><span data-stu-id="3de1e-156">audio all on</span></span></li>
<li><span data-ttu-id="3de1e-157">Audio interrotto</span><span class="sxs-lookup"><span data-stu-id="3de1e-157">audio left off</span></span></li>
<li><span data-ttu-id="3de1e-158">audio lasciato acceso</span><span class="sxs-lookup"><span data-stu-id="3de1e-158">audio left on</span></span></li>
<li><span data-ttu-id="3de1e-159">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-159">audio right off</span></span></li>
<li><span data-ttu-id="3de1e-160">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-160">audio right on</span></span></li>
<li><span data-ttu-id="3de1e-161">sportello chiuso</span><span class="sxs-lookup"><span data-stu-id="3de1e-161">door closed</span></span></li>
<li><span data-ttu-id="3de1e-162">sportello aperto</span><span class="sxs-lookup"><span data-stu-id="3de1e-162">door open</span></span></li>
<li><span data-ttu-id="3de1e-163">video disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-163">video off</span></span></li>
<li><span data-ttu-id="3de1e-164">video su</span><span class="sxs-lookup"><span data-stu-id="3de1e-164">video on</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-165">sequencer</span><span class="sxs-lookup"><span data-stu-id="3de1e-165">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="3de1e-166">audio tutto disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-166">audio all off</span></span></li>
<li><span data-ttu-id="3de1e-167">audio tutto su</span><span class="sxs-lookup"><span data-stu-id="3de1e-167">audio all on</span></span></li>
<li><span data-ttu-id="3de1e-168">Audio interrotto</span><span class="sxs-lookup"><span data-stu-id="3de1e-168">audio left off</span></span></li>
<li><span data-ttu-id="3de1e-169">audio lasciato acceso</span><span class="sxs-lookup"><span data-stu-id="3de1e-169">audio left on</span></span></li>
<li><span data-ttu-id="3de1e-170">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-170">audio right off</span></span></li>
<li><span data-ttu-id="3de1e-171">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-171">audio right on</span></span></li>
<li><span data-ttu-id="3de1e-172">sportello chiuso</span><span class="sxs-lookup"><span data-stu-id="3de1e-172">door closed</span></span></li>
<li><span data-ttu-id="3de1e-173">sportello aperto</span><span class="sxs-lookup"><span data-stu-id="3de1e-173">door open</span></span></li>
<li><span data-ttu-id="3de1e-174">MIDI Master</span><span class="sxs-lookup"><span data-stu-id="3de1e-174">master MIDI</span></span></li>
<li><span data-ttu-id="3de1e-175">nessuno Master</span><span class="sxs-lookup"><span data-stu-id="3de1e-175">master none</span></span></li>
<li><span data-ttu-id="3de1e-176">SMPTE Master</span><span class="sxs-lookup"><span data-stu-id="3de1e-176">master SMPTE</span></span></li>
<li><span data-ttu-id="3de1e-177"><em>tempo</em> di offset</span><span class="sxs-lookup"><span data-stu-id="3de1e-177">offset <em>time</em></span></span></li>
<li><span data-ttu-id="3de1e-178">Mapper porta</span><span class="sxs-lookup"><span data-stu-id="3de1e-178">port mapper</span></span></li>
<li><span data-ttu-id="3de1e-179">Nessuna porta</span><span class="sxs-lookup"><span data-stu-id="3de1e-179">port none</span></span></li>
<li><span data-ttu-id="3de1e-180"><em>port_number</em> porta</span><span class="sxs-lookup"><span data-stu-id="3de1e-180">port <em>port_number</em></span></span></li>
<li><span data-ttu-id="3de1e-181">file slave</span><span class="sxs-lookup"><span data-stu-id="3de1e-181">slave file</span></span></li>
<li><span data-ttu-id="3de1e-182">MIDI slave</span><span class="sxs-lookup"><span data-stu-id="3de1e-182">slave MIDI</span></span></li>
<li><span data-ttu-id="3de1e-183">slave None</span><span class="sxs-lookup"><span data-stu-id="3de1e-183">slave none</span></span></li>
<li><span data-ttu-id="3de1e-184">SMPTE slave</span><span class="sxs-lookup"><span data-stu-id="3de1e-184">slave SMPTE</span></span></li>
<li><span data-ttu-id="3de1e-185"><em>tempo_value</em> tempo</span><span class="sxs-lookup"><span data-stu-id="3de1e-185">tempo <em>tempo_value</em></span></span></li>
<li><span data-ttu-id="3de1e-186">millisecondi formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-186">time format milliseconds</span></span></li>
<li><span data-ttu-id="3de1e-187">formato ora SMPTE <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="3de1e-187">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="3de1e-188">formato ora SMPTE 30 drop</span><span class="sxs-lookup"><span data-stu-id="3de1e-188">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="3de1e-189">puntatore al formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-189">time format song pointer</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-190"><strong>VCR</strong></span><span class="sxs-lookup"><span data-stu-id="3de1e-190"><strong>vcr</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="3de1e-191">assembla record su</span><span class="sxs-lookup"><span data-stu-id="3de1e-191">assemble record on</span></span></li>
<li><span data-ttu-id="3de1e-192">assembla record disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-192">assemble record off</span></span></li>
<li><span data-ttu-id="3de1e-193">audio tutto disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-193">audio all off</span></span></li>
<li><span data-ttu-id="3de1e-194">audio tutto su</span><span class="sxs-lookup"><span data-stu-id="3de1e-194">audio all on</span></span></li>
<li><span data-ttu-id="3de1e-195">Audio interrotto</span><span class="sxs-lookup"><span data-stu-id="3de1e-195">audio left off</span></span></li>
<li><span data-ttu-id="3de1e-196">audio lasciato acceso</span><span class="sxs-lookup"><span data-stu-id="3de1e-196">audio left on</span></span></li>
<li><span data-ttu-id="3de1e-197">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-197">audio right off</span></span></li>
<li><span data-ttu-id="3de1e-198">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-198">audio right on</span></span></li>
<li><span data-ttu-id="3de1e-199"><em>ora</em> di clock</span><span class="sxs-lookup"><span data-stu-id="3de1e-199">clock <em>time</em></span></span></li>
<li><span data-ttu-id="3de1e-200">formato contatore</span><span class="sxs-lookup"><span data-stu-id="3de1e-200">counter format</span></span></li>
<li><span data-ttu-id="3de1e-201"><em>valore</em> contatore</span><span class="sxs-lookup"><span data-stu-id="3de1e-201">counter <em>value</em></span></span></li>
<li><span data-ttu-id="3de1e-202">sportello chiuso</span><span class="sxs-lookup"><span data-stu-id="3de1e-202">door closed</span></span></li>
<li><span data-ttu-id="3de1e-203">sportello aperto</span><span class="sxs-lookup"><span data-stu-id="3de1e-203">door open</span></span></li>
<li><span data-ttu-id="3de1e-204">contatore indice</span><span class="sxs-lookup"><span data-stu-id="3de1e-204">index counter</span></span></li>
<li><span data-ttu-id="3de1e-205">Data di indice</span><span class="sxs-lookup"><span data-stu-id="3de1e-205">index date</span></span></li>
<li><span data-ttu-id="3de1e-206">tempo di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="3de1e-206">index time</span></span></li>
<li><span data-ttu-id="3de1e-207">tempo di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="3de1e-207">index time</span></span></li>
<li><span data-ttu-id="3de1e-208"><em>durata</em> CodeLength</span><span class="sxs-lookup"><span data-stu-id="3de1e-208">codelength <em>duration</em></span></span></li>
<li><span data-ttu-id="3de1e-209"><em>timeout</em> pausa</span><span class="sxs-lookup"><span data-stu-id="3de1e-209">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="3de1e-210">durata postroll-</span><span class="sxs-lookup"><span data-stu-id="3de1e-210">postroll duration -</span></span></li>
<li><span data-ttu-id="3de1e-211"><em>duration</em></span><span class="sxs-lookup"><span data-stu-id="3de1e-211"><em>duration</em></span></span></li>
<li><span data-ttu-id="3de1e-212">accensione</span><span class="sxs-lookup"><span data-stu-id="3de1e-212">power on</span></span></li>
<li><span data-ttu-id="3de1e-213">spegnimento</span><span class="sxs-lookup"><span data-stu-id="3de1e-213">power off</span></span></li>
<li><span data-ttu-id="3de1e-214"><em>durata</em> della preregistrazione</span><span class="sxs-lookup"><span data-stu-id="3de1e-214">preroll duration <em>duration</em></span></span></li>
<li><span data-ttu-id="3de1e-215">SP formato record</span><span class="sxs-lookup"><span data-stu-id="3de1e-215">record format SP</span></span></li>
<li><span data-ttu-id="3de1e-216">formato record LP</span><span class="sxs-lookup"><span data-stu-id="3de1e-216">record format LP</span></span></li>
<li><span data-ttu-id="3de1e-217">formato record EP</span><span class="sxs-lookup"><span data-stu-id="3de1e-217">record format EP</span></span></li>
<li><span data-ttu-id="3de1e-218"><em>fattore</em> di velocità</span><span class="sxs-lookup"><span data-stu-id="3de1e-218">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="3de1e-219">frame formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-219">time format frames</span></span></li>
<li><span data-ttu-id="3de1e-220">formato ora HMS</span><span class="sxs-lookup"><span data-stu-id="3de1e-220">time format hms</span></span></li>
<li><span data-ttu-id="3de1e-221">millisecondi formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-221">time format milliseconds</span></span></li>
<li><span data-ttu-id="3de1e-222">formato ora MSF</span><span class="sxs-lookup"><span data-stu-id="3de1e-222">time format msf</span></span></li>
<li><span data-ttu-id="3de1e-223">formato ora SMPTE <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="3de1e-223">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="3de1e-224">formato ora SMPTE 30 drop</span><span class="sxs-lookup"><span data-stu-id="3de1e-224">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="3de1e-225">formato ora TMSF</span><span class="sxs-lookup"><span data-stu-id="3de1e-225">time format tmsf</span></span></li>
<li><span data-ttu-id="3de1e-226">contatore modalità ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-226">time mode counter</span></span></li>
<li><span data-ttu-id="3de1e-227">rilevamento modalità tempo</span><span class="sxs-lookup"><span data-stu-id="3de1e-227">time mode detect</span></span></li>
<li><span data-ttu-id="3de1e-228">timecode modalità ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-228">time mode timecode</span></span></li>
<li><span data-ttu-id="3de1e-229">rilevamento e</span><span class="sxs-lookup"><span data-stu-id="3de1e-229">tracking plus</span></span></li>
<li><span data-ttu-id="3de1e-230">meno rilevamento</span><span class="sxs-lookup"><span data-stu-id="3de1e-230">tracking minus</span></span></li>
<li><span data-ttu-id="3de1e-231">rilevamento reimpostazione</span><span class="sxs-lookup"><span data-stu-id="3de1e-231">tracking reset</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-232">videodisco</span><span class="sxs-lookup"><span data-stu-id="3de1e-232">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="3de1e-233">audio tutto disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-233">audio all off</span></span></li>
<li><span data-ttu-id="3de1e-234">audio tutto su</span><span class="sxs-lookup"><span data-stu-id="3de1e-234">audio all on</span></span></li>
<li><span data-ttu-id="3de1e-235">Audio interrotto</span><span class="sxs-lookup"><span data-stu-id="3de1e-235">audio left off</span></span></li>
<li><span data-ttu-id="3de1e-236">audio lasciato acceso</span><span class="sxs-lookup"><span data-stu-id="3de1e-236">audio left on</span></span></li>
<li><span data-ttu-id="3de1e-237">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-237">audio right off</span></span></li>
<li><span data-ttu-id="3de1e-238">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-238">audio right on</span></span></li>
<li><span data-ttu-id="3de1e-239">sportello chiuso</span><span class="sxs-lookup"><span data-stu-id="3de1e-239">door closed</span></span></li>
<li><span data-ttu-id="3de1e-240">sportello aperto</span><span class="sxs-lookup"><span data-stu-id="3de1e-240">door open</span></span></li>
<li><span data-ttu-id="3de1e-241">frame formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-241">time format frames</span></span></li>
<li><span data-ttu-id="3de1e-242">formato ora HMS</span><span class="sxs-lookup"><span data-stu-id="3de1e-242">time format hms</span></span></li>
<li><span data-ttu-id="3de1e-243">millisecondi formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-243">time format milliseconds</span></span></li>
<li><span data-ttu-id="3de1e-244">traccia formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-244">time format track</span></span></li>
<li><span data-ttu-id="3de1e-245">video disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-245">video off</span></span></li>
<li><span data-ttu-id="3de1e-246">video su</span><span class="sxs-lookup"><span data-stu-id="3de1e-246">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-247">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="3de1e-247">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="3de1e-248"><em>Integer</em> allineamento</span><span class="sxs-lookup"><span data-stu-id="3de1e-248">alignment <em>integer</em></span></span></li>
<li><span data-ttu-id="3de1e-249">qualsiasi input</span><span class="sxs-lookup"><span data-stu-id="3de1e-249">any input</span></span></li>
<li><span data-ttu-id="3de1e-250">qualsiasi output</span><span class="sxs-lookup"><span data-stu-id="3de1e-250">any output</span></span></li>
<li><span data-ttu-id="3de1e-251">audio tutto disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-251">audio all off</span></span></li>
<li><span data-ttu-id="3de1e-252">audio tutto su</span><span class="sxs-lookup"><span data-stu-id="3de1e-252">audio all on</span></span></li>
<li><span data-ttu-id="3de1e-253">Audio interrotto</span><span class="sxs-lookup"><span data-stu-id="3de1e-253">audio left off</span></span></li>
<li><span data-ttu-id="3de1e-254">audio lasciato acceso</span><span class="sxs-lookup"><span data-stu-id="3de1e-254">audio left on</span></span></li>
<li><span data-ttu-id="3de1e-255">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-255">audio right off</span></span></li>
<li><span data-ttu-id="3de1e-256">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-256">audio right on</span></span></li>
<li><span data-ttu-id="3de1e-257"><em>bit_count</em> BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="3de1e-257">bitspersample <em>bit_count</em></span></span></li>
<li><span data-ttu-id="3de1e-258"><em>byte_rate</em> bytespersec</span><span class="sxs-lookup"><span data-stu-id="3de1e-258">bytespersec <em>byte_rate</em></span></span></li>
<li><span data-ttu-id="3de1e-259">canali <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="3de1e-259">channels <em>channel_count</em></span></span></li>
<li><span data-ttu-id="3de1e-260">sportello chiuso</span><span class="sxs-lookup"><span data-stu-id="3de1e-260">door closed</span></span></li>
<li><span data-ttu-id="3de1e-261">sportello aperto</span><span class="sxs-lookup"><span data-stu-id="3de1e-261">door open</span></span></li>
<li><span data-ttu-id="3de1e-262">formato PCM Tag</span><span class="sxs-lookup"><span data-stu-id="3de1e-262">format tag pcm</span></span></li>
<li><span data-ttu-id="3de1e-263"><em>tag</em> di formato tag</span><span class="sxs-lookup"><span data-stu-id="3de1e-263">format tag <em>tag</em></span></span></li>
<li><span data-ttu-id="3de1e-264"><em>Integer</em> di input</span><span class="sxs-lookup"><span data-stu-id="3de1e-264">input <em>integer</em></span></span></li>
<li><span data-ttu-id="3de1e-265"><em>intero</em> di output</span><span class="sxs-lookup"><span data-stu-id="3de1e-265">output <em>integer</em></span></span></li>
<li><span data-ttu-id="3de1e-266">samplespersec <em>Integer</em></span><span class="sxs-lookup"><span data-stu-id="3de1e-266">samplespersec <em>integer</em></span></span></li>
<li><span data-ttu-id="3de1e-267">byte formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-267">time format bytes</span></span></li>
<li><span data-ttu-id="3de1e-268">millisecondi formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-268">time format milliseconds</span></span></li>
<li><span data-ttu-id="3de1e-269">esempi di formato time</span><span class="sxs-lookup"><span data-stu-id="3de1e-269">time format samples</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3de1e-270">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszSetting** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="3de1e-270">The following table lists the flags that can be specified in the **lpszSetting** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3de1e-271">Valore</span><span class="sxs-lookup"><span data-stu-id="3de1e-271">Value</span></span></th>
<th><span data-ttu-id="3de1e-272">Significato</span><span class="sxs-lookup"><span data-stu-id="3de1e-272">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3de1e-273"><em>Integer</em> allineamento</span><span class="sxs-lookup"><span data-stu-id="3de1e-273">alignment <em>integer</em></span></span></td>
<td><span data-ttu-id="3de1e-274">Imposta l'allineamento dei blocchi di dati rispetto all'inizio dei dati passati al dispositivo Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="3de1e-274">Sets the alignment of data blocks relative to the start of data passed to the waveform-audio device.</span></span> <span data-ttu-id="3de1e-275">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-275">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-276">qualsiasi input</span><span class="sxs-lookup"><span data-stu-id="3de1e-276">any input</span></span></td>
<td><span data-ttu-id="3de1e-277">Usare qualsiasi input che supporti il formato corrente durante la registrazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-277">Use any input that supports the current format when recording.</span></span> <span data-ttu-id="3de1e-278">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3de1e-278">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-279">qualsiasi output</span><span class="sxs-lookup"><span data-stu-id="3de1e-279">any output</span></span></td>
<td><span data-ttu-id="3de1e-280">Usare qualsiasi output che supporti il formato corrente durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-280">Use any output that supports the current format when playing.</span></span> <span data-ttu-id="3de1e-281">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3de1e-281">This is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-282">assembla record su</span><span class="sxs-lookup"><span data-stu-id="3de1e-282">assemble record on</span></span> <br/> <span data-ttu-id="3de1e-283">assembla record disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-283">assemble record off</span></span> <br/></td>
<td><span data-ttu-id="3de1e-284">In modalità assembla tutte le tracce vengono registrate come definito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3de1e-284">In assemble mode, all tracks are recorded as defined by the device.</span></span> <span data-ttu-id="3de1e-285">Per impostazione predefinita, la maggior parte dei VCR è in modalità assembler.</span><span class="sxs-lookup"><span data-stu-id="3de1e-285">Most VCRs are in assemble mode by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-286">audio tutto disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-286">audio all off</span></span> <br/> <span data-ttu-id="3de1e-287">audio tutto su</span><span class="sxs-lookup"><span data-stu-id="3de1e-287">audio all on</span></span> <br/></td>
<td><span data-ttu-id="3de1e-288">Disabilita o Abilita l'output audio.</span><span class="sxs-lookup"><span data-stu-id="3de1e-288">Disables or enables audio output.</span></span> <span data-ttu-id="3de1e-289">I dispositivi overlay video, MCISEQ sequencer e MCIWAVE Waveform-Audio Device non supportano questo flag.</span><span class="sxs-lookup"><span data-stu-id="3de1e-289">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-290">Audio interrotto</span><span class="sxs-lookup"><span data-stu-id="3de1e-290">audio left off</span></span> <br/> <span data-ttu-id="3de1e-291">audio lasciato acceso</span><span class="sxs-lookup"><span data-stu-id="3de1e-291">audio left on</span></span> <br/> <span data-ttu-id="3de1e-292">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-292">audio right off</span></span> <br/> <span data-ttu-id="3de1e-293">audio a destra</span><span class="sxs-lookup"><span data-stu-id="3de1e-293">audio right on</span></span> <br/></td>
<td><span data-ttu-id="3de1e-294">Disabilita o Abilita l'output sul canale audio a sinistra o a destra.</span><span class="sxs-lookup"><span data-stu-id="3de1e-294">Disables or enables output to either the left or the right audio channel.</span></span> <span data-ttu-id="3de1e-295">I dispositivi overlay video, MCISEQ sequencer e MCIWAVE Waveform-Audio Device non supportano questo flag.</span><span class="sxs-lookup"><span data-stu-id="3de1e-295">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-296"><em>bit_count</em> BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="3de1e-296">bitspersample <em>bit_count</em></span></span></td>
<td><span data-ttu-id="3de1e-297">Imposta il numero di bit per PCM (Pulse Code Modulation) campione riprodotto o registrato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-297">Sets the number of bits per PCM (Pulse Code Modulation) sample played or recorded.</span></span> <span data-ttu-id="3de1e-298">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-298">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-299"><em>byte_rate</em> bytespersec</span><span class="sxs-lookup"><span data-stu-id="3de1e-299">bytespersec <em>byte_rate</em></span></span></td>
<td><span data-ttu-id="3de1e-300">Imposta il numero medio di byte al secondo riprodotti o registrati.</span><span class="sxs-lookup"><span data-stu-id="3de1e-300">Sets the average number of bytes per second played or recorded.</span></span> <span data-ttu-id="3de1e-301">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-301">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-302">canali <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="3de1e-302">channels <em>channel_count</em></span></span></td>
<td><span data-ttu-id="3de1e-303">Imposta i canali per la riproduzione e la registrazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-303">Sets the channels for playing and recording.</span></span> <span data-ttu-id="3de1e-304">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-304">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-305"><em>ora</em> di clock</span><span class="sxs-lookup"><span data-stu-id="3de1e-305">clock <em>time</em></span></span></td>
<td><span data-ttu-id="3de1e-306">Imposta l'ora sul clock esterno per il <em>tempo.</em></span><span class="sxs-lookup"><span data-stu-id="3de1e-306">Sets time on the external clock to <em>time.</em></span></span> <span data-ttu-id="3de1e-307">Il formato è specificato come Long Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="3de1e-307">The format is specified as a long unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-308">formato contatore</span><span class="sxs-lookup"><span data-stu-id="3de1e-308">counter format</span></span></td>
<td><span data-ttu-id="3de1e-309">Imposta il formato dell'ora per il contatore, come restituito dal contatore di <a href="status.md">stato</a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="3de1e-309">Set the time format for the counter, as returned by <a href="status.md">status</a> &quot;counter&quot;.</span></span> <span data-ttu-id="3de1e-310">Per informazioni sui tipi applicabili, vedere il comando <strong>set</strong> &quot; Time Format &quot; .</span><span class="sxs-lookup"><span data-stu-id="3de1e-310">For information about applicable types, see the <strong>set</strong> &quot;time format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-311"><em>valore</em> contatore</span><span class="sxs-lookup"><span data-stu-id="3de1e-311">counter <em>value</em></span></span></td>
<td><span data-ttu-id="3de1e-312">Imposta il contatore VCR sul valore specificato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-312">Sets the VCR counter to the specified value.</span></span> <span data-ttu-id="3de1e-313">Il valore deve essere specificato nel formato del contatore corrente.</span><span class="sxs-lookup"><span data-stu-id="3de1e-313">The value must be specified in the current counter format.</span></span> <span data-ttu-id="3de1e-314">Per ulteriori informazioni, vedere il comando <strong>imposta</strong> &quot; formato contatore &quot; .</span><span class="sxs-lookup"><span data-stu-id="3de1e-314">For more information, see the <strong>set</strong> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-315">sportello chiuso</span><span class="sxs-lookup"><span data-stu-id="3de1e-315">door closed</span></span></td>
<td><span data-ttu-id="3de1e-316">Ritrae la barra e chiude la porta, se possibile.</span><span class="sxs-lookup"><span data-stu-id="3de1e-316">Retracts the tray and closes the door, if possible.</span></span> <span data-ttu-id="3de1e-317">Per i VCR, carica il nastro automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3de1e-317">For VCRs, loads the tape automatically.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-318">sportello aperto</span><span class="sxs-lookup"><span data-stu-id="3de1e-318">door open</span></span></td>
<td><span data-ttu-id="3de1e-319">Apre lo sportello ed espelle la barra o il nastro, se possibile.</span><span class="sxs-lookup"><span data-stu-id="3de1e-319">Opens the door and ejects the tray or tape, if possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-320"><em>formato</em> formato file</span><span class="sxs-lookup"><span data-stu-id="3de1e-320">file format <em>format</em></span></span></td>
<td><span data-ttu-id="3de1e-321">Specifica un formato di file utilizzato per i comandi di <a href="save.md">salvataggio</a> o <a href="capture.md">acquisizione</a> .</span><span class="sxs-lookup"><span data-stu-id="3de1e-321">Specifies a file format that is used for <a href="save.md">save</a> or <a href="capture.md">capture</a> commands.</span></span> <span data-ttu-id="3de1e-322">Se omesso, per impostazione predefinita è possibile che sia un formato definito dal driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3de1e-322">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="3de1e-323">Se il formato di file specificato è in conflitto con l'algoritmo e la qualità attualmente selezionati, verranno modificati nei valori predefiniti per il formato di file.</span><span class="sxs-lookup"><span data-stu-id="3de1e-323">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="3de1e-324">Sono definiti i formati di file seguenti:</span><span class="sxs-lookup"><span data-stu-id="3de1e-324">The following file formats are defined:</span></span>
<ul>
<li><span data-ttu-id="3de1e-325">AVI: specifica il formato AVI.</span><span class="sxs-lookup"><span data-stu-id="3de1e-325">avi: Specifies AVI format.</span></span></li>
<li><span data-ttu-id="3de1e-326">avss: specifica il formato di AVSS.</span><span class="sxs-lookup"><span data-stu-id="3de1e-326">avss: Specifies AVSS format.</span></span></li>
<li><span data-ttu-id="3de1e-327">DIB: specifica il formato DIB.</span><span class="sxs-lookup"><span data-stu-id="3de1e-327">dib: Specifies DIB format.</span></span></li>
<li><span data-ttu-id="3de1e-328">JFIF: specifica il formato di JFIF.</span><span class="sxs-lookup"><span data-stu-id="3de1e-328">jfif: Specifies JFIF format.</span></span></li>
<li><span data-ttu-id="3de1e-329">JPEG: specifica il formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="3de1e-329">jpeg: Specifies JPEG format.</span></span></li>
<li><span data-ttu-id="3de1e-330">MPEG: specifica il formato MPEG.</span><span class="sxs-lookup"><span data-stu-id="3de1e-330">mpeg: Specifies MPEG format.</span></span></li>
<li><span data-ttu-id="3de1e-331">rdib: specifica il formato DIB di RLE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-331">rdib: Specifies RLE DIB format.</span></span></li>
<li><span data-ttu-id="3de1e-332">rjpeg: specifica il formato di RJPEG.</span><span class="sxs-lookup"><span data-stu-id="3de1e-332">rjpeg: Specifies RJPEG format.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-333">formato PCM Tag</span><span class="sxs-lookup"><span data-stu-id="3de1e-333">format tag pcm</span></span></td>
<td><span data-ttu-id="3de1e-334">Imposta il tipo di formato su PCM per la riproduzione e la registrazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-334">Sets the format type to PCM for playing and recording.</span></span> <span data-ttu-id="3de1e-335">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-335">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-336"><em>tag</em> di formato tag</span><span class="sxs-lookup"><span data-stu-id="3de1e-336">format tag <em>tag</em></span></span></td>
<td><span data-ttu-id="3de1e-337">Imposta il tipo di formato per la riproduzione e la registrazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-337">Sets the format type for playing and recording.</span></span> <span data-ttu-id="3de1e-338">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-338">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-339">codice temporale indice</span><span class="sxs-lookup"><span data-stu-id="3de1e-339">index timecode</span></span> <br/> <span data-ttu-id="3de1e-340">contatore indice</span><span class="sxs-lookup"><span data-stu-id="3de1e-340">index counter</span></span> <br/> <span data-ttu-id="3de1e-341">Data di indice</span><span class="sxs-lookup"><span data-stu-id="3de1e-341">index date</span></span> <br/> <span data-ttu-id="3de1e-342">tempo di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="3de1e-342">index time</span></span> <br/></td>
<td><span data-ttu-id="3de1e-343">Imposta la schermata di visualizzazione corrente sul videoregistratore.</span><span class="sxs-lookup"><span data-stu-id="3de1e-343">Sets the current display screen on the VCR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-344"><em>Integer</em> di input</span><span class="sxs-lookup"><span data-stu-id="3de1e-344">input <em>integer</em></span></span></td>
<td><span data-ttu-id="3de1e-345">Imposta il canale audio utilizzato come input.</span><span class="sxs-lookup"><span data-stu-id="3de1e-345">Sets the audio channel used as the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-346"><em>durata</em> lunghezza</span><span class="sxs-lookup"><span data-stu-id="3de1e-346">length <em>duration</em></span></span></td>
<td><span data-ttu-id="3de1e-347">Imposta la lunghezza del nastro specificata dall'utente nel VCR.</span><span class="sxs-lookup"><span data-stu-id="3de1e-347">Sets the user-specified length of the tape in the VCR.</span></span> <span data-ttu-id="3de1e-348">Questa lunghezza viene restituita dal comando di lunghezza <a href="status.md">dello stato</a> &quot; &quot; e viene fornita per la compatibilità con le applicazioni che richiedono che questo comando restituisca una lunghezza valida.</span><span class="sxs-lookup"><span data-stu-id="3de1e-348">This length is returned by the <a href="status.md">status</a> &quot;length&quot; command and is provided for compatibility with applications that require this command to return a valid length.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-349">MIDI Master</span><span class="sxs-lookup"><span data-stu-id="3de1e-349">master midi</span></span></td>
<td><span data-ttu-id="3de1e-350">Imposta il sequencer MIDI come origine della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-350">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="3de1e-351">I dati di sincronizzazione vengono inviati in formato MIDI.</span><span class="sxs-lookup"><span data-stu-id="3de1e-351">Synchronization data is sent in MIDI format.</span></span> <span data-ttu-id="3de1e-352">MCISEQ sequencer non supporta questo flag.</span><span class="sxs-lookup"><span data-stu-id="3de1e-352">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-353">nessuno Master</span><span class="sxs-lookup"><span data-stu-id="3de1e-353">master none</span></span></td>
<td><span data-ttu-id="3de1e-354">Impedisce al sequencer MIDI di inviare i dati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-354">Inhibits the MIDI sequencer from sending synchronization data.</span></span> <span data-ttu-id="3de1e-355">MCISEQ sequencer non supporta questo flag.</span><span class="sxs-lookup"><span data-stu-id="3de1e-355">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-356">SMPTE Master</span><span class="sxs-lookup"><span data-stu-id="3de1e-356">master smpte</span></span></td>
<td><span data-ttu-id="3de1e-357">Imposta il sequencer MIDI come origine della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-357">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="3de1e-358">I dati di sincronizzazione vengono inviati in formato SMPTE (Society of Motion Picture and Television Engineers).</span><span class="sxs-lookup"><span data-stu-id="3de1e-358">Synchronization data is sent in SMPTE (Society of Motion Picture and Television Engineers) format.</span></span> <span data-ttu-id="3de1e-359">MCISEQ sequencer non supporta questo flag.</span><span class="sxs-lookup"><span data-stu-id="3de1e-359">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-360"><em>tempo</em> di offset</span><span class="sxs-lookup"><span data-stu-id="3de1e-360">offset <em>time</em></span></span></td>
<td><span data-ttu-id="3de1e-361">Imposta il <em>tempo</em>di offset SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-361">Sets the SMPTE offset <em>time</em>.</span></span> <span data-ttu-id="3de1e-362">L'offset è l'ora di inizio di una sequenza basata su SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-362">The offset is the beginning time of a SMPTE based sequence.</span></span> <span data-ttu-id="3de1e-363">Il <em>tempo</em> è espresso come <em>HH</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames.</span><span class="sxs-lookup"><span data-stu-id="3de1e-363">The <em>time</em> is expressed as <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-364"><em>intero</em> di output</span><span class="sxs-lookup"><span data-stu-id="3de1e-364">output <em>integer</em></span></span></td>
<td><span data-ttu-id="3de1e-365">Imposta il canale audio utilizzato come output.</span><span class="sxs-lookup"><span data-stu-id="3de1e-365">Sets the audio channel used as the output.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-366"><em>timeout</em> pausa</span><span class="sxs-lookup"><span data-stu-id="3de1e-366">pause <em>timeout</em></span></span></td>
<td><span data-ttu-id="3de1e-367">Imposta la durata massima, in millisecondi, di un comando di <a href="pause.md">sospensione</a> .</span><span class="sxs-lookup"><span data-stu-id="3de1e-367">Sets the maximum duration, in milliseconds, of a <a href="pause.md">pause</a> command.</span></span> <span data-ttu-id="3de1e-368">Un valore di <em>timeout</em> pari a zero indica che non si verificherà alcun timeout.</span><span class="sxs-lookup"><span data-stu-id="3de1e-368">A <em>timeout</em> value of zero indicates that no time-out will occur.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-369"><em>durata</em> della durata del postroll</span><span class="sxs-lookup"><span data-stu-id="3de1e-369">postroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="3de1e-370">Imposta la lunghezza, nel formato dell'ora corrente, necessaria per bloccare il trasporto del videoregistratore quando viene eseguito un comando di <a href="stop.md">arresto</a> o <strong>sospensione</strong> .</span><span class="sxs-lookup"><span data-stu-id="3de1e-370">Sets the length, in the current time format, needed to brake the VCR transport when a <a href="stop.md">stop</a> or <strong>pause</strong> command is issued.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-371">Mapper porta</span><span class="sxs-lookup"><span data-stu-id="3de1e-371">port mapper</span></span></td>
<td><span data-ttu-id="3de1e-372">Imposta il mapper MIDI come la porta che riceve i messaggi MIDI.</span><span class="sxs-lookup"><span data-stu-id="3de1e-372">Sets the MIDI mapper as the port receiving the MIDI messages.</span></span> <span data-ttu-id="3de1e-373">Questo comando non riesce se il mapper MIDI o una porta necessaria è usato da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-373">This command fails if the MIDI mapper or a port it needs is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-374">Nessuna porta</span><span class="sxs-lookup"><span data-stu-id="3de1e-374">port none</span></span></td>
<td><span data-ttu-id="3de1e-375">Disabilita l'invio di messaggi MIDI.</span><span class="sxs-lookup"><span data-stu-id="3de1e-375">Disables the sending of MIDI messages.</span></span> <span data-ttu-id="3de1e-376">Questo comando chiude anche una porta MIDI.</span><span class="sxs-lookup"><span data-stu-id="3de1e-376">This command also closes a MIDI port.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-377"><em>port_number</em> porta</span><span class="sxs-lookup"><span data-stu-id="3de1e-377">port <em>port_number</em></span></span></td>
<td><span data-ttu-id="3de1e-378">Imposta la porta MIDI che riceve i messaggi MIDI.</span><span class="sxs-lookup"><span data-stu-id="3de1e-378">Sets the MIDI port receiving the MIDI messages.</span></span> <span data-ttu-id="3de1e-379">Questo comando ha esito negativo se la porta che si sta tentando di aprire è utilizzata da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-379">This command fails if the port you are trying to open is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-380">accensione</span><span class="sxs-lookup"><span data-stu-id="3de1e-380">power on</span></span> <br/> <span data-ttu-id="3de1e-381">spegnimento</span><span class="sxs-lookup"><span data-stu-id="3de1e-381">power off</span></span> <br/></td>
<td><span data-ttu-id="3de1e-382">Imposta l'alimentazione del dispositivo su on o off.</span><span class="sxs-lookup"><span data-stu-id="3de1e-382">Sets the device power to on or off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-383"><em>durata</em> della preregistrazione</span><span class="sxs-lookup"><span data-stu-id="3de1e-383">preroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="3de1e-384">Imposta la lunghezza, nel formato dell'ora corrente, necessaria per stabilizzare l'output del VCR.</span><span class="sxs-lookup"><span data-stu-id="3de1e-384">Sets the length, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-385">SP formato record</span><span class="sxs-lookup"><span data-stu-id="3de1e-385">record format SP</span></span> <br/> <span data-ttu-id="3de1e-386">formato record LP</span><span class="sxs-lookup"><span data-stu-id="3de1e-386">record format LP</span></span> <br/> <span data-ttu-id="3de1e-387">formato record EP</span><span class="sxs-lookup"><span data-stu-id="3de1e-387">record format EP</span></span> <br/></td>
<td><span data-ttu-id="3de1e-388">Imposta la modalità di registrazione per il VCR su SP per la riproduzione standard, EP for Extended Play o LP per la riproduzione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="3de1e-388">Sets the recording mode for the VCR to SP for standard play, EP for extended play, or LP for long play.</span></span> <span data-ttu-id="3de1e-389">Questi valori non sono destinati a essere specifici della VHS.</span><span class="sxs-lookup"><span data-stu-id="3de1e-389">These values are not intended to be VHS specific.</span></span> <span data-ttu-id="3de1e-390">Eseguono il mapping a tre modalità appropriate con altri formati di nastro.</span><span class="sxs-lookup"><span data-stu-id="3de1e-390">They map to any three appropriate modes with other tape formats.</span></span> <span data-ttu-id="3de1e-391">Ad esempio, SP esegue il mapping alla registrazione più veloce e di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="3de1e-391">For example, SP maps to the fastest, highest quality recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-392">samplespersec <em>Integer</em></span><span class="sxs-lookup"><span data-stu-id="3de1e-392">samplespersec <em>integer</em></span></span></td>
<td><span data-ttu-id="3de1e-393">Imposta la frequenza di campionamento per la riproduzione e la registrazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-393">Sets the sample rate for playing and recording.</span></span> <span data-ttu-id="3de1e-394">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-394">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-395">Cerca esattamente in</span><span class="sxs-lookup"><span data-stu-id="3de1e-395">seek exactly on</span></span><br/> <span data-ttu-id="3de1e-396">Cerca esattamente fuori</span><span class="sxs-lookup"><span data-stu-id="3de1e-396">seek exactly off</span></span> <br/></td>
<td><span data-ttu-id="3de1e-397">Seleziona una delle due modalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="3de1e-397">Selects one of two seek modes.</span></span> <span data-ttu-id="3de1e-398">Con &quot; Seek exactly on &quot; , Seek viene sempre spostato nel frame specificato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-398">With &quot;seek exactly on&quot;, seek will always move to the frame specified.</span></span> <span data-ttu-id="3de1e-399">Con la &quot; ricerca esatta &quot; , la ricerca viene spostata nel fotogramma chiave più vicino prima del frame specificato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-399">With &quot;seek exactly off&quot;, seek will move to the closest key frame prior to the frame specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-400">file slave</span><span class="sxs-lookup"><span data-stu-id="3de1e-400">slave file</span></span></td>
<td><span data-ttu-id="3de1e-401">Imposta MIDI sequencer in modo che utilizzi i dati dei file come origine della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-401">Sets the MIDI sequencer to use file data as the synchronization source.</span></span> <span data-ttu-id="3de1e-402">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3de1e-402">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-403">MIDI slave</span><span class="sxs-lookup"><span data-stu-id="3de1e-403">slave midi</span></span></td>
<td><span data-ttu-id="3de1e-404">Imposta il sequencer MIDI per l'uso dei dati MIDI in ingresso per l'origine di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-404">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="3de1e-405">Sequencer riconosce i dati di sincronizzazione con il formato MIDI.</span><span class="sxs-lookup"><span data-stu-id="3de1e-405">The sequencer recognizes synchronization data with the MIDI format.</span></span> <span data-ttu-id="3de1e-406">MCISEQ sequencer non supporta questo flag.</span><span class="sxs-lookup"><span data-stu-id="3de1e-406">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-407">slave None</span><span class="sxs-lookup"><span data-stu-id="3de1e-407">slave none</span></span></td>
<td><span data-ttu-id="3de1e-408">Imposta il sequencer MIDI per ignorare la sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="3de1e-408">Sets the MIDI sequencer to ignore synchronization</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-409">SMPTE slave</span><span class="sxs-lookup"><span data-stu-id="3de1e-409">slave smpte</span></span></td>
<td><span data-ttu-id="3de1e-410">Imposta il sequencer MIDI per l'uso dei dati MIDI in ingresso per l'origine di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-410">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="3de1e-411">Sequencer riconosce i dati di sincronizzazione con il formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-411">The sequencer recognizes synchronization data with the SMPTE format.</span></span> <span data-ttu-id="3de1e-412">MCISEQ sequencer non supporta questo flag.</span><span class="sxs-lookup"><span data-stu-id="3de1e-412">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-413">fattore di velocità</span><span class="sxs-lookup"><span data-stu-id="3de1e-413">speed factor</span></span></td>
<td><span data-ttu-id="3de1e-414">Imposta la velocità relativa della riproduzione video e audio dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3de1e-414">Sets the relative speed of video and audio playback from the workspace.</span></span> <span data-ttu-id="3de1e-415">Factor è il rapporto tra la frequenza dei fotogrammi nominale e la frequenza dei fotogrammi desiderata, in cui la frequenza dei fotogrammi nominale viene designata come 1000.</span><span class="sxs-lookup"><span data-stu-id="3de1e-415">Factor is the ratio between the nominal frame rate and the desired frame rate, where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="3de1e-416">Una frequenza di 500 è la velocità della metà normale, 2000 è due volte la velocità normale e così via. Impostando la velocità su zero, il video viene riprodotto il più rapidamente possibile senza eliminare i frame e senza audio.</span><span class="sxs-lookup"><span data-stu-id="3de1e-416">(A rate of 500 is half normal speed, 2000 is twice normal speed, and so on.) Setting the speed to zero plays the video as fast as possible without dropping frames and without audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-417"><em>formato</em> file ancora</span><span class="sxs-lookup"><span data-stu-id="3de1e-417">still file format <em>format</em></span></span></td>
<td><span data-ttu-id="3de1e-418">Specifica il formato di file utilizzato per i comandi di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-418">Specifies the file format used for capture commands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-419">tempo_value tempo</span><span class="sxs-lookup"><span data-stu-id="3de1e-419">tempo tempo_value</span></span></td>
<td><span data-ttu-id="3de1e-420">Imposta il tempo della sequenza in base al formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3de1e-420">Sets the tempo of the sequence according to the current time format.</span></span> <span data-ttu-id="3de1e-421">Per un file basato su PPQN, il tempo_value viene interpretato come un battito al minuto.</span><span class="sxs-lookup"><span data-stu-id="3de1e-421">For a PPQN-based file, the tempo_value is interpreted as beats per minute.</span></span> <span data-ttu-id="3de1e-422">Per un file basato su SMPTE, il tempo_value viene interpretato come frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="3de1e-422">For a SMPTE-based file, the tempo_value is interpreted as frames per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-423">byte formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-423">time format bytes</span></span></td>
<td><span data-ttu-id="3de1e-424">In un formato di file PCM, imposta il formato dell'ora su byte.</span><span class="sxs-lookup"><span data-stu-id="3de1e-424">In a PCM file format, sets the time format to bytes.</span></span> <span data-ttu-id="3de1e-425">Tutte le informazioni sulla posizione vengono specificate come byte dopo questo comando.</span><span class="sxs-lookup"><span data-stu-id="3de1e-425">All position information is specified as bytes following this command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-426">frame formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-426">time format frames</span></span></td>
<td><span data-ttu-id="3de1e-427">Imposta il formato dell'ora su frame.</span><span class="sxs-lookup"><span data-stu-id="3de1e-427">Sets the time format to frames.</span></span> <span data-ttu-id="3de1e-428">Tutti i comandi che usano valori di posizione presuppongono frame.</span><span class="sxs-lookup"><span data-stu-id="3de1e-428">All commands that use position values will assume frames.</span></span> <span data-ttu-id="3de1e-429">Quando il dispositivo viene aperto, i frame sono la modalità predefinita.</span><span class="sxs-lookup"><span data-stu-id="3de1e-429">When the device is opened, frames is the default mode.</span></span> <span data-ttu-id="3de1e-430">Supportato da videodischi con formato CAV.</span><span class="sxs-lookup"><span data-stu-id="3de1e-430">Supported by videodiscs using CAV format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-431">formato ora HMS</span><span class="sxs-lookup"><span data-stu-id="3de1e-431">time format hms</span></span></td>
<td><span data-ttu-id="3de1e-432">Imposta il formato dell'ora su ore, minuti e secondi.</span><span class="sxs-lookup"><span data-stu-id="3de1e-432">Sets the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="3de1e-433">Tutti i comandi che usano i valori di posizione presuppongono la funzione HMS.</span><span class="sxs-lookup"><span data-stu-id="3de1e-433">All commands that use position values will assume HMS.</span></span> <span data-ttu-id="3de1e-434">HMS è il formato predefinito per CLV videodischi.</span><span class="sxs-lookup"><span data-stu-id="3de1e-434">HMS is the default format for CLV videodiscs.</span></span> <span data-ttu-id="3de1e-435">Specificare un valore HMS come HH: mm: SS, dove HH è hours, mm è minutes e SS è seconds.</span><span class="sxs-lookup"><span data-stu-id="3de1e-435">Specify an HMS value as hh:mm:ss, where hh is hours, mm is minutes, and ss is seconds.</span></span> <span data-ttu-id="3de1e-436">È possibile omettere un campo se e tutti i campi seguenti sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="3de1e-436">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="3de1e-437">Ad esempio, 3, 3:0 e 3:0:0 sono tutti modi validi per esprimere 3 ore.</span><span class="sxs-lookup"><span data-stu-id="3de1e-437">For example, 3, 3:0, and 3:0:0 are all valid ways to express 3 hours.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-438">millisecondi formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-438">time format milliseconds</span></span></td>
<td><span data-ttu-id="3de1e-439">Imposta il formato dell'ora su millisecondi.</span><span class="sxs-lookup"><span data-stu-id="3de1e-439">Sets the time format to milliseconds.</span></span> <span data-ttu-id="3de1e-440">Per tutti i comandi che usano valori di posizione si presuppone un millisecondo.</span><span class="sxs-lookup"><span data-stu-id="3de1e-440">All commands that use position values will assume milliseconds.</span></span> <span data-ttu-id="3de1e-441">È possibile abbreviare i millisecondi come &quot; MS &quot; .</span><span class="sxs-lookup"><span data-stu-id="3de1e-441">You can abbreviate milliseconds as &quot;ms&quot;.</span></span> <span data-ttu-id="3de1e-442">Per i dispositivi sequencer, il file di sequenza imposta il formato predefinito su PPQN o SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-442">For sequencer devices, the sequence file sets the default format to PPQN or SMPTE.</span></span> <span data-ttu-id="3de1e-443">I dispositivi overlay video non supportano questo flag.</span><span class="sxs-lookup"><span data-stu-id="3de1e-443">Video-overlay devices do not support this flag.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-444">formato ora MSF</span><span class="sxs-lookup"><span data-stu-id="3de1e-444">time format msf</span></span></td>
<td><span data-ttu-id="3de1e-445">Imposta il formato dell'ora su minuti, secondi e frame.</span><span class="sxs-lookup"><span data-stu-id="3de1e-445">Sets the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="3de1e-446">Per tutti i comandi che usano valori di posizione si presuppone MSF (il formato predefinito per audio CD).</span><span class="sxs-lookup"><span data-stu-id="3de1e-446">All commands that use position values will assume MSF (the default format for CD audio).</span></span> <span data-ttu-id="3de1e-447">Specificare un valore MSF come mm: SS: FF, dove mm è minutes, SS è seconds e FF è frames.</span><span class="sxs-lookup"><span data-stu-id="3de1e-447">Specify an MSF value as mm:ss:ff, where mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="3de1e-448">È possibile omettere un campo se e tutti i campi seguenti sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="3de1e-448">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="3de1e-449">Ad esempio, 3, 3:0 e 3:0:0 sono modi validi per esprimere 3 minuti.</span><span class="sxs-lookup"><span data-stu-id="3de1e-449">For example, 3, 3:0, and 3:0:0 are valid ways to express 3 minutes.</span></span><br/> <span data-ttu-id="3de1e-450">I campi MSF presentano i valori massimi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3de1e-450">The MSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="3de1e-451">Minuti 99</span><span class="sxs-lookup"><span data-stu-id="3de1e-451">Minutes 99</span></span></li>
<li><span data-ttu-id="3de1e-452">Secondi 59</span><span class="sxs-lookup"><span data-stu-id="3de1e-452">Seconds 59</span></span></li>
<li><span data-ttu-id="3de1e-453">Frame 74</span><span class="sxs-lookup"><span data-stu-id="3de1e-453">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-454">esempi di formato time</span><span class="sxs-lookup"><span data-stu-id="3de1e-454">time format samples</span></span></td>
<td><span data-ttu-id="3de1e-455">Imposta il formato dell'ora sugli esempi.</span><span class="sxs-lookup"><span data-stu-id="3de1e-455">Sets the time format to samples.</span></span> <span data-ttu-id="3de1e-456">Tutte le informazioni sulla posizione vengono specificate come campioni che seguono questo comando.</span><span class="sxs-lookup"><span data-stu-id="3de1e-456">All position information is specified as samples following this command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-457">formato ora SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="3de1e-457">time format smpte 24</span></span><br/> <span data-ttu-id="3de1e-458">formato ora SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="3de1e-458">time format smpte 25</span></span><br/> <span data-ttu-id="3de1e-459">formato ora SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="3de1e-459">time format smpte 30</span></span><br/></td>
<td><span data-ttu-id="3de1e-460">Imposta il formato dell'ora su una frequenza dei fotogrammi SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-460">Sets the time format to an SMPTE frame rate.</span></span> <span data-ttu-id="3de1e-461">Per i VCR, imposta il formato dell'ora su HH: mm: SS: FF, dove i valori validi sono compresi tra 00:00:00:00 e 23:59:59: XX, mentre XX è inferiore al numero di fotogrammi al secondo, come specificato dal numero 24, 25 o 30, come specificato nel flag.</span><span class="sxs-lookup"><span data-stu-id="3de1e-461">For VCRs, sets the time format to hh:mm:ss:ff, where the legal values are 00:00:00:00 through 23:59:59:xx, and xx is one less than the frames per second as specified by the number 24, 25, or 30 as specified in the flag.</span></span> <span data-ttu-id="3de1e-462">In input, i due punti (:) sono necessari per separare i componenti.</span><span class="sxs-lookup"><span data-stu-id="3de1e-462">On input, colons (:) are required to separate the components.</span></span> <span data-ttu-id="3de1e-463">Le unità meno significative possono essere omesse se sono 00; 02:00, ad esempio, corrisponde a 02:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="3de1e-463">The least significant units can be omitted if they are 00; for example, 02:00 is the same as 02:00:00:00.</span></span> <span data-ttu-id="3de1e-464">Tutti i comandi che usano valori di posizione presuppongono il formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-464">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="3de1e-465">Il file di sequenza imposta il formato predefinito su PPQN o SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-465">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-466">formato ora SMPTE 30 drop</span><span class="sxs-lookup"><span data-stu-id="3de1e-466">time format smpte 30 drop</span></span></td>
<td><span data-ttu-id="3de1e-467">Imposta il formato dell'ora su SMPTE 30 drop frame rate.</span><span class="sxs-lookup"><span data-stu-id="3de1e-467">Sets the time format to SMPTE 30 drop frame rate.</span></span> <span data-ttu-id="3de1e-468">Per i VCR, uguale a SMPTE 30, con la differenza che alcune posizioni del timecode vengono eliminate dal formato in modo che le posizioni del timecode registrate per ogni fotogramma (alla frequenza dei fotogrammi NTSC di 29,97 fps) corrispondano a tempo reale (a 30 fps).</span><span class="sxs-lookup"><span data-stu-id="3de1e-468">For VCRs, same as SMPTE 30, except that certain timecode positions are dropped from the format to have the recorded timecode positions for each frame (at the NTSC frame rate of 29.97 fps) correspond to real time (at 30 fps).</span></span> <span data-ttu-id="3de1e-469">Le posizioni del timecode eliminate sono le seguenti: due al minuto, per i primi nove di ogni dieci minuti di contenuto registrato.</span><span class="sxs-lookup"><span data-stu-id="3de1e-469">Timecode positions that are dropped are as follows: two every minute, on the minute, for the first nine of every ten minutes of recorded content.</span></span> <span data-ttu-id="3de1e-470">Ad esempio, alle 01:04:59:29, la posizione del timecode successiva sarà 01:05:00:02, non 01:05:00:00.</span><span class="sxs-lookup"><span data-stu-id="3de1e-470">For example, at 01:04:59:29, the next timecode position would be 01:05:00:02, not 01:05:00:00.</span></span> <span data-ttu-id="3de1e-471">Tutti i comandi che usano valori di posizione presuppongono il formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-471">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="3de1e-472">Il file di sequenza imposta il formato predefinito su PPQN o SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3de1e-472">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-473">puntatore al formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-473">time format song pointer</span></span></td>
<td><span data-ttu-id="3de1e-474">Imposta il formato dell'ora su puntatore al brano (sedicesimi).</span><span class="sxs-lookup"><span data-stu-id="3de1e-474">Sets the time format to song pointer (sixteenth notes).</span></span> <span data-ttu-id="3de1e-475">Per tutti i comandi che usano valori di posizione si presuppone che le unità del puntatore del brano.</span><span class="sxs-lookup"><span data-stu-id="3de1e-475">All commands that use position values will assume song pointer units.</span></span> <span data-ttu-id="3de1e-476">Questo flag è valido solo per una sequenza di tipo PPQN di divisione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-476">This flag is valid only for a sequence of division type PPQN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-477">formato ora TMSF</span><span class="sxs-lookup"><span data-stu-id="3de1e-477">time format tmsf</span></span></td>
<td><span data-ttu-id="3de1e-478">Imposta il formato dell'ora su Tracks, minutes, seconds e frames.</span><span class="sxs-lookup"><span data-stu-id="3de1e-478">Sets the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="3de1e-479">Per tutti i comandi che usano valori di posizione si presuppone TMSF.</span><span class="sxs-lookup"><span data-stu-id="3de1e-479">All commands that use position values will assume TMSF.</span></span> <span data-ttu-id="3de1e-480">Specificare un valore TMSF come TT: mm: SS: FF, dove TT è Tracks, mm è minutes, SS is seconds e FF is frames.</span><span class="sxs-lookup"><span data-stu-id="3de1e-480">Specify a TMSF value as tt:mm:ss:ff, where tt is tracks, mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="3de1e-481">È possibile omettere un campo se e tutti i campi seguenti sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="3de1e-481">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="3de1e-482">Ad esempio, 3, 3:0, 3:0:0 e 3:0:0:0 sono tutti modi validi per esprimere Track 3.</span><span class="sxs-lookup"><span data-stu-id="3de1e-482">For example, 3, 3:0, 3:0:0, and 3:0:0:0 are all valid ways to express track 3.</span></span> <br/> <span data-ttu-id="3de1e-483">I campi TMSF hanno i valori massimi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3de1e-483">The TMSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="3de1e-484">Tracce 99</span><span class="sxs-lookup"><span data-stu-id="3de1e-484">Tracks 99</span></span></li>
<li><span data-ttu-id="3de1e-485">Minuti 90</span><span class="sxs-lookup"><span data-stu-id="3de1e-485">Minutes 90</span></span></li>
<li><span data-ttu-id="3de1e-486">Secondi 59</span><span class="sxs-lookup"><span data-stu-id="3de1e-486">Seconds 59</span></span></li>
<li><span data-ttu-id="3de1e-487">Frame 74</span><span class="sxs-lookup"><span data-stu-id="3de1e-487">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-488">traccia formato ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-488">time format track</span></span></td>
<td><span data-ttu-id="3de1e-489">Imposta il formato di posizione su Tracks.</span><span class="sxs-lookup"><span data-stu-id="3de1e-489">Sets the position format to tracks.</span></span> <span data-ttu-id="3de1e-490">Tutti i comandi che usano valori di posizione presuppongono le tracce.</span><span class="sxs-lookup"><span data-stu-id="3de1e-490">All commands that use position values will assume tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-491">contatore modalità ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-491">time mode counter</span></span></td>
<td><span data-ttu-id="3de1e-492">Imposta la modalità position-Information per l'uso dei contatori VCR.</span><span class="sxs-lookup"><span data-stu-id="3de1e-492">Sets the position-information mode to use the VCR counters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-493">rilevamento modalità tempo</span><span class="sxs-lookup"><span data-stu-id="3de1e-493">time mode detect</span></span></td>
<td><span data-ttu-id="3de1e-494">Imposta la modalità informazioni sulla posizione in base al rilevamento delle informazioni sul timecode sul nastro.</span><span class="sxs-lookup"><span data-stu-id="3de1e-494">Sets the position information mode based on detection of timecode information on the tape.</span></span> <span data-ttu-id="3de1e-495">Se vengono rilevate informazioni sul timecode, il tipo di ora è impostato su &quot; timecode &quot; ; in caso contrario, il tipo di ora è impostato su &quot; Counter &quot; .</span><span class="sxs-lookup"><span data-stu-id="3de1e-495">If timecode information is detected, the time type is set to &quot;timecode&quot;; otherwise, the time type is set to &quot;counter&quot;.</span></span> <span data-ttu-id="3de1e-496">&quot;&quot;Il rilevamento è una modalità speciale.</span><span class="sxs-lookup"><span data-stu-id="3de1e-496">&quot;Detect&quot; is a special mode.</span></span> <span data-ttu-id="3de1e-497">Ogni volta che il driver viene aperto, viene inserito un nuovo nastro o &quot; viene eseguito il comando della modalità ora &quot; , il driver controlla la modalità ora corrente disponibile sul nastro e imposta il &quot; tipo di ora sul &quot; &quot; timecode &quot; o sul &quot; contatore &quot; .</span><span class="sxs-lookup"><span data-stu-id="3de1e-497">Whenever the driver is opened, a new tape is inserted, or the &quot;time mode&quot; command is issued, the driver checks the current time mode available on the tape and sets &quot;time type&quot; to either &quot;timecode&quot; or &quot;counter&quot;.</span></span> <span data-ttu-id="3de1e-498">Una volta &quot; &quot; impostato il tipo time, il driver non lo modifica fino a quando non si verifica una delle condizioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="3de1e-498">Once &quot;time type&quot; is set, the driver doesn't change it until one of the above conditions occurs again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-499">timecode modalità ora</span><span class="sxs-lookup"><span data-stu-id="3de1e-499">time mode timecode</span></span></td>
<td><span data-ttu-id="3de1e-500">Imposta la modalità informazioni sulla posizione per utilizzare le &quot; &quot; informazioni sul timecode sul nastro.</span><span class="sxs-lookup"><span data-stu-id="3de1e-500">Sets the position information mode to use &quot;timecode&quot; information on the tape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-501">rilevamento e</span><span class="sxs-lookup"><span data-stu-id="3de1e-501">tracking plus</span></span> <br/> <span data-ttu-id="3de1e-502">meno rilevamento</span><span class="sxs-lookup"><span data-stu-id="3de1e-502">tracking minus</span></span> <br/> <span data-ttu-id="3de1e-503">rilevamento reimpostazione</span><span class="sxs-lookup"><span data-stu-id="3de1e-503">tracking reset</span></span> <br/></td>
<td><span data-ttu-id="3de1e-504">Regola la velocità del trasporto di nastri in incrementi.</span><span class="sxs-lookup"><span data-stu-id="3de1e-504">Adjusts the speed of the videotape transport in fine increments.</span></span> <span data-ttu-id="3de1e-505">Usare i &quot; &quot; flag di rilevamento quando si ottiene un'immagine rumorosa da un videoregistratore.</span><span class="sxs-lookup"><span data-stu-id="3de1e-505">Use the &quot;tracking&quot; flags when a noisy picture is obtained from a VCR.</span></span> <span data-ttu-id="3de1e-506">&quot;Il rilevamento e &quot; la velocità di trasporto aumentano.</span><span class="sxs-lookup"><span data-stu-id="3de1e-506">&quot;Tracking plus&quot; increases the transport speed.</span></span> <span data-ttu-id="3de1e-507">&quot;Il rilevamento meno &quot; diminuisce la velocità del trasporto.</span><span class="sxs-lookup"><span data-stu-id="3de1e-507">&quot;Tracking minus&quot; decreases the transport speed.</span></span> <span data-ttu-id="3de1e-508">&quot;La reimpostazione &quot; del rilevamento restituisce zero per la regolazione del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="3de1e-508">&quot;Tracking reset&quot; returns the tracking adjustment to zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3de1e-509">video disattivato</span><span class="sxs-lookup"><span data-stu-id="3de1e-509">video off</span></span></td>
<td><span data-ttu-id="3de1e-510">Disabilita l'output del video.</span><span class="sxs-lookup"><span data-stu-id="3de1e-510">Disables video output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3de1e-511">video su</span><span class="sxs-lookup"><span data-stu-id="3de1e-511">video on</span></span></td>
<td><span data-ttu-id="3de1e-512">Abilita l'output del video.</span><span class="sxs-lookup"><span data-stu-id="3de1e-512">Enables video output.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="3de1e-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3de1e-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3de1e-514">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="3de1e-514">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="3de1e-515">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="3de1e-515">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="3de1e-516">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3de1e-516">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de1e-517">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3de1e-517">Return Value</span></span>

<span data-ttu-id="3de1e-518">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="3de1e-518">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de1e-519">Commenti</span><span class="sxs-lookup"><span data-stu-id="3de1e-519">Remarks</span></span>

<span data-ttu-id="3de1e-520">Quando viene creato il file in cui archiviare i dati, vengono definite diverse proprietà dei dati audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="3de1e-520">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="3de1e-521">Queste proprietà descrivono la struttura dei dati all'interno del file e non possono essere modificate una volta avviata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="3de1e-521">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="3de1e-522">L'elenco seguente identifica queste proprietà:</span><span class="sxs-lookup"><span data-stu-id="3de1e-522">The following list identifies these properties:</span></span>

-   <span data-ttu-id="3de1e-523">allineamento</span><span class="sxs-lookup"><span data-stu-id="3de1e-523">alignment</span></span>
-   <span data-ttu-id="3de1e-524">BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="3de1e-524">bitspersample</span></span>
-   <span data-ttu-id="3de1e-525">bytespersec</span><span class="sxs-lookup"><span data-stu-id="3de1e-525">bytespersec</span></span>
-   <span data-ttu-id="3de1e-526">channels</span><span class="sxs-lookup"><span data-stu-id="3de1e-526">channels</span></span>
-   <span data-ttu-id="3de1e-527">Tag di formato</span><span class="sxs-lookup"><span data-stu-id="3de1e-527">format tag</span></span>
-   <span data-ttu-id="3de1e-528">samplespersec</span><span class="sxs-lookup"><span data-stu-id="3de1e-528">samplespersec</span></span>

## <a name="examples"></a><span data-ttu-id="3de1e-529">Esempio</span><span class="sxs-lookup"><span data-stu-id="3de1e-529">Examples</span></span>

<span data-ttu-id="3de1e-530">Il seguente comando imposta il formato dell'ora su millisecondi e imposta il formato dell'audio della forma d'onda su 8 bit, mono, 11 kHz.</span><span class="sxs-lookup"><span data-stu-id="3de1e-530">The following command sets the time format to milliseconds and sets the waveform-audio format to 8 bit, mono, 11 kHz.</span></span>

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a><span data-ttu-id="3de1e-531">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3de1e-531">Requirements</span></span>



| <span data-ttu-id="3de1e-532">Requisito</span><span class="sxs-lookup"><span data-stu-id="3de1e-532">Requirement</span></span> | <span data-ttu-id="3de1e-533">Valore</span><span class="sxs-lookup"><span data-stu-id="3de1e-533">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3de1e-534">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3de1e-534">Minimum supported client</span></span><br/> | <span data-ttu-id="3de1e-535">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3de1e-535">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3de1e-536">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3de1e-536">Minimum supported server</span></span><br/> | <span data-ttu-id="3de1e-537">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3de1e-537">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3de1e-538">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3de1e-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de1e-539">MCI</span><span class="sxs-lookup"><span data-stu-id="3de1e-539">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3de1e-540">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="3de1e-540">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="3de1e-541">catturare</span><span class="sxs-lookup"><span data-stu-id="3de1e-541">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="3de1e-542">pause</span><span class="sxs-lookup"><span data-stu-id="3de1e-542">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="3de1e-543">salvataggio</span><span class="sxs-lookup"><span data-stu-id="3de1e-543">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="3de1e-544">stop</span><span class="sxs-lookup"><span data-stu-id="3de1e-544">stop</span></span>](stop.md)
</dt> </dl>

 

