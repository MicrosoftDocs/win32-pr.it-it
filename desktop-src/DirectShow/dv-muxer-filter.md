---
description: Filtro muxer DV
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro muxer DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747399"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="a9125-103">Filtro muxer DV</span><span class="sxs-lookup"><span data-stu-id="a9125-103">DV Muxer Filter</span></span>

<span data-ttu-id="a9125-104">Questo filtro combina un flusso video codificato Digital video (DV) con uno o due flussi audio per produrre un flusso DV con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="a9125-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="a9125-105">Per scrivere il flusso in un file AVI, connettere il filtro al filtro [Mux AVI](avi-mux-filter.md) e connettere il *Mux AVI* al filtro del [writer di file](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a9125-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="a9125-106">Per altre informazioni, vedere [video digitale in DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="a9125-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9125-107">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="a9125-107">Filter Interfaces</span></span>                        | <span data-ttu-id="a9125-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="a9125-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="a9125-109">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="a9125-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="a9125-110">**Video**: MEDIATYPE \_ video, MEDIASUBTYPE \_ DVSD, Format \_ videoinfo **audio**: MEDIATYPE \_ audio, MEDIASUBTYPE \_ PCM, Format \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="a9125-110">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="a9125-111">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="a9125-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="a9125-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a9125-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="a9125-113">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="a9125-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="a9125-114">MEDIATYPE con \_ interfoliazione, MEDIASUBTYPE \_ DVSD, formato \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="a9125-114">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="a9125-115">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="a9125-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a9125-116">[**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a9125-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="a9125-117">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="a9125-117">Filter CLSID</span></span>                             | <span data-ttu-id="a9125-118">\_DVMUX CLSID</span><span class="sxs-lookup"><span data-stu-id="a9125-118">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="a9125-119">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="a9125-119">Property Page CLSID</span></span>                      | <span data-ttu-id="a9125-120">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="a9125-120">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="a9125-121">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="a9125-121">Executable</span></span>                               | <span data-ttu-id="a9125-122">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="a9125-122">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="a9125-123">Merito</span><span class="sxs-lookup"><span data-stu-id="a9125-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="a9125-124">VALORE \_ improbabile</span><span class="sxs-lookup"><span data-stu-id="a9125-124">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="a9125-125">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="a9125-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a9125-126">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="a9125-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="a9125-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9125-127">Remarks</span></span>

<span data-ttu-id="a9125-128">Il muxer DV può creare due pin di input audio.</span><span class="sxs-lookup"><span data-stu-id="a9125-128">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="a9125-129">Supporta i formati audio indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a9125-129">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="a9125-130">Pin audio 1</span><span class="sxs-lookup"><span data-stu-id="a9125-130">Audio Pin 1</span></span>

<span data-ttu-id="a9125-131">Pin audio 2</span><span class="sxs-lookup"><span data-stu-id="a9125-131">Audio Pin 2</span></span>

<span data-ttu-id="a9125-132">Formato output</span><span class="sxs-lookup"><span data-stu-id="a9125-132">Output Format</span></span>

<span data-ttu-id="a9125-133">Frequenza di campionamento (kHz)</span><span class="sxs-lookup"><span data-stu-id="a9125-133">Sample Rate (kHz)</span></span>

<span data-ttu-id="a9125-134">BITS/esempio</span><span class="sxs-lookup"><span data-stu-id="a9125-134">Bits/Sample</span></span>

<span data-ttu-id="a9125-135">Canali</span><span class="sxs-lookup"><span data-stu-id="a9125-135">Channels</span></span>

<span data-ttu-id="a9125-136">Frequenza di campionamento</span><span class="sxs-lookup"><span data-stu-id="a9125-136">Sample Rate</span></span>

<span data-ttu-id="a9125-137">BITS/esempio</span><span class="sxs-lookup"><span data-stu-id="a9125-137">Bits/Sample</span></span>

<span data-ttu-id="a9125-138">Canali</span><span class="sxs-lookup"><span data-stu-id="a9125-138">Channels</span></span>

