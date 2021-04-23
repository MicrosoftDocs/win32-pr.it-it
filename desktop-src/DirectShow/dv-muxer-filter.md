---
description: Filtro DV Muxer
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro DV Muxer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908599"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="5ec7b-103">Filtro DV Muxer</span><span class="sxs-lookup"><span data-stu-id="5ec7b-103">DV Muxer Filter</span></span>

<span data-ttu-id="5ec7b-104">Questo filtro combina un flusso video codificato DV (Digital Video) con uno o due flussi audio per produrre un flusso DV interleaved.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="5ec7b-105">Per scrivere il flusso in un file AVI, connettere questo filtro al filtro [Mux AVI](avi-mux-filter.md) e connettere *mux AVI* al filtro [Writer file.](file-writer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="5ec7b-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="5ec7b-106">Per altre informazioni, vedere [Video digitale in DirectShow.](digital-video-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="5ec7b-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



| <span data-ttu-id="5ec7b-107">Label</span><span class="sxs-lookup"><span data-stu-id="5ec7b-107">Label</span></span> | <span data-ttu-id="5ec7b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="5ec7b-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec7b-109">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="5ec7b-109">Filter Interfaces</span></span>                        | <span data-ttu-id="5ec7b-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="5ec7b-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="5ec7b-111">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="5ec7b-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="5ec7b-112">**Video:** MEDIATYPE \_ Video, MEDIASUBTYPE \_ dvsd, FORMAT \_ VideoInfo **Audio:** MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="5ec7b-112">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="5ec7b-113">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="5ec7b-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="5ec7b-114">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5ec7b-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="5ec7b-115">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="5ec7b-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="5ec7b-116">MEDIATYPE \_ Interleaved, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="5ec7b-116">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="5ec7b-117">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="5ec7b-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="5ec7b-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5ec7b-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="5ec7b-119">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="5ec7b-119">Filter CLSID</span></span>                             | <span data-ttu-id="5ec7b-120">CLSID \_ DVMux</span><span class="sxs-lookup"><span data-stu-id="5ec7b-120">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="5ec7b-121">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="5ec7b-121">Property Page CLSID</span></span>                      | <span data-ttu-id="5ec7b-122">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="5ec7b-122">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="5ec7b-123">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="5ec7b-123">Executable</span></span>                               | <span data-ttu-id="5ec7b-124">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="5ec7b-124">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="5ec7b-125">Merito</span><span class="sxs-lookup"><span data-stu-id="5ec7b-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="5ec7b-126">MERITO \_ IMPROBABILE</span><span class="sxs-lookup"><span data-stu-id="5ec7b-126">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="5ec7b-127">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="5ec7b-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="5ec7b-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="5ec7b-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="5ec7b-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ec7b-129">Remarks</span></span>

<span data-ttu-id="5ec7b-130">Il DV Muxer può creare due pin di input audio.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-130">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="5ec7b-131">Supporta i formati audio illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-131">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="5ec7b-132">Pin audio 1</span><span class="sxs-lookup"><span data-stu-id="5ec7b-132">Audio Pin 1</span></span>

<span data-ttu-id="5ec7b-133">Pin audio 2</span><span class="sxs-lookup"><span data-stu-id="5ec7b-133">Audio Pin 2</span></span>

<span data-ttu-id="5ec7b-134">Formato output</span><span class="sxs-lookup"><span data-stu-id="5ec7b-134">Output Format</span></span>

<span data-ttu-id="5ec7b-135">Frequenza di campionamento (kHz)</span><span class="sxs-lookup"><span data-stu-id="5ec7b-135">Sample Rate (kHz)</span></span>

<span data-ttu-id="5ec7b-136">Bit/esempio</span><span class="sxs-lookup"><span data-stu-id="5ec7b-136">Bits/Sample</span></span>

<span data-ttu-id="5ec7b-137">Canali</span><span class="sxs-lookup"><span data-stu-id="5ec7b-137">Channels</span></span>

<span data-ttu-id="5ec7b-138">Frequenza di campionamento</span><span class="sxs-lookup"><span data-stu-id="5ec7b-138">Sample Rate</span></span>

<span data-ttu-id="5ec7b-139">Bit/esempio</span><span class="sxs-lookup"><span data-stu-id="5ec7b-139">Bits/Sample</span></span>

<span data-ttu-id="5ec7b-140">Canali</span><span class="sxs-lookup"><span data-stu-id="5ec7b-140">Channels</span></span>

<span data-ttu-id="5ec7b-141">32</span><span class="sxs-lookup"><span data-stu-id="5ec7b-141">32</span></span>

<span data-ttu-id="5ec7b-142">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-142">16</span></span>

<span data-ttu-id="5ec7b-143">Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-143">Mono</span></span>

<span data-ttu-id="5ec7b-144">Estraneo</span><span class="sxs-lookup"><span data-stu-id="5ec7b-144">Unconnected</span></span>

<span data-ttu-id="5ec7b-145">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="5ec7b-145">SD 2 Channel</span></span>

<span data-ttu-id="5ec7b-146">32</span><span class="sxs-lookup"><span data-stu-id="5ec7b-146">32</span></span>

<span data-ttu-id="5ec7b-147">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-147">16</span></span>

<span data-ttu-id="5ec7b-148">Stereo</span><span class="sxs-lookup"><span data-stu-id="5ec7b-148">Stereo</span></span>

<span data-ttu-id="5ec7b-149">Estraneo</span><span class="sxs-lookup"><span data-stu-id="5ec7b-149">Unconnected</span></span>

<span data-ttu-id="5ec7b-150">Canale SD 4</span><span class="sxs-lookup"><span data-stu-id="5ec7b-150">SD 4 Channel</span></span>

<span data-ttu-id="5ec7b-151">44.1 o 48</span><span class="sxs-lookup"><span data-stu-id="5ec7b-151">44.1 or 48</span></span>

<span data-ttu-id="5ec7b-152">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-152">16</span></span>

<span data-ttu-id="5ec7b-153">Stereo o Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-153">Stereo or Mono</span></span>

<span data-ttu-id="5ec7b-154">Estraneo</span><span class="sxs-lookup"><span data-stu-id="5ec7b-154">Unconnected</span></span>

<span data-ttu-id="5ec7b-155">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="5ec7b-155">SD 2 Channel</span></span>

<span data-ttu-id="5ec7b-156">Estraneo</span><span class="sxs-lookup"><span data-stu-id="5ec7b-156">Unconnected</span></span>

<span data-ttu-id="5ec7b-157">32</span><span class="sxs-lookup"><span data-stu-id="5ec7b-157">32</span></span>

<span data-ttu-id="5ec7b-158">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-158">16</span></span>

<span data-ttu-id="5ec7b-159">Stereo o Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-159">Stereo or Mono</span></span>

<span data-ttu-id="5ec7b-160">Non consentita</span><span class="sxs-lookup"><span data-stu-id="5ec7b-160">Disallowed</span></span>

<span data-ttu-id="5ec7b-161">Estraneo</span><span class="sxs-lookup"><span data-stu-id="5ec7b-161">Unconnected</span></span>

<span data-ttu-id="5ec7b-162">44.1 o 48</span><span class="sxs-lookup"><span data-stu-id="5ec7b-162">44.1 or 48</span></span>

<span data-ttu-id="5ec7b-163">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-163">16</span></span>

<span data-ttu-id="5ec7b-164">Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-164">Mono</span></span>

<span data-ttu-id="5ec7b-165">Non consentita</span><span class="sxs-lookup"><span data-stu-id="5ec7b-165">Disallowed</span></span>

<span data-ttu-id="5ec7b-166">Estraneo</span><span class="sxs-lookup"><span data-stu-id="5ec7b-166">Unconnected</span></span>

<span data-ttu-id="5ec7b-167">44.1 o 48</span><span class="sxs-lookup"><span data-stu-id="5ec7b-167">44.1 or 48</span></span>

<span data-ttu-id="5ec7b-168">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-168">16</span></span>

<span data-ttu-id="5ec7b-169">Stereo</span><span class="sxs-lookup"><span data-stu-id="5ec7b-169">Stereo</span></span>

<span data-ttu-id="5ec7b-170">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="5ec7b-170">SD 2 Channel</span></span>

<span data-ttu-id="5ec7b-171">32</span><span class="sxs-lookup"><span data-stu-id="5ec7b-171">32</span></span>

<span data-ttu-id="5ec7b-172">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-172">16</span></span>

<span data-ttu-id="5ec7b-173">Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-173">Mono</span></span>

<span data-ttu-id="5ec7b-174">32</span><span class="sxs-lookup"><span data-stu-id="5ec7b-174">32</span></span>

<span data-ttu-id="5ec7b-175">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-175">16</span></span>

<span data-ttu-id="5ec7b-176">Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-176">Mono</span></span>

<span data-ttu-id="5ec7b-177">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="5ec7b-177">SD 2 Channel</span></span>

<span data-ttu-id="5ec7b-178">32</span><span class="sxs-lookup"><span data-stu-id="5ec7b-178">32</span></span>

<span data-ttu-id="5ec7b-179">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-179">16</span></span>

<span data-ttu-id="5ec7b-180">Stereo o Mono\*</span><span class="sxs-lookup"><span data-stu-id="5ec7b-180">Stereo or Mono\*</span></span>

<span data-ttu-id="5ec7b-181">32</span><span class="sxs-lookup"><span data-stu-id="5ec7b-181">32</span></span>

<span data-ttu-id="5ec7b-182">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-182">16</span></span>

<span data-ttu-id="5ec7b-183">Stereo o Mono\*</span><span class="sxs-lookup"><span data-stu-id="5ec7b-183">Stereo or Mono\*</span></span>

<span data-ttu-id="5ec7b-184">Canale SD 4</span><span class="sxs-lookup"><span data-stu-id="5ec7b-184">SD 4 Channel</span></span>

<span data-ttu-id="5ec7b-185">44.1</span><span class="sxs-lookup"><span data-stu-id="5ec7b-185">44.1</span></span>

<span data-ttu-id="5ec7b-186">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-186">16</span></span>

<span data-ttu-id="5ec7b-187">Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-187">Mono</span></span>

<span data-ttu-id="5ec7b-188">44.1</span><span class="sxs-lookup"><span data-stu-id="5ec7b-188">44.1</span></span>

<span data-ttu-id="5ec7b-189">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-189">16</span></span>

<span data-ttu-id="5ec7b-190">Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-190">Mono</span></span>

<span data-ttu-id="5ec7b-191">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="5ec7b-191">SD 2 Channel</span></span>

<span data-ttu-id="5ec7b-192">48</span><span class="sxs-lookup"><span data-stu-id="5ec7b-192">48</span></span>

<span data-ttu-id="5ec7b-193">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-193">16</span></span>

<span data-ttu-id="5ec7b-194">Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-194">Mono</span></span>

<span data-ttu-id="5ec7b-195">48</span><span class="sxs-lookup"><span data-stu-id="5ec7b-195">48</span></span>

<span data-ttu-id="5ec7b-196">16</span><span class="sxs-lookup"><span data-stu-id="5ec7b-196">16</span></span>

<span data-ttu-id="5ec7b-197">Mono</span><span class="sxs-lookup"><span data-stu-id="5ec7b-197">Mono</span></span>

<span data-ttu-id="5ec7b-198">Canale SD 2</span><span class="sxs-lookup"><span data-stu-id="5ec7b-198">SD 2 Channel</span></span>

<span data-ttu-id="5ec7b-199">\* Se almeno un pin di input è stereo.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-199">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="5ec7b-200">Ai fini di questa tabella, il pin audio 1 viene definito come primo pin di input connesso a un'origine audio e il pin audio 2 viene definito come secondo pin di input connesso a un'origine audio.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-200">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="5ec7b-201">Una volta connesso un pin audio, questo schema di numerazione rimane attivo a meno che entrambi i pin audio non siano disconnessi.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-201">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="5ec7b-202">Ad esempio, se si connettono entrambi i pin audio e quindi si disconnette il pin audio 1, il pin rimanente viene comunque considerato pin 2.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-202">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="5ec7b-203">L'audio fornito al pin 1 viene registrato nel primo blocco audio dei fotogrammi DV (CH1) e l'audio fornito al pin 2 viene registrato nel secondo blocco audio (CH2).</span><span class="sxs-lookup"><span data-stu-id="5ec7b-203">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="5ec7b-204">Eccezione: se il filtro ha un singolo input stereo a 44,1 kHz o 48 kHz, il canale audio sinistro viene registrato nel primo blocco audio e il canale audio destro viene registrato nel secondo blocco audio.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-204">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="5ec7b-205">Per l'output SD a 4 canali: se l'input è stereo, la traccia sinistra viene registrata in CHa o CHc e la traccia destra viene registrata in CHb o CHd.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-205">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="5ec7b-206">Se l'input è mono, l'audio viene registrato in CHa o CHc e CHb e CHd sono invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-206">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="5ec7b-207">Connettendo e disconnettendo il pin audio 1, è possibile raggiungere un formato non consentito.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-207">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="5ec7b-208">In tal caso, il metodo [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) del filtro restituisce VFW \_ E NOT \_ \_ CONNECTED.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-208">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="5ec7b-209">Questa limitazione impedisce una situazione in cui il primo blocco audio non ha audio, ma il secondo blocco audio dispone di audio.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-209">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="5ec7b-210">Il secondo blocco deve avere audio solo se anche il primo blocco dispone di audio.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-210">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="5ec7b-211">Il DV Muxer non consente input audio con frequenze di campionamento diverse.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-211">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="5ec7b-212">Tuttavia, i metodi di creazione di grafi, ad esempio [**IGraphBuilder::Connect,**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) in genere aggiungono il filtro [wrapper ACM,](acm-wrapper-filter.md) che converte il secondo flusso audio in modo che corrisponda alla frequenza di campionamento del primo flusso.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-212">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="5ec7b-213">Se l'input audio è di 48 kHz o 32 kHz, l'output audio viene bloccato.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-213">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="5ec7b-214">Non è possibile bloccare l'audio a 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-214">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="5ec7b-215">Se non sono connessi pin audio, l'output contiene i dati audio dai fotogrammi DV in ingresso.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-215">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="5ec7b-216">Potrebbe trattarsi di un silenzio o di dati audio validi.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-216">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ec7b-217">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ec7b-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ec7b-218">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="5ec7b-218">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="5ec7b-219">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="5ec7b-219">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



