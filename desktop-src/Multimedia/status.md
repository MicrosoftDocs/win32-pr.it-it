---
title: comando status
description: Il comando di stato richiede informazioni sullo stato da un dispositivo. Tutti i dispositivi riconoscono questo comando.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- comando di stato Windows Multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "106320054"
---
# <a name="status-command"></a><span data-ttu-id="01b08-105">comando status</span><span class="sxs-lookup"><span data-stu-id="01b08-105">status command</span></span>

> [!NOTE]
> <span data-ttu-id="01b08-106">Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.</span><span class="sxs-lookup"><span data-stu-id="01b08-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="01b08-107">All'interno di questo documento sono presenti riferimenti alla parola "slave".</span><span class="sxs-lookup"><span data-stu-id="01b08-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="01b08-108">La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.</span><span class="sxs-lookup"><span data-stu-id="01b08-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="01b08-109">Questo testo viene usato in quanto è attualmente il testo usato nei comandi.</span><span class="sxs-lookup"><span data-stu-id="01b08-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="01b08-110">Per coerenza, questo documento contiene questa parola.</span><span class="sxs-lookup"><span data-stu-id="01b08-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="01b08-111">Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo da essere in allineamento.</span><span class="sxs-lookup"><span data-stu-id="01b08-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="01b08-112">Il comando di stato richiede informazioni sullo stato da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01b08-112">The status command requests status information from a device.</span></span> <span data-ttu-id="01b08-113">Tutti i dispositivi riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="01b08-113">All devices recognize this command.</span></span>

