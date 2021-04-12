---
description: Questa sezione specifica i formati ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware del livello di funzionalità Direct3D 10,0.
ms.assetid: 3C1CCA7D-9F2F-4B1B-8424-BA9C6DED4974
title: Supporto del formato per l'hardware a livello di funzionalità 10.0 di Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f298460330feb2143b20da37ae82c3a6d63790
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225350"
---
# <a name="format-support-for-direct3d-feature-level-100-hardware"></a><span data-ttu-id="755f5-103">Supporto del formato per l'hardware a livello di funzionalità 10.0 di Direct3D</span><span class="sxs-lookup"><span data-stu-id="755f5-103">Format support for Direct3D Feature Level 10.0 hardware</span></span>

<span data-ttu-id="755f5-104">Questa sezione specifica i formati ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware a livello di funzionalità Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="755f5-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.0 hardware.</span></span>

<span data-ttu-id="755f5-105">La tabella riepiloga il supporto della funzionalità, usando la chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="755f5-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="755f5-106">Simbolo</span><span class="sxs-lookup"><span data-stu-id="755f5-106">Symbol</span></span>                            | <span data-ttu-id="755f5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="755f5-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="755f5-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="755f5-108">_ *-*\*</span></span>                             | <span data-ttu-id="755f5-109">Non consentito o non disponibile.</span><span class="sxs-lookup"><span data-stu-id="755f5-109">Disallowed or not available.</span></span>                                                  |
| ![necessario](images/letter-r.jpg)  | <span data-ttu-id="755f5-111">Il supporto hardware è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="755f5-111">Hardware support is required.</span></span>                                                 |
| ![facoltative](images/letter-o.jpg)  | <span data-ttu-id="755f5-113">Supporto hardware facoltativo. il formato potrebbe essere accelerato o meno.</span><span class="sxs-lookup"><span data-stu-id="755f5-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dipendenti](images/letter-d.jpg) | <span data-ttu-id="755f5-115">Obbligatorio se è supportata la funzionalità facoltativa correlata.</span><span class="sxs-lookup"><span data-stu-id="755f5-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="755f5-116">Questo argomento contiene una sezione per formato.</span><span class="sxs-lookup"><span data-stu-id="755f5-116">This topic contains a section per format.</span></span> <span data-ttu-id="755f5-117">Una *destinazione* del formato (le tabelle contengono una riga per destinazione) può essere un tipo di risorsa, una funzione intrinseca HLSL o una particolare funzionalità che dipende da un particolare formato.</span><span class="sxs-lookup"><span data-stu-id="755f5-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="755f5-118">Per verificare a livello di codice il supporto del formato in D3D11 e D3D12, vedere [controllo della funzionalità hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="755f5-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="755f5-119">Il numero di formati è prevalentemente, ma non tutti, in ordine numerico crescente &mdash; alcuni sono fuori dall'ordine numerico ed elencati insieme ad altri formati pertinenti.</span><span class="sxs-lookup"><span data-stu-id="755f5-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="755f5-120">Si noti anche che il *tipo* in un nome di formato può indicare *parzialmente* tipizzato e non esclusivamente senza tipo (fare riferimento alla sezione [Note sul formato](#format-notes) alla fine dell'argomento).</span><span class="sxs-lookup"><span data-stu-id="755f5-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>
 
## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="755f5-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="755f5-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="755f5-122">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-122">Target</span></span> | <span data-ttu-id="755f5-123">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-123">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-124">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-125">0</span><span class="sxs-lookup"><span data-stu-id="755f5-125">0</span></span> |
| <span data-ttu-id="755f5-126">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-126">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-128">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-130">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-131">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-132">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-133">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-134">Texture2D</span></span> | \- |
| <span data-ttu-id="755f5-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-135">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-136">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-137">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-137">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-138">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-139">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-140">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-141">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-142">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-143">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-144">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-147">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-148">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-149">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-150">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-151">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-152">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-153">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-154">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-155">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-157">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-158">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-159">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-160">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-160">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-162">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-163">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-164">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-165">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-166">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-167">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-168">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-169">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-170">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-171">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-172">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-173">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="755f5-174">DXGI_FORMAT_R32G32B32A32 \_ <sup>PC</sup> non con tipi (1)</span><span class="sxs-lookup"><span data-stu-id="755f5-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="755f5-175">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-175">Target</span></span> | <span data-ttu-id="755f5-176">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-176">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-177">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-178">128</span><span class="sxs-lookup"><span data-stu-id="755f5-178">128</span></span> |
| <span data-ttu-id="755f5-179">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-179">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-181">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-182">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-183">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-184">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-185">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-187">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-189">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-191">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-193">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-193">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-194">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-195">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-196">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-197">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-198">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-199">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-199">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-201">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-203">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-204">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-205">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-206">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-207">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-208">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-209">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-210">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-211">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-212">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-214">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-215">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-216">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-217">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-217">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-219">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-220">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-221">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-222">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-223">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-224">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-225">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-225">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-227">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-228">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-229">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-230">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-230">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-232">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="755f5-233">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FCS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="755f5-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="755f5-234">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-234">Target</span></span> | <span data-ttu-id="755f5-235">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-235">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-236">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-237">128</span><span class="sxs-lookup"><span data-stu-id="755f5-237">128</span></span> |
| <span data-ttu-id="755f5-238">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-238">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-240">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-242">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-242">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-244">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-245">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-245">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-247">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-249">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-251">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-253">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-255">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-255">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-257">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-257">Shader sample (any filter)</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-259">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-260">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-261">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-262">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-263">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-265">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-265">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-267">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-269">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-269">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-271">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-272">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-273">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-274">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-275">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-276">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-277">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-278">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-279">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-281">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-282">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-283">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-284">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-284">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-286">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-286">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-288">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-288">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-290">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-290">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-292">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-292">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-294">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-294">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-296">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-297">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-297">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-299">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-300">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-301">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-302">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-302">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-304">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="755f5-305">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FCS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="755f5-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="755f5-306">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-306">Target</span></span> | <span data-ttu-id="755f5-307">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-307">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-308">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-309">128</span><span class="sxs-lookup"><span data-stu-id="755f5-309">128</span></span> |
| <span data-ttu-id="755f5-310">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-310">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-312">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-314">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-314">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-316">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-317">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-317">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-319">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-321">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-323">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-325">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-327">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-327">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-329">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-330">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-331">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-332">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-333">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-334">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-334">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-336">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-337">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-339">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-340">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-340">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-342">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-343">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-344">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-345">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-346">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-347">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-348">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-349">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-351">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-352">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-353">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-354">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-354">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-356">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-356">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-358">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-358">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-360">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-360">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-362">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-363">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-363">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-365">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-366">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-366">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-368">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-369">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-370">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-371">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-371">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-373">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="755f5-374">DXGI_FORMAT_R32G32B32A32 \_ Sint<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="755f5-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="755f5-375">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-375">Target</span></span> | <span data-ttu-id="755f5-376">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-376">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-377">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-378">128</span><span class="sxs-lookup"><span data-stu-id="755f5-378">128</span></span> |
| <span data-ttu-id="755f5-379">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-379">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-381">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-383">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-383">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-385">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-386">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-386">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-388">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-390">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-392">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-394">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-396">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-396">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-398">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-399">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-400">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-401">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-402">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-403">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-405">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-406">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-408">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-409">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-410">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-411">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-412">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-413">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-414">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-415">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-416">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-417">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-419">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-420">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-421">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-422">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-422">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-424">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-424">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-426">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-426">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-428">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-428">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-430">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-431">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-431">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-433">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-434">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-434">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-436">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-437">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-438">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-439">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-439">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-441">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="755f5-442">DXGI_FORMAT_R32G32B32 i \_ <sup>PC</sup> con tipi (5)</span><span class="sxs-lookup"><span data-stu-id="755f5-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="755f5-443">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-443">Target</span></span> | <span data-ttu-id="755f5-444">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-444">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-445">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-446">96</span><span class="sxs-lookup"><span data-stu-id="755f5-446">96</span></span> |
| <span data-ttu-id="755f5-447">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-447">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-449">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-450">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-451">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-452">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-453">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-455">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-457">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-459">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-461">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-461">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-462">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-463">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-464">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-465">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-466">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-467">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-467">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-469">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-471">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-472">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-473">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-474">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-475">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-476">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-477">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-478">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-479">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-480">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-482">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-483">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-484">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-485">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-485">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-487">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-488">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-489">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-490">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-491">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-492">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-493">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-493">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-495">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-496">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-497">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-498">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-499">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="755f5-500">DXGI_FORMAT_R32G32B32 \_ float<sup>FCS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="755f5-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="755f5-501">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-501">Target</span></span> | <span data-ttu-id="755f5-502">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-502">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-503">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-504">96</span><span class="sxs-lookup"><span data-stu-id="755f5-504">96</span></span> |
| <span data-ttu-id="755f5-505">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-505">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-507">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-509">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-509">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-511">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-512">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-512">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-514">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-516">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-518">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-520">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-522">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-522">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-524">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-524">Shader sample (any filter)</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-526">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-527">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-528">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-529">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-530">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-530">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-532">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-532">Mipmap Auto-Generation</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-534">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-536">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-536">Blendable RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="755f5-538">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-539">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-540">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-541">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-542">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-543">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-544">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-545">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-546">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-548">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-549">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-550">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-551">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-551">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-553">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-553">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="755f5-555">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-555">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="755f5-557">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-557">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-559">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-559">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-561">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-561">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-563">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-564">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-564">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-566">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-567">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-568">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-569">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-570">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="755f5-571">DXGI_FORMAT_R32G32B32 \_ uint<sup>FCS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="755f5-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="755f5-572">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-572">Target</span></span> | <span data-ttu-id="755f5-573">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-573">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-574">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-575">96</span><span class="sxs-lookup"><span data-stu-id="755f5-575">96</span></span> |
| <span data-ttu-id="755f5-576">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-576">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-578">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-580">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-580">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-582">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-583">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-583">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-585">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-587">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-589">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-591">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-593">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-593">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-595">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-596">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-597">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-598">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-599">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-600">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-602">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-603">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-605">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-606">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-606">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-608">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-609">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-610">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-611">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-612">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-613">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-614">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-615">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-617">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-618">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-619">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-620">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-620">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-622">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-622">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="755f5-624">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-624">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="755f5-626">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-626">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-628">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-629">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-629">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-631">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-632">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-632">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-634">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-635">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-636">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-637">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-638">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="755f5-639">DXGI_FORMAT_R32G32B32 \_ Sint<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="755f5-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="755f5-640">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-640">Target</span></span> | <span data-ttu-id="755f5-641">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-641">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-642">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-643">96</span><span class="sxs-lookup"><span data-stu-id="755f5-643">96</span></span> |
| <span data-ttu-id="755f5-644">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-644">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-646">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-648">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-648">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-650">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-651">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-651">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-653">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-655">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-657">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-659">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-661">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-661">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-663">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-664">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-665">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-666">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-667">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-668">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-670">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-671">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-673">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-674">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-675">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-676">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-677">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-678">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-679">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-680">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-681">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-682">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-684">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-685">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-686">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-687">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-687">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-689">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-689">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="755f5-691">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-691">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="755f5-693">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-693">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-695">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-696">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-696">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-698">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-699">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-699">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-701">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-702">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-703">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-704">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-705">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="755f5-706">DXGI_FORMAT_R16G16B16A16 \_ <sup>PC</sup> non con tipi (9)</span><span class="sxs-lookup"><span data-stu-id="755f5-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="755f5-707">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-707">Target</span></span> | <span data-ttu-id="755f5-708">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-708">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-709">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-710">64</span><span class="sxs-lookup"><span data-stu-id="755f5-710">64</span></span> |
| <span data-ttu-id="755f5-711">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-711">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-713">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-714">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-715">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-716">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-717">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-719">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-721">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-723">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-725">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-725">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-726">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-727">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-728">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-729">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-730">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-731">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-731">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-733">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-735">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-736">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-737">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-738">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-739">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-740">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-741">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-742">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-743">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-744">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-746">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-747">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-748">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-749">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-749">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-751">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-752">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-753">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-754">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-755">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-756">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-757">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-757">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-759">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-760">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-761">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-762">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-762">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-764">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="755f5-765">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FCS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="755f5-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="755f5-766">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-766">Target</span></span> | <span data-ttu-id="755f5-767">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-767">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-768">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-769">64</span><span class="sxs-lookup"><span data-stu-id="755f5-769">64</span></span> |
| <span data-ttu-id="755f5-770">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-770">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-772">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-774">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-774">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-776">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-777">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-778">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-780">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-782">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-784">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-786">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-786">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-788">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-788">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-790">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-791">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-792">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-793">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-794">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-794">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-796">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-796">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-798">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-800">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-800">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-802">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-803">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-804">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-805">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-806">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-807">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-808">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-809">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-810">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-812">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-813">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-814">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-815">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-815">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-817">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-817">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-819">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-819">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-821">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-821">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-823">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-823">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-825">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-825">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-827">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-827">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-829">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-829">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-831">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-832">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-832">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-834">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-834">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-836">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-836">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-838">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="755f5-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="755f5-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="755f5-840">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-840">Target</span></span> | <span data-ttu-id="755f5-841">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-841">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-842">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-843">64</span><span class="sxs-lookup"><span data-stu-id="755f5-843">64</span></span> |
| <span data-ttu-id="755f5-844">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-844">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-846">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-848">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-848">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-850">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-851">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-852">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-854">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-856">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-858">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-860">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-860">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-862">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-862">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-864">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-865">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-866">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-867">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-868">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-870">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-870">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-872">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-874">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-874">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-876">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-877">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-878">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-879">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-880">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-881">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-882">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-883">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-884">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-886">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-887">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-888">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-889">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-889">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-891">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-891">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-893">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-893">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-895">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-895">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-897">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-897">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-899">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-899">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-901">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-902">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-902">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-904">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-905">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-906">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-907">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-907">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-909">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="755f5-910">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FCS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="755f5-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="755f5-911">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-911">Target</span></span> | <span data-ttu-id="755f5-912">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-912">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-913">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-914">64</span><span class="sxs-lookup"><span data-stu-id="755f5-914">64</span></span> |
| <span data-ttu-id="755f5-915">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-915">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-917">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-919">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-919">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-921">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-922">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-923">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-925">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-927">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-929">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-931">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-931">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-933">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-934">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-935">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-936">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-937">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-938">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-940">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-941">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-943">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-944">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-944">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-946">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-947">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-948">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-949">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-950">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-951">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-952">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-953">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-955">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-956">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-957">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-958">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-958">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-960">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-960">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-962">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-962">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-964">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-964">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-966">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-967">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-967">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-969">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-970">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-970">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-972">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-973">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-974">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-975">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-975">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-977">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="755f5-978">DXGI_FORMAT_R16G16B16A16 \_ russare<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="755f5-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="755f5-979">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-979">Target</span></span> | <span data-ttu-id="755f5-980">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-980">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-981">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-982">64</span><span class="sxs-lookup"><span data-stu-id="755f5-982">64</span></span> |
| <span data-ttu-id="755f5-983">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-983">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-985">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-987">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-987">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-989">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-990">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-991">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-993">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-995">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-997">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-999">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-999">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1001">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1001">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1003">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1004">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1005">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1006">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1007">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1007">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1009">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1009">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1011">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1013">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1013">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1014">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1014">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1015">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1015">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1016">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1016">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1017">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1017">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1018">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1018">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1019">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1019">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1020">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1020">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1021">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1021">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1022">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1022">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1023">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1023">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1024">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1024">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1025">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1025">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1026">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1026">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1027">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1027">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1029">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1029">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1031">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1031">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1033">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1033">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1035">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1035">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1037">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1037">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1039">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1039">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1040">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1040">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1042">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1043">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1044">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1045">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1045">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1047">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1047">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="755f5-1048">DXGI_FORMAT_R16G16B16A16 \_ Sint<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="755f5-1048">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="755f5-1049">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1049">Target</span></span> | <span data-ttu-id="755f5-1050">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1050">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1051">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1051">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1052">64</span><span class="sxs-lookup"><span data-stu-id="755f5-1052">64</span></span> |
| <span data-ttu-id="755f5-1053">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1053">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1055">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1055">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1057">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1057">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1059">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1059">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1060">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1060">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1061">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1061">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1063">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1063">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1065">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1065">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1067">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1067">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1069">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1069">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1071">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1071">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1072">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1072">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1073">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1073">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1074">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1074">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1075">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1075">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1076">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1076">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1078">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1078">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1079">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1079">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1081">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1081">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1082">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1082">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1083">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1083">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1084">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1084">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1085">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1085">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1086">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1086">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1087">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1087">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1088">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1088">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1089">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1089">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1090">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1090">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1091">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1091">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1092">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1092">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1093">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1093">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1094">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1094">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1095">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1095">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1097">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1097">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1099">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1099">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1101">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1101">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1103">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1103">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1104">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1104">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1106">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1106">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1107">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1107">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1109">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1109">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1110">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1110">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1111">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1111">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1112">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1112">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1114">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="755f5-1115">DXGI_FORMAT_R32G32 \_ <sup>PC</sup> non con tipi (15)</span><span class="sxs-lookup"><span data-stu-id="755f5-1115">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="755f5-1116">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1116">Target</span></span> | <span data-ttu-id="755f5-1117">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1117">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1118">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1119">64</span><span class="sxs-lookup"><span data-stu-id="755f5-1119">64</span></span> |
| <span data-ttu-id="755f5-1120">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1120">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1122">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1122">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1123">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1124">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1125">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1126">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1128">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1130">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1132">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1134">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1134">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-1135">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1135">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1136">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1136">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1137">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1137">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1138">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1138">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1139">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1139">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1140">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1140">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1142">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1143">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1144">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1145">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1146">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1147">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1148">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1149">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1149">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1150">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1151">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1152">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1153">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1154">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1155">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1156">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1157">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1158">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1158">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1160">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1160">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1161">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1161">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1162">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1162">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-1163">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1163">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1164">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1164">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-1165">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1165">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1166">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1166">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1168">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1168">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1169">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1169">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1170">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1170">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1171">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1171">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-1172">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1172">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="755f5-1173">DXGI_FORMAT_R32G32 \_ float<sup>FCS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="755f5-1173">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="755f5-1174">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1174">Target</span></span> | <span data-ttu-id="755f5-1175">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1175">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1176">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1176">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1177">64</span><span class="sxs-lookup"><span data-stu-id="755f5-1177">64</span></span> |
| <span data-ttu-id="755f5-1178">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1178">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1180">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1180">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1182">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1182">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1184">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1185">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1185">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1187">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1189">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1189">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1191">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1191">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1193">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1193">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1195">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1195">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1197">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1197">Shader sample (any filter)</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1199">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1199">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1200">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1200">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1201">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1201">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1202">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1202">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1203">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1203">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1205">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1205">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1207">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1207">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1209">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1209">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1211">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1211">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1212">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1212">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1213">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1213">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1214">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1214">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1215">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1215">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1216">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1216">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1217">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1217">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1218">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1218">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1219">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1219">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1220">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1220">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1221">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1221">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1222">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1222">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1223">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1223">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1224">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1224">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1226">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1226">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1228">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1228">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1230">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1230">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1232">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1232">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1234">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1234">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1236">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1236">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1237">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1237">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1239">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1239">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1240">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1240">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1241">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1241">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1242">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1242">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-1243">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1243">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="755f5-1244">DXGI_FORMAT_R32G32 \_ uint<sup>FCS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="755f5-1244">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="755f5-1245">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1245">Target</span></span> | <span data-ttu-id="755f5-1246">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1246">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1247">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1247">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1248">64</span><span class="sxs-lookup"><span data-stu-id="755f5-1248">64</span></span> |
| <span data-ttu-id="755f5-1249">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1249">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1251">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1251">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1253">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1253">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1255">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1255">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1256">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1256">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1258">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1258">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1260">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1260">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1262">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1262">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1264">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1264">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1266">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1266">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1268">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1268">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1269">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1269">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1270">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1270">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1271">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1271">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1272">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1272">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1273">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1273">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1275">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1275">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1276">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1278">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1278">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1279">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1279">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1281">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1282">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1283">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1284">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1284">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1285">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1285">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1286">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1286">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1287">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1288">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1289">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1289">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1290">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1291">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1291">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1292">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1292">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1293">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1293">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1295">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1295">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1297">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1297">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1299">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1299">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1301">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1302">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1302">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1304">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1304">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1305">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1305">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1307">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1307">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1308">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1308">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1309">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1309">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1310">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1310">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-1311">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="755f5-1312">DXGI_FORMAT_R32G32 \_ Sint<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="755f5-1312">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="755f5-1313">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1313">Target</span></span> | <span data-ttu-id="755f5-1314">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1314">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1315">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1316">64</span><span class="sxs-lookup"><span data-stu-id="755f5-1316">64</span></span> |
| <span data-ttu-id="755f5-1317">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1317">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1319">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1319">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1321">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1321">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1323">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1323">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1324">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1324">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1326">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1326">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1328">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1330">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1332">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1332">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1334">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1334">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1336">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1336">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1337">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1337">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1338">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1338">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1339">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1339">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1340">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1340">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1341">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1341">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1343">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1343">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1344">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1344">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1346">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1347">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1348">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1349">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1350">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1351">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1351">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1352">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1353">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1354">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1355">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1356">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1357">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1358">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1359">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1360">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1360">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1362">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1362">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1364">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1364">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1366">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1366">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1368">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1369">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1369">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1371">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1372">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1372">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1374">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1375">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1376">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1377">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1377">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-1378">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="755f5-1379">DXGI_FORMAT_R32G8X24 i \_ <sup>PC</sup> non con tipi (19)</span><span class="sxs-lookup"><span data-stu-id="755f5-1379">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="755f5-1380">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1380">Target</span></span> | <span data-ttu-id="755f5-1381">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1381">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1382">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1383">64</span><span class="sxs-lookup"><span data-stu-id="755f5-1383">64</span></span> |
| <span data-ttu-id="755f5-1384">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1384">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1386">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1386">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1387">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1387">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1388">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1388">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1389">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1389">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1390">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1390">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1392">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1394">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-1395">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1395">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1397">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1397">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-1398">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1399">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1400">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1401">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1401">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1402">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1403">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1405">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1406">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1407">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1407">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1408">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1408">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1409">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1409">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1410">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1410">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1411">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1411">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1412">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1412">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1413">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1413">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1414">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1414">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1415">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1415">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1416">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1416">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1417">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1417">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1418">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1418">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1419">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1419">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1420">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1420">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1421">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1421">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1423">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1424">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1425">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-1426">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1427">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1427">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-1428">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1429">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1429">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1431">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1431">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1432">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1432">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1433">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1433">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1434">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1434">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-1435">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1435">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="755f5-1436">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FCS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="755f5-1436">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="755f5-1437">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1437">Target</span></span> | <span data-ttu-id="755f5-1438">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1438">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1439">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1439">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1440">64</span><span class="sxs-lookup"><span data-stu-id="755f5-1440">64</span></span> |
| <span data-ttu-id="755f5-1441">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1441">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1443">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1443">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1444">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1445">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1446">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1447">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1449">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1449">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1451">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1451">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-1452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1452">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1454">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1454">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-1455">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1456">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1457">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1458">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1459">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1460">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1460">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1462">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1462">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1463">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1463">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1464">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1464">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1465">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1465">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1466">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1466">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1468">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1469">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1470">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1471">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1472">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1473">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1474">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1475">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1476">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1477">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1478">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1479">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1479">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1481">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1481">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1483">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1483">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1485">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1485">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1487">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1487">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1488">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1488">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-1489">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1489">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1490">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1490">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1492">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1492">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1493">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1493">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1494">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1494">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1495">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1495">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-1496">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1496">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="755f5-1497">DXGI_FORMAT_R32 \_ float \_ con \_ tipo float<sup></sup> X8X24 (21)</span><span class="sxs-lookup"><span data-stu-id="755f5-1497">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="755f5-1498">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1498">Target</span></span> | <span data-ttu-id="755f5-1499">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1499">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1500">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1500">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1501">64</span><span class="sxs-lookup"><span data-stu-id="755f5-1501">64</span></span> |
| <span data-ttu-id="755f5-1502">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1502">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1504">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1504">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1505">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1505">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1506">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1506">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1507">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1507">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1508">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1508">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1510">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1512">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-1513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1513">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1515">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1515">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1517">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1517">Shader sample (any filter)</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1519">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1519">Shader sample\_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1521">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1521">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1522">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1522">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1523">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1523">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1524">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1524">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1526">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1526">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1527">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1527">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1528">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1528">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1529">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1529">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1530">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1530">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1531">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1531">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1532">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1532">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1533">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1533">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1534">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1534">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1535">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1535">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1536">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1536">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1537">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1537">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1538">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1538">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1539">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1539">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1540">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1540">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1541">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1541">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1542">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1542">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1544">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1544">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1545">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1545">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1546">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1546">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-1547">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1547">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1548">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1548">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-1549">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1549">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1550">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1550">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1552">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1552">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1553">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1553">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1554">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1554">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1555">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1555">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-1556">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1556">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="755f5-1557">G8X24 con tipo di DXGI_FORMAT_X32 \_ \_ \_ uint<sup>FCS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="755f5-1557">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="755f5-1558">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1558">Target</span></span> | <span data-ttu-id="755f5-1559">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1559">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1560">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1560">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1561">64</span><span class="sxs-lookup"><span data-stu-id="755f5-1561">64</span></span> |
| <span data-ttu-id="755f5-1562">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1562">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1564">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1564">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1565">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1565">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1566">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1566">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1567">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1567">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1568">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1568">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1570">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1570">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1572">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1572">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-1573">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1573">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1575">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1575">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1577">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1577">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1578">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1578">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1579">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1579">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1580">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1580">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1581">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1581">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1582">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1582">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1584">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1584">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1585">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1585">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1586">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1586">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1587">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1588">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1589">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1590">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1591">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1591">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1592">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1592">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1593">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1593">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1594">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1594">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1595">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1595">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1596">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1596">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1597">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1597">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1598">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1598">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1599">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1599">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1600">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1600">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1602">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1602">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1603">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1603">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1604">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1604">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-1605">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1605">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1606">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1606">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-1607">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1607">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1608">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1608">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1610">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1610">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1611">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1611">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1612">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1612">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1613">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1613">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-1614">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1614">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="755f5-1615">DXGI_FORMAT_R10G10B10A2 \_ <sup>PC</sup> non con tipi (23)</span><span class="sxs-lookup"><span data-stu-id="755f5-1615">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="755f5-1616">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1616">Target</span></span> | <span data-ttu-id="755f5-1617">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1617">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1618">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1618">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1619">32</span><span class="sxs-lookup"><span data-stu-id="755f5-1619">32</span></span> |
| <span data-ttu-id="755f5-1620">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1620">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1622">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1622">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1623">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1623">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1624">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1624">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1625">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1625">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1626">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1626">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1628">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1628">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1630">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1630">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1632">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1632">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1634">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1634">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-1635">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1635">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1636">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1636">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1637">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1637">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1638">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1638">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1639">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1639">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1640">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1640">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1642">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1642">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1643">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1643">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1644">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1644">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1645">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1645">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1646">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1646">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1647">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1647">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1648">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1648">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1649">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1649">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1650">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1650">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1651">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1651">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1652">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1652">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1653">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1653">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1654">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1654">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1655">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1655">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1656">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1656">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1657">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1657">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1658">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1658">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1660">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1660">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1661">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1661">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1662">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1662">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-1663">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1663">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1664">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1664">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-1665">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1665">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1666">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1666">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1668">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1669">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1670">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1671">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1671">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1673">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1673">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="755f5-1674">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="755f5-1674">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="755f5-1675">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1675">Target</span></span> | <span data-ttu-id="755f5-1676">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1676">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1677">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1677">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1678">32</span><span class="sxs-lookup"><span data-stu-id="755f5-1678">32</span></span> |
| <span data-ttu-id="755f5-1679">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1679">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1681">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1681">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1683">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1683">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1685">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1685">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1686">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1686">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1687">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1687">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1689">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1689">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1691">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1691">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1693">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1693">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1695">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1695">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1697">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1697">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1699">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1700">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1701">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1701">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1702">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1703">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1703">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1705">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1705">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1707">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1709">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1709">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1711">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1711">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1712">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1712">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1713">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1713">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1714">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1714">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1715">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1715">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1716">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1716">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1717">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1717">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1718">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1718">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1719">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1719">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1720">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1720">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1721">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1721">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1722">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1722">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1723">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1723">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1724">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1724">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1726">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1726">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1728">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1728">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1730">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1730">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1732">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1732">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1734">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1734">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1736">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1736">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1738">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1738">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1740">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1741">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1741">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1743">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1743">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1745">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1745">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1747">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1747">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="755f5-1748">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FCS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="755f5-1748">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="755f5-1749">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1749">Target</span></span> | <span data-ttu-id="755f5-1750">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1750">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1751">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1751">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1752">32</span><span class="sxs-lookup"><span data-stu-id="755f5-1752">32</span></span> |
| <span data-ttu-id="755f5-1753">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1753">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1755">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1755">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1757">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1757">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1759">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1760">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1761">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1763">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1765">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1765">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1767">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1767">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1769">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1769">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1771">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1771">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1772">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1772">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1773">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1773">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1774">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1774">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1775">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1775">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1776">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1776">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1778">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1778">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1779">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1781">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1781">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1782">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1782">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1784">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1785">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1786">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1787">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1787">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1788">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1789">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1790">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1791">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1793">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1794">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1795">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1796">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1796">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1798">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1798">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1800">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1800">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1802">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1802">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1804">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1805">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1805">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1807">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1807">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1808">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1808">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1810">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1810">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1811">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1811">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1812">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1812">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1813">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1813">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1815">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1815">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="755f5-1816">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="755f5-1816">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="755f5-1817">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1817">Target</span></span> | <span data-ttu-id="755f5-1818">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1818">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1819">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1820">32</span><span class="sxs-lookup"><span data-stu-id="755f5-1820">32</span></span> |
| <span data-ttu-id="755f5-1821">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1821">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1823">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1823">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1824">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1824">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1825">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1825">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1826">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1826">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1827">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1827">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-1828">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1828">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1830">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1830">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-1831">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1831">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-1832">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1832">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-1833">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1833">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1834">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1834">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1835">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1835">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1836">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1836">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1837">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1837">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1838">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1838">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-1839">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1839">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1840">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1840">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1841">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1841">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1842">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1842">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1843">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1843">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1844">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1845">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1846">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1846">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1847">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1848">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1849">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1850">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1852">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1853">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1854">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1855">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1855">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1857">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1857">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1858">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1858">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1859">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1859">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-1860">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1860">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1861">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1861">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-1862">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1862">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1864">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1864">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1866">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1867">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1867">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1869">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1869">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1871">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1871">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1873">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="755f5-1874">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="755f5-1874">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="755f5-1875">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1875">Target</span></span> | <span data-ttu-id="755f5-1876">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1876">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1877">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1878">32</span><span class="sxs-lookup"><span data-stu-id="755f5-1878">32</span></span> |
| <span data-ttu-id="755f5-1879">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1879">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1881">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1881">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1883">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1883">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1885">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1886">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1886">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1887">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1887">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1889">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1889">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1891">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1893">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1893">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1895">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1895">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1897">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1897">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1899">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1899">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1900">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1900">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1901">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1901">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1902">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1902">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1903">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1903">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1905">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1905">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1907">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1909">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1909">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1911">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1912">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1913">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1914">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1915">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1915">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1916">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1917">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1918">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1919">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1920">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1921">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1922">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1923">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1924">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1924">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1926">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1926">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1928">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1928">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1930">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1930">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1932">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1932">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1934">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1934">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-1936">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1936">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1937">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1937">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-1938">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1938">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1939">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1939">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1940">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1940">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1941">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1941">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-1942">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-1942">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="755f5-1943">DXGI_FORMAT_R8G8B8A8 \_ <sup>PC</sup> non con tipi (27)</span><span class="sxs-lookup"><span data-stu-id="755f5-1943">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="755f5-1944">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1944">Target</span></span> | <span data-ttu-id="755f5-1945">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-1945">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-1946">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-1946">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-1947">32</span><span class="sxs-lookup"><span data-stu-id="755f5-1947">32</span></span> |
| <span data-ttu-id="755f5-1948">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-1948">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1950">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-1950">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1951">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-1951">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1952">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-1952">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1953">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-1953">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-1954">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-1954">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1956">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-1956">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1958">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-1958">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1960">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-1960">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1962">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-1962">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-1963">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-1963">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-1964">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-1964">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-1965">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-1965">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-1966">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-1966">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-1967">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-1967">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-1968">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1968">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1970">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-1970">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-1971">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-1971">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1972">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-1972">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1973">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-1973">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-1974">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-1974">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-1975">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-1975">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1976">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-1976">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-1977">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-1977">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-1978">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1978">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-1979">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1979">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-1980">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1980">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-1981">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1981">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-1982">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-1982">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-1983">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1983">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-1984">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-1984">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1985">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-1985">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-1986">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-1986">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1988">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-1988">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1989">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-1989">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-1990">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-1990">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-1991">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1991">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-1992">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-1992">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-1993">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-1993">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-1994">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-1994">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-1996">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1996">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-1997">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1997">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-1998">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-1998">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-1999">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-1999">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2001">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2001">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="755f5-2002">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="755f5-2002">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="755f5-2003">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2003">Target</span></span> | <span data-ttu-id="755f5-2004">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2004">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2005">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2005">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2006">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2006">32</span></span> |
| <span data-ttu-id="755f5-2007">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2007">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2009">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2009">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2011">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2011">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2013">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2013">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2014">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2014">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2015">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2015">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2017">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2017">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2019">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2019">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2021">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2021">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2023">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2023">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2025">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2025">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2027">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2027">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2028">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2028">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2029">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2029">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2030">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2030">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2031">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2031">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2033">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2033">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2035">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2035">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2037">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2037">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2039">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2040">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2041">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2042">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2043">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2043">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2044">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2045">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2046">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2047">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2048">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2049">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2050">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2051">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2052">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2052">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2054">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2054">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2056">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2056">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2058">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2058">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2060">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2060">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2062">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2062">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2064">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2064">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2066">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2066">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2068">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2068">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2069">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2069">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2071">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2071">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2073">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2073">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2075">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="755f5-2076">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="755f5-2076">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="755f5-2077">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2077">Target</span></span> | <span data-ttu-id="755f5-2078">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2078">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2079">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2080">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2080">32</span></span> |
| <span data-ttu-id="755f5-2081">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2081">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2083">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2083">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2084">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2085">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2086">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2087">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2089">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2091">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2093">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2095">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2095">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2097">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2097">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2099">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2100">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2101">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2101">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2102">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2103">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2103">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2105">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2105">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2107">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2109">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2109">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2111">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2112">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2113">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2114">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2115">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2115">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2116">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2117">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2118">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2119">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2120">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2121">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2122">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2123">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2124">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2124">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2126">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2126">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2128">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2128">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2130">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2130">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2132">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2132">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2134">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2134">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2136">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2136">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2138">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2138">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2140">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2140">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2141">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2141">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2143">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2143">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2145">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2145">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2147">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="755f5-2148">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FCS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="755f5-2148">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="755f5-2149">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2149">Target</span></span> | <span data-ttu-id="755f5-2150">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2150">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2151">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2152">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2152">32</span></span> |
| <span data-ttu-id="755f5-2153">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2153">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2155">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2155">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2157">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2157">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2159">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2159">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2160">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2160">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2161">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2161">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2163">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2163">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2165">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2165">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2167">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2167">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2169">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2169">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2171">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2171">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-2172">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2172">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2173">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2173">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2174">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2174">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2175">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2175">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2176">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2176">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2178">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2178">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-2179">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2179">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2181">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2181">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2182">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2182">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2184">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2184">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2185">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2185">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2186">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2186">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2187">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2187">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2188">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2188">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2189">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2189">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2190">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2190">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2191">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2191">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2192">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2192">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2193">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2193">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2194">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2194">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2195">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2195">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2196">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2196">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2198">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2198">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2200">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2200">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2202">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2202">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2204">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2204">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-2205">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2205">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2207">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2207">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2208">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2208">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2210">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2210">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2211">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2211">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2212">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2212">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2213">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2213">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2215">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2215">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="755f5-2216">DXGI_FORMAT_R8G8B8A8 \_ russo<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="755f5-2216">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="755f5-2217">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2217">Target</span></span> | <span data-ttu-id="755f5-2218">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2218">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2219">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2219">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2220">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2220">32</span></span> |
| <span data-ttu-id="755f5-2221">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2221">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2223">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2223">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2225">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2225">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2227">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2227">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2228">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2228">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2229">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2229">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2231">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2231">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2233">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2233">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2235">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2235">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2237">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2237">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2239">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2239">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2241">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2241">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2242">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2242">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2243">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2243">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2244">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2244">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2245">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2245">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2247">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2247">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2249">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2249">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2251">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2251">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2252">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2252">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2253">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2253">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2254">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2254">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2255">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2255">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2256">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2256">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2257">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2257">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2258">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2258">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2259">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2259">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2260">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2260">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2261">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2261">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2262">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2262">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2263">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2263">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2264">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2264">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2265">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2265">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2267">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2267">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2269">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2269">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2271">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2271">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2273">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2273">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2275">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2275">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2277">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2277">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2278">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2278">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2280">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2281">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2282">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2283">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2283">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2285">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2285">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="755f5-2286">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="755f5-2286">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="755f5-2287">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2287">Target</span></span> | <span data-ttu-id="755f5-2288">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2288">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2289">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2289">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2290">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2290">32</span></span> |
| <span data-ttu-id="755f5-2291">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2291">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2293">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2293">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2295">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2295">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2297">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2298">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2299">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2301">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2301">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2303">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2305">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2305">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2307">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2307">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2309">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2309">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-2310">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2310">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2311">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2311">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2312">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2312">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2313">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2313">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2314">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2314">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2316">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2316">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-2317">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2317">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2319">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2319">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2320">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2320">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2321">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2321">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2322">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2322">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2323">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2323">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2324">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2324">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2325">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2325">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2326">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2326">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2327">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2327">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2328">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2328">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2329">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2329">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2330">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2330">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2331">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2331">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2332">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2332">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2333">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2333">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2335">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2335">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2337">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2337">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2339">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2339">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2341">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2341">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-2342">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2342">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2344">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2345">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2345">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2347">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2348">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2349">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2350">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2350">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2352">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2352">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="755f5-2353">DXGI_FORMAT_R16G16 \_ <sup>PC</sup> non con tipi (33)</span><span class="sxs-lookup"><span data-stu-id="755f5-2353">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="755f5-2354">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2354">Target</span></span> | <span data-ttu-id="755f5-2355">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2355">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2356">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2356">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2357">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2357">32</span></span> |
| <span data-ttu-id="755f5-2358">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2358">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2360">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2360">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2361">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2361">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2362">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2362">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2363">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2363">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2364">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2364">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2366">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2366">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2368">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2368">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2370">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2370">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2372">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2372">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-2373">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2373">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-2374">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2375">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2376">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2376">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2377">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2378">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2378">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2380">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-2381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2381">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2382">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2383">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2384">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2385">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2386">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2387">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2387">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2388">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2389">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2390">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2391">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2393">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2394">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2395">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2396">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2396">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2398">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2399">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2400">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-2401">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-2402">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2402">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-2403">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2404">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2404">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2406">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2407">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2408">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2409">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2409">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-2410">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="755f5-2411">DXGI_FORMAT_R16G16 \_ float<sup>FCS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="755f5-2411">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="755f5-2412">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2412">Target</span></span> | <span data-ttu-id="755f5-2413">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2413">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2414">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2415">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2415">32</span></span> |
| <span data-ttu-id="755f5-2416">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2416">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2418">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2418">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2420">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2420">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2422">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2422">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2423">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2423">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2424">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2424">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2426">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2426">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2428">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2428">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2430">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2430">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2432">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2432">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2434">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2434">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2436">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2436">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2437">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2437">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2438">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2438">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2439">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2439">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2440">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2440">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2442">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2442">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2444">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2444">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2446">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2446">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2448">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2448">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2449">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2449">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2450">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2450">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2451">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2451">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2452">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2452">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2453">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2453">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2454">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2454">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2455">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2455">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2456">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2456">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2457">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2457">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2458">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2458">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2459">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2459">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2460">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2460">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2461">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2461">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2463">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2463">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2465">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2465">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2467">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2467">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2469">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2469">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2471">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2471">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2473">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2474">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2474">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2476">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2476">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2477">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2477">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2478">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2478">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2479">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2479">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-2480">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2480">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="755f5-2481">DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="755f5-2481">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="755f5-2482">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2482">Target</span></span> | <span data-ttu-id="755f5-2483">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2483">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2484">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2484">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2485">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2485">32</span></span> |
| <span data-ttu-id="755f5-2486">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2486">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2488">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2488">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2490">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2490">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2492">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2493">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2494">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2496">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2496">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2498">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2498">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2500">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2502">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2502">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2504">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2504">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2506">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2507">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2508">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2508">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2509">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2510">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2512">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2512">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2514">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2516">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2516">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2518">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2518">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2519">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2519">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2520">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2520">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2521">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2521">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2522">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2522">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2523">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2523">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2524">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2524">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2525">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2525">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2526">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2526">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2527">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2527">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2528">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2528">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2529">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2529">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2530">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2530">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2531">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2531">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2533">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2533">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2535">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2535">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2537">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2537">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2539">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2539">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2541">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2541">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2543">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2544">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2544">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2546">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2546">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2547">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2547">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2548">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2548">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2549">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2549">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-2550">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="755f5-2551">DXGI_FORMAT_R16G16 \_ uint<sup>FCS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="755f5-2551">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="755f5-2552">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2552">Target</span></span> | <span data-ttu-id="755f5-2553">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2553">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2554">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2555">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2555">32</span></span> |
| <span data-ttu-id="755f5-2556">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2556">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2558">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2558">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2560">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2560">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2562">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2563">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2564">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2566">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2566">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2568">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2568">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2570">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2570">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2572">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2572">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2574">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2574">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-2575">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2575">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2576">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2576">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2577">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2577">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2578">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2578">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2579">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2579">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2581">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2581">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-2582">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2582">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2584">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2584">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2585">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2585">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2587">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2587">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2588">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2588">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2589">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2589">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2590">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2590">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2591">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2591">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2592">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2592">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2593">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2593">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2594">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2594">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2595">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2595">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2596">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2596">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2597">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2597">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2598">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2598">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2599">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2599">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2601">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2601">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2603">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2603">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2605">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2605">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2607">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2607">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-2608">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2608">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2610">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2610">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2611">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2611">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2613">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2613">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2614">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2614">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2615">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2615">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2616">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2616">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-2617">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2617">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="755f5-2618">DXGI_FORMAT_R16G16 \_ russo<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="755f5-2618">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="755f5-2619">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2619">Target</span></span> | <span data-ttu-id="755f5-2620">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2620">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2621">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2621">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2622">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2622">32</span></span> |
| <span data-ttu-id="755f5-2623">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2623">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2625">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2625">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2627">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2627">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2629">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2629">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2630">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2630">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2631">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2631">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2633">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2633">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2635">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2635">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2637">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2637">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2639">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2639">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2641">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2641">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2643">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2643">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2644">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2644">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2645">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2645">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2646">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2646">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2647">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2647">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2649">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2649">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2651">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2651">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2653">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2654">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2655">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2656">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2657">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2658">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2658">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2659">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2660">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2661">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2662">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2663">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2663">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2664">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2665">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2665">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2666">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2666">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2667">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2667">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2669">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2669">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2671">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2671">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2673">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2673">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2675">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2675">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2677">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2677">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2679">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2679">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2680">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2680">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2682">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2682">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2683">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2683">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2684">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2684">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2685">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2685">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-2686">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2686">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="755f5-2687">DXGI_FORMAT_R16G16 \_ Sint<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="755f5-2687">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="755f5-2688">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2688">Target</span></span> | <span data-ttu-id="755f5-2689">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2689">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2690">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2690">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2691">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2691">32</span></span> |
| <span data-ttu-id="755f5-2692">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2692">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2694">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2694">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2696">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2696">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2698">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2698">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2699">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2699">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2700">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2700">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2702">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2704">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2706">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2708">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2708">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2710">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-2711">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2712">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2713">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2713">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2714">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2715">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2717">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2717">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-2718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2718">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2720">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2720">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2721">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2721">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2722">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2722">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2723">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2723">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2724">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2724">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2725">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2725">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2726">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2726">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2727">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2727">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2728">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2728">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2729">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2729">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2730">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2730">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2731">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2731">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2732">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2732">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2733">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2733">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2734">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2734">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2736">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2736">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2738">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2738">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2740">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2740">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2742">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-2743">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2743">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2745">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2746">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2746">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2748">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2748">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2749">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2749">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2750">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2750">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2751">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2751">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-2752">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2752">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="755f5-2753">DXGI_FORMAT_R32 \_ <sup>PC</sup> non con tipi (39)</span><span class="sxs-lookup"><span data-stu-id="755f5-2753">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="755f5-2754">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2754">Target</span></span> | <span data-ttu-id="755f5-2755">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2755">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2756">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2756">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2757">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2757">32</span></span> |
| <span data-ttu-id="755f5-2758">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2758">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2760">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2760">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2761">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2761">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2762">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2762">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2763">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2763">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2764">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2764">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2766">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2766">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2768">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2768">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2770">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2772">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2772">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-2773">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2773">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-2774">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2774">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2775">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2775">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2776">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2776">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2777">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2777">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2778">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2778">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2780">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2780">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-2781">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2781">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2782">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2782">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2783">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2783">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2784">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2785">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2786">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2787">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2787">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2788">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2789">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2790">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2791">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2793">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2794">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2795">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2796">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2796">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2798">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2798">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2799">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2799">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2800">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2800">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-2801">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2801">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-2802">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2802">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-2803">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2803">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2804">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2804">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2806">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2807">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2807">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2808">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2808">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2809">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2809">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2811">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="755f5-2812">DXGI_FORMAT_D32 \_ float<sup>FCS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="755f5-2812">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="755f5-2813">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2813">Target</span></span> | <span data-ttu-id="755f5-2814">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2815">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2816">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2816">32</span></span> |
| <span data-ttu-id="755f5-2817">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2817">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2819">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2820">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2821">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2822">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2823">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2825">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2827">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-2828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2828">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2830">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2830">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-2831">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2831">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-2832">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2833">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2834">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2835">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2836">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2838">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2840">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2841">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2842">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2842">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2844">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2845">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2846">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2846">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2847">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2848">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2849">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2850">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2852">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2853">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2854">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2855">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2855">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2857">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2857">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2859">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2859">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2861">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2861">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2863">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2863">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-2864">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2864">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-2865">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2865">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2866">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2866">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2868">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2868">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2869">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2869">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2870">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2870">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2871">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2871">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2873">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="755f5-2874">DXGI_FORMAT_R32 \_ float<sup>FCS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="755f5-2874">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="755f5-2875">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2875">Target</span></span> | <span data-ttu-id="755f5-2876">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2876">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2877">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2878">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2878">32</span></span> |
| <span data-ttu-id="755f5-2879">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2879">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2881">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2881">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2883">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2883">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2885">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-2886">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2886">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2888">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2888">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2890">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2892">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2892">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2894">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2894">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2896">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2896">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2898">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2898">Shader sample (any filter)</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2900">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2900">Shader sample\_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2902">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2902">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2903">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2903">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2904">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2904">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2905">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2905">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2907">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2907">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2909">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2911">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2911">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2913">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2913">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-2914">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2914">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2915">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2915">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2916">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2916">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2917">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2917">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2918">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2918">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2919">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2919">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2920">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2920">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2921">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2921">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2922">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2922">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2923">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2923">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2924">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2924">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2925">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2925">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2926">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2926">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2928">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2928">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2930">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-2930">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2932">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-2932">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2934">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2934">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2936">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-2936">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2938">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-2938">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-2939">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-2939">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2941">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2941">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-2942">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2942">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-2943">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-2943">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-2944">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-2944">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2946">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-2946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="755f5-2947">DXGI_FORMAT_R32 \_ uint<sup>FCS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="755f5-2947">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="755f5-2948">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2948">Target</span></span> | <span data-ttu-id="755f5-2949">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-2949">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-2950">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-2950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-2951">32</span><span class="sxs-lookup"><span data-stu-id="755f5-2951">32</span></span> |
| <span data-ttu-id="755f5-2952">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-2952">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2954">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-2954">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2956">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-2956">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2958">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-2958">Input Assembler Index Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2960">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-2960">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-2962">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2964">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-2964">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2966">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-2966">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2968">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-2968">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2970">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-2970">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2972">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-2972">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-2973">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-2973">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-2974">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-2974">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-2975">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-2975">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-2976">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-2976">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-2977">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2977">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2979">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-2979">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-2980">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-2980">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2982">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-2982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-2983">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-2983">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-2985">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-2985">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-2986">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-2986">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2987">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-2987">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-2988">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-2988">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-2989">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2989">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-2990">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2990">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-2991">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2991">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-2992">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2992">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-2993">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-2993">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-2994">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2994">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-2995">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-2995">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2996">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-2996">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-2997">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-2997">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-2999">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-2999">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3001">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3001">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3003">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3003">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3005">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3006">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3006">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3008">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3009">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3009">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3011">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3011">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3012">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3012">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3013">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3013">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3014">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3014">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3016">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3016">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="755f5-3017">DXGI_FORMAT_R32 \_ Sint<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="755f5-3017">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="755f5-3018">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3018">Target</span></span> | <span data-ttu-id="755f5-3019">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3019">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3020">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3020">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3021">32</span><span class="sxs-lookup"><span data-stu-id="755f5-3021">32</span></span> |
| <span data-ttu-id="755f5-3022">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3022">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3024">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3024">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3026">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3026">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3028">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3029">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3029">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3031">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3031">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3033">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3033">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3035">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3035">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3037">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3037">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3039">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3039">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3041">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3041">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3042">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3042">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3043">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3043">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3044">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3044">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3045">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3045">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3046">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3046">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3048">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3048">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3049">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3049">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3051">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3051">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3052">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3052">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3053">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3053">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3054">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3054">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3055">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3055">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3056">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3056">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3057">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3057">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3058">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3058">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3059">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3059">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3060">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3060">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3061">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3061">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3062">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3062">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3063">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3063">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3064">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3064">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3065">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3065">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3067">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3067">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3069">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3069">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3071">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3071">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3073">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3073">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3074">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3074">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3076">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3076">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3077">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3077">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3079">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3079">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3080">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3080">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3081">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3081">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3082">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3082">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3084">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3084">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="755f5-3085">DXGI_FORMAT_R24G8 \_ <sup>PC</sup> non con tipi (44)</span><span class="sxs-lookup"><span data-stu-id="755f5-3085">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="755f5-3086">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3086">Target</span></span> | <span data-ttu-id="755f5-3087">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3087">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3088">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3088">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3089">32</span><span class="sxs-lookup"><span data-stu-id="755f5-3089">32</span></span> |
| <span data-ttu-id="755f5-3090">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3090">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3092">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3092">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3093">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3093">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3094">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3094">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3095">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3095">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3096">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3096">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3098">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3098">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3100">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3100">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-3101">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3101">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3103">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3103">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-3104">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3105">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3106">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3107">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3107">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3108">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3109">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3109">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3111">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3111">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3112">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3112">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3113">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3113">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3114">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3115">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3116">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3117">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3118">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3118">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3119">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3120">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3121">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3122">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3124">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3125">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3126">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3127">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3127">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3129">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3130">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3131">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-3132">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3133">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3133">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-3134">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3135">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3135">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3137">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3138">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3139">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3140">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3140">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-3141">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3141">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="755f5-3142">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="755f5-3142">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="755f5-3143">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3143">Target</span></span> | <span data-ttu-id="755f5-3144">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3144">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3145">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3145">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3146">32</span><span class="sxs-lookup"><span data-stu-id="755f5-3146">32</span></span> |
| <span data-ttu-id="755f5-3147">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3147">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3149">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3149">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3150">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3150">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3151">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3151">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3152">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3152">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3153">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3153">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3155">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3157">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-3158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3158">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3160">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3160">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-3161">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3162">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3163">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3164">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3164">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3165">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3166">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3166">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3168">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3168">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3169">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3169">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3170">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3170">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3171">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3171">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3172">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3172">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3174">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3174">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3175">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3175">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3176">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3176">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3177">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3177">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3178">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3178">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3179">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3179">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3180">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3180">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3181">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3181">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3182">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3182">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3183">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3183">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3184">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3184">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3185">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3185">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3187">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3187">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3189">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3189">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3191">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3191">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3193">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3193">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3194">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3194">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-3195">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3195">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3196">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3196">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3198">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3198">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3199">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3199">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3200">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3200">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3201">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3201">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-3202">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3202">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="755f5-3203">DXGI_FORMAT_R24 \_ UNORM \_ X8 con \_ tipo<sup>FCS</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="755f5-3203">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="755f5-3204">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3204">Target</span></span> | <span data-ttu-id="755f5-3205">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3205">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3206">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3206">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3207">32</span><span class="sxs-lookup"><span data-stu-id="755f5-3207">32</span></span> |
| <span data-ttu-id="755f5-3208">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3208">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3210">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3210">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3211">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3211">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3212">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3212">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3213">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3213">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3214">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3214">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3216">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3218">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-3219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3219">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3221">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3221">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3223">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3223">Shader sample (any filter)</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3225">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3225">Shader sample\_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3227">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3227">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3228">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3228">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3229">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3229">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3230">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3230">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3232">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3232">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3233">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3233">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3234">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3234">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3235">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3235">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3236">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3236">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3237">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3237">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3238">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3238">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3239">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3239">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3240">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3240">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3241">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3241">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3242">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3242">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3243">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3243">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3244">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3244">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3245">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3245">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3246">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3246">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3247">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3247">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3248">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3248">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3250">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3250">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3251">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3251">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3252">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3252">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-3253">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3253">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3254">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3254">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-3255">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3255">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3256">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3256">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3258">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3258">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3259">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3259">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3260">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3260">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3261">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3261">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-3262">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3262">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="755f5-3263">DXGI_FORMAT_X24 \_ tipo \_ G8 \_ UINT<sup>FCS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="755f5-3263">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="755f5-3264">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3264">Target</span></span> | <span data-ttu-id="755f5-3265">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3265">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3266">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3266">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3267">32</span><span class="sxs-lookup"><span data-stu-id="755f5-3267">32</span></span> |
| <span data-ttu-id="755f5-3268">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3268">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3270">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3270">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3271">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3271">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3272">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3272">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3273">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3273">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3274">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3274">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3276">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3276">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3278">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3278">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-3279">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3279">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3281">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3281">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3283">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3283">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3284">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3284">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3285">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3285">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3286">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3286">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3287">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3287">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3288">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3288">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3290">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3290">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3291">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3291">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3292">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3292">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3293">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3293">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3294">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3294">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3295">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3295">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3296">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3296">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3297">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3297">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3298">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3298">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3299">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3299">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3300">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3300">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3301">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3301">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3302">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3302">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3303">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3303">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3304">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3304">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3305">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3305">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3306">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3306">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3308">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3308">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3309">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3309">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3310">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3310">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-3311">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3311">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3312">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3312">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-3313">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3313">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3314">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3314">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3316">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3316">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3317">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3317">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3318">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3318">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3319">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3319">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-3320">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3320">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="755f5-3321">DXGI_FORMAT_R8G8 \_ <sup>PC</sup> non con tipi (48)</span><span class="sxs-lookup"><span data-stu-id="755f5-3321">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="755f5-3322">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3322">Target</span></span> | <span data-ttu-id="755f5-3323">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3323">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3324">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3324">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3325">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3325">16</span></span> |
| <span data-ttu-id="755f5-3326">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3326">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3328">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3328">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3329">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3329">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3330">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3331">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3332">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3334">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3336">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3338">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3340">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3340">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-3341">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3341">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3342">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3342">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3343">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3343">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3344">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3344">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3345">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3345">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3346">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3346">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3348">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3348">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3349">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3349">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3350">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3351">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3351">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3352">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3352">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3353">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3353">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3354">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3354">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3355">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3355">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3356">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3356">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3357">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3357">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3358">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3358">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3359">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3359">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3360">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3360">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3361">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3361">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3362">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3362">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3363">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3363">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3364">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3364">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3366">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3366">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3367">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3367">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3368">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3368">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-3369">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3370">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3370">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-3371">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3372">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3372">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3374">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3375">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3376">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3377">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3377">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-3378">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="755f5-3379">DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="755f5-3379">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="755f5-3380">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3380">Target</span></span> | <span data-ttu-id="755f5-3381">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3381">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3382">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3383">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3383">16</span></span> |
| <span data-ttu-id="755f5-3384">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3384">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3386">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3386">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3388">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3388">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3390">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3391">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3392">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3394">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3396">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3398">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3400">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3400">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3402">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3402">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3404">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3404">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3405">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3405">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3406">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3406">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3407">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3407">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3408">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3408">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3410">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3410">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3412">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3414">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3414">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3416">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3416">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3417">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3417">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3418">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3418">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3419">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3419">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3420">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3420">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3421">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3421">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3422">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3422">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3423">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3423">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3424">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3424">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3425">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3425">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3426">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3426">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3427">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3427">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3428">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3428">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3429">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3429">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3431">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3431">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3433">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3433">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3435">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3435">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3437">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3437">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3439">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3439">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3441">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3442">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3442">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3444">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3445">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3446">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3447">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3447">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3449">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="755f5-3450">DXGI_FORMAT_R8G8 \_ uint<sup>FCS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="755f5-3450">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="755f5-3451">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3451">Target</span></span> | <span data-ttu-id="755f5-3452">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3452">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3453">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3454">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3454">16</span></span> |
| <span data-ttu-id="755f5-3455">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3455">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3457">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3457">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3459">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3459">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3461">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3461">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3462">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3462">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3463">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3463">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3465">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3465">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3467">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3467">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3469">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3469">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3471">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3471">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3473">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3474">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3474">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3475">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3475">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3476">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3476">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3477">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3477">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3478">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3478">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3480">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3480">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3481">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3483">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3483">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3484">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3484">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3486">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3486">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3487">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3487">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3488">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3488">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3489">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3489">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3490">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3490">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3491">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3491">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3492">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3492">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3493">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3493">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3494">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3494">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3495">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3495">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3496">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3496">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3497">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3497">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3498">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3498">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3500">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3500">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3502">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3502">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3504">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3504">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3506">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3507">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3507">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3509">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3509">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3510">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3510">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3512">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3512">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3513">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3513">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3514">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3514">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3515">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3515">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-3516">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3516">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="755f5-3517">DXGI_FORMAT_R8G8 \_ russo<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="755f5-3517">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="755f5-3518">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3518">Target</span></span> | <span data-ttu-id="755f5-3519">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3519">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3520">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3520">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3521">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3521">16</span></span> |
| <span data-ttu-id="755f5-3522">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3522">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3524">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3524">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3526">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3526">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3528">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3529">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3530">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3532">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3532">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3534">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3534">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3536">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3536">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3538">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3538">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3540">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3540">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3542">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3542">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3543">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3543">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3544">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3544">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3545">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3545">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3546">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3546">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3548">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3548">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3550">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3550">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3552">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3552">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3553">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3553">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3554">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3554">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3555">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3555">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3556">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3556">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3557">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3557">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3558">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3558">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3559">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3559">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3560">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3560">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3561">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3561">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3562">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3562">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3563">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3563">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3564">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3564">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3565">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3565">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3566">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3566">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3568">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3568">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3570">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3570">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3572">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3572">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3574">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3574">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3576">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3576">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3578">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3579">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3579">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3581">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3582">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3583">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3584">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3584">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-3585">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="755f5-3586">DXGI_FORMAT_R8G8 \_ Sint<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="755f5-3586">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="755f5-3587">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3587">Target</span></span> | <span data-ttu-id="755f5-3588">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3588">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3589">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3590">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3590">16</span></span> |
| <span data-ttu-id="755f5-3591">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3591">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3593">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3593">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3595">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3595">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3597">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3598">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3599">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3601">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3603">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3605">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3607">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3607">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3609">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3610">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3611">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3612">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3612">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3613">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3614">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3614">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3616">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3617">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3619">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3619">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3620">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3620">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3621">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3621">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3622">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3622">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3623">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3623">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3624">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3624">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3625">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3625">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3626">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3626">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3627">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3627">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3628">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3628">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3629">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3629">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3630">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3630">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3631">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3631">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3632">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3632">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3633">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3633">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3635">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3635">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3637">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3637">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3639">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3639">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3641">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3642">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3642">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3644">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3645">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3645">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3647">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3647">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3648">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3648">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3649">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3649">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3650">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3650">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-3651">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3651">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="755f5-3652">DXGI_FORMAT_R16 \_ <sup>PC</sup> non con tipi (53)</span><span class="sxs-lookup"><span data-stu-id="755f5-3652">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="755f5-3653">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3653">Target</span></span> | <span data-ttu-id="755f5-3654">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3654">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3655">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3655">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3656">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3656">16</span></span> |
| <span data-ttu-id="755f5-3657">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3657">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3659">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3659">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3660">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3660">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3661">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3661">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3662">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3662">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3663">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3663">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3665">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3667">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3667">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3669">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3669">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3671">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3671">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-3672">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3672">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3673">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3673">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3674">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3674">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3675">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3675">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3676">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3676">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3677">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3677">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3679">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3679">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3680">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3680">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3681">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3681">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3682">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3682">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3683">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3683">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3684">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3684">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3685">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3685">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3686">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3686">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3687">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3687">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3688">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3688">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3689">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3689">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3690">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3690">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3691">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3691">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3692">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3692">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3693">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3693">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3694">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3694">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3695">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3695">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3697">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3697">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3698">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3698">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3699">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3699">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-3700">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3700">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3701">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3701">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-3702">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3702">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3703">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3703">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3705">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3706">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3707">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3708">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3708">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3710">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="755f5-3711">DXGI_FORMAT_R16 \_ float<sup>FCS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="755f5-3711">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="755f5-3712">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3712">Target</span></span> | <span data-ttu-id="755f5-3713">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3713">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3714">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3715">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3715">16</span></span> |
| <span data-ttu-id="755f5-3716">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3716">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3718">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3718">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3720">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3720">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3722">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3722">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3723">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3723">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3724">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3724">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3726">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3728">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3730">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3732">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3732">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3734">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3734">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3736">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3737">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3738">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3738">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3739">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3740">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3740">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3742">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3742">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3744">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3746">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3746">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3748">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3749">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3750">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3751">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3752">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3752">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3753">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3754">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3755">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3756">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3757">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3758">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3759">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3760">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3761">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3761">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3763">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3763">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3765">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3765">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3767">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3767">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3769">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3769">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3771">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3771">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3773">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3773">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3774">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3774">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3776">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3777">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3778">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3779">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3779">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3781">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3781">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="755f5-3782">DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="755f5-3782">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="755f5-3783">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3783">Target</span></span> | <span data-ttu-id="755f5-3784">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3784">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3785">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3785">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3786">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3786">16</span></span> |
| <span data-ttu-id="755f5-3787">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3787">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3789">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3789">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3790">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3790">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3791">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3792">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3793">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3795">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3797">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-3798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3798">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3800">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3800">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-3801">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3801">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3802">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3803">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3804">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3804">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3805">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3806">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3806">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3808">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3809">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3810">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3811">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3812">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3812">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3814">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3814">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3815">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3815">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3816">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3816">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3817">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3817">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3818">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3818">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3819">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3819">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3820">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3820">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3821">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3821">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3822">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3822">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3823">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3823">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3824">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3824">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3825">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3825">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3827">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3827">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3829">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3829">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3831">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3831">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3833">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3834">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3834">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-3835">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3836">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3836">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3838">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3838">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3839">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3839">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3840">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3841">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3841">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3843">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3843">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="755f5-3844">DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="755f5-3844">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="755f5-3845">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3845">Target</span></span> | <span data-ttu-id="755f5-3846">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3846">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3847">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3847">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3848">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3848">16</span></span> |
| <span data-ttu-id="755f5-3849">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3849">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3851">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3851">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3853">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3853">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3855">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3855">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3856">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3856">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3857">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3857">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3859">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3859">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3861">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3861">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3863">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3863">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3865">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3865">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3867">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3867">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3869">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3869">Shader sample\_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3871">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3871">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3872">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3872">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3873">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3873">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3874">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3874">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3876">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3876">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3878">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3878">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3880">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3880">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3882">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3882">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-3883">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3883">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3884">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3884">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3885">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3885">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3886">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3886">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3887">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3887">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3888">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3888">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3889">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3889">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3890">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3890">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3891">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3891">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3892">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3892">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3893">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3893">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3894">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3894">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3895">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3895">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3897">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3897">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3899">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3899">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3901">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3901">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3903">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3903">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3905">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3905">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3907">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3907">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3908">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3908">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3910">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3910">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3911">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3911">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3912">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3912">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3913">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3913">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3915">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3915">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="755f5-3916">DXGI_FORMAT_R16 \_ uint<sup>FCS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="755f5-3916">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="755f5-3917">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3917">Target</span></span> | <span data-ttu-id="755f5-3918">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3918">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3919">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3919">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3920">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3920">16</span></span> |
| <span data-ttu-id="755f5-3921">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3921">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3923">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3923">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3925">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3925">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3927">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3927">Input Assembler Index Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3929">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3929">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3930">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3930">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-3932">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-3934">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3936">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-3936">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3938">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-3938">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3940">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-3940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-3941">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-3941">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-3942">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-3942">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-3943">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-3943">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-3944">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-3944">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-3945">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3945">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3947">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-3947">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-3948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-3948">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3950">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-3950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-3951">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-3951">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3953">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3953">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-3954">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-3954">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3955">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-3955">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-3956">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-3956">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-3957">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3957">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-3958">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3958">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-3959">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3959">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-3960">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3960">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-3961">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-3961">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-3962">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3962">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-3963">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-3963">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3964">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-3964">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-3965">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-3965">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3967">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-3967">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3969">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-3969">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3971">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-3971">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3973">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3973">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-3974">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-3974">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-3976">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-3976">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-3977">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-3977">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3979">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3979">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-3980">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3980">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-3981">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-3981">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-3982">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-3982">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3984">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-3984">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="755f5-3985">DXGI_FORMAT_R16 \_ russo<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="755f5-3985">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="755f5-3986">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-3986">Target</span></span> | <span data-ttu-id="755f5-3987">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-3987">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-3988">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-3988">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-3989">16</span><span class="sxs-lookup"><span data-stu-id="755f5-3989">16</span></span> |
| <span data-ttu-id="755f5-3990">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-3990">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3992">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-3992">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3994">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-3994">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-3996">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-3996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3997">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-3997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-3998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-3998">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4000">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4002">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4002">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4004">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4004">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4006">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4006">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4008">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4008">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4010">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4010">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4011">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4011">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4012">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4012">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4013">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4013">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4014">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4014">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4016">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4016">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4018">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4018">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4020">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4020">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4021">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4021">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4022">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4022">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4023">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4023">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4024">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4024">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4025">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4025">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4026">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4026">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4027">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4027">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4028">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4028">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4029">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4029">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4030">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4030">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4031">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4031">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4032">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4032">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4033">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4033">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4034">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4034">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4036">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4036">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4038">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4038">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4040">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4040">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4042">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4042">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4044">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4044">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4046">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4046">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4047">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4047">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4049">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4050">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4051">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4052">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4052">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4054">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4054">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="755f5-4055">DXGI_FORMAT_R16 \_ Sint<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="755f5-4055">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="755f5-4056">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4056">Target</span></span> | <span data-ttu-id="755f5-4057">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4057">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4058">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4058">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4059">16</span><span class="sxs-lookup"><span data-stu-id="755f5-4059">16</span></span> |
| <span data-ttu-id="755f5-4060">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4060">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4062">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4062">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4064">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4064">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4066">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4066">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4067">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4067">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4068">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4068">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4070">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4072">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4074">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4076">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4076">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4078">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4078">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-4079">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4079">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4080">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4080">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4081">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4081">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4082">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4082">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4083">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4083">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4085">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4085">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4086">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4086">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4088">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4089">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4090">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4091">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4092">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4093">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4093">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4094">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4095">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4096">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4097">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4098">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4099">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4100">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4101">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4102">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4102">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4104">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4104">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4106">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4106">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4108">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4108">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4110">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4110">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4111">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4111">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4113">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4113">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4114">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4114">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4116">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4116">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4117">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4117">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4118">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4118">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4119">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4119">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4121">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4121">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="755f5-4122">DXGI_FORMAT_R8 \_ <sup>PC</sup> non con tipi (60)</span><span class="sxs-lookup"><span data-stu-id="755f5-4122">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="755f5-4123">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4123">Target</span></span> | <span data-ttu-id="755f5-4124">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4124">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4125">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4125">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4126">8</span><span class="sxs-lookup"><span data-stu-id="755f5-4126">8</span></span> |
| <span data-ttu-id="755f5-4127">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4127">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4129">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4129">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4130">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4131">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4132">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4133">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4135">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4137">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4137">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4139">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4141">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4141">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-4142">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4142">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-4143">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4143">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4144">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4144">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4145">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4145">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4146">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4146">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4147">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4147">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4149">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4149">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4150">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4150">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4151">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4151">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4152">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4152">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4153">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4153">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4154">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4154">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4155">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4155">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4156">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4156">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4157">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4157">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4158">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4158">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4159">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4159">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4160">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4160">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4161">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4161">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4162">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4162">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4163">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4163">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4164">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4164">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4165">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4165">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4167">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4167">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4168">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4168">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4169">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4169">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-4170">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4170">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4171">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4171">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-4172">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4172">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4173">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4173">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4175">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4175">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4176">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4176">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4177">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4177">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4178">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4178">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4180">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4180">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="755f5-4181">DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="755f5-4181">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="755f5-4182">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4182">Target</span></span> | <span data-ttu-id="755f5-4183">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4183">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4184">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4184">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4185">8</span><span class="sxs-lookup"><span data-stu-id="755f5-4185">8</span></span> |
| <span data-ttu-id="755f5-4186">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4186">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4188">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4188">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4190">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4190">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4192">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4193">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4194">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4196">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4196">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4198">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4198">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4200">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4202">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4202">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4204">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4204">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4206">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4207">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4208">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4209">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4210">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4210">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4212">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4212">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4214">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4214">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4216">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4216">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4218">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4218">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4219">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4219">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4220">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4220">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4221">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4221">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4222">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4222">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4223">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4223">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4224">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4224">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4225">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4225">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4226">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4226">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4227">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4227">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4228">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4228">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4229">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4229">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4230">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4230">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4231">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4231">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4233">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4233">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4235">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4235">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4237">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4237">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4239">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4239">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4241">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4241">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4243">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4243">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4244">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4244">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4246">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4246">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4247">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4247">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4248">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4248">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4249">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4249">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4251">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="755f5-4252">DXGI_FORMAT_R8 \_ uint<sup>FCS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="755f5-4252">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="755f5-4253">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4253">Target</span></span> | <span data-ttu-id="755f5-4254">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4254">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4255">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4256">8</span><span class="sxs-lookup"><span data-stu-id="755f5-4256">8</span></span> |
| <span data-ttu-id="755f5-4257">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4257">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4259">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4259">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4261">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4261">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4263">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4264">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4265">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4267">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4269">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4271">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4273">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4273">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4275">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4275">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-4276">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4276">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4277">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4277">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4278">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4278">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4279">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4279">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4280">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4280">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4282">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4282">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4283">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4283">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4285">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4286">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4286">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4288">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4289">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4290">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4291">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4291">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4292">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4293">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4294">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4295">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4296">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4296">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4297">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4298">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4298">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4299">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4299">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4300">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4300">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4302">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4302">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4304">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4304">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4306">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4306">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4308">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4308">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4309">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4309">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4311">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4311">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4312">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4312">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4314">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4314">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4315">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4315">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4316">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4316">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4317">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4317">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4319">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4319">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="755f5-4320">DXGI_FORMAT_R8 \_ russo<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="755f5-4320">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="755f5-4321">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4321">Target</span></span> | <span data-ttu-id="755f5-4322">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4322">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4323">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4323">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4324">8</span><span class="sxs-lookup"><span data-stu-id="755f5-4324">8</span></span> |
| <span data-ttu-id="755f5-4325">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4325">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4327">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4327">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4329">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4329">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4331">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4332">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4333">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4335">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4335">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4337">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4337">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4339">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4339">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4341">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4341">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4343">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4343">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4345">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4346">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4347">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4347">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4348">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4349">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4349">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4351">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4351">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4353">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4355">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4355">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4356">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4356">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4357">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4357">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4358">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4358">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4359">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4359">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4360">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4360">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4361">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4361">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4362">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4362">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4363">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4364">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4365">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4365">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4366">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4367">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4367">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4368">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4368">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4369">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4369">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4371">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4371">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4373">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4373">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4375">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4375">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4377">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4377">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4379">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4379">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4381">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4382">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4382">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4384">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4385">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4386">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4387">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4387">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4389">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="755f5-4390">DXGI_FORMAT_R8 \_ Sint<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="755f5-4390">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="755f5-4391">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4391">Target</span></span> | <span data-ttu-id="755f5-4392">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4392">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4393">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4394">8</span><span class="sxs-lookup"><span data-stu-id="755f5-4394">8</span></span> |
| <span data-ttu-id="755f5-4395">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4395">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4397">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4397">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4399">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4399">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4401">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4402">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4403">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4405">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4405">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4407">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4407">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4409">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4409">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4411">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4411">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4413">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-4414">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4415">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4416">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4416">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4417">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4418">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4420">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4420">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4421">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4421">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4423">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4424">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4425">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4426">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4427">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4428">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4429">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4430">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4431">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4432">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4433">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4434">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4435">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4436">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4437">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4437">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4439">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4439">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4441">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4441">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4443">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4443">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4445">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4445">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4446">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4446">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4448">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4448">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4449">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4449">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4451">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4451">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4452">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4452">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4453">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4453">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4454">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4454">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4456">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="755f5-4457">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="755f5-4457">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="755f5-4458">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4458">Target</span></span> | <span data-ttu-id="755f5-4459">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4459">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4460">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4461">8</span><span class="sxs-lookup"><span data-stu-id="755f5-4461">8</span></span> |
| <span data-ttu-id="755f5-4462">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4462">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4464">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4464">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4465">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4466">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4467">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4468">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4470">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4470">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4472">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4472">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4474">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4474">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4476">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4476">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4478">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4478">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4480">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4480">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4481">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4481">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4482">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4482">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4483">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4483">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4484">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4484">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4486">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4486">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4488">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4488">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4490">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4490">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4492">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4492">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4493">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4493">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4494">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4494">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4495">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4495">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4496">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4496">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4497">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4497">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4498">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4498">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4499">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4499">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4500">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4500">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4501">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4501">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4502">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4502">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4503">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4503">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4504">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4504">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4505">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4505">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4507">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4507">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4509">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4509">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4511">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4511">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4513">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4513">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4515">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4515">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-4517">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4517">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4518">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4518">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-4519">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4519">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4520">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4520">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4521">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4521">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4522">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4522">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4524">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4524">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="755f5-4525">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="755f5-4525">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="755f5-4526">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4526">Target</span></span> | <span data-ttu-id="755f5-4527">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4527">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4528">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4528">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4529">32</span><span class="sxs-lookup"><span data-stu-id="755f5-4529">32</span></span> |
| <span data-ttu-id="755f5-4530">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4530">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4532">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4532">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4533">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4533">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4534">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4534">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4535">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4535">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4536">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4538">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4540">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4542">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4544">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4544">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4546">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4546">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4548">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4548">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4549">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4549">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4550">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4550">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4551">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4551">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4552">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4552">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4554">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4554">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4555">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4555">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4556">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4556">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4557">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4557">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4558">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4558">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4559">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4559">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4560">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4560">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4561">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4561">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4562">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4562">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4563">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4563">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4564">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4564">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4565">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4565">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4566">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4566">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4567">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4567">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4568">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4568">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4569">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4569">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4570">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4570">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4572">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4572">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4573">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4573">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4574">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4574">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-4575">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4575">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4576">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4576">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-4577">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4577">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4578">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4578">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-4579">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4579">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4580">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4580">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4581">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4581">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4582">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4582">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-4583">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4583">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="755f5-4584">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="755f5-4584">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="755f5-4585">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4585">Target</span></span> | <span data-ttu-id="755f5-4586">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4586">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4587">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4587">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4588">16</span><span class="sxs-lookup"><span data-stu-id="755f5-4588">16</span></span> |
| <span data-ttu-id="755f5-4589">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4589">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4591">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4591">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4592">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4592">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4593">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4593">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4594">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4594">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4595">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4595">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4597">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4597">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4599">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4599">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4601">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4601">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4603">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4603">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4605">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4605">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4607">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4607">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4608">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4608">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4609">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4609">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4610">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4610">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4611">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4611">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4613">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4614">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4615">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4616">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4617">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4618">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4619">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4620">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4620">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4621">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4622">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4623">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4624">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4625">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4626">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4627">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4628">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4629">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4629">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4631">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4632">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4633">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-4634">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4635">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4635">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-4636">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4637">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-4638">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4638">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4639">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4639">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4640">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4640">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4641">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4641">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-4642">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4642">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="755f5-4643">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="755f5-4643">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="755f5-4644">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4644">Target</span></span> | <span data-ttu-id="755f5-4645">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4645">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4646">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4646">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4647">16</span><span class="sxs-lookup"><span data-stu-id="755f5-4647">16</span></span> |
| <span data-ttu-id="755f5-4648">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4648">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4650">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4650">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4651">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4651">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4652">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4653">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4654">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4656">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4658">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4658">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4660">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4660">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4662">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4662">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4664">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4664">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4666">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4666">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4667">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4667">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4668">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4668">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4669">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4669">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4670">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4670">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4672">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4673">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4674">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4675">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4676">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4677">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4678">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4679">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4679">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4680">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4681">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4682">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4683">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4684">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4685">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4686">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4687">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4688">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4688">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4690">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4690">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4691">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4691">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4692">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4692">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-4693">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4693">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4694">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4694">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-4695">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4695">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4696">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4696">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-4697">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4697">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4698">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4698">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4699">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4699">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4700">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4700">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-4701">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="755f5-4702">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non tipizzato (70)</span><span class="sxs-lookup"><span data-stu-id="755f5-4702">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="755f5-4703">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4703">Target</span></span> | <span data-ttu-id="755f5-4704">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4704">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4705">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4706">4</span><span class="sxs-lookup"><span data-stu-id="755f5-4706">4</span></span> |
| <span data-ttu-id="755f5-4707">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4707">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4709">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4709">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4710">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4711">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4712">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4713">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-4714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4714">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4716">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4718">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4718">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4720">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4720">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-4721">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4721">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-4722">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4722">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4723">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4723">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4724">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4724">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4725">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4725">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4726">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4726">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4728">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4729">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4730">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4731">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4732">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4733">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4734">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4735">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4735">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4736">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4737">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4738">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4739">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4740">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4741">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4742">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4743">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4744">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4744">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4746">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4747">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4748">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-4749">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4750">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4750">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-4751">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4752">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4752">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4754">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4755">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4756">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4757">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4757">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4759">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4759">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="755f5-4760">DXGI_FORMAT_BC1 \_ <sup>FCC</sup> UNORM (71)</span><span class="sxs-lookup"><span data-stu-id="755f5-4760">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="755f5-4761">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4761">Target</span></span> | <span data-ttu-id="755f5-4762">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4762">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4763">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4763">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4764">4</span><span class="sxs-lookup"><span data-stu-id="755f5-4764">4</span></span> |
| <span data-ttu-id="755f5-4765">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4765">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4767">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4767">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4768">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4768">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4769">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4769">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4770">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4770">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4771">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4771">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-4772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4772">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4774">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4776">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4778">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4778">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4780">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4780">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4782">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4782">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4783">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4783">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4784">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4784">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4785">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4785">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4786">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4786">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4788">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4788">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4789">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4789">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4790">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4790">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4791">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4791">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4792">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4792">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4793">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4793">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4794">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4794">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4795">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4795">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4796">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4796">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4797">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4797">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4798">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4798">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4799">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4799">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4800">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4800">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4801">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4801">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4802">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4802">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4803">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4803">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4804">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4804">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4806">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4806">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4807">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4807">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4808">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4808">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-4809">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4809">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4810">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4810">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-4811">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4812">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4812">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4814">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4815">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4816">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4817">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4817">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4819">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="755f5-4820">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="755f5-4820">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="755f5-4821">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4821">Target</span></span> | <span data-ttu-id="755f5-4822">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4822">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4823">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4824">4</span><span class="sxs-lookup"><span data-stu-id="755f5-4824">4</span></span> |
| <span data-ttu-id="755f5-4825">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4825">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4827">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4827">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4828">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4829">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4830">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4831">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-4832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4832">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4834">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4836">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4836">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4838">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4838">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4840">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4840">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4842">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4842">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4843">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4843">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4844">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4844">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4845">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4845">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4846">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4846">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4848">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4849">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4850">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4851">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4852">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4853">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4854">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4855">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4855">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4856">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4857">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4858">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4859">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4860">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4861">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4862">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4863">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4864">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4864">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4866">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4866">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4867">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4867">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4868">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4868">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-4869">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4870">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4870">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-4871">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4872">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4872">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4874">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4875">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4876">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4877">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4877">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4879">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="755f5-4880">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non tipizzato (73)</span><span class="sxs-lookup"><span data-stu-id="755f5-4880">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="755f5-4881">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4881">Target</span></span> | <span data-ttu-id="755f5-4882">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4882">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4883">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4884">8</span><span class="sxs-lookup"><span data-stu-id="755f5-4884">8</span></span> |
| <span data-ttu-id="755f5-4885">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4885">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4887">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4887">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4888">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4888">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4889">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4890">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4891">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-4892">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4892">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4894">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4894">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4896">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4896">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4898">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4898">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-4899">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4899">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-4900">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4900">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4901">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4901">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4902">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4902">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4903">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4903">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4904">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4904">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4906">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4906">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4907">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4908">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4908">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4909">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4909">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4910">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4910">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4911">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4911">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4912">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4912">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4913">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4913">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4914">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4914">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4915">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4915">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4916">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4916">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4917">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4917">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4918">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4918">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4919">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4919">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4920">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4920">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4921">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4921">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4922">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4922">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4924">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4924">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4925">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4925">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4926">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4926">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-4927">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4927">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4928">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4928">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-4929">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4929">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4930">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4930">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4932">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4933">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4934">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4935">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4935">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4937">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="755f5-4938">DXGI_FORMAT_BC2 \_ <sup>FCC</sup> UNORM (74)</span><span class="sxs-lookup"><span data-stu-id="755f5-4938">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="755f5-4939">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4939">Target</span></span> | <span data-ttu-id="755f5-4940">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-4940">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-4941">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-4941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-4942">8</span><span class="sxs-lookup"><span data-stu-id="755f5-4942">8</span></span> |
| <span data-ttu-id="755f5-4943">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-4943">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4945">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-4945">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4946">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-4946">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4947">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-4947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4948">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-4948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-4949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-4949">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-4950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-4950">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-4952">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4954">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-4954">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4956">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-4956">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4958">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-4958">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4960">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-4960">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-4961">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-4961">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-4962">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-4962">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-4963">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-4963">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-4964">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4964">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4966">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-4966">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-4967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-4967">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4968">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-4968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4969">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-4969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-4970">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-4971">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-4971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4972">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-4972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-4973">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-4973">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-4974">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4974">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-4975">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4975">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-4976">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4976">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-4977">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4977">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-4978">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-4978">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-4979">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4979">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-4980">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-4980">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4981">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-4981">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-4982">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-4982">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4984">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-4984">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4985">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-4985">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-4986">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-4986">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-4987">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4987">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-4988">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-4988">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-4989">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-4989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-4990">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-4990">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4992">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-4993">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-4994">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-4994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-4995">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-4995">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-4997">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-4997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="755f5-4998">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="755f5-4998">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="755f5-4999">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-4999">Target</span></span> | <span data-ttu-id="755f5-5000">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5000">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5001">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5002">8</span><span class="sxs-lookup"><span data-stu-id="755f5-5002">8</span></span> |
| <span data-ttu-id="755f5-5003">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5003">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5005">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5005">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5006">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5006">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5007">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5007">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5008">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5008">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5009">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5009">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5010">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5010">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5012">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5012">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5014">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5014">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5016">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5016">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5018">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5018">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5020">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5020">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5021">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5021">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5022">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5022">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5023">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5023">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5024">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5024">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5026">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5026">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5027">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5027">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5028">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5028">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5029">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5029">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5030">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5030">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5031">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5031">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5032">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5032">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5033">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5033">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5034">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5034">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5035">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5035">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5036">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5036">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5037">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5037">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5038">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5038">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5039">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5039">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5040">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5040">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5041">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5041">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5042">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5042">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5044">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5044">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5045">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5045">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5046">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5046">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5047">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5047">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5048">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5048">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5049">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5049">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5050">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5050">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5052">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5052">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5053">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5053">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5054">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5054">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5055">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5055">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5057">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5057">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="755f5-5058">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non tipizzato (76)</span><span class="sxs-lookup"><span data-stu-id="755f5-5058">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="755f5-5059">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5059">Target</span></span> | <span data-ttu-id="755f5-5060">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5060">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5061">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5061">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5062">8</span><span class="sxs-lookup"><span data-stu-id="755f5-5062">8</span></span> |
| <span data-ttu-id="755f5-5063">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5063">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5065">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5065">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5066">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5066">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5067">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5067">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5068">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5068">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5069">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5069">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5070">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5072">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5074">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5076">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5076">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-5077">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5077">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-5078">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5078">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5079">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5079">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5080">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5080">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5081">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5081">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5082">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5082">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5084">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5084">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5085">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5085">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5086">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5087">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5088">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5089">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5090">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5091">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5091">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5092">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5093">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5094">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5095">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5096">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5097">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5098">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5099">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5100">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5100">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5102">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5102">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5103">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5103">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5104">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5104">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5105">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5105">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5106">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5106">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5107">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5108">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5108">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5110">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5111">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5112">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5113">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5113">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5115">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="755f5-5116">DXGI_FORMAT_BC3 \_ <sup>FCC</sup> UNORM (77)</span><span class="sxs-lookup"><span data-stu-id="755f5-5116">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="755f5-5117">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5117">Target</span></span> | <span data-ttu-id="755f5-5118">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5118">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5119">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5120">8</span><span class="sxs-lookup"><span data-stu-id="755f5-5120">8</span></span> |
| <span data-ttu-id="755f5-5121">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5121">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5123">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5123">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5124">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5125">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5126">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5127">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5128">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5130">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5132">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5134">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5134">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5136">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5136">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5138">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5138">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5139">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5139">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5140">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5140">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5141">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5141">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5142">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5142">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5144">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5145">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5147">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5148">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5149">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5150">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5151">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5151">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5152">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5153">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5154">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5155">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5157">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5158">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5159">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5160">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5160">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5162">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5163">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5164">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5165">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5166">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5166">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5167">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5168">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5168">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5170">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5171">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5172">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5173">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5173">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5175">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="755f5-5176">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="755f5-5176">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="755f5-5177">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5177">Target</span></span> | <span data-ttu-id="755f5-5178">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5178">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5179">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5180">8</span><span class="sxs-lookup"><span data-stu-id="755f5-5180">8</span></span> |
| <span data-ttu-id="755f5-5181">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5181">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5183">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5183">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5184">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5184">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5185">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5186">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5186">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5187">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5188">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5188">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5190">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5190">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5192">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5192">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5194">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5194">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5196">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5196">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5198">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5198">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5199">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5199">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5200">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5200">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5201">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5201">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5202">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5202">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5204">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5204">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5205">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5206">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5207">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5208">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5209">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5210">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5211">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5211">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5212">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5213">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5214">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5215">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5216">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5217">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5218">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5218">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5219">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5219">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5220">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5220">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5222">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5223">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5224">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5225">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5226">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5226">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5227">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5228">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5228">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5230">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5231">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5232">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5233">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5233">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5235">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5235">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="755f5-5236">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non tipizzato (79)</span><span class="sxs-lookup"><span data-stu-id="755f5-5236">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="755f5-5237">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5237">Target</span></span> | <span data-ttu-id="755f5-5238">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5238">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5239">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5239">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5240">4</span><span class="sxs-lookup"><span data-stu-id="755f5-5240">4</span></span> |
| <span data-ttu-id="755f5-5241">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5241">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5243">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5243">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5244">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5244">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5245">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5245">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5246">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5246">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5247">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5248">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5250">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5252">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5254">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5254">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-5255">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5255">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-5256">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5256">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5257">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5257">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5258">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5258">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5259">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5259">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5260">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5260">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5262">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5263">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5264">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5265">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5266">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5267">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5268">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5269">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5269">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5270">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5271">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5272">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5273">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5274">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5275">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5276">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5277">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5278">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5278">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5280">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5280">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5281">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5281">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5282">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5282">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5283">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5283">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5284">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5284">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5285">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5285">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5286">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5286">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5288">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5289">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5290">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5291">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5291">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-5292">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="755f5-5293">DXGI_FORMAT_BC4 \_ <sup>FCC</sup> UNORM (80)</span><span class="sxs-lookup"><span data-stu-id="755f5-5293">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="755f5-5294">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5294">Target</span></span> | <span data-ttu-id="755f5-5295">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5295">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5296">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5297">4</span><span class="sxs-lookup"><span data-stu-id="755f5-5297">4</span></span> |
| <span data-ttu-id="755f5-5298">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5298">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5300">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5300">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5301">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5301">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5302">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5303">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5304">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5305">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5305">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5307">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5307">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5309">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5309">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5311">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5311">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5313">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5313">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5315">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5316">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5317">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5317">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5318">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5319">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5319">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5321">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5322">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5323">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5323">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5324">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5324">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5325">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5325">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5326">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5326">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5327">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5327">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5328">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5328">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5329">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5329">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5330">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5330">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5331">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5331">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5332">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5332">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5333">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5333">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5334">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5334">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5335">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5335">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5336">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5336">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5337">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5337">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5339">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5339">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5340">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5340">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5341">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5341">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5342">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5342">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5343">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5343">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5344">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5345">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5345">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5347">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5348">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5349">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5350">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5350">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-5351">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5351">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="755f5-5352">DXGI_FORMAT_BC4 \_ russare<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="755f5-5352">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="755f5-5353">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5353">Target</span></span> | <span data-ttu-id="755f5-5354">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5354">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5355">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5355">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5356">4</span><span class="sxs-lookup"><span data-stu-id="755f5-5356">4</span></span> |
| <span data-ttu-id="755f5-5357">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5357">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5359">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5359">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5360">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5360">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5361">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5361">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5362">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5362">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5363">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5363">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5364">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5364">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5366">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5366">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5368">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5368">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5370">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5370">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5372">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5372">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5374">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5375">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5376">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5376">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5377">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5378">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5378">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5380">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5381">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5382">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5383">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5384">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5385">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5386">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5387">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5387">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5388">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5389">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5390">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5391">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5393">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5394">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5395">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5396">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5396">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5398">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5399">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5400">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5401">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5402">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5402">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5403">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5404">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5404">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5406">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5407">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5408">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5409">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5409">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-5410">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="755f5-5411">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non tipizzato (82)</span><span class="sxs-lookup"><span data-stu-id="755f5-5411">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="755f5-5412">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5412">Target</span></span> | <span data-ttu-id="755f5-5413">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5413">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5414">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5415">8</span><span class="sxs-lookup"><span data-stu-id="755f5-5415">8</span></span> |
| <span data-ttu-id="755f5-5416">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5416">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5418">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5418">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5419">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5419">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5420">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5420">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5421">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5421">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5422">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5422">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5423">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5425">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5427">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5429">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5429">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-5430">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5430">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-5431">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5431">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5432">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5432">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5433">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5433">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5434">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5434">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5435">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5435">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5437">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5437">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5438">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5438">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5439">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5439">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5440">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5440">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5441">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5441">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5442">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5442">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5443">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5443">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5444">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5444">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5445">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5445">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5446">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5446">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5447">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5447">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5448">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5448">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5449">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5449">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5450">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5450">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5451">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5451">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5452">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5452">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5453">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5453">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5455">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5455">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5456">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5456">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5457">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5457">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5458">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5458">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5459">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5459">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5460">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5460">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5461">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5461">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5463">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5463">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5464">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5464">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5465">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5465">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5466">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5466">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-5467">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5467">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="755f5-5468">DXGI_FORMAT_BC5 \_ <sup>FCC</sup> UNORM (83)</span><span class="sxs-lookup"><span data-stu-id="755f5-5468">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="755f5-5469">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5469">Target</span></span> | <span data-ttu-id="755f5-5470">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5470">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5471">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5471">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5472">8</span><span class="sxs-lookup"><span data-stu-id="755f5-5472">8</span></span> |
| <span data-ttu-id="755f5-5473">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5473">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5475">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5475">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5476">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5476">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5477">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5477">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5478">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5478">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5479">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5479">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5480">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5480">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5482">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5482">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5484">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5484">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5486">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5486">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5488">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5488">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5490">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5490">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5491">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5491">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5492">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5492">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5493">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5493">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5494">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5494">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5496">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5496">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5497">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5497">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5498">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5498">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5499">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5499">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5500">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5500">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5501">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5501">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5502">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5502">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5503">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5503">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5504">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5504">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5505">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5505">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5506">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5506">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5507">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5507">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5508">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5508">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5509">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5509">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5510">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5510">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5511">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5511">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5512">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5512">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5514">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5514">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5515">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5515">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5516">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5516">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5517">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5517">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5518">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5518">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5519">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5520">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5520">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5522">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5523">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5524">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5525">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5525">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-5526">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="755f5-5527">DXGI_FORMAT_BC5 \_ russare<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="755f5-5527">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="755f5-5528">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5528">Target</span></span> | <span data-ttu-id="755f5-5529">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5529">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5530">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5531">8</span><span class="sxs-lookup"><span data-stu-id="755f5-5531">8</span></span> |
| <span data-ttu-id="755f5-5532">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5532">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5534">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5534">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5535">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5535">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5536">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5536">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5537">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5537">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5538">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5538">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-5539">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5539">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5541">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5541">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5543">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5545">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5545">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5547">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5547">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5549">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5549">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5550">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5550">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5551">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5551">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5552">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5552">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5553">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5553">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5555">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5555">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5556">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5556">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5557">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5557">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5558">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5558">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5559">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5559">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5560">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5560">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5561">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5561">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5562">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5562">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5563">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5563">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5564">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5564">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5565">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5565">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5566">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5566">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5567">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5567">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5568">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5568">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5569">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5569">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5570">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5570">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5571">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5571">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5573">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5573">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5574">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5574">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5575">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5575">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5576">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5576">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5577">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5577">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5578">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5579">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5579">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5581">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5582">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5583">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5584">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5584">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-5585">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="755f5-5586">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="755f5-5586">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="755f5-5587">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5587">Target</span></span> | <span data-ttu-id="755f5-5588">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5588">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5589">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5590">16</span><span class="sxs-lookup"><span data-stu-id="755f5-5590">16</span></span> |
| <span data-ttu-id="755f5-5591">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5591">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5593">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5593">Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5595">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5595">Input Assembler Vertex Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5597">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5598">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5599">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5601">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5603">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5605">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5607">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5607">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5609">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5609">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5611">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5612">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5613">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5613">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5614">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5615">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5615">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5617">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5617">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5619">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5621">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5621">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5623">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5623">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5624">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5624">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5625">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5625">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5626">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5626">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5627">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5627">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5628">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5628">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5629">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5629">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5630">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5630">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5631">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5631">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5632">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5632">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5633">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5633">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5634">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5634">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5635">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5635">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5636">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5636">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5638">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5638">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5640">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5640">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5642">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5642">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5644">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5644">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5646">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5646">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5648">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5648">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5649">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5649">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-5650">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5650">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5651">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5651">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5652">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5652">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5653">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5653">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-5654">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5654">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="755f5-5655">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="755f5-5655">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="755f5-5656">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5656">Target</span></span> | <span data-ttu-id="755f5-5657">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5657">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5658">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5658">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5659">16</span><span class="sxs-lookup"><span data-stu-id="755f5-5659">16</span></span> |
| <span data-ttu-id="755f5-5660">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5660">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5662">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5662">Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5664">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5664">Input Assembler Vertex Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5666">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5666">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5667">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5667">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5668">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5668">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5670">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5670">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5672">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5672">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5674">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5674">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5676">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5676">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5678">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5678">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5680">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5681">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5682">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5682">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5683">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5684">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5684">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5686">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5686">Mipmap Auto-Generation</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5688">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5688">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5690">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5690">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5692">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5692">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5693">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5693">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5694">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5694">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5695">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5695">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5696">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5696">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5697">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5697">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5698">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5698">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5699">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5699">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5700">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5700">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5701">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5701">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5702">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5702">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5703">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5703">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5704">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5704">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5705">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5705">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5707">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5707">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5709">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5709">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5711">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5711">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5713">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5713">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5715">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5715">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5717">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5718">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-5719">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5719">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5720">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5720">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5721">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5721">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5722">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5722">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-5723">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5723">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="755f5-5724">DXGI_FORMAT_B8G8R8A8 \_ <sup>PC</sup> non con tipi (90)</span><span class="sxs-lookup"><span data-stu-id="755f5-5724">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="755f5-5725">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5725">Target</span></span> | <span data-ttu-id="755f5-5726">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5726">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5727">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5727">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5728">32</span><span class="sxs-lookup"><span data-stu-id="755f5-5728">32</span></span> |
| <span data-ttu-id="755f5-5729">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5729">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5731">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5731">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5732">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5732">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5733">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5734">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5735">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5737">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5739">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5741">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5743">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5743">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-5744">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5744">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-5745">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5745">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5746">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5746">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5747">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5747">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5748">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5748">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5749">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5749">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5751">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5751">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5752">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5752">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5753">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5753">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5754">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5754">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5755">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5755">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5756">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5756">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5757">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5757">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5758">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5758">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5759">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5759">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5760">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5760">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5761">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5761">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5762">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5762">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5763">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5763">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5764">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5764">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5765">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5765">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5766">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5766">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5767">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5767">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5769">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5770">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5771">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5772">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5773">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5773">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5774">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5775">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5775">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5777">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5777">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5778">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5778">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5779">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5779">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5780">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5780">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5782">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="755f5-5783">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="755f5-5783">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="755f5-5784">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5784">Target</span></span> | <span data-ttu-id="755f5-5785">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5785">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5786">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5787">32</span><span class="sxs-lookup"><span data-stu-id="755f5-5787">32</span></span> |
| <span data-ttu-id="755f5-5788">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5788">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5790">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5790">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5792">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5792">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5794">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5794">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5795">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5795">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5796">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5796">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5798">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5798">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5800">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5800">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5802">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5802">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5804">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5804">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5806">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5806">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5808">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5808">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5809">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5809">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5810">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5810">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5811">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5811">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5812">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5812">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5814">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5814">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5816">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5816">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5818">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5818">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5820">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5820">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5821">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5821">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5822">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5822">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5823">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5823">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5824">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5824">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5825">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5825">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5826">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5826">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5827">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5827">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5828">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5828">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5829">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5829">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5830">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5830">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5831">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5831">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5832">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5832">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5833">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5833">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5835">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5835">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5837">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5837">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5839">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5839">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5841">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5841">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5843">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5843">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5845">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5845">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5847">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5847">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5849">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5849">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5850">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5850">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5852">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5852">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5854">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5854">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5856">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5856">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="755f5-5857">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="755f5-5857">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="755f5-5858">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5858">Target</span></span> | <span data-ttu-id="755f5-5859">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5859">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5860">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5860">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5861">32</span><span class="sxs-lookup"><span data-stu-id="755f5-5861">32</span></span> |
| <span data-ttu-id="755f5-5862">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5862">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5864">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5864">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5865">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5865">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5866">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5866">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5867">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5867">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5868">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5868">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5870">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5872">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5872">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5874">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5874">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5876">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5876">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5878">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5878">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5880">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5880">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5881">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5881">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5882">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5882">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5883">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5883">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5884">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5884">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5886">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5886">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5888">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5888">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5890">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5890">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5892">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5893">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5894">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5895">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5896">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5897">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5898">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5899">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5900">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5901">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5902">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5903">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5904">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5905">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5905">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5907">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5907">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5909">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5909">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5911">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5911">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5913">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5913">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5915">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5915">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5917">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5917">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5919">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5919">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5921">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5921">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5922">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5922">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5924">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5924">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-5926">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5926">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5928">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="755f5-5929">DXGI_FORMAT_B8G8R8X8 \_ <sup>PC</sup> non con tipi (92)</span><span class="sxs-lookup"><span data-stu-id="755f5-5929">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="755f5-5930">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5930">Target</span></span> | <span data-ttu-id="755f5-5931">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5931">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5932">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5933">32</span><span class="sxs-lookup"><span data-stu-id="755f5-5933">32</span></span> |
| <span data-ttu-id="755f5-5934">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5934">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5936">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5936">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5937">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5937">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5938">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5938">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5939">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-5939">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-5940">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-5940">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5942">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-5942">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5944">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-5944">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5946">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-5946">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5948">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-5948">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-5949">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-5949">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-5950">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-5950">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-5951">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-5951">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-5952">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-5952">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-5953">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-5953">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-5954">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5954">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5956">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-5956">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-5957">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-5957">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5958">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-5958">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5959">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-5959">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-5960">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5960">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-5961">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-5961">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5962">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-5962">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-5963">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-5963">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-5964">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5964">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-5965">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5965">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-5966">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5966">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-5967">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5967">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-5968">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-5968">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-5969">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5969">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-5970">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-5970">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5971">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-5971">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-5972">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-5972">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5974">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-5974">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5975">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-5975">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-5976">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-5976">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-5977">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5977">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-5978">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-5978">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-5979">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-5979">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-5980">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-5980">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5982">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5982">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-5983">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5983">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-5984">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-5984">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-5985">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-5985">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5987">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-5987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="755f5-5988">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="755f5-5988">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="755f5-5989">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-5989">Target</span></span> | <span data-ttu-id="755f5-5990">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-5990">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-5991">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-5991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-5992">32</span><span class="sxs-lookup"><span data-stu-id="755f5-5992">32</span></span> |
| <span data-ttu-id="755f5-5993">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-5993">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5995">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-5995">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5997">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-5997">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-5999">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-5999">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6000">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6000">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6001">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6001">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6003">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6005">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6007">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6009">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6009">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6011">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6011">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6013">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6013">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6014">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6014">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6015">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6015">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6016">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6016">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6017">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6017">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6019">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6019">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6021">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6021">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6023">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6023">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6025">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6025">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6026">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6026">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6027">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6027">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6028">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6028">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6029">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6029">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6030">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6030">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6031">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6031">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6032">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6032">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6033">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6033">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6034">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6034">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6035">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6035">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6036">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6036">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6037">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6037">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6038">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6038">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6040">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6040">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6042">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6042">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6044">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6044">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6046">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6046">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6048">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6048">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6050">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6050">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6051">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6051">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6053">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6053">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-6054">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6054">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6056">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6056">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6058">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6058">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6060">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6060">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="755f5-6061">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="755f5-6061">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="755f5-6062">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6062">Target</span></span> | <span data-ttu-id="755f5-6063">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6063">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6064">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6064">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6065">32</span><span class="sxs-lookup"><span data-stu-id="755f5-6065">32</span></span> |
| <span data-ttu-id="755f5-6066">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6066">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6068">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6068">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6069">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6069">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6070">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6070">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6071">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6071">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6072">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6072">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6074">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6074">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6076">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6076">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6078">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6080">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6080">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6082">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6082">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6084">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6084">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6085">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6085">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6086">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6086">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6087">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6087">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6088">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6088">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6090">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6090">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6092">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6092">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6094">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6094">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6096">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6096">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6097">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6097">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6098">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6098">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6099">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6099">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6100">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6100">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6101">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6101">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6102">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6102">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6103">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6103">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6104">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6104">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6105">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6105">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6106">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6106">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6107">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6107">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6108">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6108">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6109">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6109">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6111">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6111">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6113">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6113">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6115">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6115">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6117">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6117">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6119">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6119">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6121">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6122">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6122">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6124">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-6125">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-6126">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-6127">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6127">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6129">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6129">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="755f5-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="755f5-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="755f5-6131">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6131">Target</span></span> | <span data-ttu-id="755f5-6132">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6132">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6133">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6133">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6134">32</span><span class="sxs-lookup"><span data-stu-id="755f5-6134">32</span></span> |
| <span data-ttu-id="755f5-6135">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6135">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6137">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6137">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6138">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6138">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6139">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6139">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6140">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6140">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6141">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6141">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6142">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6142">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6144">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6144">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6145">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6145">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6146">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6146">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6148">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6148">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6150">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6150">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6151">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6151">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6152">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6152">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6153">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6153">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6154">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6154">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6156">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6156">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6158">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6158">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6160">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6160">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6162">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6162">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6163">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6163">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6164">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6164">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6165">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6165">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6166">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6166">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6167">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6167">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6168">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6168">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6169">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6169">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6170">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6170">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6171">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6171">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6172">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6172">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6173">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6173">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6174">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6174">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6175">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6175">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6177">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6178">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6179">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6180">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6181">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6181">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6182">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6183">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6184">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6184">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6186">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6186">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6188">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6188">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6190">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6190">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6192">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6192">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="755f5-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="755f5-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="755f5-6194">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6194">Target</span></span> | <span data-ttu-id="755f5-6195">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6195">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6196">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6196">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6197">32</span><span class="sxs-lookup"><span data-stu-id="755f5-6197">32</span></span> |
| <span data-ttu-id="755f5-6198">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6198">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6200">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6200">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6201">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6201">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6202">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6202">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6203">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6203">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6204">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6204">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6205">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6205">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6207">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6207">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6208">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6209">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6209">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6211">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6211">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6213">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6213">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6214">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6214">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6215">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6215">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6216">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6216">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6217">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6217">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6218">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6218">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6219">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6219">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6220">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6220">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6221">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6221">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6222">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6222">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6223">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6223">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6224">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6224">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6225">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6225">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6226">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6226">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6227">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6227">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6228">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6228">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6229">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6229">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6230">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6230">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6231">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6231">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6232">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6232">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6233">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6233">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6234">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6234">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6236">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6236">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6237">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6237">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6238">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6238">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6239">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6239">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6240">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6240">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6241">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6241">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6242">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6242">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6243">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6243">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6245">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6245">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6247">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6247">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6249">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6249">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6251">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="755f5-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="755f5-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="755f5-6253">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6253">Target</span></span> | <span data-ttu-id="755f5-6254">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6254">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6255">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6256">64</span><span class="sxs-lookup"><span data-stu-id="755f5-6256">64</span></span> |
| <span data-ttu-id="755f5-6257">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6257">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6259">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6259">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6260">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6260">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6261">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6261">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6262">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6262">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6263">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6263">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6264">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6264">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6266">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6266">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6267">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6267">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6268">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6268">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6270">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6270">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6272">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6272">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6273">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6273">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6274">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6274">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6275">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6275">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6276">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6276">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6278">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6279">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6280">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6281">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6282">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6283">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6284">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6285">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6285">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6286">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6287">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6288">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6289">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6291">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6292">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6293">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6294">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6294">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6296">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6297">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6298">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6299">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6300">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6300">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6301">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6302">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6303">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6303">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6305">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6305">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6307">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6307">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6309">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6309">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6311">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="755f5-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="755f5-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="755f5-6313">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6313">Target</span></span> | <span data-ttu-id="755f5-6314">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6314">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6315">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6316">8</span><span class="sxs-lookup"><span data-stu-id="755f5-6316">8</span></span> |
| <span data-ttu-id="755f5-6317">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6317">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6319">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6319">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6320">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6320">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6321">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6321">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6322">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6322">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6323">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6324">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6324">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6326">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6326">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6327">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6328">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6328">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6330">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6330">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6332">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6332">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6333">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6333">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6334">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6334">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6335">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6335">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6336">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6336">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6337">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6337">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6338">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6338">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6340">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6340">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6342">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6343">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6344">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6345">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6346">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6346">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6347">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6348">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6349">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6350">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6352">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6353">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6354">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6355">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6355">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6357">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6358">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6359">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6360">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6361">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6361">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6362">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6363">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6364">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6364">Video Decoder Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6366">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6366">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6368">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6368">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6370">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6370">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6372">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="755f5-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="755f5-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="755f5-6374">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6374">Target</span></span> | <span data-ttu-id="755f5-6375">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6375">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6376">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6377">16</span><span class="sxs-lookup"><span data-stu-id="755f5-6377">16</span></span> |
| <span data-ttu-id="755f5-6378">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6378">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6380">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6380">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6381">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6381">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6382">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6382">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6383">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6383">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6384">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6384">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6385">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6385">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6387">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6387">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6388">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6388">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6389">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6389">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6391">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6391">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6393">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6393">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6394">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6394">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6395">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6395">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6396">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6396">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6397">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6397">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6398">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6399">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6401">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6401">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6403">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6403">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6404">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6404">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6405">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6405">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6406">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6406">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6407">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6407">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6408">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6408">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6409">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6409">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6410">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6410">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6411">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6411">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6412">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6412">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6413">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6413">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6414">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6414">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6415">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6415">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6416">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6416">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6418">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6418">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6419">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6419">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6420">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6420">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6421">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6421">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6422">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6422">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6423">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6423">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6424">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6424">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6425">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6425">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6427">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6427">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6429">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6429">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6431">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6431">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6433">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6433">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="755f5-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="755f5-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="755f5-6435">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6435">Target</span></span> | <span data-ttu-id="755f5-6436">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6436">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6437">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6437">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6438">16</span><span class="sxs-lookup"><span data-stu-id="755f5-6438">16</span></span> |
| <span data-ttu-id="755f5-6439">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6439">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6441">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6441">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6442">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6442">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6443">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6443">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6444">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6444">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6445">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6445">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6446">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6446">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6448">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6448">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6449">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6449">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6450">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6450">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6452">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6452">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6454">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6454">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6455">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6455">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6456">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6456">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6457">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6457">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6458">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6458">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6459">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6460">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6462">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6462">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6464">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6465">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6466">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6467">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6468">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6468">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6469">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6470">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6471">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6472">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6473">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6474">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6475">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6476">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6477">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6477">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6479">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6480">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6481">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6482">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6483">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6483">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6484">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6485">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6486">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6486">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6488">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6488">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6490">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6490">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6492">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6492">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6494">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="755f5-6495">DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="755f5-6495">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="755f5-6496">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6496">Target</span></span> | <span data-ttu-id="755f5-6497">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6497">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6498">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6499">8</span><span class="sxs-lookup"><span data-stu-id="755f5-6499">8</span></span> |
| <span data-ttu-id="755f5-6500">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6500">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6502">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6502">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6503">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6503">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6504">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6504">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6505">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6505">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6506">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6506">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6507">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6507">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6509">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6509">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6510">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6510">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6511">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6511">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-6512">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6512">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-6513">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6513">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6514">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6514">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6515">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6515">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6516">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6516">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6517">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6517">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6518">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6518">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6519">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6520">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6520">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6521">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6521">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6522">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6522">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6523">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6523">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6524">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6524">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6525">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6525">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6526">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6526">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6527">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6527">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6528">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6528">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6529">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6529">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6530">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6530">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6531">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6531">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6532">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6532">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6533">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6533">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6534">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6534">CPU Lockable</span></span> | \- |
| <span data-ttu-id="755f5-6535">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6535">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6536">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6536">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6537">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6537">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6538">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6538">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6539">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6539">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6540">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6540">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6541">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6541">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6542">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6542">Video Decoder Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6544">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6544">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6546">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6546">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6548">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6548">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6550">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="755f5-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="755f5-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="755f5-6552">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6552">Target</span></span> | <span data-ttu-id="755f5-6553">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6553">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6554">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6555">16</span><span class="sxs-lookup"><span data-stu-id="755f5-6555">16</span></span> |
| <span data-ttu-id="755f5-6556">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6556">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6558">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6558">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6559">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6559">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6560">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6561">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6562">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6563">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6563">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6565">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6565">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6566">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6566">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6567">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6567">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6569">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6569">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6571">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6571">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6572">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6572">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6573">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6573">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6574">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6574">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6575">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6575">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6576">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6576">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6577">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6577">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6578">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6578">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6579">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6579">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6580">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6580">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6581">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6581">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6582">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6582">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6583">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6583">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6584">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6584">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6585">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6585">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6586">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6586">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6587">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6587">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6588">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6588">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6589">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6589">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6590">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6590">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6591">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6591">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6592">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6592">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6594">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6594">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6595">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6595">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6596">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6596">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6597">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6597">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6598">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6598">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6599">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6599">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6600">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6600">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6601">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6601">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6603">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6603">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6605">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6605">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6607">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6607">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6609">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6609">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="755f5-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="755f5-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="755f5-6611">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6611">Target</span></span> | <span data-ttu-id="755f5-6612">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6612">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6613">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6613">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6614">32</span><span class="sxs-lookup"><span data-stu-id="755f5-6614">32</span></span> |
| <span data-ttu-id="755f5-6615">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6615">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6617">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6617">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6618">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6618">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6619">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6619">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6620">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6620">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6621">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6621">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6622">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6622">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6624">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6624">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6625">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6625">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6626">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6626">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6628">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6628">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6630">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6630">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6631">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6631">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6632">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6632">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6633">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6633">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6634">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6634">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6635">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6635">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6636">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6637">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6637">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6638">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6638">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6639">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6639">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6640">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6640">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6641">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6641">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6642">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6642">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6643">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6643">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6644">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6644">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6645">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6645">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6646">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6646">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6647">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6647">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6648">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6648">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6649">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6649">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6650">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6650">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6651">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6651">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6653">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6653">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6654">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6654">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6655">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6655">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6656">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6656">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6657">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6657">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6658">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6658">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6659">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6659">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6660">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6660">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6662">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6662">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6664">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6664">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6666">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6666">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6668">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6668">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="755f5-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="755f5-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="755f5-6670">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6670">Target</span></span> | <span data-ttu-id="755f5-6671">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6671">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6672">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6672">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6673">32</span><span class="sxs-lookup"><span data-stu-id="755f5-6673">32</span></span> |
| <span data-ttu-id="755f5-6674">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6674">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6676">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6676">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6677">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6677">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6678">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6678">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6679">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6679">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6680">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6680">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6681">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6681">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6683">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6683">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6684">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6685">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6685">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6687">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6687">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6689">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6689">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6690">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6690">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6691">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6691">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6692">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6692">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6693">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6693">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6694">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6694">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6695">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6695">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6696">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6696">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6697">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6697">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6698">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6698">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6699">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6699">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6700">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6700">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6701">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6701">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6702">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6702">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6703">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6703">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6704">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6704">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6705">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6705">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6706">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6706">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6707">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6707">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6708">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6708">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6709">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6709">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6710">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6710">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6712">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6712">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6713">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6713">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6714">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6714">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6715">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6715">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6716">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6716">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6717">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6718">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6719">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6719">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6721">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6721">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6723">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6723">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6725">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6725">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6727">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6727">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="755f5-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="755f5-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="755f5-6729">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6729">Target</span></span> | <span data-ttu-id="755f5-6730">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6730">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6731">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6731">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6732">8</span><span class="sxs-lookup"><span data-stu-id="755f5-6732">8</span></span> |
| <span data-ttu-id="755f5-6733">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6733">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6735">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6735">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6736">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6736">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6737">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6737">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6738">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6738">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6739">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6739">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6740">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6740">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6742">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6742">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6743">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6743">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6744">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6744">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6746">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6746">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6748">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6748">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6749">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6749">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6750">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6750">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6751">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6752">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6752">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6753">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6753">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6754">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6754">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6756">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6756">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6758">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6758">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6759">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6759">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6760">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6760">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6761">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6761">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6762">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6762">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6763">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6763">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6764">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6764">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6765">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6765">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6766">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6766">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6767">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6767">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6768">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6768">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6769">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6769">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6770">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6770">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6771">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6771">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6773">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6773">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6774">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6774">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6775">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6775">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6776">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6776">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6777">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6777">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6778">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6778">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6779">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6779">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6780">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6780">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6782">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6782">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6784">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6784">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6786">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6786">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6788">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6788">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="755f5-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="755f5-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="755f5-6790">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6790">Target</span></span> | <span data-ttu-id="755f5-6791">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6791">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6792">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6792">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6793">8</span><span class="sxs-lookup"><span data-stu-id="755f5-6793">8</span></span> |
| <span data-ttu-id="755f5-6794">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6794">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6796">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6796">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6797">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6797">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6798">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6798">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6799">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6799">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6800">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6800">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6801">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6801">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6803">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6803">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6804">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6804">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6805">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6805">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-6806">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6806">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-6807">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6807">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6808">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6808">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6809">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6809">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6810">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6810">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6811">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6811">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6812">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6812">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6813">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6814">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6814">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6815">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6815">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6816">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6816">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6817">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6817">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6818">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6818">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6819">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6819">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6820">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6820">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6821">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6821">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6822">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6822">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6823">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6823">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6824">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6824">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6825">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6825">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6826">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6826">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6827">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6827">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6828">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6828">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6830">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6830">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6831">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6831">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6832">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6832">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6833">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6834">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6834">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6835">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6836">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6836">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6837">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6837">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-6838">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6838">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6840">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-6841">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6841">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-6842">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6842">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="755f5-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="755f5-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="755f5-6844">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6844">Target</span></span> | <span data-ttu-id="755f5-6845">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6845">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6846">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6846">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6847">8</span><span class="sxs-lookup"><span data-stu-id="755f5-6847">8</span></span> |
| <span data-ttu-id="755f5-6848">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6848">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6850">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6850">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6851">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6851">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6852">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6852">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6853">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6853">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6854">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6854">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6855">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6857">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6858">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6859">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6859">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-6860">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6860">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-6861">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6861">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6862">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6862">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6863">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6863">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6864">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6864">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6865">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6865">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6866">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6867">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6868">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6869">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6870">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6871">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6872">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6873">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6873">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6874">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6875">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6876">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6877">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6879">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6880">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6881">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6882">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6882">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6884">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6885">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6886">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6887">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6888">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6888">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6889">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6890">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6890">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6891">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6891">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-6892">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6892">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6894">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-6895">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6895">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-6896">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6896">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="755f5-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="755f5-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="755f5-6898">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6898">Target</span></span> | <span data-ttu-id="755f5-6899">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6899">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6900">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6900">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6901">8</span><span class="sxs-lookup"><span data-stu-id="755f5-6901">8</span></span> |
| <span data-ttu-id="755f5-6902">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6902">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6904">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6904">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6905">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6905">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6906">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6906">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6907">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6907">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6908">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6908">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6909">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6909">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6911">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6911">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6912">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6912">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6913">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6913">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-6914">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6914">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-6915">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6915">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6916">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6916">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6917">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6917">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6918">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6918">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6919">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6919">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6920">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6920">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6921">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6921">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6922">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6922">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6923">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6923">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6924">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6924">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6925">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6925">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6926">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6926">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6927">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6927">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6928">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6928">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6929">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6929">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6930">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6930">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6931">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6931">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6932">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6932">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6933">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6933">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6934">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6934">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6935">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6935">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6936">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6936">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6938">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6938">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6939">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6939">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6940">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6940">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6941">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6941">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6942">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6942">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6943">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6943">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6944">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6944">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6945">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6945">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-6946">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6946">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6948">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6948">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-6949">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-6949">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-6950">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-6950">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="755f5-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="755f5-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="755f5-6952">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6952">Target</span></span> | <span data-ttu-id="755f5-6953">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-6953">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-6954">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-6954">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-6955">16</span><span class="sxs-lookup"><span data-stu-id="755f5-6955">16</span></span> |
| <span data-ttu-id="755f5-6956">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-6956">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-6958">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-6958">Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6959">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-6959">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6960">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-6960">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6961">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-6961">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-6962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-6962">Texture1D</span></span> | \- |
| <span data-ttu-id="755f5-6963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-6963">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-6965">Texture3D</span></span> | \- |
| <span data-ttu-id="755f5-6966">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-6966">TextureCube</span></span> | \- |
| <span data-ttu-id="755f5-6967">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-6967">Shader ld</span></span> | \- |
| <span data-ttu-id="755f5-6968">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-6968">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="755f5-6969">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-6969">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-6970">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-6970">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-6971">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-6971">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-6972">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-6972">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-6973">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6973">Mipmap</span></span> | \- |
| <span data-ttu-id="755f5-6974">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-6974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="755f5-6975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-6975">RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6976">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-6976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6977">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-6977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-6978">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-6978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-6979">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-6979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6980">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-6980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-6981">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-6981">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-6982">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-6983">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-6984">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-6985">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-6986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-6986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-6987">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-6988">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-6988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6989">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-6989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-6990">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-6990">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-6992">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-6992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6993">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-6993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="755f5-6994">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-6994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="755f5-6995">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="755f5-6996">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-6996">Multisample Load</span></span> | \- |
| <span data-ttu-id="755f5-6997">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-6997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-6998">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-6998">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-6999">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-6999">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-7000">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-7000">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7002">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-7002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-7003">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-7003">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-7004">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-7004">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="755f5-7005">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="755f5-7005">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="755f5-7006">Destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-7006">Target</span></span> | <span data-ttu-id="755f5-7007">Supporto</span><span class="sxs-lookup"><span data-stu-id="755f5-7007">Support</span></span> |
| - | - |
| <span data-ttu-id="755f5-7008">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="755f5-7008">Bits Per Element (BPE)</span></span> | <span data-ttu-id="755f5-7009">16</span><span class="sxs-lookup"><span data-stu-id="755f5-7009">16</span></span> |
| <span data-ttu-id="755f5-7010">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="755f5-7010">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7012">Buffer</span><span class="sxs-lookup"><span data-stu-id="755f5-7012">Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-7014">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="755f5-7014">Input Assembler Vertex Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-7016">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="755f5-7016">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="755f5-7017">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="755f5-7017">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="755f5-7018">Texture1D</span><span class="sxs-lookup"><span data-stu-id="755f5-7018">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7020">Texture2D</span><span class="sxs-lookup"><span data-stu-id="755f5-7020">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7022">Texture3D</span><span class="sxs-lookup"><span data-stu-id="755f5-7022">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7024">TextureCube</span><span class="sxs-lookup"><span data-stu-id="755f5-7024">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7026">LD shader</span><span class="sxs-lookup"><span data-stu-id="755f5-7026">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7028">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="755f5-7028">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7030">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="755f5-7030">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="755f5-7031">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="755f5-7031">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="755f5-7032">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="755f5-7032">Shader gather4</span></span> | \- |
| <span data-ttu-id="755f5-7033">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="755f5-7033">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="755f5-7034">Mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-7034">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7036">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="755f5-7036">Mipmap Auto-Generation</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-7038">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="755f5-7038">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-7040">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="755f5-7040">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-7042">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="755f5-7042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="755f5-7043">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="755f5-7043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="755f5-7044">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="755f5-7044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-7045">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="755f5-7045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="755f5-7046">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-7046">Typed UAV</span></span> | \- |
| <span data-ttu-id="755f5-7047">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-7047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="755f5-7048">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-7048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="755f5-7049">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-7049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="755f5-7050">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-7050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="755f5-7051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="755f5-7051">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="755f5-7052">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-7052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="755f5-7053">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="755f5-7053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-7054">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="755f5-7054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="755f5-7055">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="755f5-7055">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7057">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="755f5-7057">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-7059">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="755f5-7059">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-7061">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="755f5-7061">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-7063">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-7063">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="755f5-7065">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="755f5-7065">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="755f5-7067">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="755f5-7067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="755f5-7068">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="755f5-7068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="755f5-7069">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="755f5-7069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="755f5-7070">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-7070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="755f5-7071">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="755f5-7071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="755f5-7072">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="755f5-7072">Shared Resource</span></span> | \- |
| <span data-ttu-id="755f5-7073">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="755f5-7073">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="755f5-7074">Note sul formato</span><span class="sxs-lookup"><span data-stu-id="755f5-7074">Format notes</span></span>

