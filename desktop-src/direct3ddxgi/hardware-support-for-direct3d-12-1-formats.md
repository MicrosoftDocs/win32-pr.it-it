---
description: Questa sezione specifica i formati ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware del livello di funzionalità Direct3D 12,1.
ms.assetid: 0DC50FF3-3193-4F3B-9976-EE504C6FCC87
title: Supporto del formato per l'hardware a livello di funzionalità 12.1 di Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d20b00a2cfb5b0343a2ebb1a56a1253ddd1966
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745375"
---
# <a name="format-support-for-direct3d-feature-level-121-hardware"></a><span data-ttu-id="f81ea-103">Supporto del formato per l'hardware a livello di funzionalità 12.1 di Direct3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-103">Format support for Direct3D Feature Level 12.1 hardware</span></span>

<span data-ttu-id="f81ea-104">Questa sezione specifica i formati ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware a livello di funzionalità Direct3D 12,1.</span><span class="sxs-lookup"><span data-stu-id="f81ea-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 12.1 hardware.</span></span>

<span data-ttu-id="f81ea-105">La tabella riepiloga il supporto della funzionalità, usando la chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="f81ea-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="f81ea-106">Simbolo</span><span class="sxs-lookup"><span data-stu-id="f81ea-106">Symbol</span></span>                            | <span data-ttu-id="f81ea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f81ea-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="f81ea-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="f81ea-108">_ *-*\*</span></span>                             | <span data-ttu-id="f81ea-109">Non consentito o non disponibile.</span><span class="sxs-lookup"><span data-stu-id="f81ea-109">Disallowed or not available.</span></span>                                                  |
| ![necessario](images/letter-r.jpg)  | <span data-ttu-id="f81ea-111">Il supporto hardware è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f81ea-111">Hardware support is required.</span></span>                                                 |
| ![facoltative](images/letter-o.jpg)  | <span data-ttu-id="f81ea-113">Supporto hardware facoltativo. il formato potrebbe essere accelerato o meno.</span><span class="sxs-lookup"><span data-stu-id="f81ea-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dipendenti](images/letter-d.jpg) | <span data-ttu-id="f81ea-115">Obbligatorio se è supportata la funzionalità facoltativa correlata.</span><span class="sxs-lookup"><span data-stu-id="f81ea-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="f81ea-116">Questo argomento contiene una sezione per formato.</span><span class="sxs-lookup"><span data-stu-id="f81ea-116">This topic contains a section per format.</span></span> <span data-ttu-id="f81ea-117">Una *destinazione* del formato (le tabelle contengono una riga per destinazione) può essere un tipo di risorsa, una funzione intrinseca HLSL o una particolare funzionalità che dipende da un particolare formato.</span><span class="sxs-lookup"><span data-stu-id="f81ea-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="f81ea-118">Per verificare a livello di codice il supporto del formato in D3D11 e D3D12, vedere [controllo della funzionalità hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="f81ea-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="f81ea-119">Il numero di formati è prevalentemente, ma non tutti, in ordine numerico crescente &mdash; alcuni sono fuori dall'ordine numerico ed elencati insieme ad altri formati pertinenti.</span><span class="sxs-lookup"><span data-stu-id="f81ea-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="f81ea-120">Si noti anche che il *tipo* in un nome di formato può indicare *parzialmente* tipizzato e non esclusivamente senza tipo (fare riferimento alla sezione [Note sul formato](#format-notes) alla fine dell'argomento).</span><span class="sxs-lookup"><span data-stu-id="f81ea-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="f81ea-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="f81ea-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="f81ea-122">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-122">Target</span></span> | <span data-ttu-id="f81ea-123">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-123">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-124">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-125">0</span><span class="sxs-lookup"><span data-stu-id="f81ea-125">0</span></span> |
| <span data-ttu-id="f81ea-126">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-126">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-128">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-130">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-131">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-132">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-133">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-134">Texture2D</span></span> | \- |
| <span data-ttu-id="f81ea-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-135">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-136">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-137">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-137">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-138">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-139">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-139">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-140">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-140">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-141">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-142">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-142">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-143">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-144">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-144">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-147">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-148">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-149">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-150">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-150">Structured UAV and SRV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-152">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-152">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-153">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-153">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-154">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-154">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-155">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-155">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-156">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-156">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-157">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-157">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-158">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-158">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-159">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-159">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-160">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-160">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-161">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-161">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-163">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-163">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-164">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-164">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-165">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-165">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-166">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-166">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-167">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-167">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-168">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-168">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-169">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-169">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-170">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-171">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-172">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-173">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-173">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-174">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-174">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-175">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-175">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="f81ea-177"><sup>Pc</sup> DXGI_FORMAT_R32G32B32A32_TYPELESS (1)</span><span class="sxs-lookup"><span data-stu-id="f81ea-177">DXGI_FORMAT_R32G32B32A32_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="f81ea-178">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-178">Target</span></span> | <span data-ttu-id="f81ea-179">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-179">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-180">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-180">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-181">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-181">128</span></span> |
| <span data-ttu-id="f81ea-182">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-182">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-184">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-184">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-185">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-185">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-186">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-186">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-187">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-187">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-188">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-190">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-192">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-194">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-196">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-196">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-197">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-197">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-198">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-198">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-199">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-199">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-200">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-200">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-201">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-201">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-202">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-202">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-204">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-204">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-205">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-206">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-207">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-208">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-209">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-210">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-211">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-211">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-212">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-213">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-214">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-215">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-217">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-218">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-219">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-220">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-220">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-222">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-223">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-224">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-225">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-226">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-226">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-227">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-228">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-228">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-230">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-231">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-232">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-233">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-233">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-235">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-235">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-236">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-236">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="f81ea-238">DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="f81ea-238">DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="f81ea-239">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-239">Target</span></span> | <span data-ttu-id="f81ea-240">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-240">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-241">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-241">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-242">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-242">128</span></span> |
| <span data-ttu-id="f81ea-243">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-243">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-245">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-245">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-247">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-247">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-249">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-250">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-250">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-252">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-252">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-254">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-256">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-256">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-258">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-258">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-260">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-260">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-262">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-262">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-264">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-264">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-265">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-265">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-266">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-266">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-268">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-268">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-269">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-269">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-271">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-271">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-273">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-273">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-275">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-275">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-277">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-277">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-278">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-278">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-279">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-279">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-280">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-280">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-281">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-281">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-283">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-283">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-285">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-285">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-287">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-288">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-289">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-289">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-290">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-291">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-291">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-292">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-292">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-293">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-293">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-295">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-295">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-297">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-297">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-299">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-299">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-301">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-301">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-303">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-303">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-305">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-306">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-306">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-308">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-309">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-310">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-311">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-311">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-313">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-313">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-314">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-314">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="f81ea-316">DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="f81ea-316">DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="f81ea-317">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-317">Target</span></span> | <span data-ttu-id="f81ea-318">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-318">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-319">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-320">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-320">128</span></span> |
| <span data-ttu-id="f81ea-321">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-321">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-323">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-323">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-325">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-325">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-327">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-328">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-328">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-330">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-332">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-332">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-334">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-334">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-336">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-338">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-338">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-340">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-340">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-341">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-341">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-342">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-342">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-343">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-343">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-344">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-344">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-345">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-345">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-347">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-347">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-348">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-348">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-350">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-351">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-351">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-353">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-353">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-354">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-354">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-355">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-355">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-356">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-356">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-358">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-358">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-360">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-360">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-362">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-363">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-364">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-365">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-366">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-366">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-367">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-367">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-368">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-368">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-370">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-370">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-372">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-372">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-374">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-374">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-376">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-377">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-377">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-379">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-380">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-380">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-382">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-382">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-383">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-383">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-384">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-384">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-385">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-385">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-387">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-387">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-388">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-388">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="f81ea-390">DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="f81ea-390">DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="f81ea-391">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-391">Target</span></span> | <span data-ttu-id="f81ea-392">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-392">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-393">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-394">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-394">128</span></span> |
| <span data-ttu-id="f81ea-395">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-395">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-397">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-397">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-399">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-399">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-401">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-402">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-402">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-404">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-404">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-406">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-406">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-408">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-408">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-410">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-412">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-412">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-414">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-414">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-415">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-415">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-416">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-416">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-417">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-417">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-418">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-418">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-419">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-419">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-421">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-421">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-422">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-424">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-424">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-425">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-425">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-426">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-426">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-427">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-427">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-428">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-428">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-429">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-429">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-431">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-431">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-433">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-433">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-435">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-435">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-436">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-436">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-437">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-437">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-438">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-438">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-439">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-439">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-440">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-440">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-441">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-441">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-443">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-443">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-445">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-445">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-447">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-447">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-449">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-449">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-450">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-450">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-452">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-452">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-453">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-453">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-455">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-455">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-456">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-456">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-457">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-457">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-458">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-458">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-460">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-460">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-461">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-461">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="f81ea-463"><sup>Pc</sup> DXGI_FORMAT_R32G32B32_TYPELESS (5)</span><span class="sxs-lookup"><span data-stu-id="f81ea-463">DXGI_FORMAT_R32G32B32_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="f81ea-464">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-464">Target</span></span> | <span data-ttu-id="f81ea-465">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-465">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-466">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-466">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-467">96</span><span class="sxs-lookup"><span data-stu-id="f81ea-467">96</span></span> |
| <span data-ttu-id="f81ea-468">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-468">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-470">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-470">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-471">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-471">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-472">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-472">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-473">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-473">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-474">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-474">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-476">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-476">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-478">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-478">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-480">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-480">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-482">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-482">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-483">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-484">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-484">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-485">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-485">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-486">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-486">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-487">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-487">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-488">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-488">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-490">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-490">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-491">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-492">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-492">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-493">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-493">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-494">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-494">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-495">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-495">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-496">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-496">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-497">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-497">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-498">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-498">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-499">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-499">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-500">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-501">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-502">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-503">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-504">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-505">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-506">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-506">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-508">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-508">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-509">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-509">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-510">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-510">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-511">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-511">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-512">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-512">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-513">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-513">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-514">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-514">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-516">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-516">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-517">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-517">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-518">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-518">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-519">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-519">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-520">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-520">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-521">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-521">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="f81ea-522">DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="f81ea-522">DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="f81ea-523">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-523">Target</span></span> | <span data-ttu-id="f81ea-524">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-524">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-525">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-525">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-526">96</span><span class="sxs-lookup"><span data-stu-id="f81ea-526">96</span></span> |
| <span data-ttu-id="f81ea-527">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-527">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-529">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-529">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-531">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-531">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-533">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-533">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-534">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-534">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-536">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-538">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-540">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-542">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-544">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-544">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-546">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-546">Shader sample (any filter)</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-548">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-548">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-549">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-549">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-550">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-550">Shader gather4</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-552">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-552">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-553">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-553">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-555">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-555">Mipmap Auto- Generation</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-557">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-557">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-559">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-559">Blendable RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="f81ea-561">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-562">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-563">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-564">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-565">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-565">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-566">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-567">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-568">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-569">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-570">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-571">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-572">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-573">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-574">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-574">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-576">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-576">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="f81ea-578">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-578">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="f81ea-580">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-580">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-582">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-582">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-584">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-584">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-586">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-586">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-587">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-587">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-589">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-590">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-591">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-592">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-593">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-593">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-594">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="f81ea-595">DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="f81ea-595">DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="f81ea-596">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-596">Target</span></span> | <span data-ttu-id="f81ea-597">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-597">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-598">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-599">96</span><span class="sxs-lookup"><span data-stu-id="f81ea-599">96</span></span> |
| <span data-ttu-id="f81ea-600">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-600">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-602">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-602">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-604">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-604">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-606">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-606">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-607">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-607">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-609">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-609">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-611">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-613">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-613">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-615">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-615">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-617">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-617">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-619">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-620">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-620">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-621">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-621">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-622">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-622">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-623">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-623">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-624">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-624">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-626">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-626">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-627">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-627">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-629">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-629">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-630">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-630">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-632">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-633">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-634">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-635">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-635">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-636">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-637">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-638">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-639">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-640">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-640">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-641">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-642">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-642">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-643">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-643">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-644">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-644">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-646">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-646">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="f81ea-648">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-648">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="f81ea-650">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-650">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-652">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-653">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-653">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-655">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-656">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-656">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-658">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-659">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-660">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-661">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-661">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-662">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-662">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-663">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="f81ea-664">DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="f81ea-664">DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="f81ea-665">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-665">Target</span></span> | <span data-ttu-id="f81ea-666">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-666">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-667">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-668">96</span><span class="sxs-lookup"><span data-stu-id="f81ea-668">96</span></span> |
| <span data-ttu-id="f81ea-669">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-669">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-671">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-671">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-673">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-673">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-675">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-675">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-676">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-676">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-678">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-678">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-680">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-680">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-682">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-682">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-684">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-686">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-686">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-688">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-688">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-689">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-689">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-690">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-690">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-691">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-691">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-692">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-692">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-693">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-693">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-695">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-695">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-696">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-696">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-698">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-698">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-699">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-699">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-700">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-700">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-701">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-701">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-702">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-702">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-703">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-703">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-704">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-704">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-705">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-705">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-706">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-706">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-707">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-707">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-708">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-708">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-709">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-709">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-710">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-710">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-711">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-711">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-712">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-712">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-714">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-714">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="f81ea-716">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-716">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="f81ea-718">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-718">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-720">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-720">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-721">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-721">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-723">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-723">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-724">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-724">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-726">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-726">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-727">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-727">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-728">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-728">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-729">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-729">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-730">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-730">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-731">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-731">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="f81ea-732"><sup>Pc</sup> DXGI_FORMAT_R16G16B16A16_TYPELESS (9)</span><span class="sxs-lookup"><span data-stu-id="f81ea-732">DXGI_FORMAT_R16G16B16A16_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="f81ea-733">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-733">Target</span></span> | <span data-ttu-id="f81ea-734">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-734">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-735">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-735">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-736">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-736">64</span></span> |
| <span data-ttu-id="f81ea-737">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-737">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-739">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-740">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-741">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-742">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-743">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-745">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-745">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-747">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-747">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-749">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-749">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-751">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-751">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-752">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-752">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-753">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-753">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-754">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-754">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-755">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-755">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-756">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-756">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-757">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-757">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-759">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-759">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-760">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-760">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-761">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-761">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-762">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-762">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-763">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-763">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-764">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-764">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-765">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-765">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-766">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-766">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-767">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-767">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-768">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-768">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-769">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-769">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-770">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-770">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-771">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-771">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-772">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-772">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-773">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-773">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-774">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-774">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-775">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-775">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-777">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-777">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-778">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-778">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-779">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-779">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-780">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-780">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-781">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-781">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-782">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-782">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-783">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-783">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-785">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-785">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-786">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-786">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-787">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-787">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-788">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-788">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-790">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-790">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-791">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-791">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="f81ea-793">DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="f81ea-793">DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="f81ea-794">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-794">Target</span></span> | <span data-ttu-id="f81ea-795">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-795">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-796">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-796">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-797">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-797">64</span></span> |
| <span data-ttu-id="f81ea-798">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-798">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-800">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-800">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-802">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-802">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-804">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-805">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-806">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-808">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-808">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-810">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-810">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-812">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-812">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-814">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-814">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-816">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-816">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-818">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-818">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-819">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-819">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-820">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-820">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-822">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-822">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-823">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-823">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-825">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-825">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-827">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-829">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-829">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-831">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-832">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-833">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-834">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-835">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-835">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-837">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-837">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-839">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-839">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-841">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-841">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-842">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-842">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-843">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-843">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-844">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-844">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-845">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-845">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-846">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-846">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-847">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-847">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-849">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-849">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-851">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-851">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-853">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-853">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-855">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-855">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-857">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-857">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-859">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-859">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-861">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-861">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-863">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-864">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-864">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-866">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-866">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-868">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-868">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-870">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-871">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-871">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="f81ea-873">DXGI_FORMAT_R16G16B16A16_UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="f81ea-873">DXGI_FORMAT_R16G16B16A16_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="f81ea-874">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-874">Target</span></span> | <span data-ttu-id="f81ea-875">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-875">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-876">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-877">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-877">64</span></span> |
| <span data-ttu-id="f81ea-878">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-878">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-880">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-880">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-882">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-882">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-884">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-885">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-886">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-888">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-890">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-892">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-894">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-894">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-896">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-896">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-898">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-898">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-899">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-899">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-900">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-900">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-902">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-902">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-903">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-903">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-905">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-905">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-907">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-909">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-909">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-911">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-912">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-913">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-914">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-915">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-915">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-917">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-917">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-919">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-919">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-921">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-922">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-923">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-924">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-925">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-925">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-926">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-926">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-927">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-927">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-929">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-929">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-931">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-931">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-933">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-933">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-935">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-935">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-937">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-937">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-939">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-939">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-940">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-940">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-942">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-943">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-944">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-945">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-945">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-947">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-947">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-948">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-948">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="f81ea-950">DXGI_FORMAT_R16G16B16A16_UINT<sup>FCS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="f81ea-950">DXGI_FORMAT_R16G16B16A16_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="f81ea-951">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-951">Target</span></span> | <span data-ttu-id="f81ea-952">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-952">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-953">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-953">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-954">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-954">64</span></span> |
| <span data-ttu-id="f81ea-955">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-955">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-957">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-957">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-959">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-959">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-961">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-961">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-962">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-962">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-963">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-963">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-965">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-965">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-967">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-967">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-969">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-969">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-971">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-971">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-973">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-973">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-974">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-974">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-975">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-975">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-976">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-976">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-977">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-977">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-978">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-978">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-980">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-980">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-981">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-983">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-983">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-984">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-984">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-986">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-986">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-987">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-987">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-988">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-988">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-989">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-989">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-991">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-991">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-993">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-993">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-995">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-995">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-996">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-996">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-997">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-997">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-998">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-998">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-999">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-999">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1000">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1000">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1001">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1001">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1003">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1003">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1005">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1005">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1007">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1007">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1009">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1010">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1010">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1012">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1012">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1013">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1013">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1015">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1015">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1016">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1016">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1017">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1017">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1018">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1018">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1020">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1020">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1021">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1021">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="f81ea-1023">DXGI_FORMAT_R16G16B16A16_SNORM<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1023">DXGI_FORMAT_R16G16B16A16_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="f81ea-1024">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1024">Target</span></span> | <span data-ttu-id="f81ea-1025">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1025">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1026">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1026">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1027">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1027">64</span></span> |
| <span data-ttu-id="f81ea-1028">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1028">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1030">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1030">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1032">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1032">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1034">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1035">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1036">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1038">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1040">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1042">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1042">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1044">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1044">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1046">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1046">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1048">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1048">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1049">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1049">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1050">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1050">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1052">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1052">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1053">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1053">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1055">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1055">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1057">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1057">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1059">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1059">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1061">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1061">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1062">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1062">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1063">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1063">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1064">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1064">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1065">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1065">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1067">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1067">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1069">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1069">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1071">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1071">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1072">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1072">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1073">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1073">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1074">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1074">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1075">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1075">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1076">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1076">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1077">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1077">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1079">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1079">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1081">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1081">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1083">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1083">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1085">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1085">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1087">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1087">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1089">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1089">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1090">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1090">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1092">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1092">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1093">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1093">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1094">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1094">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1095">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1095">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1097">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1097">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1098">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1098">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="f81ea-1100">DXGI_FORMAT_R16G16B16A16_SINT<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1100">DXGI_FORMAT_R16G16B16A16_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="f81ea-1101">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1101">Target</span></span> | <span data-ttu-id="f81ea-1102">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1102">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1103">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1103">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1104">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1104">64</span></span> |
| <span data-ttu-id="f81ea-1105">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1105">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1107">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1107">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1109">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1109">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1111">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1111">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1112">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1112">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1113">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1113">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1115">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1115">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1117">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1117">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1119">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1119">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1121">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1121">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1123">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1123">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1124">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1124">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1125">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1125">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1126">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1126">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1127">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1127">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1128">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1128">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1130">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1130">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1131">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1131">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1133">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1133">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1134">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1134">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1135">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1135">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1136">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1136">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1137">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1137">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1138">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1138">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1140">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1140">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1142">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1142">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1144">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1144">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1145">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1145">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1146">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1146">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1147">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1147">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1148">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1148">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1149">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1149">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1150">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1150">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1152">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1152">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1154">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1154">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1156">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1156">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1158">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1158">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1159">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1159">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1161">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1162">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1162">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1164">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1164">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1165">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1165">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1166">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1166">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1167">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1167">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1169">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1169">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1170">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1170">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="f81ea-1172"><sup>Pc</sup> DXGI_FORMAT_R32G32_TYPELESS (15)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1172">DXGI_FORMAT_R32G32_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="f81ea-1173">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1173">Target</span></span> | <span data-ttu-id="f81ea-1174">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1174">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1175">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1175">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1176">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1176">64</span></span> |
| <span data-ttu-id="f81ea-1177">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1177">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1179">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1179">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1180">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1180">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1181">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1181">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1182">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1182">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1183">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1183">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1185">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1185">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1187">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1187">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1189">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1191">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1191">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-1192">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1193">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1193">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1194">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1194">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1195">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1195">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1196">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1196">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1197">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1199">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1199">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1200">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1201">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1202">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1203">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1204">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1205">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1206">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1206">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-1207">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-1208">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-1209">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1210">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1211">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1212">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1213">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1213">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1214">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1214">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1215">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1215">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1217">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1218">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1219">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-1220">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1221">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1221">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-1222">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1223">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1223">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1225">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1225">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1226">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1226">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1227">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1227">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1228">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1228">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-1229">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1229">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1230">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1230">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="f81ea-1232">DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1232">DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="f81ea-1233">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1233">Target</span></span> | <span data-ttu-id="f81ea-1234">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1234">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1235">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1235">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1236">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1236">64</span></span> |
| <span data-ttu-id="f81ea-1237">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1237">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1239">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1239">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1241">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1241">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1243">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1244">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1244">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1246">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1246">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1248">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1250">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1252">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1254">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1254">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1256">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1256">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1258">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1258">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1259">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1259">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1260">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1260">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1262">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1262">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1263">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1265">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1265">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1267">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1269">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1269">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1271">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1272">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1273">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1274">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1275">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1275">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1277">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1277">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1279">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1279">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1281">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1281">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1282">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1282">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1283">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1283">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1284">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1284">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1285">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1285">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1286">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1286">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1287">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1287">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1289">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1289">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1291">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1291">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1293">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1293">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1295">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1295">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1297">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1297">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1299">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1299">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1300">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1300">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1302">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1302">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1303">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1303">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1304">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1304">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1305">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1305">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-1306">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1306">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1307">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1307">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="f81ea-1309">DXGI_FORMAT_R32G32_UINT<sup>FCS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1309">DXGI_FORMAT_R32G32_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="f81ea-1310">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1310">Target</span></span> | <span data-ttu-id="f81ea-1311">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1311">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1312">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1312">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1313">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1313">64</span></span> |
| <span data-ttu-id="f81ea-1314">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1314">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1316">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1316">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1318">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1318">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1320">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1321">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1321">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1323">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1325">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1325">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1327">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1327">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1329">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1329">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1331">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1331">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1333">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1334">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1334">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1335">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1335">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1336">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1336">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1337">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1337">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1338">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1338">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1340">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1340">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1341">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1341">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1343">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1343">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1344">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1344">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1346">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1346">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1347">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1347">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1348">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1348">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1349">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1349">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1351">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1351">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1353">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1353">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1355">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1356">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1357">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1357">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1358">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1359">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1359">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1360">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1360">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1361">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1361">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1363">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1363">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1365">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1365">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1367">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1367">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1369">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1370">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1370">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1372">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1373">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1373">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1375">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1376">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1377">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1378">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-1379">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1379">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1380">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1380">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="f81ea-1382">DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1382">DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="f81ea-1383">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1383">Target</span></span> | <span data-ttu-id="f81ea-1384">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1384">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1385">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1386">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1386">64</span></span> |
| <span data-ttu-id="f81ea-1387">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1387">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1389">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1389">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1391">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1391">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1393">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1394">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1394">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1396">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1396">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1398">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1400">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1400">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1402">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1402">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1404">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1404">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1406">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1407">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1407">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1408">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1408">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1409">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1410">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1410">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1411">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1411">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1413">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1413">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1414">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1414">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1416">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1417">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1418">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1419">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1420">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1421">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1421">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1423">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1423">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1425">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1425">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1427">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1427">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1428">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1428">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1429">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1429">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1430">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1430">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1431">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1431">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1432">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1432">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1433">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1433">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1435">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1435">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1437">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1437">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1439">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1439">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1441">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1442">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1442">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1444">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1444">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1445">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1445">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1447">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1447">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1448">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1448">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1449">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1449">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1450">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1450">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-1451">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1451">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1452">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1452">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssupvsup-19"></a><span data-ttu-id="f81ea-1454">DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1454">DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)</span></span>
| <span data-ttu-id="f81ea-1455">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1455">Target</span></span> | <span data-ttu-id="f81ea-1456">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1456">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1457">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1457">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1458">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1458">64</span></span> |
| <span data-ttu-id="f81ea-1459">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1459">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1461">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1461">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1462">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1462">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1463">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1464">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1465">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1467">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1469">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-1470">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1470">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1472">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1472">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-1473">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1474">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1474">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1475">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1475">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1476">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1476">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1477">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1477">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1478">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1478">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1480">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1480">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1481">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1482">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1482">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1483">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1483">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1484">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1484">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1485">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1485">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1486">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1486">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1487">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1487">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-1488">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1488">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-1489">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1489">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-1490">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1490">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1491">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1491">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1492">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1492">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1493">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1493">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1494">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1494">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1495">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1495">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1496">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1496">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1498">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1498">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1499">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1499">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1500">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1500">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-1501">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1501">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1502">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1502">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-1503">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1503">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1504">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1504">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1506">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1506">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1507">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1507">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1508">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1508">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1509">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1509">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-1510">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1510">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1511">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1511">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupvsup-20"></a><span data-ttu-id="f81ea-1512">DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1512">DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)</span></span>
| <span data-ttu-id="f81ea-1513">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1513">Target</span></span> | <span data-ttu-id="f81ea-1514">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1514">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1515">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1515">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1516">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1516">64</span></span> |
| <span data-ttu-id="f81ea-1517">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1517">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1519">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1519">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1520">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1520">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1521">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1521">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1522">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1522">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1523">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1523">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1525">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1525">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1527">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1527">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-1528">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1528">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1530">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1530">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-1531">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1531">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1532">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1532">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1533">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1533">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1534">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1534">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1535">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1535">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1536">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1536">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1538">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1538">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1539">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1539">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1540">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1540">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1541">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1541">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1542">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1542">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1544">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1544">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1545">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1545">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1546">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1546">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-1547">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1547">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-1548">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1548">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-1549">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1549">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1550">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1550">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1551">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1551">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1552">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1552">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1553">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1553">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1554">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1554">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1555">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1555">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1557">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1557">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1559">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1559">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1561">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1561">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1563">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1563">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1564">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1564">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-1565">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1565">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1566">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1566">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1568">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1568">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1569">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1569">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1570">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1570">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1571">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1571">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-1572">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1572">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1573">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1573">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupvsup-21"></a><span data-ttu-id="f81ea-1574">DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1574">DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)</span></span>
| <span data-ttu-id="f81ea-1575">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1575">Target</span></span> | <span data-ttu-id="f81ea-1576">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1576">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1577">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1577">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1578">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1578">64</span></span> |
| <span data-ttu-id="f81ea-1579">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1579">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1581">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1581">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1582">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1582">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1583">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1583">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1584">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1584">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1585">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1587">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1589">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-1590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1590">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1592">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1592">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1594">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1594">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1596">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1596">Shader sample_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1598">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1598">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1599">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1599">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1601">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1601">Shader gather4_c</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1603">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1603">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1605">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1605">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1606">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1606">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1607">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1607">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1608">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1608">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1609">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1609">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1610">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1610">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1611">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1611">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1612">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1612">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-1613">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1613">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-1614">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1614">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-1615">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1615">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1616">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1616">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1617">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1617">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1618">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1618">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1619">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1619">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1620">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1620">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1621">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1621">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1623">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1623">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1624">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1624">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1625">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1625">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-1626">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1626">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1627">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1627">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1629">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1629">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1630">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1630">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1632">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1632">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1633">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1633">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1634">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1634">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1635">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1635">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-1636">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1636">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1637">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1637">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupvsup-22"></a><span data-ttu-id="f81ea-1638">DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1638">DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)</span></span>
| <span data-ttu-id="f81ea-1639">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1639">Target</span></span> | <span data-ttu-id="f81ea-1640">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1640">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1641">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1641">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1642">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-1642">64</span></span> |
| <span data-ttu-id="f81ea-1643">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1643">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1645">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1645">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1646">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1646">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1647">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1647">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1648">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1648">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1649">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1649">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1651">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1651">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1653">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1653">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-1654">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1654">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1656">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1656">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1658">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1658">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1659">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1659">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1660">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1660">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1661">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1661">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1662">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1662">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1663">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1663">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1665">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1665">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1666">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1666">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1667">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1667">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1668">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1668">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1669">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1669">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1670">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1670">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1671">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1671">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1672">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1672">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-1673">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1673">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-1674">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1674">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-1675">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1675">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1676">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1676">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1677">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1677">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1678">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1678">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1679">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1679">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1680">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1680">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1681">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1681">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1683">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1684">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1685">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-1686">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1687">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1687">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1689">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1689">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1690">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1690">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1692">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1692">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1693">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1693">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1694">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1694">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1695">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1695">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-1696">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1696">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1697">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1697">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="f81ea-1698"><sup>Pc</sup> DXGI_FORMAT_R10G10B10A2_TYPELESS (23)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1698">DXGI_FORMAT_R10G10B10A2_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="f81ea-1699">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1699">Target</span></span> | <span data-ttu-id="f81ea-1700">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1700">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1701">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1701">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1702">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-1702">32</span></span> |
| <span data-ttu-id="f81ea-1703">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1703">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1705">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1705">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1706">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1706">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1707">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1707">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1708">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1708">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1709">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1709">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1711">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1711">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1713">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1715">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1717">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1717">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-1718">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1718">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1719">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1719">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1720">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1720">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1721">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1721">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1722">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1722">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1723">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1723">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1725">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1725">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1726">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1727">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1728">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1729">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1730">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1731">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1732">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1732">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-1733">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-1734">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-1735">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1736">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1737">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1738">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1739">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1739">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1740">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1740">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1741">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1741">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1743">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1744">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1745">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-1746">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1747">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1747">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-1748">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1749">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1749">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1751">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1751">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1752">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1752">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1753">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1753">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1754">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1754">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1756">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1756">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1757">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1757">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="f81ea-1759">DXGI_FORMAT_R10G10B10A2_UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1759">DXGI_FORMAT_R10G10B10A2_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="f81ea-1760">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1760">Target</span></span> | <span data-ttu-id="f81ea-1761">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1761">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1762">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1763">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-1763">32</span></span> |
| <span data-ttu-id="f81ea-1764">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1764">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1766">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1766">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1768">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1768">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1770">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1771">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1772">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1774">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1774">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1776">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1776">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1778">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1778">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1780">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1780">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1782">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1782">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1784">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1784">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1785">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1785">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1786">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1786">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1788">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1788">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1789">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1789">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1791">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1791">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1793">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1795">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1795">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1797">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1797">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1798">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1798">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1799">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1799">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1800">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1800">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1801">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1801">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1803">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1803">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1805">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1805">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1807">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1807">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1808">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1808">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1809">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1809">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1810">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1810">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1811">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1811">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1812">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1812">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1813">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1813">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1815">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1815">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1817">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1817">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1819">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1819">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1821">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1821">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1823">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1823">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1825">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1825">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1827">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1827">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1829">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1829">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1830">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1830">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1832">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1832">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1834">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1834">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1836">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1836">BackBuffer Castable Even Fully Typed</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1838">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1838">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="f81ea-1840">DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1840">DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="f81ea-1841">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1841">Target</span></span> | <span data-ttu-id="f81ea-1842">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1842">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1843">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1843">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1844">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-1844">32</span></span> |
| <span data-ttu-id="f81ea-1845">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1845">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1847">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1847">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1849">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1849">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1851">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1851">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1852">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1852">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1853">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1853">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1855">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1857">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1859">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1859">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1861">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1861">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1863">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1863">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1864">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1864">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1865">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1865">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1866">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1866">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1867">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1867">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1868">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1870">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1870">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1871">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1871">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1873">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1873">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1874">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1874">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1876">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1876">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1877">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1877">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1878">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1878">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1879">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1879">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1881">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1881">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1883">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1883">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1885">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1885">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1886">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1886">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1887">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1887">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1888">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1888">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1889">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1889">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1890">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1890">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1891">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1891">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1893">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1893">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1895">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1895">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1897">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1897">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1899">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1899">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1900">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1900">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1902">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-1903">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1903">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1905">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1906">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-1907">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-1908">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1908">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1910">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1910">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-1911">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1911">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="f81ea-1913">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1913">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="f81ea-1914">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1914">Target</span></span> | <span data-ttu-id="f81ea-1915">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1915">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1916">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1916">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1917">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-1917">32</span></span> |
| <span data-ttu-id="f81ea-1918">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1918">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1920">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1920">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1921">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1921">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1922">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1922">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1923">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1923">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1924">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1924">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-1925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1925">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1927">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-1928">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1928">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-1929">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1929">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-1930">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1930">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1931">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1931">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1932">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1932">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-1933">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-1933">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-1934">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1934">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-1935">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1935">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-1936">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-1936">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-1937">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-1937">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1938">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-1938">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1939">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-1939">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-1940">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1940">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-1941">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-1941">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1942">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1942">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-1943">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1943">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-1944">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1944">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-1945">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1945">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-1946">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1946">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-1947">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1947">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-1948">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-1948">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-1949">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1949">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-1950">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-1950">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1951">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-1951">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-1952">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-1952">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1954">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1954">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1955">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-1955">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-1956">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-1956">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-1957">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1957">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-1958">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-1958">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-1959">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-1959">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1961">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-1961">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1963">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-1964">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1964">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-1966">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-1966">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1968">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-1968">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1970">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1970">BackBuffer Castable Even Fully Typed</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1972">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-1972">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="f81ea-1974">DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1974">DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="f81ea-1975">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-1975">Target</span></span> | <span data-ttu-id="f81ea-1976">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-1976">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-1977">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-1978">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-1978">32</span></span> |
| <span data-ttu-id="f81ea-1979">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-1979">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1981">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-1981">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1983">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-1983">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1985">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-1985">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1986">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-1986">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-1987">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1987">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1989">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1989">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1991">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-1991">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1993">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-1993">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1995">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-1995">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1997">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1997">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-1999">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-1999">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2000">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2000">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2001">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2001">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2003">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2003">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2004">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2004">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2006">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2006">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2008">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2008">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2010">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2010">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2012">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2013">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2014">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2015">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2016">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2016">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2018">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2018">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2020">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2020">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2022">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2023">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2024">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2024">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2025">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2026">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2026">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2027">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2027">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2028">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2028">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2030">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2030">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2032">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2032">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2034">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2034">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2036">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2036">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2038">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2038">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2040">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2041">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2041">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-2042">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2043">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2044">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2045">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2045">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-2046">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2046">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2047">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2047">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="f81ea-2049"><sup>Pc</sup> DXGI_FORMAT_R8G8B8A8_TYPELESS (27)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2049">DXGI_FORMAT_R8G8B8A8_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="f81ea-2050">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2050">Target</span></span> | <span data-ttu-id="f81ea-2051">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2051">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2052">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2053">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2053">32</span></span> |
| <span data-ttu-id="f81ea-2054">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2054">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2056">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2056">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2057">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2057">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2058">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2058">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2059">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2059">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2060">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2062">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2064">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2066">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2068">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2068">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-2069">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2069">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2070">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2070">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2071">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2071">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2072">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2072">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-2073">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2073">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2074">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2074">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2076">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2076">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-2077">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2077">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2078">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2078">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2079">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2079">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2080">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2080">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2081">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2081">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2082">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2082">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2083">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2083">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-2084">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2084">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-2085">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2085">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-2086">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2086">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2087">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2087">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2088">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2088">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2089">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2089">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2090">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2090">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2091">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2091">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2092">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2092">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2094">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2094">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2095">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2095">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2096">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2096">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-2097">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2097">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-2098">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2098">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-2099">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2099">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2100">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2100">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2102">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2102">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2103">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2103">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2104">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2104">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2105">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2105">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2107">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2107">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2108">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2108">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="f81ea-2110">DXGI_FORMAT_R8G8B8A8_UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2110">DXGI_FORMAT_R8G8B8A8_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="f81ea-2111">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2111">Target</span></span> | <span data-ttu-id="f81ea-2112">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2112">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2113">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2113">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2114">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2114">32</span></span> |
| <span data-ttu-id="f81ea-2115">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2115">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2117">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2117">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2119">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2119">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2121">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2121">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2122">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2122">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2123">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2123">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2125">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2127">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2127">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2129">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2129">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2131">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2131">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2133">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2133">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2135">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2135">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2136">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2136">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2137">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2137">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2139">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2139">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2140">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2140">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2142">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2142">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2144">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2146">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2148">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2148">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2149">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2149">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2150">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2150">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2151">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2151">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2152">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2152">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2154">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2154">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2156">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2156">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2158">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2158">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2159">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2159">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2160">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2160">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2161">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2161">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2162">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2162">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2163">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2163">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2164">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2164">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2166">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2166">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2168">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2168">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2170">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2170">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2172">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2172">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2174">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2174">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2176">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2176">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2178">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2178">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2180">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2180">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2181">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2181">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2183">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2183">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2185">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2185">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2187">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2187">BackBuffer Castable Even Fully Typed</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2189">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2189">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="f81ea-2191">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2191">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="f81ea-2192">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2192">Target</span></span> | <span data-ttu-id="f81ea-2193">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2193">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2194">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2195">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2195">32</span></span> |
| <span data-ttu-id="f81ea-2196">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2196">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2198">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2198">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2199">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2199">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2200">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2200">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2201">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2201">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2202">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2202">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2204">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2204">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2206">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2206">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2208">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2210">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2210">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2212">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2212">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2214">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2214">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2215">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2215">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2216">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2216">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2218">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2218">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2219">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2219">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2221">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2221">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2223">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2225">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2225">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2227">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2227">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2228">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2228">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2229">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2229">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2230">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2230">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2231">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2231">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-2232">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2232">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-2233">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2233">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-2234">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2234">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2235">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2235">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2236">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2236">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2237">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2237">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2238">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2238">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2239">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2239">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2240">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2240">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2242">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2242">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2244">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2244">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2246">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2246">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2248">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2248">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2250">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2250">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2252">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2252">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2254">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2254">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2256">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2256">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2257">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2257">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2259">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2259">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2261">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2261">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2263">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2263">BackBuffer Castable Even Fully Typed</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2265">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2265">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="f81ea-2267">DXGI_FORMAT_R8G8B8A8_UINT<sup>FCS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2267">DXGI_FORMAT_R8G8B8A8_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="f81ea-2268">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2268">Target</span></span> | <span data-ttu-id="f81ea-2269">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2269">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2270">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2270">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2271">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2271">32</span></span> |
| <span data-ttu-id="f81ea-2272">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2272">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2274">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2274">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2276">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2276">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2278">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2278">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2279">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2279">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2280">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2280">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2282">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2282">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2284">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2284">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2286">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2288">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2288">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2290">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2290">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2291">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2291">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2292">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2292">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2293">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2293">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-2294">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2294">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2295">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2295">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2297">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2297">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-2298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2298">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2300">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2300">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2301">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2301">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2303">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2304">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2305">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2306">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2306">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2308">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2308">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2310">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2310">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2312">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2313">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2314">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2315">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2316">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2316">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2317">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2317">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2318">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2318">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2320">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2320">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2322">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2322">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2324">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2324">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2326">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-2327">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2327">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2329">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2329">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2330">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2330">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2332">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2332">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2333">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2333">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2334">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2334">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2335">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2335">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2337">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2337">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2338">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2338">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="f81ea-2340">DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2340">DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="f81ea-2341">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2341">Target</span></span> | <span data-ttu-id="f81ea-2342">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2342">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2343">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2343">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2344">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2344">32</span></span> |
| <span data-ttu-id="f81ea-2345">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2345">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2347">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2347">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2349">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2349">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2351">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2352">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2353">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2355">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2355">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2357">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2357">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2359">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2359">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2361">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2361">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2363">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2363">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2365">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2365">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2366">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2366">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2367">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2367">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2369">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2369">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2370">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2370">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2372">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2372">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2374">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2374">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2376">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2376">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2378">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2378">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2379">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2379">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2380">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2380">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2381">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2381">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2382">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2382">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2384">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2384">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2386">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2386">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2388">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2388">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2389">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2389">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2390">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2390">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2391">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2391">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2392">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2392">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2393">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2393">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2394">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2394">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2396">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2396">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2398">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2398">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2400">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2400">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2402">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2402">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2404">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2404">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2406">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2406">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2407">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2407">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2409">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2409">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2410">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2410">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2411">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2411">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2412">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2412">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2414">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2414">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2415">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2415">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="f81ea-2417">DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2417">DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="f81ea-2418">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2418">Target</span></span> | <span data-ttu-id="f81ea-2419">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2419">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2420">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2420">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2421">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2421">32</span></span> |
| <span data-ttu-id="f81ea-2422">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2422">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2424">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2424">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2426">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2426">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2428">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2428">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2429">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2429">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2430">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2430">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2432">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2432">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2434">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2434">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2436">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2436">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2438">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2438">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2440">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2441">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2441">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2442">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2442">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2443">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-2444">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2444">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2445">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2447">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2447">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-2448">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2448">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2450">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2450">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2451">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2451">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2452">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2452">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2453">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2453">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2454">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2454">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2455">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2455">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2457">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2457">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2459">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2459">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2461">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2461">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2462">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2462">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2463">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2463">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2464">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2464">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2465">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2465">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2466">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2466">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2467">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2467">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2469">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2469">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2471">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2471">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2473">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2473">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2475">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2475">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-2476">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2476">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2478">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2479">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2479">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2481">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2482">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2483">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2484">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2484">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2486">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2486">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2487">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2487">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="f81ea-2489"><sup>Pc</sup> DXGI_FORMAT_R16G16_TYPELESS (33)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2489">DXGI_FORMAT_R16G16_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="f81ea-2490">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2490">Target</span></span> | <span data-ttu-id="f81ea-2491">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2491">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2492">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2492">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2493">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2493">32</span></span> |
| <span data-ttu-id="f81ea-2494">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2494">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2496">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2496">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2497">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2498">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2499">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2500">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2502">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2502">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2504">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2506">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2508">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2508">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-2509">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2509">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2510">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2510">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2511">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2511">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2512">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2512">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-2513">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2513">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2514">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2514">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2516">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2516">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2518">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2519">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2520">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2521">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2522">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2523">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-2524">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-2525">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-2526">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2527">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2528">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2529">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2530">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2530">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2531">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2531">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2532">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2532">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2534">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2534">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2535">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2535">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2536">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2536">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-2537">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2537">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-2538">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2538">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-2539">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2539">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2540">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2540">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2542">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2542">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2543">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2543">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2544">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2544">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2545">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2545">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-2546">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2546">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2547">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2547">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="f81ea-2549">DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2549">DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="f81ea-2550">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2550">Target</span></span> | <span data-ttu-id="f81ea-2551">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2551">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2552">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2552">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2553">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2553">32</span></span> |
| <span data-ttu-id="f81ea-2554">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2554">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2556">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2556">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2558">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2558">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2560">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2561">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2562">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2564">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2564">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2566">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2568">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2568">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2570">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2570">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2572">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2572">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2574">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2574">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2575">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2575">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2576">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2576">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2578">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2578">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2579">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2579">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2581">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2581">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2583">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2583">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2585">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2585">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2587">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2588">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2589">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2590">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2591">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2591">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2593">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2593">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2595">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2595">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2597">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2598">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2599">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2599">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2600">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2601">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2601">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2602">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2602">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2603">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2603">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2605">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2605">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2607">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2607">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2609">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2609">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2611">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2611">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2613">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2613">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2615">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2616">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2616">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2618">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2619">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2620">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2621">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-2622">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2622">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2623">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2623">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="f81ea-2625">DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2625">DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="f81ea-2626">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2626">Target</span></span> | <span data-ttu-id="f81ea-2627">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2627">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2628">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2628">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2629">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2629">32</span></span> |
| <span data-ttu-id="f81ea-2630">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2630">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2632">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2632">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2634">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2634">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2636">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2636">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2637">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2637">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2638">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2638">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2640">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2642">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2644">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2646">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2646">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2648">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2648">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2650">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2650">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2651">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2651">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2652">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2652">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2654">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2654">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2655">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2655">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2657">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2657">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2659">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2659">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2661">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2661">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2663">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2663">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2664">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2664">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2665">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2665">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2666">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2666">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2667">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2667">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2669">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2669">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2671">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2671">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2673">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2673">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2674">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2674">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2675">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2675">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2676">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2676">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2677">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2677">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2678">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2678">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2679">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2679">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2681">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2681">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2683">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2683">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2685">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2685">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2687">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2687">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2689">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2689">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2691">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2691">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2692">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2692">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2694">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2694">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2695">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2695">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2696">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2696">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2697">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2697">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-2698">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2698">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2699">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2699">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="f81ea-2701">DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2701">DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="f81ea-2702">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2702">Target</span></span> | <span data-ttu-id="f81ea-2703">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2704">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2705">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2705">32</span></span> |
| <span data-ttu-id="f81ea-2706">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2706">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2708">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2708">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2710">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2710">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2712">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2712">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2713">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2713">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2714">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2714">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2716">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2718">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2720">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2722">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2722">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2724">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2724">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2725">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2725">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2726">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2726">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2727">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2727">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-2728">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2728">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2729">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2729">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2731">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2731">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-2732">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2732">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2734">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2734">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2735">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2735">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2737">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2738">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2739">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2740">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2740">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2742">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2742">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2744">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2744">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2746">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2746">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2747">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2747">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2748">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2748">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2749">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2749">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2750">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2750">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2751">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2751">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2752">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2752">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2754">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2754">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2756">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2756">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2758">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2758">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2760">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2760">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-2761">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2761">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2763">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2763">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2764">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2764">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2766">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2767">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2768">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2769">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2769">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-2770">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2770">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2771">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2771">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="f81ea-2773">DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2773">DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="f81ea-2774">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2774">Target</span></span> | <span data-ttu-id="f81ea-2775">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2775">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2776">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2776">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2777">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2777">32</span></span> |
| <span data-ttu-id="f81ea-2778">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2778">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2780">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2780">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2782">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2782">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2784">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2784">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2785">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2785">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2786">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2786">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2788">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2788">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2790">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2790">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2792">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2792">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2794">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2794">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2796">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2796">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2798">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2798">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2799">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2799">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2800">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2800">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2802">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2802">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2803">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2803">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2805">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2805">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2807">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2809">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2809">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2811">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2812">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2813">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2814">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2815">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2815">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2817">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2817">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2819">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2819">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2821">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2821">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2822">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2822">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2823">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2823">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2824">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2824">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2825">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2825">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2826">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2826">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2827">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2827">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2829">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2829">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2831">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2831">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2833">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2833">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2835">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2835">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2837">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2837">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2839">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2839">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2840">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2840">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2842">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2842">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2843">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2843">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2844">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2844">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2845">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2845">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-2846">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2846">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2847">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2847">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="f81ea-2849">DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2849">DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="f81ea-2850">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2850">Target</span></span> | <span data-ttu-id="f81ea-2851">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2851">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2852">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2852">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2853">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2853">32</span></span> |
| <span data-ttu-id="f81ea-2854">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2854">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2856">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2856">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2858">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2858">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2860">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2861">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2862">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2864">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2864">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2866">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2866">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2868">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2870">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2870">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2872">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2872">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2873">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2873">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2874">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2874">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2875">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2875">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-2876">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2876">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2877">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2877">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2879">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2879">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-2880">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2880">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2882">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2883">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2884">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2885">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2886">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2887">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2887">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2889">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2889">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2891">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2891">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2893">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2893">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2894">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2894">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2895">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2895">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2896">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2896">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2897">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2897">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2898">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2898">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2899">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2899">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2901">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2901">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2903">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2903">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2905">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2905">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-2907">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2907">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-2908">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2908">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2910">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2910">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2911">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2911">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2913">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2914">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2915">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2916">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-2917">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2917">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2918">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2918">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="f81ea-2920"><sup>Pc</sup> DXGI_FORMAT_R32_TYPELESS (39)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2920">DXGI_FORMAT_R32_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="f81ea-2921">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2921">Target</span></span> | <span data-ttu-id="f81ea-2922">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2922">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2923">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2924">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2924">32</span></span> |
| <span data-ttu-id="f81ea-2925">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2925">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2927">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2927">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2928">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2929">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2930">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2931">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2933">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2933">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2935">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2935">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2937">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2937">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2939">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2939">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-2940">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2941">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2941">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2942">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2942">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-2943">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-2943">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-2944">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-2944">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-2945">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2945">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2947">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-2947">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-2948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-2948">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2949">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-2949">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2950">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-2950">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-2951">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2951">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-2952">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-2952">Raw UAV and SRV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2954">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-2955">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2955">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-2956">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-2957">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-2958">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-2959">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-2960">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-2960">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-2961">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-2962">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-2962">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2963">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-2963">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-2964">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-2964">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2966">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2967">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-2967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-2968">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-2968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-2969">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-2970">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-2970">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-2971">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-2971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-2972">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-2972">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2974">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-2975">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-2976">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-2976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-2977">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-2977">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2979">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2979">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-2980">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-2980">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="f81ea-2982">DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2982">DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="f81ea-2983">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-2983">Target</span></span> | <span data-ttu-id="f81ea-2984">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-2984">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-2985">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-2985">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-2986">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-2986">32</span></span> |
| <span data-ttu-id="f81ea-2987">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-2987">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2989">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-2989">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2990">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-2990">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2991">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-2991">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2992">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-2992">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-2993">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2993">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2995">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2995">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-2997">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-2997">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-2998">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-2998">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3000">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3000">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-3001">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3001">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3002">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3002">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3003">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3003">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3004">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3004">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3005">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3005">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3006">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3006">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3008">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3008">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3009">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3009">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3010">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3010">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3011">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3011">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3012">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3012">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3014">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3015">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3016">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3016">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-3017">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-3018">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-3019">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3020">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3021">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3022">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3023">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3023">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3024">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3024">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3025">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3025">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3027">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3027">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3029">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3029">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3031">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3031">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3033">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3033">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3034">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3034">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-3035">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3035">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3036">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3036">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3038">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3038">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3039">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3039">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3040">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3040">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3041">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3041">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3043">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3043">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3044">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3044">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="f81ea-3046">DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3046">DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="f81ea-3047">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3047">Target</span></span> | <span data-ttu-id="f81ea-3048">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3048">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3049">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3049">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3050">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-3050">32</span></span> |
| <span data-ttu-id="f81ea-3051">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3051">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3053">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3053">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3055">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3055">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3057">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3057">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3058">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3058">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3060">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3062">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3064">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3066">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3068">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3068">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3070">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3070">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3072">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3072">Shader sample_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3074">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3074">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3075">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3075">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3077">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3077">Shader gather4_c</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3079">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3079">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3081">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3081">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3083">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3083">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3085">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3085">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3087">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3088">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3089">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3090">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3091">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3091">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3093">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3093">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3095">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3095">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3097">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3097">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3098">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3098">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3099">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3099">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3100">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3100">UAV Atomic Exchange</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3102">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3102">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3103">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3103">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3104">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3104">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3106">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3106">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3108">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3108">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3110">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3110">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3112">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3112">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3114">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3114">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3116">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3116">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3117">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3117">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3119">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3120">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3121">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3122">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3122">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3124">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3124">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3125">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3125">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="f81ea-3127">DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3127">DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="f81ea-3128">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3128">Target</span></span> | <span data-ttu-id="f81ea-3129">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3129">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3130">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3131">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-3131">32</span></span> |
| <span data-ttu-id="f81ea-3132">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3132">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3134">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3134">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3136">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3136">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3138">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3138">Input Assembler Index Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3140">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3140">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3142">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3144">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3146">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3148">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3150">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3150">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3152">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3152">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3153">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3153">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3154">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3154">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3155">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3155">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3156">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3156">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3157">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3157">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3159">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3159">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3160">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3160">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3162">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3163">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3163">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3165">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3166">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3167">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3168">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3168">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3170">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3170">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3172">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3172">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3174">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3174">UAV Atomic Add</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3176">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3176">UAV Atomic Bitwise Ops</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3178">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3180">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3180">UAV Atomic Exchange</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3182">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3182">UAV Atomic Signed Min/Max</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3184">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3184">UAV Atomic Unsigned Min/Max</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3186">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3186">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3188">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3188">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3190">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3190">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3192">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3192">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3194">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3194">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3195">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3195">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3197">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3197">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3198">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3198">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3200">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3200">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3201">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3201">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3202">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3202">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3203">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3203">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3205">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3205">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3206">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3206">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="f81ea-3208">DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3208">DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="f81ea-3209">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3209">Target</span></span> | <span data-ttu-id="f81ea-3210">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3210">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3211">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3211">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3212">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-3212">32</span></span> |
| <span data-ttu-id="f81ea-3213">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3213">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3215">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3215">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3217">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3217">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3219">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3220">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3220">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3222">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3222">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3224">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3226">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3228">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3228">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3230">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3230">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3232">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3232">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3233">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3233">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3234">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3234">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3235">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3235">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3236">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3236">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3237">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3237">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3239">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3239">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3240">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3240">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3242">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3243">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3244">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3245">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3246">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3247">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3247">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3249">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3249">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3251">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3251">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3253">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3253">UAV Atomic Add</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3255">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3255">UAV Atomic Bitwise Ops</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3257">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3257">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3259">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3259">UAV Atomic Exchange</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3261">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3261">UAV Atomic Signed Min/Max</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3263">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3263">UAV Atomic Unsigned Min/Max</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3265">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3265">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3267">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3267">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3269">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3269">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3271">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3271">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3273">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3273">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3274">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3274">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3276">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3276">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3277">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3277">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3279">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3279">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3280">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3280">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3281">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3281">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3282">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3282">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3284">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3284">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3285">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3285">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r24g8_typelesssupvsup-44"></a><span data-ttu-id="f81ea-3287">DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3287">DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)</span></span>
| <span data-ttu-id="f81ea-3288">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3288">Target</span></span> | <span data-ttu-id="f81ea-3289">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3289">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3290">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3290">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3291">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-3291">32</span></span> |
| <span data-ttu-id="f81ea-3292">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3292">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3294">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3294">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3295">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3295">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3296">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3296">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3297">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3297">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3298">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3298">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3300">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3302">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3302">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-3303">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3303">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3305">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3305">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-3306">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3307">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3307">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3308">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3308">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3309">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3309">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3310">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3310">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3311">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3311">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3313">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3313">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3314">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3314">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3315">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3315">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3316">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3316">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3317">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3317">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3318">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3318">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3319">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3319">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3320">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3320">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-3321">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3321">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-3322">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3322">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-3323">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3323">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3324">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3324">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3325">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3325">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3326">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3326">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3327">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3327">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3328">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3328">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3329">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3329">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3331">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3332">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3333">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-3334">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3335">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3335">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-3336">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3337">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3337">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3339">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3339">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3340">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3340">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3341">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3341">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3342">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3342">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-3343">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3343">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3344">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3344">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupvsup-45"></a><span data-ttu-id="f81ea-3345">DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3345">DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)</span></span>
| <span data-ttu-id="f81ea-3346">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3346">Target</span></span> | <span data-ttu-id="f81ea-3347">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3347">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3348">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3348">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3349">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-3349">32</span></span> |
| <span data-ttu-id="f81ea-3350">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3350">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3352">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3352">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3353">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3353">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3354">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3354">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3355">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3355">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3356">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3356">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3358">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3358">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3360">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-3361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3361">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3363">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3363">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-3364">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3364">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3365">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3365">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3366">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3366">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3367">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3367">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3368">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3368">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3369">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3369">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3371">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3371">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3372">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3373">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3374">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3375">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3375">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3377">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3377">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3378">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3378">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3379">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3379">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-3380">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3380">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-3381">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3381">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-3382">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3382">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3383">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3383">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3384">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3384">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3385">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3385">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3386">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3386">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3387">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3387">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3388">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3388">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3390">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3390">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3392">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3392">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3394">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3394">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3396">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3396">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3397">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3397">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-3398">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3398">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3399">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3399">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3401">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3401">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3402">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3402">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3403">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3403">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3404">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3404">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-3405">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3405">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3406">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3406">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupvsup-46"></a><span data-ttu-id="f81ea-3407">DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3407">DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)</span></span>
| <span data-ttu-id="f81ea-3408">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3408">Target</span></span> | <span data-ttu-id="f81ea-3409">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3409">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3410">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3410">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3411">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-3411">32</span></span> |
| <span data-ttu-id="f81ea-3412">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3412">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3414">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3414">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3415">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3415">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3416">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3416">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3417">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3417">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3418">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3418">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3420">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3420">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3422">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3422">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-3423">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3423">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3425">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3425">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3427">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3427">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3429">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3429">Shader sample_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3431">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3431">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3432">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3432">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3434">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3434">Shader gather4_c</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3436">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3436">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3438">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3438">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3439">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3440">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3440">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3441">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3441">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3442">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3442">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3443">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3443">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3444">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3444">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3445">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3445">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-3446">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3446">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-3447">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3447">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-3448">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3448">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3449">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3449">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3450">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3450">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3451">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3451">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3452">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3452">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3453">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3453">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3454">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3454">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3456">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3456">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3457">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3457">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3458">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3458">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-3459">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3459">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3460">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3460">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3462">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3462">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3463">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3463">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3465">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3465">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3466">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3466">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3467">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3467">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3468">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3468">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-3469">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3469">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3470">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3470">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupvsup-47"></a><span data-ttu-id="f81ea-3471">DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3471">DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)</span></span>
| <span data-ttu-id="f81ea-3472">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3472">Target</span></span> | <span data-ttu-id="f81ea-3473">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3473">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3474">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3474">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3475">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-3475">32</span></span> |
| <span data-ttu-id="f81ea-3476">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3476">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3478">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3478">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3479">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3479">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3480">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3480">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3481">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3481">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3482">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3482">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3484">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3484">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3486">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3486">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-3487">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3487">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3489">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3489">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3491">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3491">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3492">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3492">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3493">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3493">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3494">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3494">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3495">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3495">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3496">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3496">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3498">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3498">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3499">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3499">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3500">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3500">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3501">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3501">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3502">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3502">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3503">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3503">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3504">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3504">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3505">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3505">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-3506">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3506">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-3507">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3507">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-3508">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3508">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3509">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3509">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3510">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3510">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3511">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3511">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3512">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3512">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3513">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3513">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3514">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3514">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3516">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3516">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3517">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3517">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3518">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3518">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-3519">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3519">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3520">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3520">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3522">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3522">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3523">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3523">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3525">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3526">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3527">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3528">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3528">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-3529">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3529">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3530">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3530">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="f81ea-3531"><sup>Pc</sup> DXGI_FORMAT_R8G8_TYPELESS (48)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3531">DXGI_FORMAT_R8G8_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="f81ea-3532">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3532">Target</span></span> | <span data-ttu-id="f81ea-3533">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3533">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3534">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3534">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3535">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-3535">16</span></span> |
| <span data-ttu-id="f81ea-3536">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3536">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3538">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3538">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3539">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3539">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3540">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3541">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3542">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3544">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3546">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3548">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3550">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3550">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-3551">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3552">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3552">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3553">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3553">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3554">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3555">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3555">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3556">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3558">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3558">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3559">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3559">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3560">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3560">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3561">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3562">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3563">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3564">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3565">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3565">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-3566">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-3567">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-3568">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3569">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3570">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3571">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3572">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3573">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3574">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3574">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3576">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3576">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3577">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3577">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3578">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3578">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-3579">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3579">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3580">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3580">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-3581">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3581">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3582">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3582">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3584">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3584">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3585">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3585">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3586">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3586">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3587">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3587">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-3588">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3588">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3589">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3589">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="f81ea-3591">DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3591">DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="f81ea-3592">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3592">Target</span></span> | <span data-ttu-id="f81ea-3593">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3593">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3594">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3594">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3595">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-3595">16</span></span> |
| <span data-ttu-id="f81ea-3596">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3596">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3598">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3600">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3600">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3602">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3603">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3604">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3606">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3608">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3608">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3610">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3612">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3612">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3614">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3614">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3616">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3616">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3617">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3617">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3618">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3618">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3620">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3620">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3621">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3621">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3623">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3623">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3625">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3625">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3627">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3627">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3629">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3629">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3630">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3630">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3631">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3631">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3632">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3632">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3633">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3633">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3635">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3635">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3637">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3637">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3639">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3639">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3640">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3640">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3641">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3641">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3642">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3642">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3643">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3643">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3644">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3644">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3645">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3645">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3647">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3647">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3649">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3649">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3651">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3651">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3653">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3653">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3655">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3655">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3657">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3658">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3658">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3660">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3660">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3661">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3661">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3662">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3662">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3663">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3663">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3665">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3665">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3666">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3666">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="f81ea-3668">DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3668">DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="f81ea-3669">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3669">Target</span></span> | <span data-ttu-id="f81ea-3670">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3670">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3671">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3671">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3672">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-3672">16</span></span> |
| <span data-ttu-id="f81ea-3673">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3673">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3675">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3675">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3677">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3677">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3679">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3679">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3680">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3680">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3681">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3681">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3683">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3683">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3685">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3685">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3687">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3687">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3689">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3689">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3691">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3691">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3692">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3692">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3693">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3693">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3694">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3694">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3695">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3695">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3696">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3696">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3698">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3698">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3699">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3699">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3701">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3701">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3702">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3702">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3704">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3704">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3705">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3705">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3706">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3706">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3707">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3707">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3709">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3709">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3711">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3711">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3713">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3713">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3714">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3714">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3715">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3715">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3716">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3716">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3717">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3717">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3718">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3718">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3719">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3719">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3721">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3721">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3723">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3723">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3725">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3725">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3727">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3728">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3728">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3730">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3730">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3731">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3731">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3733">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3733">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3734">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3734">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3735">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3735">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3736">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3736">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-3737">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3737">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3738">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3738">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="f81ea-3740">DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3740">DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="f81ea-3741">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3741">Target</span></span> | <span data-ttu-id="f81ea-3742">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3742">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3743">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3743">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3744">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-3744">16</span></span> |
| <span data-ttu-id="f81ea-3745">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3745">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3747">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3747">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3749">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3749">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3751">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3752">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3753">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3755">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3757">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3759">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3761">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3761">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3763">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3763">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3765">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3765">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3766">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3766">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3767">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3767">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3769">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3769">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3770">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3770">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3772">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3772">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3774">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3776">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3776">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3778">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3778">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3779">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3779">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3780">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3780">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3781">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3781">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3782">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3782">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3784">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3784">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3786">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3786">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3788">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3789">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3790">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3791">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3792">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3793">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3794">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3794">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3796">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3796">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3798">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3798">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3800">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3800">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3802">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3802">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3804">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3804">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3806">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3807">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3807">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3809">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3809">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3810">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3810">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3811">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3811">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3812">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3812">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-3813">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3813">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3814">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3814">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="f81ea-3816">DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3816">DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="f81ea-3817">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3817">Target</span></span> | <span data-ttu-id="f81ea-3818">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3818">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3819">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3820">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-3820">16</span></span> |
| <span data-ttu-id="f81ea-3821">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3821">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3823">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3823">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3825">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3825">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3827">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3828">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3829">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3831">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3833">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3835">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3837">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3837">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3839">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3839">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3840">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3840">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3841">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3841">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3842">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3842">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3843">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3843">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3844">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3844">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3846">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3846">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3847">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3847">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3849">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3849">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3850">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3850">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3851">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3851">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3852">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3852">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3853">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3853">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3854">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3854">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3856">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3856">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3858">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3858">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3860">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3860">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3861">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3861">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3862">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3862">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3863">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3863">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3864">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3864">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3865">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3865">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3866">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3866">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3868">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3868">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3870">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3870">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3872">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3872">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-3874">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3874">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3875">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3875">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3877">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3877">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3878">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3878">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3880">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3881">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3882">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3883">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3883">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-3884">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3885">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3885">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="f81ea-3887"><sup>Pc</sup> DXGI_FORMAT_R16_TYPELESS (53)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3887">DXGI_FORMAT_R16_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="f81ea-3888">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3888">Target</span></span> | <span data-ttu-id="f81ea-3889">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3889">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3890">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3891">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-3891">16</span></span> |
| <span data-ttu-id="f81ea-3892">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3892">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3894">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3894">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3895">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3896">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3897">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3898">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3900">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3902">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3904">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3906">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3906">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-3907">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3907">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3908">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3908">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3909">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3909">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3910">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3910">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-3911">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3911">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3912">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3912">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3914">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3914">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-3915">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3915">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3916">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3916">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3917">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3917">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3918">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3918">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3919">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3919">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3920">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3920">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3921">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3921">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-3922">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3922">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-3923">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3923">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-3924">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3924">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3925">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3925">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3926">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3926">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3927">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3927">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-3928">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3928">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3929">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-3929">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-3930">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-3930">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3932">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3932">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3933">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-3933">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-3934">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-3934">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-3935">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3935">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-3936">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-3936">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-3937">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-3937">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-3938">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-3938">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3940">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3940">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-3941">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3941">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-3942">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-3942">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-3943">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-3943">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3945">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3945">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-3946">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-3946">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="f81ea-3948">DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3948">DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="f81ea-3949">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3949">Target</span></span> | <span data-ttu-id="f81ea-3950">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-3950">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-3951">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-3952">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-3952">16</span></span> |
| <span data-ttu-id="f81ea-3953">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3953">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3955">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-3955">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3957">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-3957">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3959">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-3959">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3960">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-3960">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-3961">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3961">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3963">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-3965">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3967">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-3967">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3969">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3969">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3971">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3971">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3973">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3973">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3974">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-3974">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-3975">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-3975">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3977">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-3977">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-3978">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3978">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3980">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-3980">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3982">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-3982">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3984">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-3984">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3986">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-3986">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-3987">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-3987">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-3988">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-3988">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3989">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3989">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-3990">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-3990">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3992">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3992">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3994">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3994">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-3996">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-3997">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-3998">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-3998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-3999">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-3999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4000">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4000">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4001">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4001">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4002">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4002">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4004">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4004">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4006">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4006">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4008">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4008">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4010">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4010">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4012">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4012">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4014">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4014">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4015">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4015">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4017">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4017">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4018">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4018">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4019">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4019">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4020">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4020">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4022">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4022">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4023">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4023">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="f81ea-4025">DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4025">DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="f81ea-4026">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4026">Target</span></span> | <span data-ttu-id="f81ea-4027">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4027">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4028">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4028">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4029">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-4029">16</span></span> |
| <span data-ttu-id="f81ea-4030">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4030">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4032">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4032">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4033">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4033">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4034">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4035">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4036">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4038">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4040">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-4041">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4041">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4043">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4043">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-4044">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4044">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4045">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4045">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4046">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4046">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4047">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4047">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-4048">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4048">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4049">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4049">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4051">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4051">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-4052">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4052">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4053">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4053">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4054">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4054">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4055">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4055">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4057">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4057">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4058">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4058">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4059">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4059">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-4060">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4060">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-4061">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4061">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-4062">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4062">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4063">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4063">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4064">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4064">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4065">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4065">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4066">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4066">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4067">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4067">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4068">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4068">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4070">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4070">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4072">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4072">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4074">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4074">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4076">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4076">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-4077">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4077">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-4078">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4078">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4079">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4079">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4081">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4081">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4082">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4082">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4083">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4083">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4084">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4084">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4086">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4086">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4087">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4087">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="f81ea-4089">DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4089">DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="f81ea-4090">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4090">Target</span></span> | <span data-ttu-id="f81ea-4091">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4091">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4092">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4093">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-4093">16</span></span> |
| <span data-ttu-id="f81ea-4094">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4094">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4096">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4096">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4098">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4098">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4100">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4100">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4101">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4101">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4102">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4102">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4104">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4106">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4108">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4110">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4110">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4112">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4112">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4114">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4114">Shader sample_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4116">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4116">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4117">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4117">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4119">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4119">Shader gather4_c</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4121">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4121">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4123">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4123">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4125">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4125">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4127">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4127">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4129">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4129">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4130">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4130">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4131">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4131">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4132">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4132">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4133">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4133">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4135">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4135">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4137">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4137">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4139">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4139">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4140">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4140">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4141">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4141">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4142">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4142">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4143">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4143">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4144">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4144">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4145">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4145">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4147">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4147">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4149">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4149">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4151">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4151">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4153">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4153">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4155">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4155">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4157">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4157">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4158">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4158">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4160">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4160">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4161">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4161">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4162">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4162">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4163">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4163">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4165">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4165">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4166">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4166">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="f81ea-4168">DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4168">DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="f81ea-4169">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4169">Target</span></span> | <span data-ttu-id="f81ea-4170">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4170">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4171">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4172">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-4172">16</span></span> |
| <span data-ttu-id="f81ea-4173">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4173">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4175">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4175">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4177">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4177">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4179">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4179">Input Assembler Index Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4181">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4182">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4184">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4184">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4186">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4186">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4188">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4188">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4190">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4190">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4192">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4193">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4193">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4194">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4194">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4195">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4195">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-4196">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4196">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4197">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4199">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4199">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-4200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4200">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4202">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4202">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4203">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4203">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4205">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4206">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4207">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4208">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4208">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4210">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4210">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4212">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4212">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4214">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4215">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4217">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4218">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4219">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4220">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4220">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4222">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4222">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4224">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4224">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4226">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4226">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4228">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4228">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-4229">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4229">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4231">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4231">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4232">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4232">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4234">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4235">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4236">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4237">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4237">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4239">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4239">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4240">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4240">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="f81ea-4242">DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4242">DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="f81ea-4243">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4243">Target</span></span> | <span data-ttu-id="f81ea-4244">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4244">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4245">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4245">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4246">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-4246">16</span></span> |
| <span data-ttu-id="f81ea-4247">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4247">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4249">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4251">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4251">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4253">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4253">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4254">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4254">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4255">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4255">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4257">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4259">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4259">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4261">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4261">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4263">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4263">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4265">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4265">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4267">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4267">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4268">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4268">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4269">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4269">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4271">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4271">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4272">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4272">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4274">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4274">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4276">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4278">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4278">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4280">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4280">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4281">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4282">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4283">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4284">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4284">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4286">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4286">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4288">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4288">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4290">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4291">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4292">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4292">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4293">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4294">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4294">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4295">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4295">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4296">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4296">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4298">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4298">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4300">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4300">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4302">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4302">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4304">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4304">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4306">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4306">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4308">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4308">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4309">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4309">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4311">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4311">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4312">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4312">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4313">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4313">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4314">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4314">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4316">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4316">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4317">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4317">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="f81ea-4319">DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4319">DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="f81ea-4320">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4320">Target</span></span> | <span data-ttu-id="f81ea-4321">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4321">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4322">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4323">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-4323">16</span></span> |
| <span data-ttu-id="f81ea-4324">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4324">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4326">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4326">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4328">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4328">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4330">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4331">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4332">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4334">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4336">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4338">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4340">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4340">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4342">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4342">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4343">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4343">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4344">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4344">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4345">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4345">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-4346">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4346">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4347">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4347">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4349">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4349">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-4350">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4350">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4352">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4353">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4354">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4355">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4356">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4357">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4357">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4359">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4359">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4361">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4361">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4363">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4364">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4365">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4365">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4366">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4367">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4367">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4368">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4368">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4369">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4369">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4371">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4371">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4373">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4373">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4375">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4375">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4377">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-4378">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4378">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4380">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4380">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4381">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4381">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4383">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4383">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4384">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4384">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4385">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4385">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4386">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4386">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4388">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4388">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4389">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4389">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="f81ea-4391"><sup>Pc</sup> DXGI_FORMAT_R8_TYPELESS (60)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4391">DXGI_FORMAT_R8_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="f81ea-4392">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4392">Target</span></span> | <span data-ttu-id="f81ea-4393">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4393">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4394">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4395">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-4395">8</span></span> |
| <span data-ttu-id="f81ea-4396">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4396">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4398">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4398">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4399">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4399">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4400">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4401">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4402">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4404">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4406">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4408">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4410">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4410">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-4411">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4411">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4412">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4412">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4413">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4413">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4414">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4414">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-4415">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4415">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4416">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4416">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4418">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4418">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-4419">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4419">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4420">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4420">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4421">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4421">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4422">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4422">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4423">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4423">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4424">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4424">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4425">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4425">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-4426">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4426">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-4427">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4427">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-4428">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4428">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4429">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4429">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4430">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4430">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4431">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4431">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4432">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4432">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4433">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4433">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4434">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4434">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4436">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4437">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4438">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-4439">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-4440">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4440">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-4441">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4442">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4442">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4444">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4445">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4446">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4447">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4447">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4449">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4449">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4450">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4450">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="f81ea-4452">DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4452">DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="f81ea-4453">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4453">Target</span></span> | <span data-ttu-id="f81ea-4454">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4454">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4455">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4455">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4456">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-4456">8</span></span> |
| <span data-ttu-id="f81ea-4457">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4457">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4459">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4459">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4461">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4461">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4463">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4464">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4465">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4467">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4469">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4471">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4471">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4473">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4473">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4475">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4475">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4477">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4477">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4478">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4478">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4479">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4479">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4481">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4481">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4482">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4482">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4484">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4484">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4486">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4486">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4488">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4488">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4490">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4490">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4491">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4491">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4492">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4492">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4493">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4493">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4494">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4494">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4496">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4496">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4498">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4498">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4500">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4501">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4502">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4503">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4504">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4505">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4506">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4506">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4508">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4508">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4510">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4510">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4512">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4512">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4514">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4514">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4516">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4516">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4518">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4518">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4519">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4519">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4521">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4521">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4522">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4522">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4523">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4523">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4524">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4524">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4526">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4526">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4527">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4527">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="f81ea-4529">DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4529">DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="f81ea-4530">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4530">Target</span></span> | <span data-ttu-id="f81ea-4531">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4531">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4532">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4532">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4533">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-4533">8</span></span> |
| <span data-ttu-id="f81ea-4534">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4534">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4536">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4536">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4538">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4538">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4540">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4541">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4542">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4544">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4546">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4548">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4550">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4550">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4552">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4552">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4553">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4553">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4554">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4554">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4555">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4555">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-4556">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4556">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4557">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4557">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4559">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4559">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-4560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4560">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4562">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4562">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4563">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4563">Output Merger Logic Op</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4565">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4566">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4567">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4568">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4568">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4570">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4570">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4572">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4572">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4574">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4575">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4576">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4577">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4578">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4578">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4579">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4579">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4580">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4580">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4582">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4582">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4584">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4584">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4586">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4586">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4588">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4588">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-4589">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4589">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4591">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4591">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4592">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4592">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4594">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4594">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4595">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4595">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4596">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4596">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4597">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4597">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4599">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4599">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4600">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4600">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="f81ea-4602">DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4602">DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="f81ea-4603">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4603">Target</span></span> | <span data-ttu-id="f81ea-4604">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4605">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4606">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-4606">8</span></span> |
| <span data-ttu-id="f81ea-4607">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4607">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4609">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4611">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4611">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4613">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4613">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4614">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4614">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4615">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4615">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4617">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4617">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4619">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4619">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4621">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4621">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4623">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4623">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4625">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4625">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4627">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4627">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4628">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4628">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4629">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4629">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4631">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4631">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4632">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4632">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4634">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4634">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4636">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4638">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4638">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4640">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4640">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4641">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4641">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4642">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4642">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4643">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4643">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4644">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4644">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4646">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4646">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4648">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4648">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4650">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4650">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4651">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4651">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4652">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4652">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4653">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4653">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4654">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4654">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4655">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4655">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4656">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4656">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4658">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4658">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4660">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4660">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4662">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4662">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4664">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4664">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4666">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4666">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4668">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4668">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4669">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4669">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4671">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4671">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4672">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4672">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4673">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4673">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4674">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4674">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4676">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4676">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4677">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4677">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="f81ea-4679">DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4679">DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="f81ea-4680">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4680">Target</span></span> | <span data-ttu-id="f81ea-4681">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4681">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4682">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4682">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4683">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-4683">8</span></span> |
| <span data-ttu-id="f81ea-4684">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4684">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4686">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4686">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4688">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4688">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4690">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4690">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4691">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4691">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4692">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4692">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4694">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4696">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4696">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4698">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4700">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4700">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4702">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4702">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4703">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4703">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4704">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4704">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4705">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4705">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-4706">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4706">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4707">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4707">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4709">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4709">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-4710">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4710">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4712">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4712">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4713">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4713">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4714">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4714">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4715">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4715">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4716">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4716">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4717">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4717">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4719">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4719">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4721">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4721">UAV Typed Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4723">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4723">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4724">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4724">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4725">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4725">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4726">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4726">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4727">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4727">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4728">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4728">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4729">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4729">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4731">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4731">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4733">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4733">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4735">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4735">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4737">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-4738">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4738">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4740">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4741">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4741">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4743">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4744">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4745">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4746">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4746">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4748">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4748">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4749">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4749">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="f81ea-4751">DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4751">DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="f81ea-4752">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4752">Target</span></span> | <span data-ttu-id="f81ea-4753">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4753">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4754">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4755">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-4755">8</span></span> |
| <span data-ttu-id="f81ea-4756">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4756">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4758">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4758">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4759">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4760">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4761">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4762">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4764">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4764">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4766">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4766">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4768">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4768">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4770">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4770">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4772">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4772">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4774">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4774">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4775">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4775">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4776">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4776">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4778">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4778">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4779">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4779">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4781">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4781">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4783">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4785">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4785">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4787">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4787">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4788">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4789">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4790">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4791">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4791">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4793">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4793">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4795">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4795">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4797">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4797">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4798">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4798">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4799">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4799">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4800">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4800">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4801">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4801">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4802">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4802">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4803">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4803">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4805">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4805">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4807">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4807">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4809">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4809">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-4811">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4811">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4813">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4813">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4815">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4815">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4816">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4816">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-4817">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4817">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4818">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4818">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4819">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4819">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4820">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4820">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4822">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4822">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4823">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4823">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="f81ea-4825">DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4825">DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="f81ea-4826">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4826">Target</span></span> | <span data-ttu-id="f81ea-4827">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4827">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4828">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4829">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-4829">32</span></span> |
| <span data-ttu-id="f81ea-4830">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4830">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4832">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4832">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4833">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4833">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4834">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4834">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4835">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4835">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4836">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4836">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4838">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4840">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4840">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4842">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4842">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4844">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4844">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4846">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4846">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4848">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4848">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4849">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4849">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4850">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4850">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4852">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4852">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4853">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4853">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4855">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4855">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-4856">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4856">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4857">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4857">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4858">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4858">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4859">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4859">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4860">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4860">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4861">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4861">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4862">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4862">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-4863">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4863">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-4864">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4864">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-4865">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4865">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4866">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4866">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4867">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4867">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4868">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4868">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4869">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4869">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4870">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4870">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4871">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4871">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4873">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4873">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4874">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4874">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4875">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4875">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-4876">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4876">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-4877">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4877">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-4878">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4878">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4879">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4879">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-4880">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4881">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4882">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4883">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4883">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-4884">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4885">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4885">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="f81ea-4887">DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4887">DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="f81ea-4888">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4888">Target</span></span> | <span data-ttu-id="f81ea-4889">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4889">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4890">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4891">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-4891">16</span></span> |
| <span data-ttu-id="f81ea-4892">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4892">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4894">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4894">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4895">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4896">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4897">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4898">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4900">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4902">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4904">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4906">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4906">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4908">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4908">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4910">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4910">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4911">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4911">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4912">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4912">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4914">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4914">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4915">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4915">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4917">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4917">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-4918">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4918">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4919">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4919">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4920">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4921">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4922">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4923">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4924">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4924">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-4925">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-4926">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-4927">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4928">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4929">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4929">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4930">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4931">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4931">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4932">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4932">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4933">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4933">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4935">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4935">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4936">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4936">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4937">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4937">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-4938">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4938">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-4939">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4939">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-4940">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-4940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-4941">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-4941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-4942">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-4943">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-4944">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-4944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-4945">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-4945">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-4946">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4946">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-4947">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-4947">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="f81ea-4948">DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4948">DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="f81ea-4949">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4949">Target</span></span> | <span data-ttu-id="f81ea-4950">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-4950">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-4951">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-4952">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-4952">16</span></span> |
| <span data-ttu-id="f81ea-4953">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4953">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4955">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-4955">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4956">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-4956">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4957">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-4957">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4958">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-4958">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-4959">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4959">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4961">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4961">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4963">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-4963">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4965">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-4965">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4967">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4967">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4969">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4969">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4971">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4971">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4972">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-4972">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-4973">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-4973">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4975">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-4975">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-4976">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4976">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4978">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-4978">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-4979">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-4979">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4980">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-4980">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4981">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-4981">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-4982">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-4982">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-4983">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-4983">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4984">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4984">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-4985">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-4985">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-4986">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4986">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-4987">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4987">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-4988">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4988">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-4989">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4989">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-4990">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-4990">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-4991">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4991">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-4992">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-4992">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4993">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-4993">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-4994">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-4994">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-4996">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4996">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4997">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-4997">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-4998">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-4998">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-4999">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-4999">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5000">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5000">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5001">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5001">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5002">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5002">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-5003">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5003">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5004">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5004">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5005">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5005">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5006">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5006">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-5007">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5007">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5008">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="f81ea-5009"><sup>PCC</sup> DXGI_FORMAT_BC1_TYPELESS (70)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5009">DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="f81ea-5010">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5010">Target</span></span> | <span data-ttu-id="f81ea-5011">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5012">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5013">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-5013">64</span></span> |
| <span data-ttu-id="f81ea-5014">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5014">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5016">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5017">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5018">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5019">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5021">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5023">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5025">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5027">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5027">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-5028">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5028">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5029">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5029">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5030">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5030">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5031">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5031">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-5032">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5032">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5033">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5033">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5035">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5035">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5036">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5036">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5037">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5037">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5038">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5038">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5039">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5039">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5040">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5040">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5041">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5041">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5042">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5042">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5043">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5043">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5044">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5044">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5045">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5045">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5046">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5046">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5047">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5047">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5048">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5048">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5049">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5049">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5050">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5050">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5051">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5051">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5053">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5054">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5055">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5056">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5057">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5057">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5058">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5059">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5059">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5061">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5061">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5062">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5062">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5063">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5063">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5064">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5064">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5066">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5066">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5067">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5067">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a><span data-ttu-id="f81ea-5069">DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5069">DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="f81ea-5070">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5070">Target</span></span> | <span data-ttu-id="f81ea-5071">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5071">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5072">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5072">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5073">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-5073">64</span></span> |
| <span data-ttu-id="f81ea-5074">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5074">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5076">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5076">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5077">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5077">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5078">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5078">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5079">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5079">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5080">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5080">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5081">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5081">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5083">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5083">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5085">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5085">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5087">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5087">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5089">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5089">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5091">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5091">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5092">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5092">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5093">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5093">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5095">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5095">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5096">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5096">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5098">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5098">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5099">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5100">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5101">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5102">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5103">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5104">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5105">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5105">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5106">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5107">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5108">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5109">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5110">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5111">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5112">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5112">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5113">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5113">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5114">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5114">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5116">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5116">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5117">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5117">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5118">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5118">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5119">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5119">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5120">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5120">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5121">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5122">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5122">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5124">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5125">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5126">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5127">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5127">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5129">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5129">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5130">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5130">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a><span data-ttu-id="f81ea-5132">DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5132">DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="f81ea-5133">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5133">Target</span></span> | <span data-ttu-id="f81ea-5134">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5134">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5135">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5136">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-5136">64</span></span> |
| <span data-ttu-id="f81ea-5137">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5137">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5139">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5139">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5140">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5141">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5142">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5143">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5144">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5146">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5148">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5150">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5150">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5152">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5152">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5154">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5154">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5155">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5155">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5156">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5156">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5158">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5158">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5159">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5159">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5161">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5161">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5162">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5162">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5163">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5163">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5164">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5164">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5165">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5166">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5167">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5168">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5168">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5169">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5169">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5170">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5170">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5171">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5171">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5172">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5172">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5173">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5173">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5174">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5174">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5175">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5175">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5176">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5176">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5177">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5177">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5179">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5180">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5181">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5182">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5183">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5183">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5184">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5185">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5185">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5187">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5187">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5188">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5188">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5189">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5189">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5190">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5190">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5192">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5192">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5193">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5193">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="f81ea-5195"><sup>PCC</sup> DXGI_FORMAT_BC2_TYPELESS (73)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5195">DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="f81ea-5196">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5196">Target</span></span> | <span data-ttu-id="f81ea-5197">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5197">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5198">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5198">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5199">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-5199">128</span></span> |
| <span data-ttu-id="f81ea-5200">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5200">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5202">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5202">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5203">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5204">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5205">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5206">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5207">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5209">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5209">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5211">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5211">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5213">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5213">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-5214">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5214">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5215">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5215">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5216">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5216">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5217">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5217">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-5218">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5218">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5219">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5219">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5221">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5221">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5222">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5222">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5223">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5223">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5224">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5224">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5225">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5225">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5226">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5226">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5227">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5227">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5228">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5228">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5229">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5229">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5230">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5230">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5231">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5231">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5232">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5232">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5233">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5233">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5234">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5234">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5235">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5235">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5236">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5236">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5237">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5237">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5239">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5239">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5240">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5240">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5241">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5241">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5242">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5242">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5243">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5243">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5244">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5244">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5245">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5245">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5247">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5247">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5248">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5248">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5249">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5249">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5250">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5250">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5252">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5252">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5253">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5253">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a><span data-ttu-id="f81ea-5255">DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5255">DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="f81ea-5256">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5256">Target</span></span> | <span data-ttu-id="f81ea-5257">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5258">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5259">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-5259">128</span></span> |
| <span data-ttu-id="f81ea-5260">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5260">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5262">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5263">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5264">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5265">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5267">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5269">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5271">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5273">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5273">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5275">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5275">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5277">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5277">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5278">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5278">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5279">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5279">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5281">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5281">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5282">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5282">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5284">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5284">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5285">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5285">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5286">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5286">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5287">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5287">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5288">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5289">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5290">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5291">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5291">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5292">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5293">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5294">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5295">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5296">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5296">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5297">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5298">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5298">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5299">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5299">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5300">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5300">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5302">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5303">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5304">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5305">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5306">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5306">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5307">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5308">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5308">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5310">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5310">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5311">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5311">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5312">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5312">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5313">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5313">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5315">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5315">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5316">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5316">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a><span data-ttu-id="f81ea-5318">DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5318">DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="f81ea-5319">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5319">Target</span></span> | <span data-ttu-id="f81ea-5320">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5320">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5321">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5321">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5322">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-5322">128</span></span> |
| <span data-ttu-id="f81ea-5323">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5323">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5325">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5325">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5326">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5326">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5327">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5328">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5328">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5329">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5329">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5330">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5330">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5332">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5332">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5334">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5336">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5336">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5338">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5338">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5340">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5340">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5341">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5341">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5342">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5342">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5344">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5344">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5345">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5345">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5347">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5347">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5348">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5348">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5349">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5349">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5350">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5350">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5351">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5351">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5352">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5352">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5353">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5353">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5354">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5354">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5355">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5355">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5356">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5357">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5358">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5359">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5360">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5361">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5362">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5363">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5363">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5365">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5366">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5367">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5368">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5369">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5369">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5370">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5371">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5371">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5373">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5373">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5374">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5374">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5375">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5375">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5376">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5376">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5378">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5378">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5379">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5379">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="f81ea-5381"><sup>PCC</sup> DXGI_FORMAT_BC3_TYPELESS (76)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5381">DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="f81ea-5382">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5382">Target</span></span> | <span data-ttu-id="f81ea-5383">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5383">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5384">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5385">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-5385">128</span></span> |
| <span data-ttu-id="f81ea-5386">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5386">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5388">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5388">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5389">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5389">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5390">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5391">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5392">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5393">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5395">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5397">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5399">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5399">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-5400">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5401">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5401">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5402">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5402">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5403">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5403">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-5404">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5404">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5405">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5407">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5407">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5408">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5408">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5409">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5409">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5410">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5410">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5411">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5411">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5412">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5412">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5413">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5413">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5414">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5414">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5415">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5415">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5416">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5416">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5417">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5417">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5418">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5418">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5419">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5419">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5420">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5420">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5421">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5421">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5422">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5422">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5423">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5423">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5425">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5426">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5427">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5428">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5429">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5429">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5430">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5431">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5431">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5433">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5433">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5434">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5434">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5435">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5435">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5436">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5436">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5438">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5438">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5439">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5439">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a><span data-ttu-id="f81ea-5441">DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5441">DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="f81ea-5442">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5442">Target</span></span> | <span data-ttu-id="f81ea-5443">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5443">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5444">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5444">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5445">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-5445">128</span></span> |
| <span data-ttu-id="f81ea-5446">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5446">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5448">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5448">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5449">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5450">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5451">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5452">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5453">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5455">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5457">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5457">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5459">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5459">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5461">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5461">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5463">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5463">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5464">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5464">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5465">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5465">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5467">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5467">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5468">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5468">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5470">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5470">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5471">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5471">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5472">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5472">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5473">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5473">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5474">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5474">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5475">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5475">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5476">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5476">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5477">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5477">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5478">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5478">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5479">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5479">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5480">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5480">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5481">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5481">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5482">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5482">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5483">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5483">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5484">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5484">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5485">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5485">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5486">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5486">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5488">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5489">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5490">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5491">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5492">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5492">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5493">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5494">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5494">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5496">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5496">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5497">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5497">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5498">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5498">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5499">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5499">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5501">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5501">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5502">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5502">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a><span data-ttu-id="f81ea-5504">DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5504">DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="f81ea-5505">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5505">Target</span></span> | <span data-ttu-id="f81ea-5506">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5506">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5507">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5507">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5508">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-5508">128</span></span> |
| <span data-ttu-id="f81ea-5509">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5509">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5511">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5511">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5512">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5512">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5513">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5513">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5514">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5514">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5515">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5515">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5516">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5518">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5520">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5522">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5522">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5524">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5524">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5526">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5526">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5527">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5527">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5528">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5528">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5530">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5530">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5531">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5531">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5533">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5533">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5534">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5535">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5536">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5537">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5538">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5539">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5540">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5540">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5541">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5542">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5543">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5544">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5545">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5546">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5547">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5548">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5549">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5549">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5551">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5552">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5553">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5554">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5555">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5555">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5556">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5557">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5557">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5559">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5560">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5561">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5562">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5562">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5564">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5564">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5565">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5565">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="f81ea-5567"><sup>PCC</sup> DXGI_FORMAT_BC4_TYPELESS (79)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5567">DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="f81ea-5568">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5568">Target</span></span> | <span data-ttu-id="f81ea-5569">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5569">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5570">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5570">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5571">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-5571">64</span></span> |
| <span data-ttu-id="f81ea-5572">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5572">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5574">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5574">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5575">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5575">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5576">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5576">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5577">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5577">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5578">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5578">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5579">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5579">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5581">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5581">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5583">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5583">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5585">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5585">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-5586">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5586">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5587">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5587">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5588">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5588">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5589">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5589">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-5590">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5590">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5591">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5591">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5593">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5593">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5594">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5594">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5595">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5595">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5596">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5596">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5597">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5597">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5598">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5598">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5599">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5599">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5600">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5600">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5601">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5601">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5602">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5602">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5603">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5603">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5604">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5604">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5605">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5605">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5606">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5606">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5607">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5607">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5608">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5608">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5609">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5609">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5611">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5611">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5612">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5612">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5613">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5613">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5614">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5614">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5615">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5615">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5616">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5616">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5617">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5617">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5619">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5619">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5620">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5620">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5621">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5621">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5622">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5622">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-5623">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5623">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5624">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5624">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a><span data-ttu-id="f81ea-5626">DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5626">DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="f81ea-5627">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5627">Target</span></span> | <span data-ttu-id="f81ea-5628">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5628">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5629">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5629">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5630">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-5630">64</span></span> |
| <span data-ttu-id="f81ea-5631">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5631">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5633">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5633">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5634">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5634">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5635">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5635">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5636">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5636">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5637">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5637">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5638">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5640">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5642">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5644">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5644">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5646">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5646">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5648">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5648">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5649">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5649">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5650">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5650">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5652">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5652">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5653">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5653">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5655">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5655">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5656">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5657">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5657">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5658">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5658">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5659">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5659">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5660">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5660">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5661">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5661">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5662">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5662">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5663">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5663">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5664">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5664">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5665">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5665">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5666">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5666">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5667">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5667">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5668">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5668">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5669">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5669">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5670">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5670">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5671">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5671">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5673">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5673">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5674">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5674">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5675">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5675">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5676">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5676">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5677">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5677">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5678">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5678">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5679">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5679">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5681">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5681">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5682">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5682">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5683">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5683">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5684">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5684">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-5685">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5685">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5686">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5686">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a><span data-ttu-id="f81ea-5688">DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5688">DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="f81ea-5689">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5689">Target</span></span> | <span data-ttu-id="f81ea-5690">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5690">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5691">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5691">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5692">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-5692">64</span></span> |
| <span data-ttu-id="f81ea-5693">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5693">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5695">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5695">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5696">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5696">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5697">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5697">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5698">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5698">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5699">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5699">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5700">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5700">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5702">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5702">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5704">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5704">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5706">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5706">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5708">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5708">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5710">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5710">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5711">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5711">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5712">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5712">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5714">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5714">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5715">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5717">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5717">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5718">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5719">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5719">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5720">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5720">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5721">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5721">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5722">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5722">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5723">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5723">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5724">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5724">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5725">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5725">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5726">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5726">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5727">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5727">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5728">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5728">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5729">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5729">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5730">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5730">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5731">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5731">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5732">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5732">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5733">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5733">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5735">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5735">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5736">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5736">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5737">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5737">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5738">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5738">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5739">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5739">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5740">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5741">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5741">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5743">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5744">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5745">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5746">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5746">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-5747">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5747">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5748">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5748">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="f81ea-5750"><sup>PCC</sup> DXGI_FORMAT_BC5_TYPELESS (82)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5750">DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="f81ea-5751">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5751">Target</span></span> | <span data-ttu-id="f81ea-5752">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5752">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5753">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5753">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5754">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-5754">128</span></span> |
| <span data-ttu-id="f81ea-5755">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5755">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5757">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5757">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5758">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5759">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5760">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5761">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5762">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5764">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5766">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5766">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5768">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5768">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-5769">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5769">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5770">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5770">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5771">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5771">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5772">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5772">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-5773">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5773">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5774">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5774">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5776">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5776">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5777">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5777">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5778">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5778">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5779">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5779">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5780">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5780">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5781">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5781">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5782">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5782">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5783">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5783">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5784">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5784">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5785">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5785">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5786">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5786">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5787">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5787">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5788">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5788">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5789">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5789">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5790">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5790">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5791">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5791">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5792">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5792">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5794">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5794">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5795">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5795">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5796">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5796">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5797">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5797">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5798">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5798">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5799">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5799">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5800">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5800">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5802">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5802">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5803">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5803">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5804">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5804">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5805">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5805">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-5806">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5806">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5807">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5807">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a><span data-ttu-id="f81ea-5809">DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5809">DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="f81ea-5810">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5810">Target</span></span> | <span data-ttu-id="f81ea-5811">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5811">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5812">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5812">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5813">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-5813">128</span></span> |
| <span data-ttu-id="f81ea-5814">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5814">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5816">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5816">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5817">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5817">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5818">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5818">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5819">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5819">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5820">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5820">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5821">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5821">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5823">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5823">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5825">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5825">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5827">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5827">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5829">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5829">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5831">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5831">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5832">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5832">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5833">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5833">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5835">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5835">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5836">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5838">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5838">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5839">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5840">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5841">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5842">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5843">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5844">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5845">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5845">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5846">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5847">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5848">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5849">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5850">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5851">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5852">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5852">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5853">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5853">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5854">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5854">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5856">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5857">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5858">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5859">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5860">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5860">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5861">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5862">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5862">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5864">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5864">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5865">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5865">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5866">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5866">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5867">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5867">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-5868">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5868">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5869">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5869">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a><span data-ttu-id="f81ea-5871">DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5871">DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="f81ea-5872">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5872">Target</span></span> | <span data-ttu-id="f81ea-5873">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5873">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5874">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5875">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-5875">128</span></span> |
| <span data-ttu-id="f81ea-5876">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5876">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5878">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5878">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5879">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5880">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5881">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5882">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-5883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5883">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5885">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5887">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5887">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5889">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5889">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5891">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5891">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5893">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5893">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5894">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5894">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5895">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5895">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5897">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5897">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5898">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5898">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5900">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5900">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-5901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5901">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5902">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5903">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5904">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5905">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5906">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5907">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5907">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-5908">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-5909">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-5910">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5911">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5912">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5913">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5914">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5914">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5915">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5915">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5916">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5916">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5918">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5918">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5919">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5919">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-5920">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5920">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-5921">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5921">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-5922">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5922">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-5923">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5923">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-5924">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-5924">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5926">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5926">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-5927">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5927">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-5928">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-5928">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-5929">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-5929">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-5930">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5930">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-5931">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-5931">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="f81ea-5933">DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5933">DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="f81ea-5934">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5934">Target</span></span> | <span data-ttu-id="f81ea-5935">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-5935">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-5936">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5936">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-5937">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-5937">16</span></span> |
| <span data-ttu-id="f81ea-5938">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5938">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5940">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-5940">Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-5942">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-5942">Input Assembler Vertex Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-5944">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-5944">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5945">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-5945">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-5946">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5946">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5948">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5948">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-5950">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-5952">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5954">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5954">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5956">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5956">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5958">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5958">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5959">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-5959">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-5960">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-5960">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5962">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-5962">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-5963">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5963">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5965">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-5965">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-5967">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5969">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-5969">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5971">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-5971">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-5972">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-5972">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-5973">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-5973">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5974">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5974">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-5975">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-5975">Typed UAV</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-5977">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5977">UAV Typed Store</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-5979">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5979">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-5981">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5981">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-5982">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5982">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-5983">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-5983">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-5984">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5984">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-5985">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-5985">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5986">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-5986">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-5987">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-5987">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5989">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5989">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5991">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-5991">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5993">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-5993">Other Multisample Count RT</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5995">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5995">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5997">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-5997">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-5999">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-5999">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6000">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6000">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-6001">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6001">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6002">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6002">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6003">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6003">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6004">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6004">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-6005">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6005">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6006">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6006">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="f81ea-6008">DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6008">DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="f81ea-6009">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6009">Target</span></span> | <span data-ttu-id="f81ea-6010">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6010">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6011">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6011">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6012">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-6012">16</span></span> |
| <span data-ttu-id="f81ea-6013">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6013">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6015">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6015">Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6017">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6017">Input Assembler Vertex Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6019">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6019">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6020">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6020">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6021">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6021">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6023">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6023">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6025">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6025">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6027">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6027">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6029">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6029">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6031">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6031">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6033">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6033">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6034">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6034">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6035">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6035">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6037">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6037">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6038">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6038">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6040">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6040">Mipmap Auto- Generation</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6042">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6044">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6044">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6046">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6046">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6047">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6047">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6048">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6048">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6049">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6049">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6050">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6050">Typed UAV</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6052">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6052">UAV Typed Store</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6054">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6054">UAV Typed Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6056">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6057">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6058">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6059">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6060">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6060">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6061">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6061">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6062">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6062">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6064">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6064">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6066">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6066">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6068">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6068">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6070">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6070">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6072">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6072">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6074">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6074">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6075">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6075">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-6076">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6076">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6077">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6077">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6078">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6078">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6079">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6079">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-6080">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6080">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6081">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6081">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="f81ea-6083"><sup>Pc</sup> DXGI_FORMAT_B8G8R8A8_TYPELESS (90)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6083">DXGI_FORMAT_B8G8R8A8_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="f81ea-6084">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6084">Target</span></span> | <span data-ttu-id="f81ea-6085">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6085">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6086">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6086">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6087">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-6087">32</span></span> |
| <span data-ttu-id="f81ea-6088">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6088">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6090">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6090">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6091">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6091">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6092">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6092">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6093">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6093">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6094">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6094">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6096">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6096">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6098">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6098">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6100">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6100">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6102">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6102">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-6103">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6103">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6104">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6104">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6105">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6105">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6106">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6106">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-6107">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6107">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6108">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6108">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6110">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6110">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-6111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6111">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6112">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6113">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6114">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6115">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6116">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6117">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6117">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6118">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6119">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6120">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6121">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6122">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6123">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6124">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6124">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6125">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6125">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6126">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6126">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6128">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6128">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6129">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6129">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6130">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6130">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6131">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6131">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6132">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6132">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6133">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6133">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6134">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6134">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6136">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6137">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6138">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6139">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6139">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6141">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6141">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6142">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6142">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="f81ea-6144">DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6144">DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="f81ea-6145">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6145">Target</span></span> | <span data-ttu-id="f81ea-6146">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6146">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6147">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6148">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-6148">32</span></span> |
| <span data-ttu-id="f81ea-6149">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6149">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6151">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6151">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6153">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6153">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6155">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6155">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6156">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6156">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6157">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6157">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6159">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6159">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6161">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6161">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6163">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6165">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6165">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6167">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6167">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6169">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6169">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6170">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6170">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6171">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6171">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6173">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6173">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6174">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6174">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6176">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6176">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6178">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6178">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6180">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6180">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6182">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6182">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6183">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6183">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6184">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6184">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6185">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6185">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6186">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6186">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6187">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6187">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6188">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6188">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6189">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6189">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6190">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6190">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6191">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6191">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6192">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6192">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6193">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6193">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6194">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6194">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6195">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6195">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6197">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6197">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6199">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6199">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6201">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6201">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6203">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6203">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6205">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6205">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6207">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6207">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6209">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6209">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6211">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6211">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6212">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6212">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6214">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6214">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6216">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6216">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6218">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6218">BackBuffer Castable Even Fully Typed</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6220">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6220">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="f81ea-6222">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6222">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="f81ea-6223">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6223">Target</span></span> | <span data-ttu-id="f81ea-6224">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6224">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6225">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6225">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6226">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-6226">32</span></span> |
| <span data-ttu-id="f81ea-6227">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6227">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6229">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6229">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6230">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6230">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6231">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6232">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6233">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6235">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6237">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6239">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6241">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6241">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6243">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6243">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6245">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6245">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6246">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6246">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6247">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6247">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6249">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6249">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6250">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6250">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6252">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6252">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6254">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6254">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6256">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6256">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6258">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6258">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6259">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6259">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6260">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6260">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6261">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6261">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6262">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6262">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6263">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6263">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6264">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6264">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6265">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6265">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6266">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6266">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6267">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6267">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6268">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6268">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6269">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6269">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6270">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6270">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6271">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6271">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6273">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6273">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6275">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6275">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6277">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6277">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6279">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6279">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6281">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6281">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6283">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6283">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6285">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6285">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6287">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6287">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6288">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6288">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6290">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6290">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6292">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6292">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6294">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6294">BackBuffer Castable Even Fully Typed</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6296">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6296">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="f81ea-6298"><sup>Pc</sup> DXGI_FORMAT_B8G8R8X8_TYPELESS (92)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6298">DXGI_FORMAT_B8G8R8X8_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="f81ea-6299">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6299">Target</span></span> | <span data-ttu-id="f81ea-6300">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6300">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6301">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6301">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6302">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-6302">32</span></span> |
| <span data-ttu-id="f81ea-6303">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6303">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6305">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6305">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6306">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6306">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6307">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6307">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6308">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6308">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6309">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6309">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6311">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6311">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6313">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6313">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6315">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6315">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6317">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6317">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-6318">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6318">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6319">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6319">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6320">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6320">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6321">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6321">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-6322">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6322">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6323">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6323">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6325">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6325">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-6326">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6326">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6327">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6327">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6328">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6328">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6329">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6329">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6330">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6330">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6331">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6331">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6332">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6332">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6333">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6333">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6334">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6334">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6335">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6335">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6336">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6336">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6337">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6337">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6338">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6338">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6339">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6339">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6340">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6340">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6341">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6341">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6343">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6343">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6344">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6344">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6345">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6345">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6346">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6347">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6347">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6348">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6348">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6349">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6349">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6351">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6351">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6352">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6352">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6353">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6353">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6354">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6354">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6356">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6356">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6357">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6357">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="f81ea-6359">DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6359">DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="f81ea-6360">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6360">Target</span></span> | <span data-ttu-id="f81ea-6361">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6361">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6362">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6362">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6363">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-6363">32</span></span> |
| <span data-ttu-id="f81ea-6364">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6364">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6366">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6366">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6368">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6368">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6370">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6370">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6371">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6371">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6372">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6372">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6374">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6374">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6376">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6376">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6378">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6378">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6380">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6380">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6382">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6382">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6384">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6384">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6385">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6385">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6386">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6386">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6388">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6388">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6389">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6389">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6391">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6391">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6393">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6393">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6395">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6395">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6397">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6398">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6399">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6400">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6401">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6401">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6402">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6403">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6404">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6405">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6406">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6407">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6408">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6408">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6409">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6409">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6410">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6410">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6412">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6412">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6414">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6414">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6416">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6416">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6418">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6418">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6420">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6420">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6422">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6422">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6423">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6423">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6425">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6425">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6426">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6426">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6428">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6428">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6430">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6430">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6432">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6432">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6433">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6433">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="f81ea-6435">DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6435">DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="f81ea-6436">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6436">Target</span></span> | <span data-ttu-id="f81ea-6437">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6437">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6438">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6439">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-6439">32</span></span> |
| <span data-ttu-id="f81ea-6440">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6440">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6442">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6442">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6443">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6443">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6444">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6444">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6445">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6445">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6446">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6446">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6448">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6450">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6450">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6452">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6454">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6454">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6456">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6456">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6458">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6458">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6459">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6459">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6460">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6460">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6462">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6462">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6463">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6463">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6465">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6465">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6467">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6469">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6469">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6471">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6471">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6472">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6472">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6473">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6473">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6474">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6474">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6475">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6475">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6476">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6476">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6477">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6477">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6478">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6478">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6479">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6479">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6480">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6480">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6481">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6481">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6482">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6482">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6483">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6483">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6484">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6484">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6486">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6486">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6488">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6488">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6490">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6490">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6492">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6492">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6494">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6494">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6496">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6497">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6497">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6499">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6499">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6500">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6500">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6501">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6501">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6502">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6502">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6504">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6504">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6505">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6505">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a><span data-ttu-id="f81ea-6507"><sup>PCC</sup> DXGI_FORMAT_BC6H_TYPELESS (94)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6507">DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)</span></span>
| <span data-ttu-id="f81ea-6508">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6508">Target</span></span> | <span data-ttu-id="f81ea-6509">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6509">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6510">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6510">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6511">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-6511">128</span></span> |
| <span data-ttu-id="f81ea-6512">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6512">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6514">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6514">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6515">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6515">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6516">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6516">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6517">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6517">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6518">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6518">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-6519">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6519">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6521">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6521">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6523">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6525">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6525">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-6526">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6526">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6527">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6527">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6528">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6528">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6529">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6529">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-6530">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6530">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6531">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6531">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6533">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6533">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-6534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6534">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6535">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6536">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6537">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6538">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6539">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6540">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6540">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6541">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6542">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6543">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6544">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6545">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6546">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6547">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6548">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6549">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6549">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6551">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6552">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6553">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6554">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6555">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6555">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6556">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6557">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6557">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6559">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6560">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6561">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6562">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6562">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-6563">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6563">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6564">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6564">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a><span data-ttu-id="f81ea-6566">DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6566">DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)</span></span>
| <span data-ttu-id="f81ea-6567">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6567">Target</span></span> | <span data-ttu-id="f81ea-6568">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6568">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6569">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6569">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6570">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-6570">128</span></span> |
| <span data-ttu-id="f81ea-6571">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6571">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6573">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6573">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6574">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6574">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6575">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6575">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6576">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6576">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6577">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6577">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-6578">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6578">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6580">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6580">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6582">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6582">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6584">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6584">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6586">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6586">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6588">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6588">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6589">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6589">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6590">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6590">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6592">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6592">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6593">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6593">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6595">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6595">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-6596">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6596">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6597">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6597">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6598">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6598">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6599">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6599">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6600">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6600">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6601">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6601">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6602">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6602">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6603">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6603">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6604">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6604">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6605">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6605">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6606">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6606">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6607">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6607">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6608">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6608">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6609">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6609">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6610">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6610">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6611">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6611">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6613">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6613">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6614">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6614">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6615">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6615">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6616">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6616">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6617">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6617">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6618">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6618">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6619">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6619">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6621">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6622">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6622">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6623">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6623">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6624">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6624">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-6625">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6625">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6626">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6626">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a><span data-ttu-id="f81ea-6628">DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6628">DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)</span></span>
| <span data-ttu-id="f81ea-6629">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6629">Target</span></span> | <span data-ttu-id="f81ea-6630">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6630">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6631">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6632">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-6632">128</span></span> |
| <span data-ttu-id="f81ea-6633">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6633">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6635">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6635">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6636">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6637">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6638">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6639">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-6640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6640">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6642">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6644">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6646">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6646">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6648">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6648">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6650">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6650">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6651">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6651">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6652">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6652">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6654">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6654">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6655">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6655">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6657">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6657">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-6658">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6658">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6659">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6659">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6660">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6661">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6662">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6663">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6664">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6664">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6665">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6666">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6667">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6668">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6669">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6669">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6670">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6671">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6671">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6672">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6672">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6673">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6673">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6675">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6675">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6676">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6676">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6677">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6677">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6678">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6678">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6679">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6679">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6680">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6680">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6681">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6681">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6683">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6683">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6684">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6684">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6685">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6685">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6686">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6686">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-6687">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6687">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6688">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6688">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a><span data-ttu-id="f81ea-6690"><sup>PCC</sup> DXGI_FORMAT_BC7_TYPELESS (97)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6690">DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)</span></span>
| <span data-ttu-id="f81ea-6691">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6691">Target</span></span> | <span data-ttu-id="f81ea-6692">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6692">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6693">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6693">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6694">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-6694">128</span></span> |
| <span data-ttu-id="f81ea-6695">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6695">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6697">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6697">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6698">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6698">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6699">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6699">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6700">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6700">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6701">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6701">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-6702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6702">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6704">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6706">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6708">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6708">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-6709">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6709">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6710">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6710">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6711">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6711">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6712">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6712">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-6713">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6713">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6714">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6714">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6716">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6716">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-6717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6717">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6718">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6719">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6720">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6721">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6722">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6723">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6723">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6724">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6725">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6726">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6727">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6728">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6729">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6730">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6730">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6731">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6731">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6732">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6732">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6734">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6734">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6735">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6735">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6736">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6736">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6737">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6738">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6738">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6739">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6739">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6740">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6740">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6742">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6742">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6743">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6743">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6744">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6744">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6745">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6745">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-6746">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6746">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6747">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6747">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a><span data-ttu-id="f81ea-6749">DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6749">DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)</span></span>
| <span data-ttu-id="f81ea-6750">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6750">Target</span></span> | <span data-ttu-id="f81ea-6751">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6751">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6752">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6752">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6753">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-6753">128</span></span> |
| <span data-ttu-id="f81ea-6754">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6754">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6756">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6756">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6757">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6757">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6758">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6758">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6759">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6759">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6760">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6760">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-6761">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6761">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6763">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6765">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6767">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6767">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6769">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6769">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6771">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6771">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6772">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6772">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6773">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6773">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6775">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6775">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6776">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6776">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6778">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6778">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-6779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6779">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6780">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6780">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6781">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6781">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6782">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6782">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6783">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6783">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6784">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6784">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6785">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6785">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6786">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6786">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6787">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6787">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6788">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6789">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6790">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6791">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6792">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6793">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6794">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6794">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6796">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6796">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6797">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6797">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6798">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6798">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6799">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6799">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6800">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6800">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6801">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6801">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6802">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6802">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6804">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6804">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6805">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6805">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6806">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6806">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6807">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6807">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-6808">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6808">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6809">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6809">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a><span data-ttu-id="f81ea-6811">DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6811">DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)</span></span>
| <span data-ttu-id="f81ea-6812">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6812">Target</span></span> | <span data-ttu-id="f81ea-6813">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6813">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6814">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6814">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6815">128</span><span class="sxs-lookup"><span data-stu-id="f81ea-6815">128</span></span> |
| <span data-ttu-id="f81ea-6816">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6816">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6818">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6818">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6819">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6819">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6820">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6820">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6821">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6821">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6822">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6822">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-6823">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6823">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6825">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6825">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6827">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6829">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6829">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6831">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6831">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6833">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6833">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6834">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6834">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6835">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6835">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6837">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6837">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6838">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6838">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6840">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6840">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6842">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6843">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6844">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6845">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6846">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6847">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-6848">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-6849">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6850">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6851">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6852">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6852">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6853">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6854">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6854">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6855">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6855">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6856">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6856">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6858">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6859">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6860">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6861">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6862">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6863">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6864">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6864">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6866">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-6867">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6867">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f81ea-6868">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-6869">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-6870">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6871">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6871">Tiled Resource</span></span> | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="f81ea-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="f81ea-6874">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6874">Target</span></span> | <span data-ttu-id="f81ea-6875">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6875">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6876">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6877">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-6877">32</span></span> |
| <span data-ttu-id="f81ea-6878">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6878">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6880">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6880">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6881">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6881">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6882">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6882">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6883">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6883">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6884">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6884">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-6885">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6885">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6887">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6887">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-6888">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6888">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-6889">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6889">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6891">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6891">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6893">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6893">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6894">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6894">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6895">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6895">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6897">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6897">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6898">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6898">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6900">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6900">Mipmap Auto- Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6902">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6902">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6904">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6904">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6906">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6906">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6907">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6907">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6908">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6908">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6909">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6909">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6910">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6910">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6912">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6912">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6914">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6914">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6915">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6915">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6916">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6916">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6917">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6917">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6918">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6918">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6919">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6919">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6920">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6920">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6921">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6921">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6923">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6923">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6924">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6924">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6925">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6925">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6926">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6926">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6927">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6927">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6928">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6928">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6929">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6929">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-6930">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6930">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6932">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6932">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6934">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6934">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6936">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6936">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6938">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6938">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-6939">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-6939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="f81ea-6940">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6940">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="f81ea-6941">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6941">Target</span></span> | <span data-ttu-id="f81ea-6942">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-6942">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-6943">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-6944">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-6944">32</span></span> |
| <span data-ttu-id="f81ea-6945">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6945">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6947">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-6947">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6948">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-6948">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6949">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-6949">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6950">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-6950">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-6951">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6951">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-6952">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6952">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6954">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-6954">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-6955">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-6955">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-6956">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6956">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6958">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6958">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6960">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6960">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6961">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-6961">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-6962">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-6962">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6964">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-6964">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-6965">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6965">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-6966">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-6966">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-6967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-6967">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6968">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-6968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6969">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-6969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-6970">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-6970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-6971">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-6971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6972">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-6973">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-6973">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6975">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6975">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6977">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6977">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-6978">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6978">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-6979">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6979">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-6980">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-6980">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-6981">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6981">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-6982">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-6982">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6983">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-6983">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-6984">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-6984">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-6986">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6986">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6987">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-6987">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-6988">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-6988">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-6989">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6989">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-6990">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-6990">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-6991">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-6991">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-6992">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-6992">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-6993">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6993">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6995">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6995">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6997">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-6997">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-6999">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-6999">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7001">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7001">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7002">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7002">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="f81ea-7003">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7003">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="f81ea-7004">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7004">Target</span></span> | <span data-ttu-id="f81ea-7005">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7005">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7006">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7006">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7007">64</span><span class="sxs-lookup"><span data-stu-id="f81ea-7007">64</span></span> |
| <span data-ttu-id="f81ea-7008">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7008">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7010">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7010">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7011">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7011">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7012">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7012">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7013">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7013">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7014">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7014">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7015">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7015">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7017">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7017">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7018">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7018">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7019">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7019">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7021">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7021">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7023">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7023">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7024">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7024">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7025">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7025">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7027">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7027">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7028">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7028">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7030">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7030">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7031">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7031">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7032">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7032">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7033">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7033">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7034">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7034">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7035">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7035">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7036">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7036">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7037">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7037">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7039">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7039">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7041">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7041">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7042">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7042">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7043">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7043">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7044">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7044">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7045">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7045">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7046">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7046">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7047">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7047">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7048">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7048">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7050">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7050">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7051">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7051">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7052">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7052">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7053">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7053">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7054">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7054">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7055">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7055">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7056">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7056">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7057">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7057">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7059">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7059">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7061">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7061">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7063">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7063">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7065">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7065">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7066">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7066">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="f81ea-7067">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7067">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="f81ea-7068">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7068">Target</span></span> | <span data-ttu-id="f81ea-7069">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7069">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7070">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7070">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7071">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-7071">8</span></span> |
| <span data-ttu-id="f81ea-7072">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7072">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7074">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7074">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7075">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7075">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7076">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7076">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7077">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7077">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7078">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7078">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7079">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7079">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7081">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7081">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7082">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7082">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7083">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7083">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7085">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7085">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7087">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7087">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7088">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7088">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7089">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7089">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7091">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7091">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7092">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7092">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7093">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7093">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7094">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7094">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7096">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7096">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7098">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7099">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7100">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7101">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7102">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7102">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7104">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7104">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7106">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7106">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7107">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7107">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7108">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7108">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7109">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7109">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7110">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7110">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7111">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7111">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7112">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7112">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7113">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7113">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7115">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7116">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7117">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7118">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7119">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7119">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7120">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7121">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7122">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7122">Video Decoder Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7124">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7124">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7126">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7126">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7128">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7128">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7130">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7130">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7131">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7131">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="f81ea-7132">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7132">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="f81ea-7133">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7133">Target</span></span> | <span data-ttu-id="f81ea-7134">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7134">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7135">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7136">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-7136">16</span></span> |
| <span data-ttu-id="f81ea-7137">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7137">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7139">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7139">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7140">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7141">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7142">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7143">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7144">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7146">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7147">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7147">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7148">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7148">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7150">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7150">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7152">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7152">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7153">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7153">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7154">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7154">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7156">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7156">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7157">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7157">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7158">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7158">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7159">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7159">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7161">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7161">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7163">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7164">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7165">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7166">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7167">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7167">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7169">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7169">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7171">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7172">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7173">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7175">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7176">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7176">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7177">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7177">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7178">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7178">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7180">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7181">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7182">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7183">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7184">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7184">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7185">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7186">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7186">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7187">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7187">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7189">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7189">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7191">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7191">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7193">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7193">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7195">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7195">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7196">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7196">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="f81ea-7197">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7197">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="f81ea-7198">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7198">Target</span></span> | <span data-ttu-id="f81ea-7199">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7199">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7200">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7200">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7201">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-7201">16</span></span> |
| <span data-ttu-id="f81ea-7202">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7202">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7204">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7204">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7205">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7205">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7206">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7206">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7207">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7207">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7208">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7208">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7209">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7209">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7211">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7211">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7212">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7212">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7213">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7213">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7215">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7215">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7217">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7217">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7218">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7218">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7219">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7219">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7221">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7221">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7222">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7222">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7223">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7223">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7224">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7224">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7226">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7226">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7228">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7228">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7229">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7229">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7230">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7230">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7231">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7231">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7232">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7232">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7234">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7234">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7236">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7237">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7238">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7239">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7240">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7241">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7241">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7242">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7242">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7243">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7243">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7245">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7246">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7247">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7248">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7249">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7249">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7250">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7251">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7252">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7252">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7254">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7254">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7256">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7256">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7258">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7258">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7260">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7260">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7261">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7261">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="f81ea-7262">DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7262">DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="f81ea-7263">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7263">Target</span></span> | <span data-ttu-id="f81ea-7264">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7264">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7265">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7265">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7266">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-7266">8</span></span> |
| <span data-ttu-id="f81ea-7267">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7267">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7269">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7269">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7270">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7270">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7271">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7271">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7272">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7272">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7273">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7273">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7274">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7274">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7276">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7276">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7277">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7277">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7278">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7278">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-7279">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7279">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7280">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7280">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7281">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7281">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7282">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7282">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-7283">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7283">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7284">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7284">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7285">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7285">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7286">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7286">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7287">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7287">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7288">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7288">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7289">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7289">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7290">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7290">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7291">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7291">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7292">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7292">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-7293">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7293">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-7294">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7294">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7295">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7295">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7296">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7296">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7297">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7297">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7298">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7298">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7299">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7299">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7300">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7300">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7301">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7301">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f81ea-7302">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7303">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7304">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7305">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7306">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7306">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7307">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7308">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7308">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7309">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7309">Video Decoder Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7311">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7311">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7313">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7313">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7315">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7315">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7317">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7317">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7318">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7318">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="f81ea-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="f81ea-7320">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7320">Target</span></span> | <span data-ttu-id="f81ea-7321">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7321">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7322">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7323">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-7323">16</span></span> |
| <span data-ttu-id="f81ea-7324">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7324">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7326">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7326">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7327">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7327">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7328">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7328">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7329">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7329">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7330">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7331">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7331">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7333">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7333">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7334">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7335">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7335">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7337">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7337">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7339">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7339">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7340">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7340">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7341">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7341">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7343">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7343">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7344">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7344">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7345">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7345">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7346">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7346">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7347">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7348">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7349">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7350">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7351">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7352">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7352">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7354">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7354">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7356">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7357">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7358">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7359">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7360">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7361">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7362">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7363">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7363">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7365">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7366">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7367">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7368">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7369">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7369">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7370">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7371">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7371">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7372">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7372">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7374">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7374">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7376">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7376">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7378">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7378">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7380">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7380">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7381">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7381">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="f81ea-7382">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7382">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="f81ea-7383">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7383">Target</span></span> | <span data-ttu-id="f81ea-7384">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7384">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7385">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7386">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-7386">32</span></span> |
| <span data-ttu-id="f81ea-7387">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7387">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7389">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7389">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7390">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7390">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7391">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7391">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7392">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7392">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7393">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7393">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7394">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7396">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7397">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7398">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7398">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7400">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7400">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7402">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7402">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7403">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7403">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7404">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7404">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7406">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7406">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7407">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7407">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7408">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7408">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7409">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7410">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7411">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7412">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7413">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7414">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7415">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7415">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7417">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7417">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7419">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7419">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7420">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7420">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7421">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7421">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7422">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7422">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7423">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7423">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7424">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7424">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7425">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7425">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7426">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7426">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7428">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7429">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7430">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7431">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7432">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7432">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7433">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7434">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7435">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7435">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7437">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7437">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7439">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7439">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7441">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7441">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7443">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7443">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7444">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7444">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="f81ea-7445">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7445">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="f81ea-7446">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7446">Target</span></span> | <span data-ttu-id="f81ea-7447">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7447">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7448">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7448">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7449">32</span><span class="sxs-lookup"><span data-stu-id="f81ea-7449">32</span></span> |
| <span data-ttu-id="f81ea-7450">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7450">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7452">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7452">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7453">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7453">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7454">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7454">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7455">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7455">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7456">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7456">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7457">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7457">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7459">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7459">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7460">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7460">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7461">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7461">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7463">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7463">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7465">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7465">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7466">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7466">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7467">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7467">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7469">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7469">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7470">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7470">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7471">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7471">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7472">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7473">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7474">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7475">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7476">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7477">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7478">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7478">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7480">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7480">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7482">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7482">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7483">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7483">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7484">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7484">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7485">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7485">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7486">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7486">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7487">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7487">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7488">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7488">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7489">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7489">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7491">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7491">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7492">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7492">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7493">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7493">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7494">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7494">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7495">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7495">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7496">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7497">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7497">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7498">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7498">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7500">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7500">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7502">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7502">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7504">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7504">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7506">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7506">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7507">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7507">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="f81ea-7508">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7508">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="f81ea-7509">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7509">Target</span></span> | <span data-ttu-id="f81ea-7510">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7510">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7511">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7511">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7512">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-7512">8</span></span> |
| <span data-ttu-id="f81ea-7513">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7513">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7515">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7515">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7516">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7516">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7517">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7517">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7518">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7518">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7519">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7519">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7520">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7520">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7522">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7522">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7523">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7524">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7524">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7526">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7526">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7528">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7528">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7529">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7529">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7530">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7530">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7532">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7532">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7533">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7533">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7534">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7534">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7535">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7535">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7537">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7537">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7539">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7539">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7540">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7540">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7541">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7541">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7542">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7542">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7543">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7543">Typed UAV</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7545">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7545">UAV Typed Store</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7547">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7547">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7548">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7548">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7549">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7549">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7550">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7550">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7551">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7551">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7552">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7552">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7553">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7553">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7554">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7554">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7556">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7556">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7557">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7557">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7558">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7558">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7559">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7559">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7560">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7560">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7561">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7561">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7562">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7562">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7563">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7563">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7565">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7565">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7567">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7567">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7569">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7569">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7571">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7571">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7572">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7572">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="f81ea-7573">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7573">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="f81ea-7574">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7574">Target</span></span> | <span data-ttu-id="f81ea-7575">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7575">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7576">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7576">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7577">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-7577">8</span></span> |
| <span data-ttu-id="f81ea-7578">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7578">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7580">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7580">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7581">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7581">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7582">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7583">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7583">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7584">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7584">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7585">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7585">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7587">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7587">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7588">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7588">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7589">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7589">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-7590">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7590">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7591">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7591">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7592">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7592">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7593">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7593">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-7594">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7594">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7595">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7595">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7596">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7596">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7597">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7597">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7598">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7598">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7599">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7599">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7600">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7600">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7601">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7601">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7602">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7602">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7603">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7603">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-7604">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7604">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-7605">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7605">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7606">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7606">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7607">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7607">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7608">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7608">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7609">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7609">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7610">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7610">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7611">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7611">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7612">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7612">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7614">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7614">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7615">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7615">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7616">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7616">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7617">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7617">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7618">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7618">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7619">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7619">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7620">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7620">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7621">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-7622">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7622">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7624">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7624">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-7625">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7625">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-7626">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7626">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7627">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7627">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="f81ea-7628">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7628">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="f81ea-7629">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7629">Target</span></span> | <span data-ttu-id="f81ea-7630">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7630">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7631">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7632">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-7632">8</span></span> |
| <span data-ttu-id="f81ea-7633">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7633">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7635">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7635">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7636">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7637">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7638">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7639">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7640">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7642">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7643">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7643">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7644">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7644">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-7645">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7645">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7646">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7646">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7647">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7647">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7648">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7648">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-7649">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7649">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7650">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7650">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7651">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7651">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7652">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7652">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7653">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7654">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7655">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7656">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7657">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7658">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7658">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-7659">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-7660">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7661">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7662">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7663">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7663">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7664">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7665">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7665">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7666">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7666">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7667">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7667">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7669">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7669">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7670">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7670">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7671">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7671">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7672">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7672">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7673">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7673">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7674">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7674">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7675">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7675">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7676">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7676">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-7677">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7677">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7679">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-7680">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7680">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-7681">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7681">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7682">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="f81ea-7683">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7683">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="f81ea-7684">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7684">Target</span></span> | <span data-ttu-id="f81ea-7685">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7685">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7686">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7687">8</span><span class="sxs-lookup"><span data-stu-id="f81ea-7687">8</span></span> |
| <span data-ttu-id="f81ea-7688">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7688">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7690">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7690">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7691">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7691">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7692">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7692">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7693">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7693">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7694">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7694">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7695">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7695">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7697">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7697">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7698">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7699">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7699">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-7700">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7700">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7701">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7701">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7702">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7702">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7703">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7703">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-7704">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7704">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7705">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7705">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7706">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7706">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7707">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7708">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7708">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7709">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7709">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7710">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7710">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7711">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7711">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7712">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7712">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7713">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7713">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-7714">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7714">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-7715">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7715">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7716">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7716">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7717">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7717">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7718">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7718">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7719">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7719">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7720">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7720">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7721">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7721">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7722">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7722">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7724">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7724">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7725">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7725">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7726">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7726">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7727">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7728">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7728">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7729">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7729">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7730">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7730">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7731">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7731">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-7732">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7732">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7734">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7734">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-7735">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7735">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-7736">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7736">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7737">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7737">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="f81ea-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="f81ea-7739">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7739">Target</span></span> | <span data-ttu-id="f81ea-7740">Supporto</span><span class="sxs-lookup"><span data-stu-id="f81ea-7740">Support</span></span> |
| - | - |
| <span data-ttu-id="f81ea-7741">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7741">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f81ea-7742">16</span><span class="sxs-lookup"><span data-stu-id="f81ea-7742">16</span></span> |
| <span data-ttu-id="f81ea-7743">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7743">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="f81ea-7745">Buffer</span><span class="sxs-lookup"><span data-stu-id="f81ea-7745">Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7746">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="f81ea-7746">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7747">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="f81ea-7747">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7748">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7748">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f81ea-7749">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7749">Texture1D</span></span> | \- |
| <span data-ttu-id="f81ea-7750">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7750">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7752">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f81ea-7752">Texture3D</span></span> | \- |
| <span data-ttu-id="f81ea-7753">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f81ea-7753">TextureCube</span></span> | \- |
| <span data-ttu-id="f81ea-7754">LD shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7754">Shader ld</span></span> | \- |
| <span data-ttu-id="f81ea-7755">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7755">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7756">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7756">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7757">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="f81ea-7757">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="f81ea-7758">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="f81ea-7758">Shader gather4</span></span> | \- |
| <span data-ttu-id="f81ea-7759">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="f81ea-7759">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="f81ea-7760">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7760">Mipmap</span></span> | \- |
| <span data-ttu-id="f81ea-7761">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="f81ea-7761">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="f81ea-7762">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f81ea-7762">RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7763">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f81ea-7763">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7764">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="f81ea-7764">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f81ea-7765">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="f81ea-7765">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f81ea-7766">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="f81ea-7766">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7767">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7767">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f81ea-7768">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7768">Typed UAV</span></span> | \- |
| <span data-ttu-id="f81ea-7769">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7769">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f81ea-7770">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7770">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f81ea-7771">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7771">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f81ea-7772">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7772">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f81ea-7773">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f81ea-7773">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f81ea-7774">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7774">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f81ea-7775">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="f81ea-7775">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7776">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="f81ea-7776">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="f81ea-7777">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="f81ea-7777">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7779">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7779">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7780">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="f81ea-7780">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f81ea-7781">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="f81ea-7781">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f81ea-7782">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7782">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f81ea-7783">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="f81ea-7783">Multisample Load</span></span> | \- |
| <span data-ttu-id="f81ea-7784">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f81ea-7784">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f81ea-7785">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="f81ea-7785">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f81ea-7786">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7786">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f81ea-7787">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7787">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="f81ea-7789">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7789">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f81ea-7790">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="f81ea-7790">Shared Resource</span></span> | \- |
| <span data-ttu-id="f81ea-7791">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7791">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="f81ea-7792">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="f81ea-7792">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="f81ea-7793">Note sul formato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7793">Format notes</span></span>