<span data-ttu-id="01b08-114">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="01b08-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="01b08-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="01b08-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b08-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="01b08-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="01b08-117">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="01b08-117">Identifier of an MCI device.</span></span> <span data-ttu-id="01b08-118">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="01b08-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="01b08-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="01b08-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="01b08-120">Flag per la richiesta delle informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="01b08-120">Flag for requesting status information.</span></span> <span data-ttu-id="01b08-121">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando di **stato** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="01b08-121">The following table lists device types that recognize the **status** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01b08-122">Tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="01b08-122">Device Type</span></span></th>
<th><span data-ttu-id="01b08-123">Flag di richiesta</span><span class="sxs-lookup"><span data-stu-id="01b08-123">Request Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01b08-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="01b08-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="01b08-125"><em>numero</em> di traccia del tipo CDAudio</span><span class="sxs-lookup"><span data-stu-id="01b08-125">cdaudio type track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-126">traccia corrente</span><span class="sxs-lookup"><span data-stu-id="01b08-126">current track</span></span></li>
<li><span data-ttu-id="01b08-127">length</span><span class="sxs-lookup"><span data-stu-id="01b08-127">length</span></span></li>
<li><span data-ttu-id="01b08-128"><em>numero</em> traccia lunghezza</span><span class="sxs-lookup"><span data-stu-id="01b08-128">length track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-129">supporti presenti</span><span class="sxs-lookup"><span data-stu-id="01b08-129">media present</span></span></li>
<li><span data-ttu-id="01b08-130">mode</span><span class="sxs-lookup"><span data-stu-id="01b08-130">mode</span></span></li>
<li><span data-ttu-id="01b08-131">numero di tracce</span><span class="sxs-lookup"><span data-stu-id="01b08-131">number of tracks</span></span></li>
<li><span data-ttu-id="01b08-132">position</span><span class="sxs-lookup"><span data-stu-id="01b08-132">position</span></span></li>
<li><span data-ttu-id="01b08-133"><em>numero</em> di traccia posizione</span><span class="sxs-lookup"><span data-stu-id="01b08-133">position track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-134">pronto</span><span class="sxs-lookup"><span data-stu-id="01b08-134">ready</span></span></li>
<li><span data-ttu-id="01b08-135">posizione iniziale</span><span class="sxs-lookup"><span data-stu-id="01b08-135">start position</span></span></li>
<li><span data-ttu-id="01b08-136">formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="01b08-136">time format</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-137">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="01b08-137">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="01b08-138">Audio</span><span class="sxs-lookup"><span data-stu-id="01b08-138">audio</span></span></li>
<li><span data-ttu-id="01b08-139">allineamento audio</span><span class="sxs-lookup"><span data-stu-id="01b08-139">audio alignment</span></span></li>
<li><span data-ttu-id="01b08-140">BitsPerSample audio</span><span class="sxs-lookup"><span data-stu-id="01b08-140">audio bitspersample</span></span></li>
<li><span data-ttu-id="01b08-141">interruzioni audio</span><span class="sxs-lookup"><span data-stu-id="01b08-141">audio breaks</span></span></li>
<li><span data-ttu-id="01b08-142">bytespersec audio</span><span class="sxs-lookup"><span data-stu-id="01b08-142">audio bytespersec</span></span></li>
<li><span data-ttu-id="01b08-143">input audio</span><span class="sxs-lookup"><span data-stu-id="01b08-143">audio input</span></span></li>
<li><span data-ttu-id="01b08-144">record audio</span><span class="sxs-lookup"><span data-stu-id="01b08-144">audio record</span></span></li>
<li><span data-ttu-id="01b08-145">origine audio</span><span class="sxs-lookup"><span data-stu-id="01b08-145">audio source</span></span></li>
<li><span data-ttu-id="01b08-146">samplespersec audio</span><span class="sxs-lookup"><span data-stu-id="01b08-146">audio samplespersec</span></span></li>
<li><span data-ttu-id="01b08-147">flusso audio</span><span class="sxs-lookup"><span data-stu-id="01b08-147">audio stream</span></span></li>
<li><span data-ttu-id="01b08-148">basso</span><span class="sxs-lookup"><span data-stu-id="01b08-148">bass</span></span></li>
<li><span data-ttu-id="01b08-149">BitsPerPel</span><span class="sxs-lookup"><span data-stu-id="01b08-149">bitsperpel</span></span></li>
<li><span data-ttu-id="01b08-150">luminosità</span><span class="sxs-lookup"><span data-stu-id="01b08-150">brightness</span></span></li>
<li><span data-ttu-id="01b08-151">color</span><span class="sxs-lookup"><span data-stu-id="01b08-151">color</span></span></li>
<li><span data-ttu-id="01b08-152">elevato</span><span class="sxs-lookup"><span data-stu-id="01b08-152">contrast</span></span></li>
<li><span data-ttu-id="01b08-153">traccia corrente</span><span class="sxs-lookup"><span data-stu-id="01b08-153">current track</span></span></li>
<li><span data-ttu-id="01b08-154"><em>unità</em> spazio su disco</span><span class="sxs-lookup"><span data-stu-id="01b08-154">disk space <em>drive</em></span></span></li>
<li><span data-ttu-id="01b08-155">completamento file</span><span class="sxs-lookup"><span data-stu-id="01b08-155">file completion</span></span></li>
<li><span data-ttu-id="01b08-156">formato file</span><span class="sxs-lookup"><span data-stu-id="01b08-156">file format</span></span></li>
<li><span data-ttu-id="01b08-157">modalità file</span><span class="sxs-lookup"><span data-stu-id="01b08-157">file mode</span></span></li>
<li><span data-ttu-id="01b08-158">forward</span><span class="sxs-lookup"><span data-stu-id="01b08-158">forward</span></span></li>
<li><span data-ttu-id="01b08-159">frame ignorati</span><span class="sxs-lookup"><span data-stu-id="01b08-159">frames skipped</span></span></li>
<li><span data-ttu-id="01b08-160">gamma</span><span class="sxs-lookup"><span data-stu-id="01b08-160">gamma</span></span></li>
<li><span data-ttu-id="01b08-161">input</span><span class="sxs-lookup"><span data-stu-id="01b08-161">input</span></span></li>
<li><span data-ttu-id="01b08-162">volume sinistro</span><span class="sxs-lookup"><span data-stu-id="01b08-162">left volume</span></span></li>
<li><span data-ttu-id="01b08-163">length</span><span class="sxs-lookup"><span data-stu-id="01b08-163">length</span></span></li>
<li><span data-ttu-id="01b08-164"><em>numero</em> traccia lunghezza</span><span class="sxs-lookup"><span data-stu-id="01b08-164">length track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-165">supporti presenti</span><span class="sxs-lookup"><span data-stu-id="01b08-165">media present</span></span></li>
<li><span data-ttu-id="01b08-166">mode</span><span class="sxs-lookup"><span data-stu-id="01b08-166">mode</span></span></li>
<li><span data-ttu-id="01b08-167">monitoraggio</span><span class="sxs-lookup"><span data-stu-id="01b08-167">monitor</span></span></li>
<li><span data-ttu-id="01b08-168">Metodo Monitor</span><span class="sxs-lookup"><span data-stu-id="01b08-168">monitor method</span></span></li>
<li><span data-ttu-id="01b08-169">nominale</span><span class="sxs-lookup"><span data-stu-id="01b08-169">nominal</span></span></li>
<li><span data-ttu-id="01b08-170">frequenza fotogrammi nominale</span><span class="sxs-lookup"><span data-stu-id="01b08-170">nominal frame rate</span></span></li>
<li><span data-ttu-id="01b08-171">frequenza fotogrammi record nominale</span><span class="sxs-lookup"><span data-stu-id="01b08-171">nominal record frame rate</span></span></li>
<li><span data-ttu-id="01b08-172">numero di tracce</span><span class="sxs-lookup"><span data-stu-id="01b08-172">number of tracks</span></span></li>
<li><span data-ttu-id="01b08-173">output</span><span class="sxs-lookup"><span data-stu-id="01b08-173">output</span></span></li>
<li><span data-ttu-id="01b08-174">handle tavolozza</span><span class="sxs-lookup"><span data-stu-id="01b08-174">palette handle</span></span></li>
<li><span data-ttu-id="01b08-175">modalità di sospensione</span><span class="sxs-lookup"><span data-stu-id="01b08-175">pause mode</span></span></li>
<li><span data-ttu-id="01b08-176">velocità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="01b08-176">play speed</span></span></li>
<li><span data-ttu-id="01b08-177">position</span><span class="sxs-lookup"><span data-stu-id="01b08-177">position</span></span></li>
<li><span data-ttu-id="01b08-178"><em>numero</em> di traccia posizione</span><span class="sxs-lookup"><span data-stu-id="01b08-178">position track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-179">pronto</span><span class="sxs-lookup"><span data-stu-id="01b08-179">ready</span></span></li>
<li><span data-ttu-id="01b08-180">frequenza fotogrammi record</span><span class="sxs-lookup"><span data-stu-id="01b08-180">record frame rate</span></span></li>
<li><span data-ttu-id="01b08-181"><em>frame</em> di riferimento</span><span class="sxs-lookup"><span data-stu-id="01b08-181">reference <em>frame</em></span></span></li>
<li><span data-ttu-id="01b08-182">dimensioni riservate</span><span class="sxs-lookup"><span data-stu-id="01b08-182">reserved size</span></span></li>
<li><span data-ttu-id="01b08-183">volume giusto</span><span class="sxs-lookup"><span data-stu-id="01b08-183">right volume</span></span></li>
<li><span data-ttu-id="01b08-184">ricerca esatta</span><span class="sxs-lookup"><span data-stu-id="01b08-184">seek exactly</span></span></li>
<li><span data-ttu-id="01b08-185">nitidezza</span><span class="sxs-lookup"><span data-stu-id="01b08-185">sharpness</span></span></li>
<li><span data-ttu-id="01b08-186">SMPTE</span><span class="sxs-lookup"><span data-stu-id="01b08-186">smpte</span></span></li>
<li><span data-ttu-id="01b08-187">velocità</span><span class="sxs-lookup"><span data-stu-id="01b08-187">speed</span></span></li>
<li><span data-ttu-id="01b08-188">posizione iniziale</span><span class="sxs-lookup"><span data-stu-id="01b08-188">start position</span></span></li>
<li><span data-ttu-id="01b08-189">formato file ancora</span><span class="sxs-lookup"><span data-stu-id="01b08-189">still file format</span></span></li>
<li><span data-ttu-id="01b08-190">formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="01b08-190">time format</span></span></li>
<li><span data-ttu-id="01b08-191">tinta</span><span class="sxs-lookup"><span data-stu-id="01b08-191">tint</span></span></li>
<li><span data-ttu-id="01b08-192">acuti</span><span class="sxs-lookup"><span data-stu-id="01b08-192">treble</span></span></li>
<li><span data-ttu-id="01b08-193">unsaved</span><span class="sxs-lookup"><span data-stu-id="01b08-193">unsaved</span></span></li>
<li><span data-ttu-id="01b08-194">Video</span><span class="sxs-lookup"><span data-stu-id="01b08-194">video</span></span></li>
<li><span data-ttu-id="01b08-195">indice chiave video</span><span class="sxs-lookup"><span data-stu-id="01b08-195">video key index</span></span></li>
<li><span data-ttu-id="01b08-196">colore della chiave video</span><span class="sxs-lookup"><span data-stu-id="01b08-196">video key color</span></span></li>
<li><span data-ttu-id="01b08-197">record video</span><span class="sxs-lookup"><span data-stu-id="01b08-197">video record</span></span></li>
<li><span data-ttu-id="01b08-198">origine video</span><span class="sxs-lookup"><span data-stu-id="01b08-198">video source</span></span></li>
<li><span data-ttu-id="01b08-199">numero di origine video</span><span class="sxs-lookup"><span data-stu-id="01b08-199">video source number</span></span></li>
<li><span data-ttu-id="01b08-200">flusso video</span><span class="sxs-lookup"><span data-stu-id="01b08-200">video stream</span></span></li>
<li><span data-ttu-id="01b08-201">volume</span><span class="sxs-lookup"><span data-stu-id="01b08-201">volume</span></span></li>
<li><span data-ttu-id="01b08-202">handle finestra</span><span class="sxs-lookup"><span data-stu-id="01b08-202">window handle</span></span></li>
<li><span data-ttu-id="01b08-203">finestra visibile</span><span class="sxs-lookup"><span data-stu-id="01b08-203">window visible</span></span></li>
<li><span data-ttu-id="01b08-204">finestra ridotta a icona</span><span class="sxs-lookup"><span data-stu-id="01b08-204">window minimized</span></span></li>
<li><span data-ttu-id="01b08-205">finestra ingrandita</span><span class="sxs-lookup"><span data-stu-id="01b08-205">window maximized</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-206">overlay</span><span class="sxs-lookup"><span data-stu-id="01b08-206">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="01b08-207">supporti presenti</span><span class="sxs-lookup"><span data-stu-id="01b08-207">media present</span></span></li>
<li><span data-ttu-id="01b08-208">mode</span><span class="sxs-lookup"><span data-stu-id="01b08-208">mode</span></span></li>
<li><span data-ttu-id="01b08-209">numero di tracce</span><span class="sxs-lookup"><span data-stu-id="01b08-209">number of tracks</span></span></li>
<li><span data-ttu-id="01b08-210">pronto</span><span class="sxs-lookup"><span data-stu-id="01b08-210">ready</span></span></li>
<li><span data-ttu-id="01b08-211">adattamento</span><span class="sxs-lookup"><span data-stu-id="01b08-211">stretch</span></span></li>
<li><span data-ttu-id="01b08-212">handle finestra</span><span class="sxs-lookup"><span data-stu-id="01b08-212">window handle</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-213">sequencer</span><span class="sxs-lookup"><span data-stu-id="01b08-213">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="01b08-214">traccia corrente</span><span class="sxs-lookup"><span data-stu-id="01b08-214">current track</span></span></li>
<li><span data-ttu-id="01b08-215">tipo divisione</span><span class="sxs-lookup"><span data-stu-id="01b08-215">division type</span></span></li>
<li><span data-ttu-id="01b08-216">length</span><span class="sxs-lookup"><span data-stu-id="01b08-216">length</span></span></li>
<li><span data-ttu-id="01b08-217">Master <em>numero</em> traccia lunghezza</span><span class="sxs-lookup"><span data-stu-id="01b08-217">length track <em>number</em> master</span></span></li>
<li><span data-ttu-id="01b08-218">supporti presenti</span><span class="sxs-lookup"><span data-stu-id="01b08-218">media present</span></span></li>
<li><span data-ttu-id="01b08-219">mode</span><span class="sxs-lookup"><span data-stu-id="01b08-219">mode</span></span></li>
<li><span data-ttu-id="01b08-220">numero di tracce</span><span class="sxs-lookup"><span data-stu-id="01b08-220">number of tracks</span></span></li>
<li><span data-ttu-id="01b08-221">offset</span><span class="sxs-lookup"><span data-stu-id="01b08-221">offset</span></span></li>
<li><span data-ttu-id="01b08-222">port</span><span class="sxs-lookup"><span data-stu-id="01b08-222">port</span></span></li>
<li><span data-ttu-id="01b08-223">position</span><span class="sxs-lookup"><span data-stu-id="01b08-223">position</span></span></li>
<li><span data-ttu-id="01b08-224"><em>numero</em> di traccia posizione</span><span class="sxs-lookup"><span data-stu-id="01b08-224">position track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-225">pronto</span><span class="sxs-lookup"><span data-stu-id="01b08-225">ready</span></span></li>
<li><span data-ttu-id="01b08-226">schiavo</span><span class="sxs-lookup"><span data-stu-id="01b08-226">slave</span></span></li>
<li><span data-ttu-id="01b08-227">posizione iniziale</span><span class="sxs-lookup"><span data-stu-id="01b08-227">start position</span></span></li>
<li><span data-ttu-id="01b08-228">tempo</span><span class="sxs-lookup"><span data-stu-id="01b08-228">tempo</span></span></li>
<li><span data-ttu-id="01b08-229">formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="01b08-229">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-230">VCR</span><span class="sxs-lookup"><span data-stu-id="01b08-230">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="01b08-231">assembla record</span><span class="sxs-lookup"><span data-stu-id="01b08-231">assemble record</span></span></li>
<li><span data-ttu-id="01b08-232">monitoraggio audio</span><span class="sxs-lookup"><span data-stu-id="01b08-232">audio monitor</span></span></li>
<li><span data-ttu-id="01b08-233">numero di monitor audio</span><span class="sxs-lookup"><span data-stu-id="01b08-233">audio monitor number</span></span></li>
<li><span data-ttu-id="01b08-234">record audio</span><span class="sxs-lookup"><span data-stu-id="01b08-234">audio record</span></span></li>
<li><span data-ttu-id="01b08-235"><em>numero</em> di traccia del record audio</span><span class="sxs-lookup"><span data-stu-id="01b08-235">audio record track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-236">origine audio</span><span class="sxs-lookup"><span data-stu-id="01b08-236">audio source</span></span></li>
<li><span data-ttu-id="01b08-237">numero di origine audio</span><span class="sxs-lookup"><span data-stu-id="01b08-237">audio source number</span></span></li>
<li><span data-ttu-id="01b08-238">channel</span><span class="sxs-lookup"><span data-stu-id="01b08-238">channel</span></span></li>
<li><span data-ttu-id="01b08-239"><em>numero</em> Tuner del canale</span><span class="sxs-lookup"><span data-stu-id="01b08-239">channel tuner <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-240">clock</span><span class="sxs-lookup"><span data-stu-id="01b08-240">clock</span></span></li>
<li><span data-ttu-id="01b08-241">ID Clock</span><span class="sxs-lookup"><span data-stu-id="01b08-241">clock id</span></span></li>
<li><span data-ttu-id="01b08-242">counter</span><span class="sxs-lookup"><span data-stu-id="01b08-242">counter</span></span></li>
<li><span data-ttu-id="01b08-243">formato contatore</span><span class="sxs-lookup"><span data-stu-id="01b08-243">counter format</span></span></li>
<li><span data-ttu-id="01b08-244">risoluzione del contatore</span><span class="sxs-lookup"><span data-stu-id="01b08-244">counter resolution</span></span></li>
<li><span data-ttu-id="01b08-245">traccia corrente</span><span class="sxs-lookup"><span data-stu-id="01b08-245">current track</span></span></li>
<li><span data-ttu-id="01b08-246">frequenza fotogrammi</span><span class="sxs-lookup"><span data-stu-id="01b08-246">frame rate</span></span></li>
<li><span data-ttu-id="01b08-247">indice</span><span class="sxs-lookup"><span data-stu-id="01b08-247">index</span></span></li>
<li><span data-ttu-id="01b08-248">Indice in</span><span class="sxs-lookup"><span data-stu-id="01b08-248">index on</span></span></li>
<li><span data-ttu-id="01b08-249">length</span><span class="sxs-lookup"><span data-stu-id="01b08-249">length</span></span></li>
<li><span data-ttu-id="01b08-250"><em>numero</em> traccia lunghezza</span><span class="sxs-lookup"><span data-stu-id="01b08-250">length track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-251">supporti presenti</span><span class="sxs-lookup"><span data-stu-id="01b08-251">media present</span></span></li>
<li><span data-ttu-id="01b08-252">tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="01b08-252">media type</span></span></li>
<li><span data-ttu-id="01b08-253">mode</span><span class="sxs-lookup"><span data-stu-id="01b08-253">mode</span></span></li>
<li><span data-ttu-id="01b08-254">numero di tracce audio</span><span class="sxs-lookup"><span data-stu-id="01b08-254">number of audio tracks</span></span></li>
<li><span data-ttu-id="01b08-255">numero di tracce</span><span class="sxs-lookup"><span data-stu-id="01b08-255">number of tracks</span></span></li>
<li><span data-ttu-id="01b08-256">numero di tracce video</span><span class="sxs-lookup"><span data-stu-id="01b08-256">number of video tracks</span></span></li>
<li><span data-ttu-id="01b08-257"><em>timeout</em> pausa</span><span class="sxs-lookup"><span data-stu-id="01b08-257">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="01b08-258">formato di riproduzione</span><span class="sxs-lookup"><span data-stu-id="01b08-258">play format</span></span></li>
<li><span data-ttu-id="01b08-259">position</span><span class="sxs-lookup"><span data-stu-id="01b08-259">position</span></span></li>
<li><span data-ttu-id="01b08-260">inizio posizione</span><span class="sxs-lookup"><span data-stu-id="01b08-260">position start</span></span></li>
<li><span data-ttu-id="01b08-261"><em>numero</em> di traccia posizione</span><span class="sxs-lookup"><span data-stu-id="01b08-261">position track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-262"><em>durata</em> postroll</span><span class="sxs-lookup"><span data-stu-id="01b08-262">postroll <em>duration</em></span></span></li>
<li><span data-ttu-id="01b08-263">accensione</span><span class="sxs-lookup"><span data-stu-id="01b08-263">power on</span></span></li>
<li><span data-ttu-id="01b08-264"><em>durata</em> preroll</span><span class="sxs-lookup"><span data-stu-id="01b08-264">preroll <em>duration</em></span></span></li>
<li><span data-ttu-id="01b08-265">pronto</span><span class="sxs-lookup"><span data-stu-id="01b08-265">ready</span></span></li>
<li><span data-ttu-id="01b08-266">formato record</span><span class="sxs-lookup"><span data-stu-id="01b08-266">record format</span></span></li>
<li><span data-ttu-id="01b08-267">velocità</span><span class="sxs-lookup"><span data-stu-id="01b08-267">speed</span></span></li>
<li><span data-ttu-id="01b08-268">formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="01b08-268">time format</span></span></li>
<li><span data-ttu-id="01b08-269">modalità ora</span><span class="sxs-lookup"><span data-stu-id="01b08-269">time mode</span></span></li>
<li><span data-ttu-id="01b08-270">tipo Time</span><span class="sxs-lookup"><span data-stu-id="01b08-270">time type</span></span></li>
<li><span data-ttu-id="01b08-271">codice temporale presente</span><span class="sxs-lookup"><span data-stu-id="01b08-271">timecode present</span></span></li>
<li><span data-ttu-id="01b08-272">record timecode</span><span class="sxs-lookup"><span data-stu-id="01b08-272">timecode record</span></span></li>
<li><span data-ttu-id="01b08-273">tipo di timecode</span><span class="sxs-lookup"><span data-stu-id="01b08-273">timecode type</span></span></li>
<li><span data-ttu-id="01b08-274">numero Tuner</span><span class="sxs-lookup"><span data-stu-id="01b08-274">tuner number</span></span></li>
<li><span data-ttu-id="01b08-275">monitoraggio video</span><span class="sxs-lookup"><span data-stu-id="01b08-275">video monitor</span></span></li>
<li><span data-ttu-id="01b08-276">numero di monitor video</span><span class="sxs-lookup"><span data-stu-id="01b08-276">video monitor number</span></span></li>
<li><span data-ttu-id="01b08-277">record video</span><span class="sxs-lookup"><span data-stu-id="01b08-277">video record</span></span></li>
<li><span data-ttu-id="01b08-278"><em>numero</em> di traccia del record video</span><span class="sxs-lookup"><span data-stu-id="01b08-278">video record track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-279">origine video</span><span class="sxs-lookup"><span data-stu-id="01b08-279">video source</span></span></li>
<li><span data-ttu-id="01b08-280">numero di origine video</span><span class="sxs-lookup"><span data-stu-id="01b08-280">video source number</span></span></li>
<li><span data-ttu-id="01b08-281">scrittura protetta</span><span class="sxs-lookup"><span data-stu-id="01b08-281">write protected</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-282">videodisco</span><span class="sxs-lookup"><span data-stu-id="01b08-282">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="01b08-283">traccia corrente</span><span class="sxs-lookup"><span data-stu-id="01b08-283">current track</span></span></li>
<li><span data-ttu-id="01b08-284">dimensioni del disco</span><span class="sxs-lookup"><span data-stu-id="01b08-284">disc size</span></span></li>
<li><span data-ttu-id="01b08-285">forward</span><span class="sxs-lookup"><span data-stu-id="01b08-285">forward</span></span></li>
<li><span data-ttu-id="01b08-286">length</span><span class="sxs-lookup"><span data-stu-id="01b08-286">length</span></span></li>
<li><span data-ttu-id="01b08-287"><em>numero</em> traccia lunghezza</span><span class="sxs-lookup"><span data-stu-id="01b08-287">length track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-288">supporti presenti</span><span class="sxs-lookup"><span data-stu-id="01b08-288">media present</span></span></li>
<li><span data-ttu-id="01b08-289">tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="01b08-289">media type</span></span></li>
<li><span data-ttu-id="01b08-290">mode</span><span class="sxs-lookup"><span data-stu-id="01b08-290">mode</span></span></li>
<li><span data-ttu-id="01b08-291">numero di tracce</span><span class="sxs-lookup"><span data-stu-id="01b08-291">number of tracks</span></span></li>
<li><span data-ttu-id="01b08-292">position</span><span class="sxs-lookup"><span data-stu-id="01b08-292">position</span></span></li>
<li><span data-ttu-id="01b08-293"><em>numero</em> di traccia posizione</span><span class="sxs-lookup"><span data-stu-id="01b08-293">position track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-294">pronto</span><span class="sxs-lookup"><span data-stu-id="01b08-294">ready</span></span></li>
<li><span data-ttu-id="01b08-295">lato</span><span class="sxs-lookup"><span data-stu-id="01b08-295">side</span></span></li>
<li><span data-ttu-id="01b08-296">velocità</span><span class="sxs-lookup"><span data-stu-id="01b08-296">speed</span></span></li>
<li><span data-ttu-id="01b08-297">posizione iniziale</span><span class="sxs-lookup"><span data-stu-id="01b08-297">start position</span></span></li>
<li><span data-ttu-id="01b08-298">formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="01b08-298">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-299">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="01b08-299">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="01b08-300">allineamento</span><span class="sxs-lookup"><span data-stu-id="01b08-300">alignment</span></span></li>
<li><span data-ttu-id="01b08-301">BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="01b08-301">bitspersample</span></span></li>
<li><span data-ttu-id="01b08-302">bytespersec</span><span class="sxs-lookup"><span data-stu-id="01b08-302">bytespersec</span></span></li>
<li><span data-ttu-id="01b08-303">channels</span><span class="sxs-lookup"><span data-stu-id="01b08-303">channels</span></span></li>
<li><span data-ttu-id="01b08-304">traccia corrente</span><span class="sxs-lookup"><span data-stu-id="01b08-304">current track</span></span></li>
<li><span data-ttu-id="01b08-305">Tag di formato</span><span class="sxs-lookup"><span data-stu-id="01b08-305">format tag</span></span></li>
<li><span data-ttu-id="01b08-306">input</span><span class="sxs-lookup"><span data-stu-id="01b08-306">input</span></span></li>
<li><span data-ttu-id="01b08-307">length</span><span class="sxs-lookup"><span data-stu-id="01b08-307">length</span></span></li>
<li><span data-ttu-id="01b08-308"><em>numero</em> traccia lunghezza</span><span class="sxs-lookup"><span data-stu-id="01b08-308">length track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-309">livello</span><span class="sxs-lookup"><span data-stu-id="01b08-309">level</span></span></li>
<li><span data-ttu-id="01b08-310">supporti presenti</span><span class="sxs-lookup"><span data-stu-id="01b08-310">media present</span></span></li>
<li><span data-ttu-id="01b08-311">mode</span><span class="sxs-lookup"><span data-stu-id="01b08-311">mode</span></span></li>
<li><span data-ttu-id="01b08-312">numero di tracce</span><span class="sxs-lookup"><span data-stu-id="01b08-312">number of tracks</span></span></li>
<li><span data-ttu-id="01b08-313">output</span><span class="sxs-lookup"><span data-stu-id="01b08-313">output</span></span></li>
<li><span data-ttu-id="01b08-314">position</span><span class="sxs-lookup"><span data-stu-id="01b08-314">position</span></span></li>
<li><span data-ttu-id="01b08-315"><em>numero</em> di traccia posizione</span><span class="sxs-lookup"><span data-stu-id="01b08-315">position track <em>number</em></span></span></li>
<li><span data-ttu-id="01b08-316">pronto</span><span class="sxs-lookup"><span data-stu-id="01b08-316">ready</span></span></li>
<li><span data-ttu-id="01b08-317">samplespersec</span><span class="sxs-lookup"><span data-stu-id="01b08-317">samplespersec</span></span></li>
<li><span data-ttu-id="01b08-318">posizione iniziale</span><span class="sxs-lookup"><span data-stu-id="01b08-318">start position</span></span></li>
<li><span data-ttu-id="01b08-319">formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="01b08-319">time format</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="01b08-320">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszRequest** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="01b08-320">The following table lists the flags that can be specified in the **lpszRequest** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01b08-321">Valore</span><span class="sxs-lookup"><span data-stu-id="01b08-321">Value</span></span></th>
<th><span data-ttu-id="01b08-322">Significato</span><span class="sxs-lookup"><span data-stu-id="01b08-322">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01b08-323">allineamento</span><span class="sxs-lookup"><span data-stu-id="01b08-323">alignment</span></span></td>
<td><span data-ttu-id="01b08-324">Restituisce l'allineamento del blocco dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="01b08-324">Returns the block alignment of data, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-325">assembla record</span><span class="sxs-lookup"><span data-stu-id="01b08-325">assemble record</span></span></td>
<td><span data-ttu-id="01b08-326">Restituisce <strong>true</strong> se il dispositivo è impostato per assemblare la registrazione in modalità.</span><span class="sxs-lookup"><span data-stu-id="01b08-326">Returns <strong>TRUE</strong> if the device is set to assemble mode recording.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-327">Audio</span><span class="sxs-lookup"><span data-stu-id="01b08-327">audio</span></span></td>
<td><span data-ttu-id="01b08-328">Restituisce &quot; on &quot; o &quot; off &quot; a seconda del <a href="setaudio.md"></a> &quot; &quot; comando di &quot; disconnessione o disattivazione più recente &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-328">Returns &quot;on&quot; or &quot;off&quot; depending on the most recent <a href="setaudio.md">setaudio</a> &quot;on&quot; or &quot;off&quot; command.</span></span> <span data-ttu-id="01b08-329">Restituisce &quot; on &quot; se uno o entrambi gli altoparlanti sono abilitati e &quot; disattivato &quot; in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="01b08-329">It returns &quot;on&quot; if either or both speakers are enabled, and &quot;off&quot; otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-330">allineamento audio</span><span class="sxs-lookup"><span data-stu-id="01b08-330">audio alignment</span></span></td>
<td><span data-ttu-id="01b08-331">Restituisce l'allineamento dei blocchi di dati rispetto all'inizio dei dati audio della forma d'onda di input.</span><span class="sxs-lookup"><span data-stu-id="01b08-331">Returns the alignment of data blocks relative to the start of input waveform-audio data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-332">BitsPerSample audio</span><span class="sxs-lookup"><span data-stu-id="01b08-332">audio bitspersample</span></span></td>
<td><span data-ttu-id="01b08-333">Restituisce il numero di bit per campione usato dal dispositivo per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="01b08-333">Returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="01b08-334">Questo flag si applica solo ai dispositivi che supportano l' &quot; &quot; algoritmo PCM.</span><span class="sxs-lookup"><span data-stu-id="01b08-334">This flag applies only to devices supporting the &quot;pcm&quot; algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-335">interruzioni audio</span><span class="sxs-lookup"><span data-stu-id="01b08-335">audio breaks</span></span></td>
<td><span data-ttu-id="01b08-336">Restituisce il numero di volte in cui la parte audio dell'ultima sequenza AVI è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="01b08-336">Returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="01b08-337">Il sistema conta un'interruzioni audio ogni volta che tenta di scrivere i dati audio nel driver di dispositivo e rileva che il driver ha già eseguito tutti i dati disponibili.</span><span class="sxs-lookup"><span data-stu-id="01b08-337">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="01b08-338">Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="01b08-338">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="01b08-339">È destinato solo alla valutazione delle prestazioni. il valore restituito è difficile da interpretare.</span><span class="sxs-lookup"><span data-stu-id="01b08-339">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-340">bytespersec audio</span><span class="sxs-lookup"><span data-stu-id="01b08-340">audio bytespersec</span></span></td>
<td><span data-ttu-id="01b08-341">Restituisce il numero medio di byte al secondo usati per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="01b08-341">Returns the average number of bytes per second used for recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-342">input audio</span><span class="sxs-lookup"><span data-stu-id="01b08-342">audio input</span></span></td>
<td><span data-ttu-id="01b08-343">Restituisce il livello di audio istantaneo approssimativo del segnale audio di input analogico.</span><span class="sxs-lookup"><span data-stu-id="01b08-343">Returns the approximate instantaneous audio level of the analog input audio signal.</span></span> <span data-ttu-id="01b08-344">Un valore maggiore di 1000 implica la distorsione di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="01b08-344">A value greater than 1000 implies clipping distortion.</span></span> <span data-ttu-id="01b08-345">Alcuni dispositivi possono restituire questo valore solo durante la registrazione dell'audio.</span><span class="sxs-lookup"><span data-stu-id="01b08-345">Some devices can return this value only while recording audio.</span></span> <span data-ttu-id="01b08-346">Al valore non è associato alcun comando <a href="set.md">set</a> o <a href="setaudio.md">seaudio</a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-346">The value has no associated <a href="set.md">set</a> or <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-347">monitoraggio audio</span><span class="sxs-lookup"><span data-stu-id="01b08-347">audio monitor</span></span></td>
<td><span data-ttu-id="01b08-348">Restituisce &quot; &quot; l'output o uno dei tipi di input di origine validi.</span><span class="sxs-lookup"><span data-stu-id="01b08-348">Returns &quot;output&quot;, or one of the valid source-input types.</span></span> <span data-ttu-id="01b08-349">Per ulteriori informazioni, vedere il comando di monitoraggio <strong>sefonica</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-349">For more information, see the <strong>setaudio</strong> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-350">numero di monitor audio</span><span class="sxs-lookup"><span data-stu-id="01b08-350">audio monitor number</span></span></td>
<td><span data-ttu-id="01b08-351">Restituisce il numero del video monitorato del tipo specificato dal <strong></strong> &quot; monitoraggio audio di stato &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-351">Returns the monitored-video number of the type specified by <strong>status</strong> &quot;audio monitor&quot;.</span></span> <span data-ttu-id="01b08-352">Per ulteriori informazioni, vedere il comando <a href="setaudio.md">seaudio</a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-352">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-353">record audio</span><span class="sxs-lookup"><span data-stu-id="01b08-353">audio record</span></span></td>
<td><span data-ttu-id="01b08-354">Restituisce &quot; on &quot; o &quot; off &quot; , che riflette lo stato impostato dal record <strong>seaudio</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-354">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by <strong>setaudio</strong> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-355"><em>numero</em> di traccia del record audio</span><span class="sxs-lookup"><span data-stu-id="01b08-355">audio record track <em>number</em></span></span></td>
<td><span data-ttu-id="01b08-356">Restituisce <strong>true</strong> se il VCR è impostato per registrare l'audio.</span><span class="sxs-lookup"><span data-stu-id="01b08-356">Returns <strong>TRUE</strong> if the VCR is set to record audio.</span></span> <span data-ttu-id="01b08-357">Se non viene specificato alcun numero di traccia, viene utilizzato il valore predefinito 1.</span><span class="sxs-lookup"><span data-stu-id="01b08-357">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-358">samplespersec audio</span><span class="sxs-lookup"><span data-stu-id="01b08-358">audio samplespersec</span></span></td>
<td><span data-ttu-id="01b08-359">Restituisce il numero di campioni al secondo registrati.</span><span class="sxs-lookup"><span data-stu-id="01b08-359">Returns the number of samples per second recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-360">origine audio</span><span class="sxs-lookup"><span data-stu-id="01b08-360">audio source</span></span></td>
<td><span data-ttu-id="01b08-361">Restituisce l'origine del digitalizzatore audio corrente: a &quot; sinistra &quot; , a &quot; destra &quot; , a &quot; media &quot; o &quot; stereo &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-361">Returns the current audio digitizer source: &quot;left&quot;, &quot;right&quot;, &quot;average&quot;, or &quot;stereo&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-362">numero di origine audio</span><span class="sxs-lookup"><span data-stu-id="01b08-362">audio source number</span></span></td>
<td><span data-ttu-id="01b08-363">Restituisce il numero di origine audio del tipo restituito dall' <strong></strong> &quot; origine audio di stato &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-363">Returns the audio-source number of the type returned by <strong>status</strong> &quot;audio source&quot;.</span></span> <span data-ttu-id="01b08-364">Per ulteriori informazioni, vedere il comando <a href="setaudio.md">seaudio</a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-364">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-365">flusso audio</span><span class="sxs-lookup"><span data-stu-id="01b08-365">audio stream</span></span></td>
<td><span data-ttu-id="01b08-366">Restituisce il numero di flusso audio corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-366">Returns the current audio-stream number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-367">basso</span><span class="sxs-lookup"><span data-stu-id="01b08-367">bass</span></span></td>
<td><span data-ttu-id="01b08-368">Restituisce il livello di bassi audio corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-368">Returns the current audio-bass level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-369">BitsPerPel</span><span class="sxs-lookup"><span data-stu-id="01b08-369">bitsperpel</span></span></td>
<td><span data-ttu-id="01b08-370">Restituisce il numero di bit per pixel per il salvataggio dei dati acquisiti o registrati.</span><span class="sxs-lookup"><span data-stu-id="01b08-370">Returns the number of bits per pixel for saving captured or recorded data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-371">BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="01b08-371">bitspersample</span></span></td>
<td><span data-ttu-id="01b08-372">Restituisce i bit per campione.</span><span class="sxs-lookup"><span data-stu-id="01b08-372">Returns the bits per sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-373">luminosità</span><span class="sxs-lookup"><span data-stu-id="01b08-373">brightness</span></span></td>
<td><span data-ttu-id="01b08-374">Restituisce il livello di luminosità video corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-374">Returns the current video-brightness level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-375">bytespersec</span><span class="sxs-lookup"><span data-stu-id="01b08-375">bytespersec</span></span></td>
<td><span data-ttu-id="01b08-376">Restituisce il numero medio di byte al secondo riprodotti o registrati.</span><span class="sxs-lookup"><span data-stu-id="01b08-376">Returns the average number of bytes per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-377"><em>numero</em> di traccia del tipo CDAudio</span><span class="sxs-lookup"><span data-stu-id="01b08-377">cdaudio type track <em>number</em></span></span></td>
<td><span data-ttu-id="01b08-378">Restituisce il tipo del numero di traccia specificato.</span><span class="sxs-lookup"><span data-stu-id="01b08-378">Returns the type of the specified track number.</span></span> <span data-ttu-id="01b08-379">Può trattarsi di un &quot; audio o di un &quot; &quot; altro.&quot;</span><span class="sxs-lookup"><span data-stu-id="01b08-379">This can be &quot;audio&quot; or &quot;other.&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-380">channel</span><span class="sxs-lookup"><span data-stu-id="01b08-380">channel</span></span></td>
<td><span data-ttu-id="01b08-381">Restituisce il valore intero del set di canali sul sintonizzatore.</span><span class="sxs-lookup"><span data-stu-id="01b08-381">Returns the integer value of the channel set on the tuner.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-382"><em>numero</em> Tuner del canale</span><span class="sxs-lookup"><span data-stu-id="01b08-382">channel tuner <em>number</em></span></span></td>
<td><span data-ttu-id="01b08-383">Se &quot; &quot; viene specificato un <em>numero</em> di Tuner, viene restituito il canale attualmente selezionato sul <em>numero</em> di sintonizzatore logico.</span><span class="sxs-lookup"><span data-stu-id="01b08-383">If &quot;tuner&quot; <em>number</em> is given, then the currently selected channel on the logical tuner <em>number</em> will be returned.</span></span> <span data-ttu-id="01b08-384">Si noti che possono essere presenti diversi sintonizzatori logici.</span><span class="sxs-lookup"><span data-stu-id="01b08-384">Note that there can be several logical tuners.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-385">channels</span><span class="sxs-lookup"><span data-stu-id="01b08-385">channels</span></span></td>
<td><span data-ttu-id="01b08-386">Restituisce il numero di canali impostati (1 per mono, 2 per stereo).</span><span class="sxs-lookup"><span data-stu-id="01b08-386">Returns the number of channels set (1 for mono, 2 for stereo).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-387">clock</span><span class="sxs-lookup"><span data-stu-id="01b08-387">clock</span></span></td>
<td><span data-ttu-id="01b08-388">Restituisce l'ora esterna.</span><span class="sxs-lookup"><span data-stu-id="01b08-388">Returns the external time.</span></span> <span data-ttu-id="01b08-389">L'ora deve essere un unsigned long integer che esprime gli incrementi totali.</span><span class="sxs-lookup"><span data-stu-id="01b08-389">The time must be an unsigned long integer expressing total increments.</span></span> <span data-ttu-id="01b08-390">Per ulteriori informazioni, vedere il comando <a href="capability.md">Capability</a> &quot; Clock rate rate &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-390">For more information, see the <a href="capability.md">capability</a> &quot;clock increment rate&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-391">ID Clock</span><span class="sxs-lookup"><span data-stu-id="01b08-391">clock id</span></span></td>
<td><span data-ttu-id="01b08-392">Restituisce un intero univoco che identifica il clock.</span><span class="sxs-lookup"><span data-stu-id="01b08-392">Returns a unique integer identifying the clock.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-393">color</span><span class="sxs-lookup"><span data-stu-id="01b08-393">color</span></span></td>
<td><span data-ttu-id="01b08-394">Restituisce il livello di colore corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-394">Returns the current color level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-395">elevato</span><span class="sxs-lookup"><span data-stu-id="01b08-395">contrast</span></span></td>
<td><span data-ttu-id="01b08-396">Restituisce il livello di contrasto corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-396">Returns the current contrast level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-397">counter</span><span class="sxs-lookup"><span data-stu-id="01b08-397">counter</span></span></td>
<td><span data-ttu-id="01b08-398">Restituisce la posizione del contatore, nel formato del contatore corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-398">Returns the counter position, in the current counter format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-399">formato contatore</span><span class="sxs-lookup"><span data-stu-id="01b08-399">counter format</span></span></td>
<td><span data-ttu-id="01b08-400">Restituisce il formato del contatore corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-400">Returns the current counter format.</span></span> <span data-ttu-id="01b08-401">Per ulteriori informazioni, vedere il comando <a href="set.md">imposta</a> &quot; formato contatore &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-401">For more information, see the <a href="set.md">set</a> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-402">risoluzione del contatore</span><span class="sxs-lookup"><span data-stu-id="01b08-402">counter resolution</span></span></td>
<td><span data-ttu-id="01b08-403">Restituisce &quot; &quot; i frame &quot; o &quot; i secondi, che indicano la risoluzione del contatore.</span><span class="sxs-lookup"><span data-stu-id="01b08-403">Returns &quot;frames&quot; or &quot;seconds&quot;, indicating the counter's resolution.</span></span> <span data-ttu-id="01b08-404">Questa operazione non è identica a quella dell'accuratezza.</span><span class="sxs-lookup"><span data-stu-id="01b08-404">This is not the same as accuracy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-405">traccia corrente</span><span class="sxs-lookup"><span data-stu-id="01b08-405">current track</span></span></td>
<td><span data-ttu-id="01b08-406">Restituisce la traccia corrente. Il sequencer MCISEQ restituisce 1.</span><span class="sxs-lookup"><span data-stu-id="01b08-406">Returns the current track. The MCISEQ sequencer returns 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-407">dimensioni del disco</span><span class="sxs-lookup"><span data-stu-id="01b08-407">disc size</span></span></td>
<td><span data-ttu-id="01b08-408">Restituisce 8 o 12, che indica le dimensioni in pollici del disco caricato.</span><span class="sxs-lookup"><span data-stu-id="01b08-408">Returns either 8 or 12, indicating the size of the loaded disc in inches.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-409"><em>unità</em> spazio su disco</span><span class="sxs-lookup"><span data-stu-id="01b08-409">disk space <em>drive</em></span></span></td>
<td><span data-ttu-id="01b08-410">Restituisce lo spazio su disco approssimativo, nel formato dell'ora corrente, che può essere ottenuto da un comando di <a href="reserve.md">riserva</a> per l'unità disco specificata <em>.</em></span><span class="sxs-lookup"><span data-stu-id="01b08-410">Returns the approximate disk space, in the current time format, that can be obtained by a <a href="reserve.md">reserve</a> command for the specified disk <em>drive.</em></span></span> <span data-ttu-id="01b08-411">L' <em>unità</em> viene in genere specificata come una singola lettera o una singola lettera seguita da due punti (:).</span><span class="sxs-lookup"><span data-stu-id="01b08-411">The <em>drive</em> is usually specified as a single letter or a single letter followed by a colon (:).</span></span> <span data-ttu-id="01b08-412">Alcuni dispositivi, tuttavia, potrebbero usare un percorso.</span><span class="sxs-lookup"><span data-stu-id="01b08-412">Some devices, however, might use a path.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-413">tipo divisione</span><span class="sxs-lookup"><span data-stu-id="01b08-413">division type</span></span></td>
<td><span data-ttu-id="01b08-414">Restituisce uno dei seguenti tipi di divisione file:</span><span class="sxs-lookup"><span data-stu-id="01b08-414">Returns one of the following file division types:</span></span>
<ul>
<li><span data-ttu-id="01b08-415">PPQN</span><span class="sxs-lookup"><span data-stu-id="01b08-415">PPQN</span></span></li>
<li><span data-ttu-id="01b08-416">Frame SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="01b08-416">SMPTE 24 frame</span></span></li>
<li><span data-ttu-id="01b08-417">Frame SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="01b08-417">SMPTE 25 frame</span></span></li>
<li><span data-ttu-id="01b08-418">Frame di rilascio SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="01b08-418">SMPTE 30 drop frame</span></span></li>
<li><span data-ttu-id="01b08-419">Frame SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="01b08-419">SMPTE 30 frame</span></span></li>
</ul>
<br/> <span data-ttu-id="01b08-420">Usare queste informazioni per determinare il formato del file MIDI e il significato delle informazioni sul tempo e sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="01b08-420">Use this information to determine the format of the MIDI file and the meaning of tempo and position information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-421">completamento file</span><span class="sxs-lookup"><span data-stu-id="01b08-421">file completion</span></span></td>
<td><span data-ttu-id="01b08-422">Restituisce la percentuale stimata di un'operazione di <a href="load.md">caricamento</a>, <a href="save.md">salvataggio</a>, <a href="capture.md">acquisizione</a>, <a href="cut.md">taglia</a>, <a href="copy.md">copia</a>, <a href="delete.md">eliminazione</a>, <a href="paste.md">Incolla</a>o <a href="undo.md">annullamento</a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-422">Returns the estimated percentage a <a href="load.md">load</a>, <a href="save.md">save</a>, <a href="capture.md">capture</a>, <a href="cut.md">cut</a>, <a href="copy.md">copy</a>, <a href="delete.md">delete</a>, <a href="paste.md">paste</a>, or <a href="undo.md">undo</a> operation has progressed.</span></span> <span data-ttu-id="01b08-423">(Le applicazioni possono usare questa operazione per fornire un indicatore visivo dello stato di avanzamento).</span><span class="sxs-lookup"><span data-stu-id="01b08-423">(Applications can use this to provide a visual indicator of progress.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-424">formato file</span><span class="sxs-lookup"><span data-stu-id="01b08-424">file format</span></span></td>
<td><span data-ttu-id="01b08-425">Restituisce il formato di file corrente per i comandi <a href="record.md">record</a> o <strong>Save</strong> .</span><span class="sxs-lookup"><span data-stu-id="01b08-425">Returns the current file format for <a href="record.md">record</a> or <strong>save</strong> commands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-426">modalità file</span><span class="sxs-lookup"><span data-stu-id="01b08-426">file mode</span></span></td>
<td><span data-ttu-id="01b08-427">Restituisce il &quot; caricamento &quot; , il &quot; salvataggio, la modifica o il tempo &quot; &quot; &quot; di &quot; inattività &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-427">Returns &quot;loading&quot;, &quot;saving&quot;, &quot;editing&quot;, or &quot;idle&quot;.</span></span> <span data-ttu-id="01b08-428">Durante un'operazione di <a href="load.md"><strong>caricamento</strong></a> , viene restituito il &quot; caricamento &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-428">During a <a href="load.md"><strong>load</strong></a> operation, it returns &quot;loading&quot;.</span></span> <span data-ttu-id="01b08-429">Durante le operazioni di <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>salvataggio</strong></a> e <a href="capture.md"><strong>acquisizione</strong></a> , viene restituito il &quot; salvataggio &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-429">During <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>save</strong></a> and <a href="capture.md"><strong>capture</strong></a> operations, it returns &quot;saving&quot;.</span></span> <span data-ttu-id="01b08-430">Durante le operazioni <a href="cut.md"><strong>Cut</strong></a>, <a href="copy.md"><strong>Copy</strong></a>, <a href="delete.md"><strong>Delete</strong></a>, <a href="paste.md"><strong>paste</strong></a>o <a href="undo.md"><strong>Undo</strong></a> , viene restituita la &quot; modifica &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-430">During <a href="cut.md"><strong>cut</strong></a>, <a href="copy.md"><strong>copy</strong></a>, <a href="delete.md"><strong>delete</strong></a>, <a href="paste.md"><strong>paste</strong></a>, or <a href="undo.md"><strong>undo</strong></a> operations, it returns &quot;editing&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-431">Tag di formato</span><span class="sxs-lookup"><span data-stu-id="01b08-431">format tag</span></span></td>
<td><span data-ttu-id="01b08-432">Restituisce il tag di formato.</span><span class="sxs-lookup"><span data-stu-id="01b08-432">Returns the format tag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-433">forward</span><span class="sxs-lookup"><span data-stu-id="01b08-433">forward</span></span></td>
<td><span data-ttu-id="01b08-434">Restituisce <strong>true</strong> se la direzione di riproduzione è diretta o se il dispositivo non viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="01b08-434">Returns <strong>TRUE</strong> if the play direction is forward or if the device is not playing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-435">frequenza fotogrammi</span><span class="sxs-lookup"><span data-stu-id="01b08-435">frame rate</span></span></td>
<td><span data-ttu-id="01b08-436">Restituisce il numero di fotogrammi al secondo che il dispositivo utilizzerà per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="01b08-436">Returns the number of frames per second that the device will use by default.</span></span> <span data-ttu-id="01b08-437">I dispositivi NTSC restituiscono 30, PAL 25 e così via.</span><span class="sxs-lookup"><span data-stu-id="01b08-437">NTSC devices return 30, PAL 25, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-438">frame ignorati</span><span class="sxs-lookup"><span data-stu-id="01b08-438">frames skipped</span></span></td>
<td><span data-ttu-id="01b08-439">Restituisce il numero di frame che non sono stati disegnati quando è stata riprodotta l'ultima sequenza AVI.</span><span class="sxs-lookup"><span data-stu-id="01b08-439">Returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="01b08-440">Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="01b08-440">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="01b08-441">È destinato solo alla valutazione delle prestazioni. il valore restituito è difficile da interpretare.</span><span class="sxs-lookup"><span data-stu-id="01b08-441">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-442">gamma</span><span class="sxs-lookup"><span data-stu-id="01b08-442">gamma</span></span></td>
<td><span data-ttu-id="01b08-443">Restituisce il valore impostato con <a href="setvideo.md"><strong>sevideo</strong></a> &quot; gamma su &quot; <em>value</em>.</span><span class="sxs-lookup"><span data-stu-id="01b08-443">Returns the value set with <a href="setvideo.md"><strong>setvideo</strong></a> &quot;gamma to&quot; <em>value</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-444">indice</span><span class="sxs-lookup"><span data-stu-id="01b08-444">index</span></span></td>
<td><span data-ttu-id="01b08-445">Restituisce la visualizzazione dell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-445">Returns the current index display.</span></span> <span data-ttu-id="01b08-446">Per ulteriori informazioni, vedere il comando <a href="set.md"><strong>set</strong></a> &quot; index &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-446">For more information, see the <a href="set.md"><strong>set</strong></a> &quot;index&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-447">Indice in</span><span class="sxs-lookup"><span data-stu-id="01b08-447">index on</span></span></td>
<td><span data-ttu-id="01b08-448">Restituisce <strong>true</strong> se l'indice è impostato su on.</span><span class="sxs-lookup"><span data-stu-id="01b08-448">Returns <strong>TRUE</strong> if the index is on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-449">input</span><span class="sxs-lookup"><span data-stu-id="01b08-449">input</span></span></td>
<td><span data-ttu-id="01b08-450">Restituisce il set di input.</span><span class="sxs-lookup"><span data-stu-id="01b08-450">Returns the input set.</span></span> <span data-ttu-id="01b08-451">Se non è impostata, l'errore restituito indica che è possibile usare qualsiasi dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01b08-451">If one is not set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="01b08-452">Per i dispositivi digitali video, modifica il &quot; &quot; flag Bass, &quot; Treble &quot; , &quot; volume &quot; , &quot; luminosità &quot; , &quot; colore &quot; , &quot; contrasto &quot; , &quot; gamma &quot; , &quot; nitidezza &quot; o &quot; tinta, &quot; in modo che venga applicato solo all'input.</span><span class="sxs-lookup"><span data-stu-id="01b08-452">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the input.</span></span> <span data-ttu-id="01b08-453">Si tratta dell'impostazione predefinita durante il monitoraggio dell'input.</span><span class="sxs-lookup"><span data-stu-id="01b08-453">This is the default when monitoring the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-454">volume sinistro</span><span class="sxs-lookup"><span data-stu-id="01b08-454">left volume</span></span></td>
<td><span data-ttu-id="01b08-455">Restituisce il set di volumi per il canale audio sinistro.</span><span class="sxs-lookup"><span data-stu-id="01b08-455">Returns the volume set for the left audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-456">length</span><span class="sxs-lookup"><span data-stu-id="01b08-456">length</span></span></td>
<td><span data-ttu-id="01b08-457">Restituisce la lunghezza totale del supporto, nel formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-457">Returns the total length of the media, in the current time format.</span></span> <span data-ttu-id="01b08-458">Per i file PPQN, la lunghezza viene restituita nelle unità del puntatore del brano.</span><span class="sxs-lookup"><span data-stu-id="01b08-458">For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="01b08-459">Per i file SMPTE, viene restituito come <em>hh: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames.</span><span class="sxs-lookup"><span data-stu-id="01b08-459">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="01b08-460">Per i dispositivi VCR, la lunghezza è di 2 ore, a meno che la lunghezza non sia stata modificata in modo esplicito con il comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-460">For VCR devices, the length is 2 hours (unless the length has been explicitly changed using the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> command).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-461"><em>numero</em> traccia lunghezza</span><span class="sxs-lookup"><span data-stu-id="01b08-461">length track <em>number</em></span></span></td>
<td><span data-ttu-id="01b08-462">Restituisce la lunghezza della traccia, nel tempo o nei frame, specificata per <em>numero</em>. Per i file PPQN, la lunghezza viene restituita nelle unità del puntatore del brano.</span><span class="sxs-lookup"><span data-stu-id="01b08-462">Returns the length of the track, in time or frames, specified by <em>number</em>.For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="01b08-463">Per i file SMPTE, viene restituito come <em>hh: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames.</span><span class="sxs-lookup"><span data-stu-id="01b08-463">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-464">livello</span><span class="sxs-lookup"><span data-stu-id="01b08-464">level</span></span></td>
<td><span data-ttu-id="01b08-465">Restituisce il valore di esempio dell'audio PCM corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-465">Returns the current PCM audio sample value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-466">master</span><span class="sxs-lookup"><span data-stu-id="01b08-466">master</span></span></td>
<td><span data-ttu-id="01b08-467">Restituisce &quot; MIDI &quot; , &quot; None &quot; o &quot; SMPTE &quot; a seconda del tipo di set di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="01b08-467">Returns &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-468">supporti presenti</span><span class="sxs-lookup"><span data-stu-id="01b08-468">media present</span></span></td>
<td><span data-ttu-id="01b08-469">Restituisce <strong>true</strong> se il supporto viene inserito nel dispositivo o <strong>false</strong> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="01b08-469">Returns <strong>TRUE</strong> if the media is inserted in the device or <strong>FALSE</strong> otherwise.</span></span> <span data-ttu-id="01b08-470">Sequencer, video overlay, Digital-video e waveform-i dispositivi audio restituiscono <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="01b08-470">Sequencer, video-overlay, digital-video, and waveform-audio devices return <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-471">tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="01b08-471">media type</span></span></td>
<td><span data-ttu-id="01b08-472">Restituisce il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="01b08-472">Returns the type of the media.</span></span> <span data-ttu-id="01b08-473">Per i VCR, questo è &quot; 8 mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; o &quot; altro &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-473">For VCRS, this is &quot;8mm&quot;, &quot;vhs&quot;, &quot;svhs&quot;, &quot;beta&quot;, &quot;Hi8&quot;, &quot;edbeta&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="01b08-474">Per videodischi, si tratta di &quot; CAV &quot; , &quot; CLV &quot; o &quot; other &quot; , a seconda del tipo di videodisco.</span><span class="sxs-lookup"><span data-stu-id="01b08-474">For videodiscs, this is &quot;CAV&quot;, &quot;CLV&quot;, or &quot;other&quot;, depending on the type of videodisc.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-475">mode</span><span class="sxs-lookup"><span data-stu-id="01b08-475">mode</span></span></td>
<td><span data-ttu-id="01b08-476">Restituisce la modalità corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01b08-476">Returns the current mode of the device.</span></span> <span data-ttu-id="01b08-477">Tutti i dispositivi possono restituire i &quot; valori non pronti &quot; , &quot; sospesi, in &quot; &quot; riproduzione &quot; e &quot; interrotti &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-477">All devices can return the &quot;not ready&quot;, &quot;paused&quot;, &quot;playing&quot;, and &quot;stopped&quot; values.</span></span> <span data-ttu-id="01b08-478">Alcuni dispositivi possono restituire &quot; &quot; valori aperti, &quot; parcheggiati, &quot; &quot; di registrazione &quot; e di &quot; ricerca aggiuntivi &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-478">Some devices can return the additional &quot;open&quot;, &quot;parked&quot;, &quot;recording&quot;, and &quot;seeking&quot; values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-479">monitoraggio</span><span class="sxs-lookup"><span data-stu-id="01b08-479">monitor</span></span></td>
<td><span data-ttu-id="01b08-480">Restituisce un &quot; file &quot; o un &quot; input &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-480">Returns &quot;file&quot; or &quot;input&quot;.</span></span> <span data-ttu-id="01b08-481">Il valore restituito indica l'origine della presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-481">The returned value indicates the current presentation source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-482">Metodo Monitor</span><span class="sxs-lookup"><span data-stu-id="01b08-482">monitor method</span></span></td>
<td><span data-ttu-id="01b08-483">Restituisce &quot; pre &quot; , &quot; Post &quot; o &quot; diretto &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-483">Returns &quot;pre&quot;, &quot;post&quot;, or &quot;direct&quot;.</span></span> <span data-ttu-id="01b08-484">Il valore restituito indica il metodo utilizzato per il monitoraggio dell'input.</span><span class="sxs-lookup"><span data-stu-id="01b08-484">The returned value indicates the method used for input monitoring.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-485">nominale</span><span class="sxs-lookup"><span data-stu-id="01b08-485">nominal</span></span></td>
<td><span data-ttu-id="01b08-486">L'elemento modifica i &quot; &quot; flag Bass, &quot; luminosità &quot; , &quot; Color &quot; , &quot; Contrast &quot; , &quot; gamma &quot; , &quot; nitidezza &quot; , &quot; tinta, &quot; &quot; Treble &quot; e &quot; volume &quot; per restituire il valore nominale anziché l'impostazione corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-486">The item modifies the &quot;bass&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, &quot;tint&quot;, &quot;treble,&quot; and &quot;volume&quot; flags to return the nominal value instead of the current setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-487">frequenza fotogrammi nominale</span><span class="sxs-lookup"><span data-stu-id="01b08-487">nominal frame rate</span></span></td>
<td><span data-ttu-id="01b08-488">Restituisce la frequenza dei fotogrammi nominale associata al file.</span><span class="sxs-lookup"><span data-stu-id="01b08-488">Returns the nominal frame rate associated with the file.</span></span> <span data-ttu-id="01b08-489">Le unità sono in frame al secondo moltiplicate per 1000.</span><span class="sxs-lookup"><span data-stu-id="01b08-489">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-490">frequenza fotogrammi record nominale</span><span class="sxs-lookup"><span data-stu-id="01b08-490">nominal record frame rate</span></span></td>
<td><span data-ttu-id="01b08-491">Restituisce la frequenza di fotogrammi nominale associata al segnale video di input.</span><span class="sxs-lookup"><span data-stu-id="01b08-491">Returns the nominal frame rate associated with the input video signal.</span></span> <span data-ttu-id="01b08-492">Le unità sono in frame al secondo moltiplicate per 1000.</span><span class="sxs-lookup"><span data-stu-id="01b08-492">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-493">numero di tracce audio</span><span class="sxs-lookup"><span data-stu-id="01b08-493">number of audio tracks</span></span></td>
<td><span data-ttu-id="01b08-494">Restituisce il numero di tracce audio sul supporto.</span><span class="sxs-lookup"><span data-stu-id="01b08-494">Returns the number of audio tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-495">numero di tracce</span><span class="sxs-lookup"><span data-stu-id="01b08-495">number of tracks</span></span></td>
<td><span data-ttu-id="01b08-496">Restituisce il numero di tracce sui supporti.</span><span class="sxs-lookup"><span data-stu-id="01b08-496">Returns the number of tracks on the media.</span></span> <span data-ttu-id="01b08-497">I dispositivi MCISEQ e MCIWAVE restituiscono 1, come per la maggior parte dei dispositivi VCR.</span><span class="sxs-lookup"><span data-stu-id="01b08-497">The MCISEQ and MCIWAVE devices return 1, as do most VCR devices.</span></span> <span data-ttu-id="01b08-498">Il dispositivo MCIPIONR non supporta questo flag.</span><span class="sxs-lookup"><span data-stu-id="01b08-498">The MCIPIONR device does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-499">numero di tracce video</span><span class="sxs-lookup"><span data-stu-id="01b08-499">number of video tracks</span></span></td>
<td><span data-ttu-id="01b08-500">Restituisce il numero di tracce video sui supporti.</span><span class="sxs-lookup"><span data-stu-id="01b08-500">Returns the number of video tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-501">offset</span><span class="sxs-lookup"><span data-stu-id="01b08-501">offset</span></span></td>
<td><span data-ttu-id="01b08-502">Restituisce l'offset di un file basato su SMPTE.</span><span class="sxs-lookup"><span data-stu-id="01b08-502">Returns the offset of a SMPTE-based file.</span></span> <span data-ttu-id="01b08-503">L'offset è l'ora di inizio di una sequenza basata su SMPTE.</span><span class="sxs-lookup"><span data-stu-id="01b08-503">The offset is the start time of a SMPTE-based sequence.</span></span> <span data-ttu-id="01b08-504">L'ora viene restituita <em>come HH: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames.</span><span class="sxs-lookup"><span data-stu-id="01b08-504">The time is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-505">output</span><span class="sxs-lookup"><span data-stu-id="01b08-505">output</span></span></td>
<td><span data-ttu-id="01b08-506">Restituisce l'output attualmente impostato.</span><span class="sxs-lookup"><span data-stu-id="01b08-506">Returns the currently set output.</span></span> <span data-ttu-id="01b08-507">Se non è impostato alcun output, l'errore restituito indica che è possibile usare qualsiasi dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01b08-507">If no output is set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="01b08-508">Per i dispositivi digitali video, modifica il &quot; &quot; flag Bass, &quot; Treble &quot; , &quot; volume &quot; , &quot; luminosità &quot; , &quot; colore &quot; , &quot; contrasto &quot; , &quot; gamma &quot; , &quot; nitidezza &quot; o &quot; tinta, &quot; in modo che venga applicato solo all'output.</span><span class="sxs-lookup"><span data-stu-id="01b08-508">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the output.</span></span> <span data-ttu-id="01b08-509">Si tratta dell'impostazione predefinita durante il monitoraggio di un file.</span><span class="sxs-lookup"><span data-stu-id="01b08-509">This is the default when monitoring a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-510">modalità di sospensione</span><span class="sxs-lookup"><span data-stu-id="01b08-510">pause mode</span></span></td>
<td><span data-ttu-id="01b08-511">Restituisce &quot; &quot; la registrazione se il dispositivo viene sospeso durante la registrazione.</span><span class="sxs-lookup"><span data-stu-id="01b08-511">Returns &quot;recording&quot; if the device is paused while recording.</span></span> <span data-ttu-id="01b08-512">Restituisce &quot; la riproduzione &quot; se il dispositivo viene sospeso durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="01b08-512">It returns &quot;playing&quot; if the device is paused while playing.</span></span> <span data-ttu-id="01b08-513">Restituisce l' &quot; azione di errore non applicabile nella modalità corrente &quot; se il dispositivo non è sospeso.</span><span class="sxs-lookup"><span data-stu-id="01b08-513">It returns the error &quot;Action not applicable in current mode&quot; if the device is not paused.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-514">timeout pausa</span><span class="sxs-lookup"><span data-stu-id="01b08-514">pause timeout</span></span></td>
<td><span data-ttu-id="01b08-515">Restituisce la durata massima, in millisecondi, di un comando di <a href="pause.md"><strong>sospensione</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-515">Returns the maximum duration, in milliseconds, of a <a href="pause.md"><strong>pause</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-516">formato di riproduzione</span><span class="sxs-lookup"><span data-stu-id="01b08-516">play format</span></span></td>
<td><span data-ttu-id="01b08-517">Restituisce un codice che indica il formato in cui verrà riprodotto il nastro, se rilevabile: &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; o &quot; altro &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-517">Returns a code indicating the format that the videotape will be played back in, if detectable: &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="01b08-518">Per ulteriori informazioni, vedere il &quot; flag del formato di record &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-518">For more information, see the &quot;record format&quot; flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-519">velocità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="01b08-519">play speed</span></span></td>
<td><span data-ttu-id="01b08-520">Restituisce un valore che rappresenta la precisione del tempo di riproduzione effettivo dell'ultima sequenza AVI corrispondente al tempo di riproduzione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="01b08-520">Returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="01b08-521">Il valore 1000 indica che l'ora di destinazione e l'ora effettiva sono uguali.</span><span class="sxs-lookup"><span data-stu-id="01b08-521">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="01b08-522">Il valore 2000, ad esempio, indicherebbe che la sequenza AVI ha richiesto due volte la riproduzione del tempo necessario.</span><span class="sxs-lookup"><span data-stu-id="01b08-522">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="01b08-523">Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="01b08-523">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="01b08-524">È destinato solo alla valutazione delle prestazioni. il valore restituito è difficile da interpretare.</span><span class="sxs-lookup"><span data-stu-id="01b08-524">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-525">port</span><span class="sxs-lookup"><span data-stu-id="01b08-525">port</span></span></td>
<td><span data-ttu-id="01b08-526">Restituisce il numero di porta MIDI assegnato alla sequenza.</span><span class="sxs-lookup"><span data-stu-id="01b08-526">Returns the MIDI port number assigned to the sequence.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-527">position</span><span class="sxs-lookup"><span data-stu-id="01b08-527">position</span></span></td>
<td><span data-ttu-id="01b08-528">Restituisce la posizione corrente. Per i file PPQN, la posizione viene restituita nelle unità del puntatore del brano.</span><span class="sxs-lookup"><span data-stu-id="01b08-528">Returns the current position.For PPQN files, the position is returned in song pointer units.</span></span> <span data-ttu-id="01b08-529">Per i file SMPTE, viene restituito come <em>hh: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, SS è seconds e <em>FF</em> è frames.</span><span class="sxs-lookup"><span data-stu-id="01b08-529">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, ss is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-530">inizio posizione</span><span class="sxs-lookup"><span data-stu-id="01b08-530">position start</span></span></td>
<td><span data-ttu-id="01b08-531">Restituisce la posizione dell'inizio del supporto utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="01b08-531">Returns the position of the start of the usable media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-532"><em>numero</em> di traccia posizione</span><span class="sxs-lookup"><span data-stu-id="01b08-532">position track <em>number</em></span></span></td>
<td><span data-ttu-id="01b08-533">Restituisce la posizione dell'inizio della traccia specificata dal <em>numero</em>.</span><span class="sxs-lookup"><span data-stu-id="01b08-533">Returns the position of the start of the track specified by <em>number</em>.</span></span> <span data-ttu-id="01b08-534">Per i file PPQN, il formato dell'ora viene restituito nelle unità del puntatore del brano.</span><span class="sxs-lookup"><span data-stu-id="01b08-534">For PPQN files, the time format is returned in song pointer units.</span></span> <span data-ttu-id="01b08-535">Per i file SMPTE, viene restituito come <em>hh: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames.</span><span class="sxs-lookup"><span data-stu-id="01b08-535">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="01b08-536">MCISEQ Sequencer restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="01b08-536">The MCISEQ sequencer returns zero.</span></span> <span data-ttu-id="01b08-537">Il dispositivo MCIPIONR non supporta questo flag.</span><span class="sxs-lookup"><span data-stu-id="01b08-537">The MCIPIONR device does not support this flag.</span></span> <span data-ttu-id="01b08-538">Il dispositivo MCIWAVE restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="01b08-538">The MCIWAVE device returns zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-539">durata postroll</span><span class="sxs-lookup"><span data-stu-id="01b08-539">postroll duration</span></span></td>
<td><span data-ttu-id="01b08-540">Restituisce la lunghezza del nastro, nel formato ora corrente, necessario per bloccare il trasporto del videoregistratore quando viene emesso un comando di <a href="stop.md"><strong>arresto</strong></a> o <a href="pause.md"><strong>sospensione</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-540">Returns the length of videotape, in the current time format, needed to brake the VCR transport when a <a href="stop.md"><strong>stop</strong></a> or <a href="pause.md"><strong>pause</strong></a> command is issued.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-541">accensione</span><span class="sxs-lookup"><span data-stu-id="01b08-541">power on</span></span></td>
<td><span data-ttu-id="01b08-542">Restituisce <strong>true</strong> se l'alimentazione del VCR è accesa.</span><span class="sxs-lookup"><span data-stu-id="01b08-542">Returns <strong>TRUE</strong> if the VCR's power is on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-543">durata preroll</span><span class="sxs-lookup"><span data-stu-id="01b08-543">preroll duration</span></span></td>
<td><span data-ttu-id="01b08-544">Restituisce la lunghezza del nastro, nel formato dell'ora corrente, necessario per stabilizzare l'output del videoregistratore.</span><span class="sxs-lookup"><span data-stu-id="01b08-544">Returns the length of videotape, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-545">pronto</span><span class="sxs-lookup"><span data-stu-id="01b08-545">ready</span></span></td>
<td><span data-ttu-id="01b08-546">Restituisce <strong>true</strong> se il dispositivo è pronto per accettare un altro comando.</span><span class="sxs-lookup"><span data-stu-id="01b08-546">Returns <strong>TRUE</strong> if the device is ready to accept another command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-547">formato record</span><span class="sxs-lookup"><span data-stu-id="01b08-547">record format</span></span></td>
<td><span data-ttu-id="01b08-548">Restituisce un codice che indica il formato in cui verrà registrato il nastro.</span><span class="sxs-lookup"><span data-stu-id="01b08-548">Returns a code indicating the format that the videotape will be recorded in.</span></span> <span data-ttu-id="01b08-549">I tipi restituiti correnti sono &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; o &quot; other &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-549">The current return types are &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="01b08-550">Questi formati non sono specifici di VHS e possono essere applicati a qualsiasi VCR con più formati di registrazione selezionabili.</span><span class="sxs-lookup"><span data-stu-id="01b08-550">These formats are not VHS specific and can be applied to any VCR that has multiple selectable recording formats.</span></span> <span data-ttu-id="01b08-551">Il &quot; &quot; tipo SP è il formato di registrazione più veloce e di alta qualità e viene usato come impostazione predefinita nel VCR con singolo formato.</span><span class="sxs-lookup"><span data-stu-id="01b08-551">The &quot;sp&quot; type is the fastest, highest quality recording format and is used as default on single format VCRs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-552">frequenza fotogrammi record</span><span class="sxs-lookup"><span data-stu-id="01b08-552">record frame rate</span></span></td>
<td><span data-ttu-id="01b08-553">Restituisce la frequenza dei fotogrammi, in frame al secondo moltiplicata per 1000, utilizzata per la compressione.</span><span class="sxs-lookup"><span data-stu-id="01b08-553">Returns the frame rate, in frames per second multiplied by 1000, used for compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-554"><em>frame</em> di riferimento</span><span class="sxs-lookup"><span data-stu-id="01b08-554">reference <em>frame</em></span></span></td>
<td><span data-ttu-id="01b08-555">Restituisce il numero di frame per l'immagine del fotogramma chiave più vicina che precede il <em>frame</em>specificato.</span><span class="sxs-lookup"><span data-stu-id="01b08-555">Returns the frame number for the nearest key frame image that precedes the specified <em>frame</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-556">dimensioni riservate</span><span class="sxs-lookup"><span data-stu-id="01b08-556">reserved size</span></span></td>
<td><span data-ttu-id="01b08-557">Restituisce la dimensione, nel formato dell'ora corrente, dell'area di lavoro riservata.</span><span class="sxs-lookup"><span data-stu-id="01b08-557">Returns the size, in the current time format, of the reserved workspace.</span></span> <span data-ttu-id="01b08-558">Le dimensioni corrispondono al tempo approssimativo necessario per riprodurre i dati compressi da un'area di lavoro completa.</span><span class="sxs-lookup"><span data-stu-id="01b08-558">The size corresponds to the approximate time it would take to play the compressed data from a full workspace.</span></span> <span data-ttu-id="01b08-559">Restituisce zero se non è disponibile spazio su disco riservato.</span><span class="sxs-lookup"><span data-stu-id="01b08-559">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="01b08-560">Questo flag restituisce le dimensioni approssimative perché lo spazio su disco preciso per i dati compressi non può essere stimato, in generale, fino a quando i dati non sono stati compressi.</span><span class="sxs-lookup"><span data-stu-id="01b08-560">This flag returns the approximate size because the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-561">volume giusto</span><span class="sxs-lookup"><span data-stu-id="01b08-561">right volume</span></span></td>
<td><span data-ttu-id="01b08-562">Restituisce il set di volumi per il canale audio destro.</span><span class="sxs-lookup"><span data-stu-id="01b08-562">Returns the volume set for the right audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-563">samplespersec</span><span class="sxs-lookup"><span data-stu-id="01b08-563">samplespersec</span></span></td>
<td><span data-ttu-id="01b08-564">Restituisce il numero di campioni al secondo riprodotti o registrati.</span><span class="sxs-lookup"><span data-stu-id="01b08-564">Returns the number of samples per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-565">ricerca esatta</span><span class="sxs-lookup"><span data-stu-id="01b08-565">seek exactly</span></span></td>
<td><span data-ttu-id="01b08-566">Restituisce &quot; on &quot; o &quot; off &quot; , che indica se &quot; è impostato il flag Seek exactly &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-566">Returns &quot;on&quot; or &quot;off&quot;, indicating whether or not the &quot;seek exactly&quot; flag is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-567">nitidezza</span><span class="sxs-lookup"><span data-stu-id="01b08-567">sharpness</span></span></td>
<td><span data-ttu-id="01b08-568">Restituisce il livello di nitidezza corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01b08-568">Returns the current sharpness level of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-569">lato</span><span class="sxs-lookup"><span data-stu-id="01b08-569">side</span></span></td>
<td><span data-ttu-id="01b08-570">Restituisce 1 o 2 per indicare quale lato di videodisco è caricato.</span><span class="sxs-lookup"><span data-stu-id="01b08-570">Returns 1 or 2 to indicate which side of the videodisc is loaded.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-571">schiavo</span><span class="sxs-lookup"><span data-stu-id="01b08-571">slave</span></span></td>
<td><span data-ttu-id="01b08-572">Restituisce &quot; file &quot; , &quot; MIDI &quot; , &quot; None &quot; o &quot; SMPTE, &quot; a seconda del tipo di set di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="01b08-572">Returns &quot;file&quot; , &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-573">SMPTE</span><span class="sxs-lookup"><span data-stu-id="01b08-573">smpte</span></span></td>
<td><span data-ttu-id="01b08-574">Restituisce il timecode SMPTE associato alla posizione corrente nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="01b08-574">Returns the SMPTE timecode associated with the current position in the workspace.</span></span> <span data-ttu-id="01b08-575">Si tratta di una stringa nel formato <em>GG: DD: DD</em>: DD, dove ogni <em>d</em> indica una cifra da 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="01b08-575">This is a string with the form <em>dd:dd:dd:dd</em>, where each <em>d</em> denotes a digit from 0 to 9.</span></span> <span data-ttu-id="01b08-576">Se i dati dell'area di lavoro non includono i dati del timecode, questo flag restituisce 00:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="01b08-576">If the workspace data does not include timecode data, then this flag returns 00:00:00:00.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-577">velocità</span><span class="sxs-lookup"><span data-stu-id="01b08-577">speed</span></span></td>
<td><span data-ttu-id="01b08-578">Restituisce la velocità corrente del dispositivo in frame al secondo (o nello stesso formato utilizzato dal comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot; Speed &quot; ).</span><span class="sxs-lookup"><span data-stu-id="01b08-578">Returns the current speed of the device in frames per second (or in the same format used by the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot;speed&quot; command).</span></span> <span data-ttu-id="01b08-579">Il lettore videodisco MCIPIONR non supporta questo flag.</span><span class="sxs-lookup"><span data-stu-id="01b08-579">The MCIPIONR videodisc player does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-580">posizione iniziale</span><span class="sxs-lookup"><span data-stu-id="01b08-580">start position</span></span></td>
<td><span data-ttu-id="01b08-581">Restituisce la posizione iniziale del supporto.</span><span class="sxs-lookup"><span data-stu-id="01b08-581">Returns the starting position of the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-582">formato file ancora</span><span class="sxs-lookup"><span data-stu-id="01b08-582">still file format</span></span></td>
<td><span data-ttu-id="01b08-583">Restituisce il formato di file corrente per il comando di <a href="capture.md"><strong>acquisizione</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-583">Returns the current file format for the <a href="capture.md"><strong>capture</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-584">adattamento</span><span class="sxs-lookup"><span data-stu-id="01b08-584">stretch</span></span></td>
<td><span data-ttu-id="01b08-585">Restituisce <strong>true</strong> se l'estensione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="01b08-585">Returns <strong>TRUE</strong> if stretching is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-586">tempo</span><span class="sxs-lookup"><span data-stu-id="01b08-586">tempo</span></span></td>
<td><span data-ttu-id="01b08-587">Restituisce il tempo corrente di una sequenza MIDI nel formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-587">Returns the current tempo of a MIDI sequence in the current time format.</span></span> <span data-ttu-id="01b08-588">Per i file con formato PPQN, il tempo è in battute al minuto.</span><span class="sxs-lookup"><span data-stu-id="01b08-588">For files with PPQN format, the tempo is in beats per minute.</span></span> <span data-ttu-id="01b08-589">Per i file con formato SMPTE, il tempo è in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="01b08-589">For files with SMPTE format, the tempo is in frames per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-590">formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="01b08-590">time format</span></span></td>
<td><span data-ttu-id="01b08-591">Restituisce il formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-591">Returns the current time format.</span></span> <span data-ttu-id="01b08-592">Per ulteriori informazioni, vedere i formati di ora nel comando <a href="set.md"><strong>set</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-592">For more information, see the time formats in the <a href="set.md"><strong>set</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-593">modalità ora</span><span class="sxs-lookup"><span data-stu-id="01b08-593">time mode</span></span></td>
<td><span data-ttu-id="01b08-594">Restituisce la modalità temporale di posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-594">Returns the current position time mode.</span></span> <span data-ttu-id="01b08-595">Può essere &quot; Detect &quot; , &quot; timecode &quot; o &quot; Counter &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-595">It can be &quot;detect&quot;, &quot;timecode&quot;, or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-596">tipo Time</span><span class="sxs-lookup"><span data-stu-id="01b08-596">time type</span></span></td>
<td><span data-ttu-id="01b08-597">Restituisce il tempo di posizione corrente in uso: &quot; timecode &quot; o &quot; contatore &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-597">Returns the current position time in use: &quot;timecode&quot; or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-598">codice temporale presente</span><span class="sxs-lookup"><span data-stu-id="01b08-598">timecode present</span></span></td>
<td><span data-ttu-id="01b08-599">Restituisce <strong>true</strong> se il codice temporale è stato registrato nella posizione corrente sul nastro.</span><span class="sxs-lookup"><span data-stu-id="01b08-599">Returns <strong>TRUE</strong> if timecode has been recorded at the current position on the tape.</span></span> <span data-ttu-id="01b08-600">Il codice temporale deve avanzare dalla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-600">The timecode must advance from the current position.</span></span> <span data-ttu-id="01b08-601">Potrebbe essere necessario riprodurre un VCR per verificare questa condizione.</span><span class="sxs-lookup"><span data-stu-id="01b08-601">A VCR might need to be played to check this condition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-602">record timecode</span><span class="sxs-lookup"><span data-stu-id="01b08-602">timecode record</span></span></td>
<td><span data-ttu-id="01b08-603">Restituisce <strong>true</strong> se il VCR è impostato in modo da registrare il codice temporale.</span><span class="sxs-lookup"><span data-stu-id="01b08-603">Returns <strong>TRUE</strong> if the VCR is set to record timecode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-604">tipo di timecode</span><span class="sxs-lookup"><span data-stu-id="01b08-604">timecode type</span></span></td>
<td><span data-ttu-id="01b08-605">Restituisce &quot; SMPTE &quot; , &quot; SMPTE Drop &quot; , &quot; other &quot; o &quot; None &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-605">Returns &quot;smpte&quot;, &quot;smpte drop&quot;, &quot;other&quot;, or &quot;none&quot;.</span></span> <span data-ttu-id="01b08-606">Si noti che i frame al secondo possono essere ottenuti dal &quot; comando della frequenza dei fotogrammi di stato &quot; e l'accuratezza del dispositivo può essere restituita dal comando <a href="capability.md"><strong>Capability</strong></a> &quot; Seek accuratezza &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-606">Note the frames per second can be obtained from the status &quot;frame rate&quot; command, and the accuracy of the device can be returned by the <a href="capability.md"><strong>capability</strong></a> &quot;seek accuracy&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-607">tinta</span><span class="sxs-lookup"><span data-stu-id="01b08-607">tint</span></span></td>
<td><span data-ttu-id="01b08-608">Restituisce il livello di tinta del video corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-608">Returns the current video-tint level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-609">acuti</span><span class="sxs-lookup"><span data-stu-id="01b08-609">treble</span></span></td>
<td><span data-ttu-id="01b08-610">Restituisce il livello audio-acuti corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-610">Returns the current audio-treble level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-611">numero Tuner</span><span class="sxs-lookup"><span data-stu-id="01b08-611">tuner number</span></span></td>
<td><span data-ttu-id="01b08-612">Restituisce il numero del sintonizzatore logico corrente.</span><span class="sxs-lookup"><span data-stu-id="01b08-612">Returns the current logical-tuner number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-613">unsaved</span><span class="sxs-lookup"><span data-stu-id="01b08-613">unsaved</span></span></td>
<td><span data-ttu-id="01b08-614">Restituisce <strong>true</strong> se nell'area di lavoro sono presenti dati registrati che potrebbero andare perduti a seguito di un comando <a href="close.md"><strong>Close</strong></a>, <a href="load.md"><strong>Load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>Reserve</strong></a>, <a href="cut.md"><strong>Cut</strong></a>, <a href="delete.md"><strong>Delete</strong></a>o <a href="paste.md"><strong>paste</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-614">Returns <strong>TRUE</strong> if there is recorded data in the workspace that might be lost as a result of a <a href="close.md"><strong>close</strong></a>, <a href="load.md"><strong>load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>reserve</strong></a>, <a href="cut.md"><strong>cut</strong></a>, <a href="delete.md"><strong>delete</strong></a>, or <a href="paste.md"><strong>paste</strong></a> command.</span></span> <span data-ttu-id="01b08-615">In caso contrario, restituisce <strong>false</strong> .</span><span class="sxs-lookup"><span data-stu-id="01b08-615">Returns <strong>FALSE</strong> otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-616">Video</span><span class="sxs-lookup"><span data-stu-id="01b08-616">video</span></span></td>
<td><span data-ttu-id="01b08-617">Restituisce &quot; on &quot; o &quot; off &quot; , che riflette lo stato impostato dal comando <a href="setvideo.md"><strong>sevideo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-617">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-618">colore della chiave video</span><span class="sxs-lookup"><span data-stu-id="01b08-618">video key color</span></span></td>
<td><span data-ttu-id="01b08-619">Restituisce il valore per il colore della chiave.</span><span class="sxs-lookup"><span data-stu-id="01b08-619">Returns the value for the key color.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-620">indice chiave video</span><span class="sxs-lookup"><span data-stu-id="01b08-620">video key index</span></span></td>
<td><span data-ttu-id="01b08-621">Restituisce il valore per l'indice della chiave.</span><span class="sxs-lookup"><span data-stu-id="01b08-621">Returns the value for the key index.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-622">monitoraggio video</span><span class="sxs-lookup"><span data-stu-id="01b08-622">video monitor</span></span></td>
<td><span data-ttu-id="01b08-623">Restituisce &quot; &quot; l'output o uno dei tipi di input di origine validi.</span><span class="sxs-lookup"><span data-stu-id="01b08-623">Returns &quot;output&quot; or one of the valid source-input types.</span></span> <span data-ttu-id="01b08-624">Per ulteriori informazioni, vedere il comando <a href="setvideo.md"><strong>sevideo</strong></a> &quot; Monitor &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-624">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-625">numero di monitor video</span><span class="sxs-lookup"><span data-stu-id="01b08-625">video monitor number</span></span></td>
<td><span data-ttu-id="01b08-626">Restituisce il numero del video monitorato del tipo restituito dal &quot; monitoraggio video di stato &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-626">Returns the monitored-video number of the type returned by status &quot;video monitor&quot;.</span></span> <span data-ttu-id="01b08-627">Per ulteriori informazioni, vedere il comando <a href="setvideo.md">sevideo</a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-627">For more information, see the <a href="setvideo.md">setvideo</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-628">record video</span><span class="sxs-lookup"><span data-stu-id="01b08-628">video record</span></span></td>
<td><span data-ttu-id="01b08-629">Restituisce &quot; on &quot; o &quot; off &quot; , che riflette lo stato corrente impostato dal record <a href="setvideo.md"><strong>sevideo</strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="01b08-629">Returns &quot;on&quot; or &quot;off&quot;, reflecting the current state set by <a href="setvideo.md"><strong>setvideo</strong></a> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-630"><em>numero</em> di traccia del record video</span><span class="sxs-lookup"><span data-stu-id="01b08-630">video record track <em>number</em></span></span></td>
<td><span data-ttu-id="01b08-631">Restituisce <strong>true</strong> se il VCR è impostato per registrare il video.</span><span class="sxs-lookup"><span data-stu-id="01b08-631">Return <strong>TRUE</strong> if the VCR is set to record video.</span></span> <span data-ttu-id="01b08-632">Se non viene specificato alcun numero di traccia, viene utilizzato il valore predefinito 1.</span><span class="sxs-lookup"><span data-stu-id="01b08-632">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-633">origine video</span><span class="sxs-lookup"><span data-stu-id="01b08-633">video source</span></span></td>
<td><span data-ttu-id="01b08-634">Restituisce il tipo di origine video.</span><span class="sxs-lookup"><span data-stu-id="01b08-634">Returns the video-source type.</span></span> <span data-ttu-id="01b08-635">Per ulteriori informazioni, vedere il comando <a href="setvideo.md"><strong>sevideo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01b08-635">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-636">numero di origine video</span><span class="sxs-lookup"><span data-stu-id="01b08-636">video source number</span></span></td>
<td><span data-ttu-id="01b08-637">Restituisce un numero corrispondente all'origine video del tipo in uso.</span><span class="sxs-lookup"><span data-stu-id="01b08-637">Returns a number corresponding to the video source of the type in use.</span></span> <span data-ttu-id="01b08-638">Ad esempio, restituisce 2 Se viene usato il secondo input di origine video NTSC.</span><span class="sxs-lookup"><span data-stu-id="01b08-638">For example, it returns 2 if the second NTSC video source input is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-639">flusso video</span><span class="sxs-lookup"><span data-stu-id="01b08-639">video stream</span></span></td>
<td><span data-ttu-id="01b08-640">Restituisce il numero corrente del flusso video.</span><span class="sxs-lookup"><span data-stu-id="01b08-640">Returns the current video-stream number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-641">volume</span><span class="sxs-lookup"><span data-stu-id="01b08-641">volume</span></span></td>
<td><span data-ttu-id="01b08-642">Restituisce il volume medio all'altoparlante sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="01b08-642">Returns the average volume to the left and right speaker.</span></span> <span data-ttu-id="01b08-643">Viene restituito un errore se il dispositivo non è stato riprodotto o il volume non è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="01b08-643">This returns an error if the device has not been played or volume has not been set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-644">handle finestra</span><span class="sxs-lookup"><span data-stu-id="01b08-644">window handle</span></span></td>
<td><span data-ttu-id="01b08-645">Restituisce il valore decimale ASCII per l'handle di finestra nella parola di basso livello del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="01b08-645">Returns the ASCII decimal value for the window handle in the low-order word of the return value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-646">finestra ingrandita</span><span class="sxs-lookup"><span data-stu-id="01b08-646">window maximized</span></span></td>
<td><span data-ttu-id="01b08-647">Restituisce <strong>true</strong> se la finestra è ingrandita.</span><span class="sxs-lookup"><span data-stu-id="01b08-647">Returns <strong>TRUE</strong> if the window is maximized.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-648">finestra ridotta a icona</span><span class="sxs-lookup"><span data-stu-id="01b08-648">window minimized</span></span></td>
<td><span data-ttu-id="01b08-649">Restituisce <strong>true</strong> se la finestra è ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="01b08-649">Returns <strong>TRUE</strong> if the window is minimized.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b08-650">finestra visibile</span><span class="sxs-lookup"><span data-stu-id="01b08-650">window visible</span></span></td>
<td><span data-ttu-id="01b08-651">Restituisce <strong>true</strong> se la finestra non è nascosta.</span><span class="sxs-lookup"><span data-stu-id="01b08-651">Returns <strong>TRUE</strong> if the window is not hidden.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b08-652">scrittura protetta</span><span class="sxs-lookup"><span data-stu-id="01b08-652">write protected</span></span></td>
<td><span data-ttu-id="01b08-653">Restituisce <strong>true</strong> se il dispositivo rileva che non è in grado di registrare, ovvero se la protezione da scrittura è impostata su on.</span><span class="sxs-lookup"><span data-stu-id="01b08-653">Returns <strong>TRUE</strong> if the device detects that it cannot record (that is, if the write protect is on).</span></span> <span data-ttu-id="01b08-654">Se può registrare o se non è in grado di determinare se può registrare o meno (senza scrivere effettivamente), il driver restituisce <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="01b08-654">If it can record, or if it is unable to determine whether or not it can record (without actually writing), the driver returns <strong>FALSE</strong>.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="01b08-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="01b08-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="01b08-656">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="01b08-656">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="01b08-657">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="01b08-657">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="01b08-658">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="01b08-658">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01b08-659">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01b08-659">Return Value</span></span>