<span data-ttu-id="a9125-139">32</span><span class="sxs-lookup"><span data-stu-id="a9125-139">32</span></span>

<span data-ttu-id="a9125-140">16</span><span class="sxs-lookup"><span data-stu-id="a9125-140">16</span></span>

<span data-ttu-id="a9125-141">Mono</span><span class="sxs-lookup"><span data-stu-id="a9125-141">Mono</span></span>

<span data-ttu-id="a9125-142">Non connesso</span><span class="sxs-lookup"><span data-stu-id="a9125-142">Unconnected</span></span>

<span data-ttu-id="a9125-143">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="a9125-143">SD 2 Channel</span></span>

<span data-ttu-id="a9125-144">32</span><span class="sxs-lookup"><span data-stu-id="a9125-144">32</span></span>

<span data-ttu-id="a9125-145">16</span><span class="sxs-lookup"><span data-stu-id="a9125-145">16</span></span>

<span data-ttu-id="a9125-146">Stereo</span><span class="sxs-lookup"><span data-stu-id="a9125-146">Stereo</span></span>

<span data-ttu-id="a9125-147">Non connesso</span><span class="sxs-lookup"><span data-stu-id="a9125-147">Unconnected</span></span>

<span data-ttu-id="a9125-148">Canale SD 4</span><span class="sxs-lookup"><span data-stu-id="a9125-148">SD 4 Channel</span></span>

<span data-ttu-id="a9125-149">44,1 o 48</span><span class="sxs-lookup"><span data-stu-id="a9125-149">44.1 or 48</span></span>

<span data-ttu-id="a9125-150">16</span><span class="sxs-lookup"><span data-stu-id="a9125-150">16</span></span>

<span data-ttu-id="a9125-151">Stereo o mono</span><span class="sxs-lookup"><span data-stu-id="a9125-151">Stereo or Mono</span></span>

<span data-ttu-id="a9125-152">Non connesso</span><span class="sxs-lookup"><span data-stu-id="a9125-152">Unconnected</span></span>

<span data-ttu-id="a9125-153">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="a9125-153">SD 2 Channel</span></span>

<span data-ttu-id="a9125-154">Non connesso</span><span class="sxs-lookup"><span data-stu-id="a9125-154">Unconnected</span></span>

<span data-ttu-id="a9125-155">32</span><span class="sxs-lookup"><span data-stu-id="a9125-155">32</span></span>

<span data-ttu-id="a9125-156">16</span><span class="sxs-lookup"><span data-stu-id="a9125-156">16</span></span>

<span data-ttu-id="a9125-157">Stereo o mono</span><span class="sxs-lookup"><span data-stu-id="a9125-157">Stereo or Mono</span></span>

<span data-ttu-id="a9125-158">Non consentita</span><span class="sxs-lookup"><span data-stu-id="a9125-158">Disallowed</span></span>

<span data-ttu-id="a9125-159">Non connesso</span><span class="sxs-lookup"><span data-stu-id="a9125-159">Unconnected</span></span>

<span data-ttu-id="a9125-160">44,1 o 48</span><span class="sxs-lookup"><span data-stu-id="a9125-160">44.1 or 48</span></span>

<span data-ttu-id="a9125-161">16</span><span class="sxs-lookup"><span data-stu-id="a9125-161">16</span></span>

<span data-ttu-id="a9125-162">Mono</span><span class="sxs-lookup"><span data-stu-id="a9125-162">Mono</span></span>

<span data-ttu-id="a9125-163">Non consentita</span><span class="sxs-lookup"><span data-stu-id="a9125-163">Disallowed</span></span>

<span data-ttu-id="a9125-164">Non connesso</span><span class="sxs-lookup"><span data-stu-id="a9125-164">Unconnected</span></span>

<span data-ttu-id="a9125-165">44,1 o 48</span><span class="sxs-lookup"><span data-stu-id="a9125-165">44.1 or 48</span></span>