<span data-ttu-id="755f5-7075">Lo scopo del formato può variare da un livello di funzionalità hardware a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="755f5-7075">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="755f5-7076"><sup>L</sup> : formato non tipizzato</span><span class="sxs-lookup"><span data-stu-id="755f5-7076"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="755f5-7077"><sup>PC</sup> : layout parzialmente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="755f5-7077"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="755f5-7078"><sup>FCS</sup> : layout completamente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="755f5-7078"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="755f5-7079"><sup>FNS</sup> : layout completamente tipizzato, non ristabile e semplice</span><span class="sxs-lookup"><span data-stu-id="755f5-7079"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="755f5-7080"><sup>PCC</sup> : layout parzialmente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="755f5-7080"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="755f5-7081"><sup>FCC</sup> : layout completamente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="755f5-7081"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="755f5-7082"><sup>FNC</sup> : layout completamente tipizzato, non ristabile e complesso</span><span class="sxs-lookup"><span data-stu-id="755f5-7082"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="755f5-7083"><sup>V</sup> : formato video</span><span class="sxs-lookup"><span data-stu-id="755f5-7083"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="755f5-7084">I buffer indietro e le analisi con il [**formato \_ DXGI \_ R16G16B16A16 \_ float**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) contengono dati gamma con valori lineari.</span><span class="sxs-lookup"><span data-stu-id="755f5-7084">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="755f5-7085">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="755f5-7085">Related topics</span></span>

[<span data-ttu-id="755f5-7086">Livelli di funzionalità hardware D3D12</span><span class="sxs-lookup"><span data-stu-id="755f5-7086">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="755f5-7087">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="755f5-7087">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="755f5-7088">Guida per programmatori per DXGI</span><span class="sxs-lookup"><span data-stu-id="755f5-7088">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