<span data-ttu-id="01b08-660">Restituisce le informazioni nel parametro *lpszReturnString* di [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="01b08-660">Returns information in the *lpszReturnString* parameter of [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span></span> <span data-ttu-id="01b08-661">Le informazioni dipendono dal tipo di richiesta.</span><span class="sxs-lookup"><span data-stu-id="01b08-661">The information is dependent on the request type.</span></span>

## <a name="remarks"></a><span data-ttu-id="01b08-662">Commenti</span><span class="sxs-lookup"><span data-stu-id="01b08-662">Remarks</span></span>

<span data-ttu-id="01b08-663">Prima di emettere i comandi che usano i valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="01b08-663">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="01b08-664">Esempio</span><span class="sxs-lookup"><span data-stu-id="01b08-664">Examples</span></span>

<span data-ttu-id="01b08-665">Il seguente comando restituisce la modalità corrente del dispositivo "audio".</span><span class="sxs-lookup"><span data-stu-id="01b08-665">The following command returns the current mode of the "mysound" device.</span></span>

``` syntax
status mysound mode
```

## <a name="requirements"></a><span data-ttu-id="01b08-666">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01b08-666">Requirements</span></span>



| <span data-ttu-id="01b08-667">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b08-667">Requirement</span></span> | <span data-ttu-id="01b08-668">Valore</span><span class="sxs-lookup"><span data-stu-id="01b08-668">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="01b08-669">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b08-669">Minimum supported client</span></span><br/> | <span data-ttu-id="01b08-670">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01b08-670">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="01b08-671">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b08-671">Minimum supported server</span></span><br/> | <span data-ttu-id="01b08-672">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01b08-672">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="01b08-673">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01b08-673">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b08-674">MCI</span><span class="sxs-lookup"><span data-stu-id="01b08-674">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="01b08-675">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="01b08-675">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="01b08-676">capability</span><span class="sxs-lookup"><span data-stu-id="01b08-676">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="01b08-677">catturare</span><span class="sxs-lookup"><span data-stu-id="01b08-677">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="01b08-678">close</span><span class="sxs-lookup"><span data-stu-id="01b08-678">close</span></span>](close.md)
</dt> <dt>

[<span data-ttu-id="01b08-679">tagliare</span><span class="sxs-lookup"><span data-stu-id="01b08-679">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="01b08-680">delete</span><span class="sxs-lookup"><span data-stu-id="01b08-680">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="01b08-681">carico</span><span class="sxs-lookup"><span data-stu-id="01b08-681">load</span></span>](load.md)
</dt> <dt>

[<span data-ttu-id="01b08-682">pause</span><span class="sxs-lookup"><span data-stu-id="01b08-682">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="01b08-683">Incolla</span><span class="sxs-lookup"><span data-stu-id="01b08-683">paste</span></span>](paste.md)
</dt> <dt>

[<span data-ttu-id="01b08-684">record</span><span class="sxs-lookup"><span data-stu-id="01b08-684">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="01b08-685">riserva</span><span class="sxs-lookup"><span data-stu-id="01b08-685">reserve</span></span>](reserve.md)
</dt> <dt>

[<span data-ttu-id="01b08-686">salvataggio</span><span class="sxs-lookup"><span data-stu-id="01b08-686">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="01b08-687">set</span><span class="sxs-lookup"><span data-stu-id="01b08-687">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="01b08-688">SetAudio</span><span class="sxs-lookup"><span data-stu-id="01b08-688">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="01b08-689">video</span><span class="sxs-lookup"><span data-stu-id="01b08-689">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="01b08-690">stop</span><span class="sxs-lookup"><span data-stu-id="01b08-690">stop</span></span>](stop.md)
</dt> <dt>

[<span data-ttu-id="01b08-691">cancella</span><span class="sxs-lookup"><span data-stu-id="01b08-691">undo</span></span>](undo.md)
</dt> </dl>

 