<span data-ttu-id="a9125-166">16</span><span class="sxs-lookup"><span data-stu-id="a9125-166">16</span></span>

<span data-ttu-id="a9125-167">Stereo</span><span class="sxs-lookup"><span data-stu-id="a9125-167">Stereo</span></span>

<span data-ttu-id="a9125-168">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="a9125-168">SD 2 Channel</span></span>

<span data-ttu-id="a9125-169">32</span><span class="sxs-lookup"><span data-stu-id="a9125-169">32</span></span>

<span data-ttu-id="a9125-170">16</span><span class="sxs-lookup"><span data-stu-id="a9125-170">16</span></span>

<span data-ttu-id="a9125-171">Mono</span><span class="sxs-lookup"><span data-stu-id="a9125-171">Mono</span></span>

<span data-ttu-id="a9125-172">32</span><span class="sxs-lookup"><span data-stu-id="a9125-172">32</span></span>

<span data-ttu-id="a9125-173">16</span><span class="sxs-lookup"><span data-stu-id="a9125-173">16</span></span>

<span data-ttu-id="a9125-174">Mono</span><span class="sxs-lookup"><span data-stu-id="a9125-174">Mono</span></span>

<span data-ttu-id="a9125-175">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="a9125-175">SD 2 Channel</span></span>

<span data-ttu-id="a9125-176">32</span><span class="sxs-lookup"><span data-stu-id="a9125-176">32</span></span>

<span data-ttu-id="a9125-177">16</span><span class="sxs-lookup"><span data-stu-id="a9125-177">16</span></span>

<span data-ttu-id="a9125-178">Stereo o mono\*</span><span class="sxs-lookup"><span data-stu-id="a9125-178">Stereo or Mono\*</span></span>

<span data-ttu-id="a9125-179">32</span><span class="sxs-lookup"><span data-stu-id="a9125-179">32</span></span>

<span data-ttu-id="a9125-180">16</span><span class="sxs-lookup"><span data-stu-id="a9125-180">16</span></span>

<span data-ttu-id="a9125-181">Stereo o mono\*</span><span class="sxs-lookup"><span data-stu-id="a9125-181">Stereo or Mono\*</span></span>

<span data-ttu-id="a9125-182">Canale SD 4</span><span class="sxs-lookup"><span data-stu-id="a9125-182">SD 4 Channel</span></span>

<span data-ttu-id="a9125-183">44,1</span><span class="sxs-lookup"><span data-stu-id="a9125-183">44.1</span></span>

<span data-ttu-id="a9125-184">16</span><span class="sxs-lookup"><span data-stu-id="a9125-184">16</span></span>

<span data-ttu-id="a9125-185">Mono</span><span class="sxs-lookup"><span data-stu-id="a9125-185">Mono</span></span>

<span data-ttu-id="a9125-186">44,1</span><span class="sxs-lookup"><span data-stu-id="a9125-186">44.1</span></span>

<span data-ttu-id="a9125-187">16</span><span class="sxs-lookup"><span data-stu-id="a9125-187">16</span></span>

<span data-ttu-id="a9125-188">Mono</span><span class="sxs-lookup"><span data-stu-id="a9125-188">Mono</span></span>

<span data-ttu-id="a9125-189">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="a9125-189">SD 2 Channel</span></span>

<span data-ttu-id="a9125-190">48</span><span class="sxs-lookup"><span data-stu-id="a9125-190">48</span></span>

<span data-ttu-id="a9125-191">16</span><span class="sxs-lookup"><span data-stu-id="a9125-191">16</span></span>

<span data-ttu-id="a9125-192">Mono</span><span class="sxs-lookup"><span data-stu-id="a9125-192">Mono</span></span>

<span data-ttu-id="a9125-193">48</span><span class="sxs-lookup"><span data-stu-id="a9125-193">48</span></span>

<span data-ttu-id="a9125-194">16</span><span class="sxs-lookup"><span data-stu-id="a9125-194">16</span></span>

<span data-ttu-id="a9125-195">Mono</span><span class="sxs-lookup"><span data-stu-id="a9125-195">Mono</span></span>