<span data-ttu-id="f81ea-7794">Lo scopo del formato può variare da un livello di funzionalità hardware a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="f81ea-7794">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="f81ea-7795"><sup>L</sup> : formato non tipizzato</span><span class="sxs-lookup"><span data-stu-id="f81ea-7795"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="f81ea-7796"><sup>PC</sup> : layout parzialmente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="f81ea-7796"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="f81ea-7797"><sup>FCS</sup> : layout completamente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="f81ea-7797"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="f81ea-7798"><sup>FNS</sup> : layout completamente tipizzato, non ristabile e semplice</span><span class="sxs-lookup"><span data-stu-id="f81ea-7798"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="f81ea-7799"><sup>PCC</sup> : layout parzialmente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7799"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="f81ea-7800"><sup>FCC</sup> : layout completamente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7800"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="f81ea-7801"><sup>FNC</sup> : layout completamente tipizzato, non ristabile e complesso</span><span class="sxs-lookup"><span data-stu-id="f81ea-7801"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="f81ea-7802"><sup>V</sup> : formato video</span><span class="sxs-lookup"><span data-stu-id="f81ea-7802"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="dxgi_format_related-topics"></a><span data-ttu-id="f81ea-7803">Argomenti di DXGI_FORMAT_Related</span><span class="sxs-lookup"><span data-stu-id="f81ea-7803">DXGI_FORMAT_Related topics</span></span>

[<span data-ttu-id="f81ea-7804">Livelli di funzionalità hardware D3D12</span><span class="sxs-lookup"><span data-stu-id="f81ea-7804">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="f81ea-7805">Guida per programmatori per DXGI</span><span class="sxs-lookup"><span data-stu-id="f81ea-7805">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