<span data-ttu-id="a9125-196">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="a9125-196">SD 2 Channel</span></span>

<span data-ttu-id="a9125-197">\* Se almeno un pin di input è stereo.</span><span class="sxs-lookup"><span data-stu-id="a9125-197">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="a9125-198">Ai fini di questa tabella, il pin audio 1 viene definito come primo pin di input connesso a un'origine audio e il pin audio 2 viene definito come il secondo pin di input connesso a un'origine audio.</span><span class="sxs-lookup"><span data-stu-id="a9125-198">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="a9125-199">Una volta connesso un pin audio, questo schema di numerazione rimane attivo, a meno che entrambi i pin audio non siano disconnessi.</span><span class="sxs-lookup"><span data-stu-id="a9125-199">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="a9125-200">Ad esempio, se si connettono entrambi i pin audio e si disconnette il pin audio 1, il pin rimanente verrà ancora considerato pin 2.</span><span class="sxs-lookup"><span data-stu-id="a9125-200">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="a9125-201">L'audio fornito al pin 1 viene registrato nel primo blocco audio dei frame DV (CH1) e l'audio fornito al pin 2 viene registrato nel secondo blocco audio (CH2).</span><span class="sxs-lookup"><span data-stu-id="a9125-201">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="a9125-202">Eccezione: se il filtro ha un singolo input stereo a 44,1 kHz o 48 kHz, il canale audio sinistro viene registrato nel primo blocco audio e il canale audio destro viene registrato nel secondo blocco audio.</span><span class="sxs-lookup"><span data-stu-id="a9125-202">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="a9125-203">Per l'output del canale SD 4: se l'input è stereo, il tracciato a sinistra viene registrato in CHa o CHc e la traccia corretta viene registrata in CHb o CHd.</span><span class="sxs-lookup"><span data-stu-id="a9125-203">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="a9125-204">Se l'input è mono, l'audio viene registrato in CHa o CHc e CHb e CHd sono invisibili.</span><span class="sxs-lookup"><span data-stu-id="a9125-204">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="a9125-205">Con la connessione e la disconnessione del pin audio 1, è possibile raggiungere un formato non consentito.</span><span class="sxs-lookup"><span data-stu-id="a9125-205">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="a9125-206">In tal caso, il metodo [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) del filtro restituisce VFW \_ E \_ non \_ connesso.</span><span class="sxs-lookup"><span data-stu-id="a9125-206">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="a9125-207">Questa limitazione impedisce una situazione in cui il primo blocco audio non dispone di audio, ma il secondo blocco audio dispone di audio.</span><span class="sxs-lookup"><span data-stu-id="a9125-207">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="a9125-208">Il secondo blocco deve avere audio solo se il primo blocco include anche audio.</span><span class="sxs-lookup"><span data-stu-id="a9125-208">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="a9125-209">Il muxer DV non consente input audio con frequenze di campionamento diverse.</span><span class="sxs-lookup"><span data-stu-id="a9125-209">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="a9125-210">Tuttavia, i metodi per la creazione di grafici, ad esempio [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , aggiungono in genere il filtro del [wrapper ACM](acm-wrapper-filter.md) , che converte il secondo flusso audio in modo che corrisponda alla frequenza di campionamento del primo flusso.</span><span class="sxs-lookup"><span data-stu-id="a9125-210">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="a9125-211">Se l'input audio è 48 kHz o 32 kHz, l'output audio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="a9125-211">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="a9125-212">Non è possibile bloccare l'audio a 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="a9125-212">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="a9125-213">Se non è connesso alcun pin audio, l'output contiene i dati audio dei frame DV in arrivo.</span><span class="sxs-lookup"><span data-stu-id="a9125-213">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="a9125-214">Potrebbe trattarsi di un silenzio o di dati audio validi.</span><span class="sxs-lookup"><span data-stu-id="a9125-214">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9125-215">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9125-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9125-216">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="a9125-216">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="a9125-217">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a9125-217">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



