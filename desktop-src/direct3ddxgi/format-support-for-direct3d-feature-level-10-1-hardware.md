---
description: Questa sezione specifica i formati ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware del livello di funzionalità Direct3D 10,1.
ms.assetid: 2C7E16D7-EEF0-4EA7-A819-5274C9105F68
title: Supporto del formato per l'hardware a livello di funzionalità 10.1 di Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edb5c81ef0a99bc14031a9a7a505736e91e13d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481293"
---
# <a name="format-support-for-direct3d-feature-level-101-hardware"></a><span data-ttu-id="b648e-103">Supporto del formato per l'hardware a livello di funzionalità 10.1 di Direct3D</span><span class="sxs-lookup"><span data-stu-id="b648e-103">Format support for Direct3D Feature Level 10.1 hardware</span></span>

<span data-ttu-id="b648e-104">Questa sezione specifica i formati ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware a livello di funzionalità Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="b648e-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.1 hardware.</span></span>

<span data-ttu-id="b648e-105">La tabella riepiloga il supporto della funzionalità, usando la chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="b648e-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="b648e-106">Simbolo</span><span class="sxs-lookup"><span data-stu-id="b648e-106">Symbol</span></span>                            | <span data-ttu-id="b648e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b648e-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="b648e-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="b648e-108">_ *-*\*</span></span>                             | <span data-ttu-id="b648e-109">Non consentito o non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b648e-109">Disallowed or not available.</span></span>                                                  |
| ![necessario](images/letter-r.jpg)  | <span data-ttu-id="b648e-111">Il supporto hardware è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b648e-111">Hardware support is required.</span></span>                                                 |
| ![facoltative](images/letter-o.jpg)  | <span data-ttu-id="b648e-113">Supporto hardware facoltativo. il formato potrebbe essere accelerato o meno.</span><span class="sxs-lookup"><span data-stu-id="b648e-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dipendenti](images/letter-d.jpg) | <span data-ttu-id="b648e-115">Obbligatorio se è supportata la funzionalità facoltativa correlata.</span><span class="sxs-lookup"><span data-stu-id="b648e-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="b648e-116">Questo argomento contiene una sezione per formato.</span><span class="sxs-lookup"><span data-stu-id="b648e-116">This topic contains a section per format.</span></span> <span data-ttu-id="b648e-117">Una *destinazione* del formato (le tabelle contengono una riga per destinazione) può essere un tipo di risorsa, una funzione intrinseca HLSL o una particolare funzionalità che dipende da un particolare formato.</span><span class="sxs-lookup"><span data-stu-id="b648e-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="b648e-118">Per verificare a livello di codice il supporto del formato in D3D11 e D3D12, vedere [controllo della funzionalità hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="b648e-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="b648e-119">Il numero di formati è prevalentemente, ma non tutti, in ordine numerico crescente &mdash; alcuni sono fuori dall'ordine numerico ed elencati insieme ad altri formati pertinenti.</span><span class="sxs-lookup"><span data-stu-id="b648e-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="b648e-120">Si noti anche che il *tipo* in un nome di formato può indicare *parzialmente* tipizzato e non esclusivamente senza tipo (fare riferimento alla sezione [Note sul formato](#format-notes) alla fine dell'argomento).</span><span class="sxs-lookup"><span data-stu-id="b648e-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="b648e-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="b648e-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="b648e-122">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-122">Target</span></span> | <span data-ttu-id="b648e-123">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-123">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-124">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-125">0</span><span class="sxs-lookup"><span data-stu-id="b648e-125">0</span></span> |
| <span data-ttu-id="b648e-126">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-126">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-128">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-130">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-131">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-132">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-133">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-134">Texture2D</span></span> | \- |
| <span data-ttu-id="b648e-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-135">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-136">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-137">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-137">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-138">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-139">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-140">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-141">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-142">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-143">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-144">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-147">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-148">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-149">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-150">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-151">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-152">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-153">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-154">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-155">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-157">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-158">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-159">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-160">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-160">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-162">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-163">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-164">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-165">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-166">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-167">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-168">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-169">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-170">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-171">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-172">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-173">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="b648e-174">DXGI_FORMAT_R32G32B32A32 \_ <sup>PC</sup> non con tipi (1)</span><span class="sxs-lookup"><span data-stu-id="b648e-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="b648e-175">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-175">Target</span></span> | <span data-ttu-id="b648e-176">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-176">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-177">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-178">128</span><span class="sxs-lookup"><span data-stu-id="b648e-178">128</span></span> |
| <span data-ttu-id="b648e-179">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-179">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-181">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-182">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-183">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-184">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-185">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-187">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-189">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-191">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-193">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-193">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-194">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-195">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-196">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-197">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-198">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-199">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-199">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-201">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-203">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-204">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-205">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-206">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-207">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-208">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-209">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-210">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-211">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-212">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-214">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-215">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-216">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-217">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-217">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-219">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-220">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-221">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-222">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-223">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-224">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-225">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-225">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-227">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-228">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-229">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-230">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-230">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-232">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="b648e-233">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FCS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="b648e-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="b648e-234">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-234">Target</span></span> | <span data-ttu-id="b648e-235">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-235">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-236">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-237">128</span><span class="sxs-lookup"><span data-stu-id="b648e-237">128</span></span> |
| <span data-ttu-id="b648e-238">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-238">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-240">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-242">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-242">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-244">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-245">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-245">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-247">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-249">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-251">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-253">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-255">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-255">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-257">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-257">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-259">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-260">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-261">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-262">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-263">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-265">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-265">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-267">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-269">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-269">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-271">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-272">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-273">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-274">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-275">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-276">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-277">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-278">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-279">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-281">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-282">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-283">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-284">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-284">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-286">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-286">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-288">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-288">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-290">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-290">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-292">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-292">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-294">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-294">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-296">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-297">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-297">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-299">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-300">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-301">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-302">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-302">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-304">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="b648e-305">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FCS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="b648e-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="b648e-306">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-306">Target</span></span> | <span data-ttu-id="b648e-307">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-307">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-308">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-309">128</span><span class="sxs-lookup"><span data-stu-id="b648e-309">128</span></span> |
| <span data-ttu-id="b648e-310">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-310">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-312">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-314">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-314">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-316">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-317">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-317">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-319">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-321">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-323">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-325">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-327">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-327">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-329">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-330">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-331">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-332">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-333">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-334">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-334">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-336">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-337">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-339">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-340">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-340">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-342">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-343">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-344">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-345">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-346">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-347">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-348">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-349">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-351">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-352">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-353">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-354">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-354">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-356">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-356">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-358">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-358">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-360">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-360">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-362">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-363">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-363">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-365">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-366">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-366">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-368">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-369">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-370">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-371">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-371">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-373">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="b648e-374">DXGI_FORMAT_R32G32B32A32 \_ Sint<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="b648e-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="b648e-375">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-375">Target</span></span> | <span data-ttu-id="b648e-376">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-376">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-377">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-378">128</span><span class="sxs-lookup"><span data-stu-id="b648e-378">128</span></span> |
| <span data-ttu-id="b648e-379">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-379">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-381">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-383">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-383">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-385">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-386">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-386">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-388">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-390">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-392">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-394">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-396">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-396">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-398">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-399">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-400">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-401">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-402">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-403">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-405">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-406">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-408">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-409">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-410">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-411">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-412">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-413">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-414">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-415">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-416">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-417">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-419">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-420">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-421">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-422">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-422">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-424">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-424">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-426">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-426">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-428">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-428">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-430">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-431">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-431">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-433">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-434">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-434">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-436">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-437">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-438">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-439">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-439">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-441">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="b648e-442">DXGI_FORMAT_R32G32B32 i \_ <sup>PC</sup> con tipi (5)</span><span class="sxs-lookup"><span data-stu-id="b648e-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="b648e-443">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-443">Target</span></span> | <span data-ttu-id="b648e-444">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-444">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-445">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-446">96</span><span class="sxs-lookup"><span data-stu-id="b648e-446">96</span></span> |
| <span data-ttu-id="b648e-447">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-447">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-449">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-450">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-451">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-452">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-453">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-455">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-457">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-459">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-461">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-461">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-462">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-463">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-464">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-465">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-466">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-467">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-467">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-469">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-471">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-472">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-473">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-474">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-475">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-476">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-477">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-478">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-479">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-480">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-482">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-483">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-484">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-485">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-485">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-487">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-488">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-489">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-490">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-491">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-492">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-493">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-493">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-495">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-496">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-497">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-498">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-499">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="b648e-500">DXGI_FORMAT_R32G32B32 \_ float<sup>FCS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="b648e-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="b648e-501">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-501">Target</span></span> | <span data-ttu-id="b648e-502">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-502">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-503">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-504">96</span><span class="sxs-lookup"><span data-stu-id="b648e-504">96</span></span> |
| <span data-ttu-id="b648e-505">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-505">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-507">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-509">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-509">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-511">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-512">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-512">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-514">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-516">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-518">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-520">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-522">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-522">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-524">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-524">Shader sample (any filter)</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-526">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-527">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-528">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-529">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-530">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-530">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-532">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-532">Mipmap Auto-Generation</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-534">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-536">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-536">Blendable RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="b648e-538">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-539">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-540">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-541">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-542">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-543">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-544">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-545">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-546">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-548">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-549">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-550">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-551">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-551">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-553">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-553">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="b648e-555">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-555">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="b648e-557">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-557">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-559">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-559">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-561">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-561">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-563">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-564">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-564">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-566">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-567">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-568">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-569">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-570">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="b648e-571">DXGI_FORMAT_R32G32B32 \_ uint<sup>FCS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="b648e-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="b648e-572">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-572">Target</span></span> | <span data-ttu-id="b648e-573">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-573">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-574">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-575">96</span><span class="sxs-lookup"><span data-stu-id="b648e-575">96</span></span> |
| <span data-ttu-id="b648e-576">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-576">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-578">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-580">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-580">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-582">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-583">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-583">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-585">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-587">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-589">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-591">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-593">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-593">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-595">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-596">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-597">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-598">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-599">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-600">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-602">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-603">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-605">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-606">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-606">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-608">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-609">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-610">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-611">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-612">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-613">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-614">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-615">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-617">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-618">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-619">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-620">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-620">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-622">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-622">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="b648e-624">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-624">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="b648e-626">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-626">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-628">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-629">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-629">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-631">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-632">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-632">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-634">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-635">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-636">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-637">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-638">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="b648e-639">DXGI_FORMAT_R32G32B32 \_ Sint<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="b648e-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="b648e-640">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-640">Target</span></span> | <span data-ttu-id="b648e-641">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-641">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-642">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-643">96</span><span class="sxs-lookup"><span data-stu-id="b648e-643">96</span></span> |
| <span data-ttu-id="b648e-644">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-644">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-646">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-648">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-648">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-650">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-651">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-651">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-653">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-655">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-657">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-659">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-661">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-661">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-663">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-664">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-665">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-666">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-667">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-668">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-670">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-671">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-673">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-674">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-675">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-676">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-677">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-678">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-679">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-680">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-681">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-682">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-684">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-685">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-686">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-687">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-687">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-689">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-689">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="b648e-691">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-691">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="b648e-693">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-693">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-695">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-696">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-696">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-698">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-699">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-699">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-701">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-702">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-703">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-704">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-705">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="b648e-706">DXGI_FORMAT_R16G16B16A16 \_ <sup>PC</sup> non con tipi (9)</span><span class="sxs-lookup"><span data-stu-id="b648e-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="b648e-707">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-707">Target</span></span> | <span data-ttu-id="b648e-708">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-708">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-709">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-710">64</span><span class="sxs-lookup"><span data-stu-id="b648e-710">64</span></span> |
| <span data-ttu-id="b648e-711">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-711">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-713">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-714">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-715">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-716">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-717">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-719">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-721">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-723">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-725">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-725">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-726">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-727">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-728">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-729">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-730">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-731">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-731">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-733">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-735">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-736">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-737">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-738">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-739">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-740">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-741">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-742">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-743">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-744">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-746">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-747">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-748">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-749">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-749">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-751">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-752">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-753">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-754">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-755">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-756">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-757">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-757">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-759">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-760">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-761">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-762">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-762">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-764">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="b648e-765">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FCS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="b648e-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="b648e-766">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-766">Target</span></span> | <span data-ttu-id="b648e-767">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-767">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-768">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-769">64</span><span class="sxs-lookup"><span data-stu-id="b648e-769">64</span></span> |
| <span data-ttu-id="b648e-770">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-770">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-772">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-774">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-774">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-776">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-777">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-778">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-780">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-782">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-784">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-786">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-786">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-788">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-788">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-790">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-791">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-792">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-793">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-794">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-794">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-796">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-796">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-798">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-800">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-800">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-802">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-803">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-804">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-805">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-806">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-807">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-808">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-809">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-810">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-812">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-813">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-814">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-815">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-815">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-817">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-817">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-819">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-819">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-821">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-821">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-823">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-823">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-825">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-825">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-827">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-827">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-829">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-829">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-831">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-832">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-832">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-834">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-834">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-836">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-836">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-838">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="b648e-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="b648e-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="b648e-840">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-840">Target</span></span> | <span data-ttu-id="b648e-841">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-841">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-842">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-843">64</span><span class="sxs-lookup"><span data-stu-id="b648e-843">64</span></span> |
| <span data-ttu-id="b648e-844">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-844">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-846">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-848">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-848">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-850">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-851">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-852">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-854">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-856">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-858">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-860">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-860">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-862">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-862">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-864">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-865">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-866">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-867">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-868">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-870">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-870">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-872">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-874">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-874">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-876">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-877">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-878">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-879">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-880">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-881">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-882">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-883">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-884">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-886">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-887">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-888">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-889">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-889">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-891">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-891">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-893">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-893">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-895">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-895">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-897">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-897">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-899">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-899">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-901">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-902">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-902">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-904">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-905">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-906">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-907">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-907">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-909">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="b648e-910">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FCS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="b648e-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="b648e-911">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-911">Target</span></span> | <span data-ttu-id="b648e-912">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-912">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-913">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-914">64</span><span class="sxs-lookup"><span data-stu-id="b648e-914">64</span></span> |
| <span data-ttu-id="b648e-915">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-915">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-917">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-919">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-919">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-921">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-922">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-923">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-925">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-927">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-929">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-931">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-931">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-933">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-934">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-935">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-936">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-937">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-938">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-940">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-941">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-943">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-944">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-944">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-946">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-947">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-948">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-949">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-950">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-951">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-952">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-953">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-955">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-956">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-957">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-958">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-958">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-960">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-960">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-962">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-962">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-964">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-964">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-966">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-967">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-967">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-969">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-970">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-970">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-972">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-973">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-974">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-975">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-975">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-977">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="b648e-978">DXGI_FORMAT_R16G16B16A16 \_ russare<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="b648e-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="b648e-979">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-979">Target</span></span> | <span data-ttu-id="b648e-980">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-980">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-981">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-982">64</span><span class="sxs-lookup"><span data-stu-id="b648e-982">64</span></span> |
| <span data-ttu-id="b648e-983">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-983">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-985">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-987">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-987">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-989">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-990">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-991">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-993">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-995">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-997">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-999">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-999">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1001">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1001">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1003">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1004">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1005">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1006">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1007">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1007">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1009">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1009">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1011">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1013">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1013">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1015">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1015">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1016">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1016">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1017">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1017">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1018">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1018">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1019">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1019">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1020">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1020">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1021">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1021">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1022">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1023">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1024">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1024">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1025">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1026">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1026">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1027">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1027">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1028">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1028">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1030">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1030">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1032">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1032">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1034">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1034">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1036">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1036">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1038">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1038">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1040">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1041">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1041">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1043">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1043">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1044">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1044">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1045">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1045">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1046">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1046">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1048">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1048">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="b648e-1049">DXGI_FORMAT_R16G16B16A16 \_ Sint<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="b648e-1049">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="b648e-1050">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1050">Target</span></span> | <span data-ttu-id="b648e-1051">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1051">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1052">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1053">64</span><span class="sxs-lookup"><span data-stu-id="b648e-1053">64</span></span> |
| <span data-ttu-id="b648e-1054">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1054">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1056">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1056">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1058">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1058">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1060">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1060">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1061">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1061">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1062">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1062">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1064">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1064">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1066">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1066">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1068">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1068">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1070">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1070">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1072">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1072">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1073">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1073">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1074">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1074">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1075">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1075">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1076">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1076">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1077">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1077">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1079">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1079">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1080">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1080">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1082">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1082">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1083">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1083">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1084">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1084">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1085">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1085">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1086">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1086">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1087">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1087">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1088">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1088">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1089">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1089">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1090">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1090">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1091">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1091">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1092">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1092">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1093">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1093">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1094">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1094">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1095">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1095">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1096">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1096">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1098">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1098">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1100">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1100">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1102">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1102">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1104">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1104">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1105">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1105">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1107">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1108">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1108">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1110">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1111">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1112">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1113">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1113">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1115">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="b648e-1116">DXGI_FORMAT_R32G32 \_ <sup>PC</sup> non con tipi (15)</span><span class="sxs-lookup"><span data-stu-id="b648e-1116">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="b648e-1117">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1117">Target</span></span> | <span data-ttu-id="b648e-1118">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1118">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1119">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1120">64</span><span class="sxs-lookup"><span data-stu-id="b648e-1120">64</span></span> |
| <span data-ttu-id="b648e-1121">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1121">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1123">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1123">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1124">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1125">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1126">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1127">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1129">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1131">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1131">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1133">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1133">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1135">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1135">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-1136">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1137">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1138">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1139">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1139">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1140">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1141">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1143">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1143">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1144">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1145">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1145">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1146">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1146">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1147">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1147">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1148">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1148">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1149">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1149">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1150">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1150">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1151">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1151">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1152">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1152">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1153">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1153">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1154">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1154">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1155">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1155">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1156">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1156">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1157">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1157">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1158">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1158">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1159">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1159">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1161">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1161">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1162">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1162">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1163">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1163">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-1164">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1164">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1165">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1165">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-1166">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1166">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1167">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1167">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1169">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1170">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1171">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1172">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1172">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-1173">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="b648e-1174">DXGI_FORMAT_R32G32 \_ float<sup>FCS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="b648e-1174">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="b648e-1175">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1175">Target</span></span> | <span data-ttu-id="b648e-1176">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1176">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1177">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1178">64</span><span class="sxs-lookup"><span data-stu-id="b648e-1178">64</span></span> |
| <span data-ttu-id="b648e-1179">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1179">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1181">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1181">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1183">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1183">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1185">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1186">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1186">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1188">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1190">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1192">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1194">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1196">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1196">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1198">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1198">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1200">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1201">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1202">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1202">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1203">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1204">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1204">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1206">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1206">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1208">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1208">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1210">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1210">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1212">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1212">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1213">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1213">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1214">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1214">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1215">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1215">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1216">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1216">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1217">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1217">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1218">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1218">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1219">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1219">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1220">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1220">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1221">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1221">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1222">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1222">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1223">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1223">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1224">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1224">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1225">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1225">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1227">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1227">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1229">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1229">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1231">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1231">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1233">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1233">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1235">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1235">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1237">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1237">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1238">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1238">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1240">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1240">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1241">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1241">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1242">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1242">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1243">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1243">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-1244">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1244">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="b648e-1245">DXGI_FORMAT_R32G32 \_ uint<sup>FCS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="b648e-1245">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="b648e-1246">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1246">Target</span></span> | <span data-ttu-id="b648e-1247">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1247">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1248">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1248">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1249">64</span><span class="sxs-lookup"><span data-stu-id="b648e-1249">64</span></span> |
| <span data-ttu-id="b648e-1250">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1250">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1252">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1252">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1254">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1254">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1256">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1256">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1257">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1257">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1259">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1259">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1261">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1261">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1263">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1263">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1265">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1265">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1267">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1267">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1269">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1269">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1270">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1270">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1271">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1271">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1272">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1272">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1273">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1273">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1274">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1274">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1276">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1276">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1277">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1277">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1279">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1279">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1280">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1280">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1282">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1283">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1284">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1285">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1285">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1286">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1287">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1288">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1289">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1291">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1292">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1293">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1294">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1294">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1296">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1296">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1298">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1298">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1300">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1300">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1302">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1302">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1303">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1303">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1305">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1306">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1306">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1308">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1309">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1310">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1311">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1311">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-1312">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1312">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="b648e-1313">DXGI_FORMAT_R32G32 \_ Sint<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="b648e-1313">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="b648e-1314">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1314">Target</span></span> | <span data-ttu-id="b648e-1315">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1315">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1316">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1316">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1317">64</span><span class="sxs-lookup"><span data-stu-id="b648e-1317">64</span></span> |
| <span data-ttu-id="b648e-1318">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1318">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1320">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1320">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1322">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1322">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1324">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1324">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1325">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1325">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1327">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1329">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1329">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1331">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1331">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1333">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1333">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1335">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1335">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1337">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1337">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1338">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1338">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1339">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1339">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1340">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1340">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1341">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1341">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1342">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1342">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1344">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1345">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1347">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1348">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1349">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1350">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1351">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1352">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1352">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1353">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1353">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1354">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1354">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1355">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1356">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1357">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1357">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1358">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1359">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1359">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1360">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1360">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1361">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1361">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1363">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1363">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1365">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1365">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1367">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1367">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1369">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1370">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1370">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1372">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1373">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1373">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1375">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1376">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1377">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1378">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-1379">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1379">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="b648e-1380">DXGI_FORMAT_R32G8X24 i \_ <sup>PC</sup> non con tipi (19)</span><span class="sxs-lookup"><span data-stu-id="b648e-1380">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="b648e-1381">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1381">Target</span></span> | <span data-ttu-id="b648e-1382">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1382">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1383">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1383">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1384">64</span><span class="sxs-lookup"><span data-stu-id="b648e-1384">64</span></span> |
| <span data-ttu-id="b648e-1385">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1385">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1387">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1387">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1388">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1389">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1390">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1391">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1393">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1395">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-1396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1396">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1398">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1398">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-1399">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1399">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1400">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1400">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1401">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1401">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1402">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1402">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1403">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1403">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1404">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1404">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1406">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1407">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1408">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1409">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1410">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1411">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1412">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1413">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1413">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1414">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1415">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1416">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1417">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1419">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1420">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1421">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1422">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1422">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1424">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1424">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1425">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1425">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1426">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1426">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-1427">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1427">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1428">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1428">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-1429">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1429">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1430">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1430">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1432">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1433">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1434">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1435">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1435">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-1436">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="b648e-1437">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FCS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="b648e-1437">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="b648e-1438">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1438">Target</span></span> | <span data-ttu-id="b648e-1439">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1439">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1440">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1441">64</span><span class="sxs-lookup"><span data-stu-id="b648e-1441">64</span></span> |
| <span data-ttu-id="b648e-1442">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1442">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1444">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1444">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1445">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1445">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1446">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1446">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1447">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1447">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1448">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1448">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1450">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1450">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1453">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1455">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1455">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-1456">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1456">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1457">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1457">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1458">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1458">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1459">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1459">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1460">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1460">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1461">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1461">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1463">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1465">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1466">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1467">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1467">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1469">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1470">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1471">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1471">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1472">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1473">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1474">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1475">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1476">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1477">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1478">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1479">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1480">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1480">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1482">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1482">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1484">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1484">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1486">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1486">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1488">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1488">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1489">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1489">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-1490">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1490">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1491">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1491">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1493">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1494">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1495">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1496">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1496">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-1497">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="b648e-1498">DXGI_FORMAT_R32 \_ float \_ con \_ tipo float<sup></sup> X8X24 (21)</span><span class="sxs-lookup"><span data-stu-id="b648e-1498">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="b648e-1499">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1499">Target</span></span> | <span data-ttu-id="b648e-1500">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1500">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1501">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1502">64</span><span class="sxs-lookup"><span data-stu-id="b648e-1502">64</span></span> |
| <span data-ttu-id="b648e-1503">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1503">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1505">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1505">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1506">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1507">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1508">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1509">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1511">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1513">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1513">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-1514">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1514">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1516">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1516">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1518">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1518">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1520">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1520">Shader sample\_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1522">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1522">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1523">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1523">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1525">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1525">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1526">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1526">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1528">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1528">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1529">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1529">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1530">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1530">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1531">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1531">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1532">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1532">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1533">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1533">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1534">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1534">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1535">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1535">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1536">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1536">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1537">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1537">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1538">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1538">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1539">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1539">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1540">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1540">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1541">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1541">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1542">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1542">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1543">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1543">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1544">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1544">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1546">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1546">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1547">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1547">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1548">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1548">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-1549">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1549">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1550">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1550">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1552">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1552">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1553">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1553">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1555">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1555">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1556">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1556">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1557">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1557">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1558">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1558">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-1559">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1559">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="b648e-1560">G8X24 con tipo di DXGI_FORMAT_X32 \_ \_ \_ uint<sup>FCS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="b648e-1560">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="b648e-1561">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1561">Target</span></span> | <span data-ttu-id="b648e-1562">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1562">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1563">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1563">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1564">64</span><span class="sxs-lookup"><span data-stu-id="b648e-1564">64</span></span> |
| <span data-ttu-id="b648e-1565">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1565">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1567">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1567">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1568">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1568">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1569">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1569">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1570">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1570">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1571">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1571">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1573">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1573">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1575">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1575">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-1576">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1576">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1578">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1578">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1580">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1580">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1581">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1581">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1582">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1582">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1583">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1583">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1584">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1584">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1585">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1585">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1587">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1587">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1588">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1588">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1589">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1590">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1590">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1591">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1591">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1592">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1592">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1593">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1593">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1594">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1594">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1595">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1595">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1596">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1596">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1597">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1598">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1599">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1599">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1600">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1601">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1601">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1602">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1602">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1603">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1603">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1605">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1605">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1606">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1606">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1607">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1607">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-1608">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1608">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1609">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1609">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1611">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1611">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1612">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1612">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1614">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1614">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1615">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1615">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1616">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1616">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1617">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1617">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-1618">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1618">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="b648e-1619">DXGI_FORMAT_R10G10B10A2 \_ <sup>PC</sup> non con tipi (23)</span><span class="sxs-lookup"><span data-stu-id="b648e-1619">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="b648e-1620">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1620">Target</span></span> | <span data-ttu-id="b648e-1621">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1621">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1622">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1622">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1623">32</span><span class="sxs-lookup"><span data-stu-id="b648e-1623">32</span></span> |
| <span data-ttu-id="b648e-1624">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1624">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1626">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1626">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1627">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1627">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1628">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1628">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1629">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1629">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1630">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1630">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1632">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1632">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1634">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1634">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1636">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1636">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1638">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1638">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-1639">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1639">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1640">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1640">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1641">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1641">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1642">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1642">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1643">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1643">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1644">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1644">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1646">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1646">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1647">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1647">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1648">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1648">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1649">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1649">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1650">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1650">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1651">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1651">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1652">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1652">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1653">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1653">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1654">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1654">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1655">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1655">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1656">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1656">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1657">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1657">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1658">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1658">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1659">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1659">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1660">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1660">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1661">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1661">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1662">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1662">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1664">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1664">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1665">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1665">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1666">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1666">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-1667">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1667">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1668">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1668">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-1669">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1669">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1670">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1670">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1672">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1672">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1673">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1673">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1674">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1674">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1675">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1675">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1677">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1677">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="b648e-1678">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="b648e-1678">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="b648e-1679">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1679">Target</span></span> | <span data-ttu-id="b648e-1680">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1680">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1681">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1681">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1682">32</span><span class="sxs-lookup"><span data-stu-id="b648e-1682">32</span></span> |
| <span data-ttu-id="b648e-1683">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1683">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1685">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1685">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1687">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1687">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1689">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1689">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1690">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1690">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1691">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1691">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1693">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1693">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1695">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1697">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1697">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1699">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1699">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1701">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1701">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1703">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1703">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1704">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1704">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1705">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1705">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1706">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1706">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1707">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1707">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1709">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1709">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1711">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1711">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1713">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1713">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1715">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1715">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1716">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1716">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1717">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1717">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1718">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1718">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1719">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1719">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1720">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1720">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1721">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1721">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1722">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1722">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1723">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1723">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1724">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1724">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1725">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1725">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1726">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1726">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1727">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1727">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1728">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1728">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1730">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1730">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1732">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1732">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1734">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1734">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1736">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1736">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1738">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1738">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1740">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1740">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1742">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1742">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1744">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1744">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1745">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1745">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1747">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1747">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1749">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1749">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1751">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="b648e-1752">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FCS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="b648e-1752">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="b648e-1753">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1753">Target</span></span> | <span data-ttu-id="b648e-1754">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1754">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1755">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1756">32</span><span class="sxs-lookup"><span data-stu-id="b648e-1756">32</span></span> |
| <span data-ttu-id="b648e-1757">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1757">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1759">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1759">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1761">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1761">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1763">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1763">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1764">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1764">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1765">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1765">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1767">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1769">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1771">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1771">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1773">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1773">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1775">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1776">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1777">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1778">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1778">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1779">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1780">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1782">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1783">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1785">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1786">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1786">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1788">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1789">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1790">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1791">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1791">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1792">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1792">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1793">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1793">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1794">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1794">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1795">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1795">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1796">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1796">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1797">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1797">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1798">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1798">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1799">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1799">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1800">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1800">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1802">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1802">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1804">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1804">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1806">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1806">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1808">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1808">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1809">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1809">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1811">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1812">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1812">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1814">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1815">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1816">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1817">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1817">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1819">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="b648e-1820">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="b648e-1820">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="b648e-1821">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1821">Target</span></span> | <span data-ttu-id="b648e-1822">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1822">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1823">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1824">32</span><span class="sxs-lookup"><span data-stu-id="b648e-1824">32</span></span> |
| <span data-ttu-id="b648e-1825">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1825">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1827">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1827">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1828">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1829">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1830">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1831">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-1832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1832">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1834">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-1835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1835">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-1836">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1836">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-1837">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1838">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1839">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1840">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1840">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1841">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1842">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1842">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-1843">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1843">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1844">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1844">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1845">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1845">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1846">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1846">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1847">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1847">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1848">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1848">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1849">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1849">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1850">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1850">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1851">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1851">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1852">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1852">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1853">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1853">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1854">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1854">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1855">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1855">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1856">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1856">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1857">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1857">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1858">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1858">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1859">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1859">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1861">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1861">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1862">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1862">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1863">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1863">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-1864">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1864">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1865">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1865">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-1866">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1866">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1868">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1868">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1870">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1870">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1871">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1871">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1873">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1873">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1875">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1875">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1877">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1877">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="b648e-1878">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="b648e-1878">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="b648e-1879">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1879">Target</span></span> | <span data-ttu-id="b648e-1880">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1880">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1881">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1881">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1882">32</span><span class="sxs-lookup"><span data-stu-id="b648e-1882">32</span></span> |
| <span data-ttu-id="b648e-1883">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1883">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1885">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1885">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1887">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1887">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1889">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1890">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1891">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1893">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1893">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1895">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1895">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1897">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1897">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1899">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1899">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1901">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1901">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1903">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1904">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1905">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1905">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1906">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1907">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1907">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1909">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1909">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1911">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1911">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1913">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1913">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1915">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1915">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1916">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1916">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1917">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1917">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1918">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1918">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1919">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1919">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1920">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1920">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1921">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1921">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1922">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1922">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1923">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1923">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1924">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1924">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1925">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1925">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1926">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1926">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1927">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1927">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1928">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1928">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1930">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1930">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1932">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1932">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1934">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1934">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-1936">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1936">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1938">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1938">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1940">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1941">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-1942">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-1943">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-1944">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-1944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-1945">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-1945">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-1946">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-1946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="b648e-1947">DXGI_FORMAT_R8G8B8A8 \_ <sup>PC</sup> non con tipi (27)</span><span class="sxs-lookup"><span data-stu-id="b648e-1947">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="b648e-1948">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1948">Target</span></span> | <span data-ttu-id="b648e-1949">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-1949">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-1950">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-1950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-1951">32</span><span class="sxs-lookup"><span data-stu-id="b648e-1951">32</span></span> |
| <span data-ttu-id="b648e-1952">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-1952">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1954">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-1954">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1955">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-1955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1956">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-1956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1957">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-1957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-1958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-1958">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-1960">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-1962">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-1964">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1966">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-1966">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-1967">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-1967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-1968">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-1968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-1969">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-1969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-1970">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-1970">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-1971">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-1971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-1972">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1972">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1974">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-1974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-1975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-1975">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1976">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-1976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1977">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-1977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-1978">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-1978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-1979">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-1979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1980">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-1980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-1981">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-1981">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-1982">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-1983">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-1984">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-1985">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-1986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-1986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-1987">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-1988">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-1988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1989">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-1989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-1990">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-1990">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-1992">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-1992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1993">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-1993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-1994">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-1994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-1995">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-1996">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-1996">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-1997">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-1997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-1998">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-1998">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2000">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2001">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2002">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2003">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2003">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2005">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="b648e-2006">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="b648e-2006">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="b648e-2007">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2007">Target</span></span> | <span data-ttu-id="b648e-2008">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2008">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2009">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2010">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2010">32</span></span> |
| <span data-ttu-id="b648e-2011">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2011">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2013">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2013">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2015">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2015">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2017">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2018">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2019">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2021">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2023">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2025">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2027">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2027">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2029">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2029">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2031">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2032">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2033">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2033">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2034">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2035">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2037">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2037">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2039">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2041">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2041">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2043">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2044">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2045">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2046">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2047">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2047">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2048">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2049">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2050">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2051">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2053">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2054">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2055">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2056">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2056">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2058">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2058">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2060">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2060">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2062">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2062">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2064">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2064">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2066">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2066">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2068">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2068">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2070">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2070">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2072">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2072">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2073">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2073">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2075">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2075">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2077">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2077">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2079">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2079">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="b648e-2080">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="b648e-2080">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="b648e-2081">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2081">Target</span></span> | <span data-ttu-id="b648e-2082">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2082">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2083">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2083">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2084">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2084">32</span></span> |
| <span data-ttu-id="b648e-2085">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2085">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2087">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2087">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2088">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2088">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2089">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2089">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2090">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2090">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2091">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2091">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2093">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2093">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2095">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2095">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2097">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2097">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2099">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2099">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2101">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2101">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2103">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2103">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2104">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2104">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2105">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2105">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2106">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2106">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2107">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2107">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2109">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2109">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2111">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2113">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2113">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2115">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2116">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2117">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2118">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2119">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2119">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2120">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2121">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2122">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2123">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2124">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2125">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2126">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2127">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2128">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2128">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2130">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2130">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2132">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2132">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2134">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2134">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2136">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2136">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2138">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2138">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2140">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2140">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2142">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2142">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2144">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2145">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2145">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2147">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2147">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2149">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2149">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2151">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2151">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="b648e-2152">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FCS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="b648e-2152">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="b648e-2153">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2153">Target</span></span> | <span data-ttu-id="b648e-2154">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2154">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2155">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2155">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2156">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2156">32</span></span> |
| <span data-ttu-id="b648e-2157">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2157">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2159">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2159">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2161">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2161">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2163">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2163">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2164">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2164">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2165">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2165">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2167">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2167">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2169">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2169">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2171">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2171">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2173">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2173">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2175">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2175">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-2176">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2176">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2177">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2177">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2178">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2178">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2179">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2179">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2180">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2180">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2182">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2182">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-2183">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2183">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2185">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2185">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2186">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2186">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2188">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2188">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2189">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2189">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2190">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2190">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2191">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2191">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2192">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2192">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2193">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2193">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2194">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2194">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2195">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2195">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2196">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2196">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2197">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2197">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2198">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2198">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2199">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2199">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2200">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2200">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2202">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2202">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2204">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2204">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2206">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2206">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2208">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2208">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-2209">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2209">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2211">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2211">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2212">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2212">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2214">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2214">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2215">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2215">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2216">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2216">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2217">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2217">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2219">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2219">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="b648e-2220">DXGI_FORMAT_R8G8B8A8 \_ russo<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="b648e-2220">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="b648e-2221">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2221">Target</span></span> | <span data-ttu-id="b648e-2222">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2222">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2223">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2223">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2224">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2224">32</span></span> |
| <span data-ttu-id="b648e-2225">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2225">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2227">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2227">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2229">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2229">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2231">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2232">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2233">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2235">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2237">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2239">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2241">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2241">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2243">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2243">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2245">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2246">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2247">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2248">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2249">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2249">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2251">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2251">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2253">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2255">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2255">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2257">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2257">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2258">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2258">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2259">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2259">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2260">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2260">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2261">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2261">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2262">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2262">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2263">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2263">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2264">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2264">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2265">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2265">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2266">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2266">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2267">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2267">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2268">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2268">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2269">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2269">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2270">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2270">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2272">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2272">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2274">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2274">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2276">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2276">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2278">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2278">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2280">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2280">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2282">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2283">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2283">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2285">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2285">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2286">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2286">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2287">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2287">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2288">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2288">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2290">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="b648e-2291">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="b648e-2291">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="b648e-2292">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2292">Target</span></span> | <span data-ttu-id="b648e-2293">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2293">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2294">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2295">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2295">32</span></span> |
| <span data-ttu-id="b648e-2296">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2296">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2298">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2298">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2300">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2300">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2302">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2303">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2304">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2306">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2306">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2308">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2308">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2310">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2310">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2312">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2312">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2314">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2314">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-2315">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2316">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2317">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2317">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2318">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2319">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2319">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2321">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-2322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2322">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2324">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2324">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2325">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2325">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2326">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2326">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2327">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2327">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2328">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2328">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2329">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2329">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2330">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2330">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2331">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2331">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2332">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2332">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2333">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2333">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2334">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2334">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2335">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2335">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2336">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2336">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2337">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2337">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2338">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2338">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2340">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2340">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2342">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2342">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2344">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2344">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2346">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-2347">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2347">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2349">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2349">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2350">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2350">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2352">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2352">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2353">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2353">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2354">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2354">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2355">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2355">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2357">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2357">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="b648e-2358">DXGI_FORMAT_R16G16 \_ <sup>PC</sup> non con tipi (33)</span><span class="sxs-lookup"><span data-stu-id="b648e-2358">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="b648e-2359">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2359">Target</span></span> | <span data-ttu-id="b648e-2360">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2360">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2361">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2361">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2362">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2362">32</span></span> |
| <span data-ttu-id="b648e-2363">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2363">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2365">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2365">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2366">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2366">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2367">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2367">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2368">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2368">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2369">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2369">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2371">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2371">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2373">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2373">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2375">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2375">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2377">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2377">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-2378">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2378">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-2379">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2379">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2380">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2380">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2381">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2381">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2382">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2382">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2383">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2383">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2385">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2385">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-2386">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2386">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2387">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2387">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2388">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2388">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2389">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2389">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2390">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2390">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2391">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2391">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2392">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2392">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2393">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2393">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2394">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2394">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2395">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2395">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2396">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2396">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2397">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2397">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2398">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2398">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2399">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2399">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2400">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2400">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2401">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2401">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2403">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2403">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2404">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2404">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2405">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2405">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-2406">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2406">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-2407">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2407">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-2408">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2408">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2409">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2409">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2411">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2411">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2412">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2412">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2413">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2413">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2414">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2414">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-2415">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2415">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="b648e-2416">DXGI_FORMAT_R16G16 \_ float<sup>FCS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="b648e-2416">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="b648e-2417">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2417">Target</span></span> | <span data-ttu-id="b648e-2418">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2418">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2419">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2419">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2420">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2420">32</span></span> |
| <span data-ttu-id="b648e-2421">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2421">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2423">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2423">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2425">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2425">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2427">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2427">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2428">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2428">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2429">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2429">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2431">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2431">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2433">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2433">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2435">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2435">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2437">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2437">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2439">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2439">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2441">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2442">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2443">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2444">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2445">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2447">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2447">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2449">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2449">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2451">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2451">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2453">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2454">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2455">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2456">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2457">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2457">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2458">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2459">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2460">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2461">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2462">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2463">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2464">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2465">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2466">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2466">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2468">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2468">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2470">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2470">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2472">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2472">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2474">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2474">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2476">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2476">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2478">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2479">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2479">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2481">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2482">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2483">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2484">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2484">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-2485">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="b648e-2486">DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="b648e-2486">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="b648e-2487">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2487">Target</span></span> | <span data-ttu-id="b648e-2488">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2488">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2489">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2490">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2490">32</span></span> |
| <span data-ttu-id="b648e-2491">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2491">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2493">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2493">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2495">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2495">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2497">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2497">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2498">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2498">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2499">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2499">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2501">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2503">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2503">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2505">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2507">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2507">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2509">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2509">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2511">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2512">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2513">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2514">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2515">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2515">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2517">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2517">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2519">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2521">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2521">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2523">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2523">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2524">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2524">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2525">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2525">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2526">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2526">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2527">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2527">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2528">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2528">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2529">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2529">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2530">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2530">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2531">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2531">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2532">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2532">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2533">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2533">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2534">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2534">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2535">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2535">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2536">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2536">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2538">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2538">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2540">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2540">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2542">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2542">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2544">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2544">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2546">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2546">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2548">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2548">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2549">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2549">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2551">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2551">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2552">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2552">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2553">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2553">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2554">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2554">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-2555">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2555">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="b648e-2556">DXGI_FORMAT_R16G16 \_ uint<sup>FCS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="b648e-2556">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="b648e-2557">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2557">Target</span></span> | <span data-ttu-id="b648e-2558">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2558">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2559">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2559">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2560">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2560">32</span></span> |
| <span data-ttu-id="b648e-2561">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2561">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2563">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2563">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2565">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2565">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2567">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2567">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2568">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2568">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2569">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2569">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2571">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2571">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2573">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2573">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2575">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2575">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2577">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2577">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2579">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2579">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-2580">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2580">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2581">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2581">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2582">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2582">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2583">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2583">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2584">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2584">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2586">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2586">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-2587">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2587">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2589">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2590">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2590">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2592">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2592">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2593">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2593">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2594">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2594">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2595">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2595">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2596">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2596">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2597">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2597">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2598">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2598">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2599">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2599">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2600">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2600">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2601">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2601">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2602">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2602">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2603">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2603">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2604">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2604">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2606">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2606">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2608">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2608">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2610">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2610">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2612">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2612">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-2613">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2613">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2615">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2616">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2616">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2618">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2619">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2620">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2621">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-2622">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2622">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="b648e-2623">DXGI_FORMAT_R16G16 \_ russo<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="b648e-2623">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="b648e-2624">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2624">Target</span></span> | <span data-ttu-id="b648e-2625">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2625">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2626">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2626">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2627">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2627">32</span></span> |
| <span data-ttu-id="b648e-2628">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2628">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2630">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2630">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2632">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2632">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2634">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2634">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2635">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2635">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2636">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2636">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2638">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2640">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2642">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2644">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2644">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2646">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2646">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2648">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2649">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2650">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2650">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2651">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2652">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2652">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2654">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2654">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2656">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2658">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2658">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2660">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2661">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2662">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2663">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2664">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2664">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2665">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2666">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2667">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2668">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2669">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2669">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2670">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2671">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2671">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2672">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2672">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2673">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2673">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2675">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2675">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2677">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2677">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2679">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2679">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2681">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2681">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2683">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2683">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2685">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2685">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2686">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2686">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2688">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2688">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2689">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2689">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2690">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2690">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2691">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2691">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-2692">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2692">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="b648e-2693">DXGI_FORMAT_R16G16 \_ Sint<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="b648e-2693">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="b648e-2694">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2694">Target</span></span> | <span data-ttu-id="b648e-2695">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2695">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2696">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2696">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2697">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2697">32</span></span> |
| <span data-ttu-id="b648e-2698">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2698">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2700">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2700">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2702">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2702">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2704">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2705">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2706">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2708">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2708">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2710">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2710">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2712">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2712">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2714">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2714">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2716">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-2717">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2718">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2719">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2720">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2721">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2721">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2723">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-2724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2724">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2726">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2726">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2727">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2727">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2728">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2728">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2729">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2729">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2730">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2730">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2731">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2731">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2732">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2732">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2733">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2733">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2734">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2734">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2735">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2735">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2736">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2736">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2737">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2737">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2738">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2738">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2739">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2739">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2740">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2740">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2742">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2742">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2744">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2744">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2746">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2746">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2748">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2748">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-2749">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2749">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2751">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2752">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2752">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2754">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2755">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2756">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2757">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2757">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-2758">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="b648e-2759">DXGI_FORMAT_R32 \_ <sup>PC</sup> non con tipi (39)</span><span class="sxs-lookup"><span data-stu-id="b648e-2759">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="b648e-2760">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2760">Target</span></span> | <span data-ttu-id="b648e-2761">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2761">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2762">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2763">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2763">32</span></span> |
| <span data-ttu-id="b648e-2764">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2764">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2766">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2766">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2767">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2768">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2769">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2770">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2772">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2774">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2776">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2778">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2778">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-2779">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2779">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-2780">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2780">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2781">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2781">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2782">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2782">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2783">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2783">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2784">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2784">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2786">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2786">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-2787">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2787">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2788">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2788">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2789">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2789">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2790">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2790">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2791">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2791">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2792">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2792">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2793">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2793">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2794">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2794">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2795">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2795">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2796">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2796">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2797">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2797">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2798">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2798">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2799">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2799">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2800">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2800">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2801">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2801">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2802">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2802">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2804">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2804">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2805">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2805">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2806">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2806">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-2807">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2807">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-2808">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2808">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-2809">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2809">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2810">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2810">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2812">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2812">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2813">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2813">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2814">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2814">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2815">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2815">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2817">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2817">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="b648e-2818">DXGI_FORMAT_D32 \_ float<sup>FCS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="b648e-2818">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="b648e-2819">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2819">Target</span></span> | <span data-ttu-id="b648e-2820">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2820">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2821">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2821">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2822">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2822">32</span></span> |
| <span data-ttu-id="b648e-2823">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2823">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2825">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2825">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2826">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2826">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2827">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2828">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2829">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2831">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2833">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-2834">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2834">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2836">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2836">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-2837">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-2838">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2839">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2840">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2840">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2841">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2842">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2842">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2844">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2844">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-2845">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2845">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2846">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2846">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2847">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2847">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2848">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2848">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2850">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2850">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2851">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2851">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2852">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2852">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2853">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2853">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2854">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2854">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2855">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2855">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2856">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2856">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2857">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2857">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2858">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2858">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2859">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2859">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2860">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2860">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2861">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2861">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2863">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2863">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2865">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2865">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2867">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2867">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2869">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-2870">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2870">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-2871">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2872">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2872">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2874">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2875">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2876">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2877">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2877">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2879">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="b648e-2880">DXGI_FORMAT_R32 \_ float<sup>FCS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="b648e-2880">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="b648e-2881">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2881">Target</span></span> | <span data-ttu-id="b648e-2882">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2882">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2883">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2884">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2884">32</span></span> |
| <span data-ttu-id="b648e-2885">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2885">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2887">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2887">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2889">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2889">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2891">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2891">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-2892">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2892">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2894">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2894">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2896">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2896">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2898">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2898">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2900">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2902">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2902">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2904">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2904">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2906">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2906">Shader sample\_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2908">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2908">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2909">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2909">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2911">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2911">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2912">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2912">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2914">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2914">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2916">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2916">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2918">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2918">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2920">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-2921">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2922">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2923">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2924">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2924">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2925">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2926">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2927">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2928">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-2929">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-2929">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-2930">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-2931">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2931">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2932">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-2932">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-2933">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-2933">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2935">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-2935">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2937">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-2937">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2939">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-2939">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2941">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2941">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2943">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-2943">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2945">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-2945">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-2946">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-2946">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2948">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2948">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-2949">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2949">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-2950">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-2950">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-2951">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-2951">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2953">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-2953">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="b648e-2954">DXGI_FORMAT_R32 \_ uint<sup>FCS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="b648e-2954">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="b648e-2955">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2955">Target</span></span> | <span data-ttu-id="b648e-2956">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-2956">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-2957">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-2957">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-2958">32</span><span class="sxs-lookup"><span data-stu-id="b648e-2958">32</span></span> |
| <span data-ttu-id="b648e-2959">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-2959">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2961">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-2961">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2963">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-2963">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2965">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-2965">Input Assembler Index Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2967">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-2967">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-2969">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2971">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-2971">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2973">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-2973">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-2975">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2977">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-2977">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2979">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-2979">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-2980">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-2980">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-2981">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-2981">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-2982">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-2982">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-2983">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-2983">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-2984">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2984">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2986">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-2987">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-2989">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-2989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-2990">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-2990">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-2992">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-2992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-2993">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-2993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2994">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-2994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-2995">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-2995">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-2996">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-2997">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-2998">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-2999">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-2999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3000">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3001">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3002">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3003">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3004">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3004">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3006">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3006">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3008">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3008">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3010">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3010">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3012">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3012">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3013">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3013">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3015">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3015">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3016">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3016">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3018">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3018">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3019">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3019">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3020">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3020">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3021">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3021">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3023">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3023">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="b648e-3024">DXGI_FORMAT_R32 \_ Sint<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="b648e-3024">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="b648e-3025">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3025">Target</span></span> | <span data-ttu-id="b648e-3026">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3026">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3027">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3027">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3028">32</span><span class="sxs-lookup"><span data-stu-id="b648e-3028">32</span></span> |
| <span data-ttu-id="b648e-3029">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3029">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3031">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3031">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3033">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3033">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3035">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3035">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3036">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3036">Stream Output Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3038">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3038">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3040">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3040">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3042">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3042">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3044">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3044">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3046">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3046">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3048">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3048">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3049">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3049">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3050">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3050">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3051">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3051">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3052">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3052">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3053">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3053">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3055">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3055">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3056">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3056">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3058">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3058">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3059">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3059">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3060">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3060">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3061">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3061">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3062">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3062">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3063">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3063">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3064">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3064">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3065">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3065">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3066">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3066">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3067">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3067">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3068">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3068">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3069">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3069">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3070">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3070">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3071">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3071">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3072">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3072">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3074">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3074">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3076">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3076">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3078">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3078">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3080">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3081">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3081">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3083">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3083">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3084">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3084">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3086">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3087">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3088">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3089">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3089">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3091">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="b648e-3092">DXGI_FORMAT_R24G8 \_ <sup>PC</sup> non con tipi (44)</span><span class="sxs-lookup"><span data-stu-id="b648e-3092">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="b648e-3093">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3093">Target</span></span> | <span data-ttu-id="b648e-3094">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3094">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3095">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3096">32</span><span class="sxs-lookup"><span data-stu-id="b648e-3096">32</span></span> |
| <span data-ttu-id="b648e-3097">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3097">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3099">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3099">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3100">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3101">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3102">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3103">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3105">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3105">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3107">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3107">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-3108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3108">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3110">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3110">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-3111">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3111">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3112">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3112">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3113">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3113">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3114">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3114">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3115">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3115">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3116">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3116">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3118">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3118">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3119">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3119">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3120">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3120">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3121">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3121">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3122">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3122">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3123">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3123">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3124">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3124">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3125">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3125">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3126">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3126">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3127">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3127">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3128">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3128">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3129">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3129">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3130">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3130">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3131">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3131">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3132">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3132">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3133">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3133">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3134">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3134">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3136">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3136">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3137">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3137">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3138">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3138">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-3139">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3139">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3140">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3140">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-3141">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3141">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3142">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3142">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3144">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3145">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3145">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3146">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3146">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3147">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3147">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-3148">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3148">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="b648e-3149">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="b648e-3149">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="b648e-3150">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3150">Target</span></span> | <span data-ttu-id="b648e-3151">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3151">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3152">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3152">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3153">32</span><span class="sxs-lookup"><span data-stu-id="b648e-3153">32</span></span> |
| <span data-ttu-id="b648e-3154">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3154">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3156">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3156">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3157">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3157">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3158">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3158">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3159">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3159">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3160">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3160">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3162">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3162">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3164">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3164">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-3165">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3165">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3167">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3167">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-3168">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3168">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3169">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3169">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3170">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3170">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3171">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3171">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3172">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3173">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3173">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3175">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3175">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3176">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3176">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3177">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3177">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3178">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3178">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3179">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3179">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3181">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3181">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3182">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3182">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3183">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3183">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3184">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3184">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3185">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3185">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3186">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3186">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3187">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3187">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3188">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3188">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3189">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3189">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3190">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3190">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3191">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3191">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3192">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3192">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3194">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3194">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3196">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3196">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3198">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3198">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3200">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3200">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3201">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3201">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-3202">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3202">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3203">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3203">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3205">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3205">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3206">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3206">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3207">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3207">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3208">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3208">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-3209">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3209">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="b648e-3210">DXGI_FORMAT_R24 \_ UNORM \_ X8 con \_ tipo<sup>FCS</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="b648e-3210">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="b648e-3211">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3211">Target</span></span> | <span data-ttu-id="b648e-3212">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3212">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3213">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3213">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3214">32</span><span class="sxs-lookup"><span data-stu-id="b648e-3214">32</span></span> |
| <span data-ttu-id="b648e-3215">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3215">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3217">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3217">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3218">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3218">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3219">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3220">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3220">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3221">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3221">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3223">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3223">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3225">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3225">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-3226">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3226">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3228">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3228">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3230">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3230">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3232">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3232">Shader sample\_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3234">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3234">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3235">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3235">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3237">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3237">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3238">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3238">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3240">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3240">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3241">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3241">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3242">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3243">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3244">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3245">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3246">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3247">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3247">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3248">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3248">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3249">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3249">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3250">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3250">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3251">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3251">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3252">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3252">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3253">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3253">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3254">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3254">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3255">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3255">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3256">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3256">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3258">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3258">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3259">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3259">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3260">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3260">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-3261">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3261">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3262">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3262">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3264">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3264">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3265">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3265">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3267">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3267">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3268">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3268">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3269">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3269">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3270">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3270">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-3271">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="b648e-3272">DXGI_FORMAT_X24 \_ tipo \_ G8 \_ UINT<sup>FCS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="b648e-3272">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="b648e-3273">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3273">Target</span></span> | <span data-ttu-id="b648e-3274">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3274">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3275">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3276">32</span><span class="sxs-lookup"><span data-stu-id="b648e-3276">32</span></span> |
| <span data-ttu-id="b648e-3277">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3277">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3279">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3279">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3280">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3281">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3282">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3283">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3285">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3285">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3287">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3287">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-3288">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3288">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3290">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3290">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3292">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3292">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3293">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3293">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3294">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3294">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3295">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3295">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3296">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3297">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3297">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3299">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3300">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3301">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3302">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3303">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3304">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3305">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3306">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3306">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3307">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3308">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3309">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3310">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3312">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3313">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3314">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3315">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3315">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3317">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3318">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3319">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-3320">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3321">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3321">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3323">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3323">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3324">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3324">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3326">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3327">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3328">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3329">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-3330">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="b648e-3331">DXGI_FORMAT_R8G8 \_ <sup>PC</sup> non con tipi (48)</span><span class="sxs-lookup"><span data-stu-id="b648e-3331">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="b648e-3332">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3332">Target</span></span> | <span data-ttu-id="b648e-3333">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3334">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3335">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3335">16</span></span> |
| <span data-ttu-id="b648e-3336">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3336">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3338">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3338">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3339">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3339">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3340">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3340">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3341">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3341">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3342">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3342">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3344">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3344">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3346">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3346">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3348">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3350">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3350">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-3351">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3351">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3352">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3352">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3353">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3353">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3354">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3354">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3355">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3355">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3356">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3356">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3358">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3358">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3359">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3359">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3360">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3360">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3361">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3361">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3362">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3362">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3363">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3363">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3364">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3364">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3365">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3365">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3366">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3366">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3367">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3367">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3368">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3368">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3369">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3369">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3370">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3370">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3371">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3371">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3372">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3372">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3373">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3373">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3374">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3374">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3376">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3376">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3377">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3377">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3378">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3378">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-3379">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3379">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3380">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3380">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-3381">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3382">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3382">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3384">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3385">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3386">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3387">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3387">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-3388">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3388">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="b648e-3389">DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="b648e-3389">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="b648e-3390">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3390">Target</span></span> | <span data-ttu-id="b648e-3391">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3391">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3392">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3392">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3393">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3393">16</span></span> |
| <span data-ttu-id="b648e-3394">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3394">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3396">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3396">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3398">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3398">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3400">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3401">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3402">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3404">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3406">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3408">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3410">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3410">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3412">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3412">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3414">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3415">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3416">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3416">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3417">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3418">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3420">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3420">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3422">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3424">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3424">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3426">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3427">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3428">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3429">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3430">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3430">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3431">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3432">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3433">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3434">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3436">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3437">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3438">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3439">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3439">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3441">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3441">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3443">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3443">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3445">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3445">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3447">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3447">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3449">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3449">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3451">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3451">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3452">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3452">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3454">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3454">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3455">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3455">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3456">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3456">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3457">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3457">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3459">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3459">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="b648e-3460">DXGI_FORMAT_R8G8 \_ uint<sup>FCS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="b648e-3460">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="b648e-3461">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3461">Target</span></span> | <span data-ttu-id="b648e-3462">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3462">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3463">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3463">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3464">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3464">16</span></span> |
| <span data-ttu-id="b648e-3465">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3465">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3467">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3467">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3469">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3469">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3471">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3471">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3472">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3472">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3473">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3473">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3475">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3475">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3477">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3477">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3479">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3479">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3481">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3481">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3483">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3484">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3484">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3485">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3485">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3486">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3486">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3487">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3487">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3488">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3488">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3490">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3490">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3491">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3493">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3493">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3494">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3494">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3496">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3496">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3497">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3497">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3498">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3498">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3499">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3499">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3500">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3500">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3501">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3501">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3502">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3502">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3503">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3503">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3504">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3504">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3505">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3505">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3506">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3506">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3507">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3507">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3508">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3508">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3510">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3510">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3512">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3512">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3514">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3514">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3516">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3516">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3517">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3517">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3519">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3520">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3520">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3522">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3523">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3524">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3525">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3525">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-3526">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="b648e-3527">DXGI_FORMAT_R8G8 \_ russo<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="b648e-3527">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="b648e-3528">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3528">Target</span></span> | <span data-ttu-id="b648e-3529">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3529">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3530">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3531">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3531">16</span></span> |
| <span data-ttu-id="b648e-3532">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3532">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3534">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3534">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3536">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3536">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3538">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3539">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3540">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3542">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3542">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3544">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3544">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3546">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3546">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3548">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3548">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3550">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3550">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3552">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3553">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3554">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3555">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3556">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3558">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3558">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3560">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3562">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3562">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3564">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3565">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3566">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3567">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3568">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3568">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3569">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3570">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3571">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3572">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3573">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3574">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3575">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3576">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3577">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3577">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3579">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3579">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3581">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3581">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3583">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3583">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3585">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3585">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3587">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3587">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3589">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3589">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3590">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3590">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3592">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3592">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3593">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3593">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3594">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3594">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3595">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3595">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-3596">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3596">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="b648e-3597">DXGI_FORMAT_R8G8 \_ Sint<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="b648e-3597">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="b648e-3598">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3598">Target</span></span> | <span data-ttu-id="b648e-3599">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3599">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3600">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3600">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3601">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3601">16</span></span> |
| <span data-ttu-id="b648e-3602">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3602">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3604">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3604">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3606">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3606">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3608">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3609">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3610">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3612">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3612">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3614">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3614">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3616">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3616">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3618">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3618">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3620">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3620">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3621">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3621">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3622">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3622">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3623">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3623">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3624">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3624">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3625">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3625">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3627">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3627">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3628">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3628">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3630">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3630">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3631">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3631">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3632">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3633">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3634">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3635">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3635">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3636">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3637">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3638">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3639">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3640">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3640">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3641">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3642">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3642">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3643">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3643">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3644">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3644">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3646">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3646">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3648">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3648">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3650">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3650">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3652">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3653">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3653">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3655">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3656">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3656">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3658">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3659">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3660">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3661">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3661">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-3662">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3662">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="b648e-3663">DXGI_FORMAT_R16 \_ <sup>PC</sup> non con tipi (53)</span><span class="sxs-lookup"><span data-stu-id="b648e-3663">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="b648e-3664">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3664">Target</span></span> | <span data-ttu-id="b648e-3665">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3665">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3666">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3666">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3667">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3667">16</span></span> |
| <span data-ttu-id="b648e-3668">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3668">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3670">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3670">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3671">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3672">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3673">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3674">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3676">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3676">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3678">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3678">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3680">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3680">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3682">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3682">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-3683">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3683">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3684">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3685">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3686">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3686">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3687">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3688">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3688">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3690">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3691">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3692">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3693">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3694">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3695">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3696">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3697">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3697">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3698">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3699">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3700">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3701">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3703">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3704">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3705">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3706">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3706">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3708">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3709">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3710">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-3711">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3712">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3712">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-3713">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3714">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3714">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3716">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3716">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3717">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3717">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3718">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3718">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3719">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3719">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3721">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3721">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="b648e-3722">DXGI_FORMAT_R16 \_ float<sup>FCS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="b648e-3722">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="b648e-3723">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3723">Target</span></span> | <span data-ttu-id="b648e-3724">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3724">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3725">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3725">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3726">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3726">16</span></span> |
| <span data-ttu-id="b648e-3727">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3727">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3729">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3729">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3731">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3731">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3733">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3734">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3735">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3737">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3739">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3741">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3743">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3743">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3745">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3745">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3747">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3748">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3749">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3749">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3751">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3752">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3752">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3754">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3754">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3756">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3756">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3758">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3758">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3760">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3760">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3761">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3761">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3762">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3762">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3763">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3763">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3764">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3764">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3765">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3765">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3766">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3766">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3767">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3767">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3768">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3768">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3769">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3769">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3770">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3770">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3771">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3771">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3772">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3772">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3773">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3773">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3775">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3775">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3777">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3777">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3779">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3779">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3781">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3781">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3783">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3783">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3785">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3785">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3786">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3786">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3788">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3788">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3789">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3789">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3790">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3790">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3791">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3791">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3793">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3793">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="b648e-3794">DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="b648e-3794">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="b648e-3795">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3795">Target</span></span> | <span data-ttu-id="b648e-3796">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3796">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3797">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3797">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3798">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3798">16</span></span> |
| <span data-ttu-id="b648e-3799">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3799">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3801">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3801">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3802">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3802">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3803">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3803">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3804">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3804">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3805">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3805">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3807">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3810">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3812">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3812">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-3813">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3813">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3814">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3814">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3815">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3815">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3816">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3816">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3817">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3817">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3818">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3818">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3820">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3820">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3821">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3821">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3822">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3822">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3823">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3823">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3824">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3824">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3826">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3826">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3827">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3827">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3828">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3828">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3829">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3829">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3830">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3830">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3831">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3831">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3832">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3832">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3833">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3833">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3834">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3834">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3835">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3835">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3836">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3836">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3837">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3837">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3839">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3839">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3841">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3841">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3843">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3843">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3845">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3845">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3846">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3846">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-3847">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3847">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3848">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3848">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3850">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3850">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3851">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3851">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3852">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3852">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3853">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3853">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3855">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3855">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="b648e-3856">DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="b648e-3856">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="b648e-3857">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3857">Target</span></span> | <span data-ttu-id="b648e-3858">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3858">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3859">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3859">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3860">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3860">16</span></span> |
| <span data-ttu-id="b648e-3861">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3861">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3863">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3863">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3865">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3865">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3867">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3868">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3869">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3871">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3871">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3873">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3873">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3875">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3875">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3877">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3877">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3879">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3879">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3881">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3881">Shader sample\_c (comparison filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3883">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3883">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3884">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3884">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3886">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3886">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3887">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3887">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3889">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3889">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3891">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3891">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3893">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3893">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3895">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3895">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-3896">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3896">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3897">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3897">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3898">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3898">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3899">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3899">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3900">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3900">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3901">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3901">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3902">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3902">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3903">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3903">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3904">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3904">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3905">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3905">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3906">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3906">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3907">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3907">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3908">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3908">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3910">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3910">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3912">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3912">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3914">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3914">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3916">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3916">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3918">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3918">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3920">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3920">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3921">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3921">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3923">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3923">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3924">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3924">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3925">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3925">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3926">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3926">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3928">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="b648e-3929">DXGI_FORMAT_R16 \_ uint<sup>FCS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="b648e-3929">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="b648e-3930">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3930">Target</span></span> | <span data-ttu-id="b648e-3931">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-3931">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-3932">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-3932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-3933">16</span><span class="sxs-lookup"><span data-stu-id="b648e-3933">16</span></span> |
| <span data-ttu-id="b648e-3934">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-3934">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3936">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-3936">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3938">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-3938">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3940">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-3940">Input Assembler Index Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3942">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-3942">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-3943">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-3943">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3945">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-3945">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3947">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-3947">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3949">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-3949">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3951">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-3951">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3953">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-3953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-3954">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-3954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-3955">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-3955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-3956">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-3956">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-3957">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-3957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-3958">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3958">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3960">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-3960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-3961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-3961">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3963">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-3963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-3964">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-3964">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3966">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3966">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-3967">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-3967">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3968">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-3968">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-3969">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-3969">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-3970">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3970">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-3971">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3971">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-3972">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3972">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-3973">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3973">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-3974">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-3974">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-3975">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3975">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-3976">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-3976">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3977">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-3977">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-3978">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-3978">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3980">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-3980">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3982">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-3982">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3984">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-3984">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-3986">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3986">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-3987">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-3987">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3989">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-3989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-3990">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-3990">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3992">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-3993">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-3994">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-3994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-3995">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-3995">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-3997">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-3997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="b648e-3998">DXGI_FORMAT_R16 \_ russo<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="b648e-3998">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="b648e-3999">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-3999">Target</span></span> | <span data-ttu-id="b648e-4000">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4000">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4001">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4002">16</span><span class="sxs-lookup"><span data-stu-id="b648e-4002">16</span></span> |
| <span data-ttu-id="b648e-4003">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4003">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4005">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4005">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4007">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4007">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4009">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4009">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4010">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4010">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4011">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4011">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4013">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4013">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4015">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4015">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4017">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4017">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4019">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4019">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4021">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4021">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4023">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4023">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4024">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4024">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4025">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4025">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4027">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4027">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4028">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4028">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4030">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4030">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4032">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4032">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4034">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4034">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4036">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4036">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4037">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4037">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4038">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4038">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4039">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4039">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4040">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4040">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4041">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4041">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4042">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4042">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4043">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4043">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4044">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4044">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4045">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4045">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4046">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4046">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4047">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4047">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4048">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4048">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4049">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4049">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4051">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4051">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4053">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4053">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4055">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4055">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4057">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4057">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4059">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4059">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4061">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4062">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4062">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4064">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4064">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4065">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4065">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4066">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4066">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4067">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4067">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4069">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4069">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="b648e-4070">DXGI_FORMAT_R16 \_ Sint<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="b648e-4070">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="b648e-4071">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4071">Target</span></span> | <span data-ttu-id="b648e-4072">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4072">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4073">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4073">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4074">16</span><span class="sxs-lookup"><span data-stu-id="b648e-4074">16</span></span> |
| <span data-ttu-id="b648e-4075">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4075">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4077">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4077">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4079">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4079">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4081">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4081">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4082">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4082">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4083">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4083">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4085">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4087">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4087">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4089">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4089">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4091">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4091">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4093">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4093">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-4094">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4094">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4095">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4095">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4096">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4096">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4097">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4097">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4098">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4098">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4100">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4100">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4101">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4101">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4103">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4103">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4104">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4104">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4105">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4105">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4106">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4106">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4107">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4107">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4108">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4108">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4109">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4109">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4110">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4110">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4111">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4111">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4112">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4112">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4113">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4113">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4114">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4114">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4115">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4115">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4116">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4116">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4117">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4117">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4119">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4119">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4121">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4121">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4123">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4123">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4125">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4125">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4126">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4126">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4128">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4128">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4129">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4129">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4131">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4131">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4132">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4132">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4133">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4133">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4134">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4134">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4136">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4136">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="b648e-4137">DXGI_FORMAT_R8 \_ <sup>PC</sup> non con tipi (60)</span><span class="sxs-lookup"><span data-stu-id="b648e-4137">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="b648e-4138">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4138">Target</span></span> | <span data-ttu-id="b648e-4139">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4139">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4140">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4140">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4141">8</span><span class="sxs-lookup"><span data-stu-id="b648e-4141">8</span></span> |
| <span data-ttu-id="b648e-4142">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4142">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4144">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4144">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4145">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4145">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4146">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4146">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4147">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4147">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4148">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4148">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4150">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4152">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4152">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4154">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4156">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4156">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-4157">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4157">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-4158">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4158">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4159">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4159">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4160">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4160">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4161">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4161">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4162">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4162">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4164">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4164">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4165">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4165">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4166">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4166">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4167">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4167">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4168">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4168">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4169">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4169">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4170">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4170">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4171">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4171">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4172">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4172">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4173">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4173">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4174">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4174">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4175">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4175">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4176">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4176">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4177">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4177">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4178">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4178">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4179">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4179">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4180">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4180">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4182">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4182">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4183">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4183">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4184">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4184">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-4185">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4185">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4186">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4186">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-4187">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4187">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4188">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4188">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4190">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4190">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4191">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4191">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4192">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4192">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4193">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4193">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4195">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="b648e-4196">DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="b648e-4196">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="b648e-4197">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4197">Target</span></span> | <span data-ttu-id="b648e-4198">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4198">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4199">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4200">8</span><span class="sxs-lookup"><span data-stu-id="b648e-4200">8</span></span> |
| <span data-ttu-id="b648e-4201">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4201">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4203">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4203">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4205">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4205">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4207">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4207">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4208">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4208">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4209">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4209">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4211">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4213">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4215">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4215">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4217">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4217">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4219">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4219">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4221">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4221">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4222">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4222">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4223">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4223">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4225">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4226">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4226">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4228">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4228">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4230">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4230">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4232">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4232">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4234">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4234">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4235">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4235">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4236">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4236">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4237">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4237">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4238">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4238">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4239">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4239">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4240">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4240">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4241">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4241">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4242">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4242">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4243">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4243">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4244">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4244">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4245">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4245">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4246">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4246">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4247">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4247">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4249">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4249">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4251">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4251">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4253">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4253">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4255">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4255">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4257">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4257">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4259">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4259">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4260">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4260">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4262">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4262">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4263">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4263">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4264">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4264">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4265">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4265">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4267">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4267">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="b648e-4268">DXGI_FORMAT_R8 \_ uint<sup>FCS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="b648e-4268">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="b648e-4269">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4269">Target</span></span> | <span data-ttu-id="b648e-4270">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4270">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4271">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4271">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4272">8</span><span class="sxs-lookup"><span data-stu-id="b648e-4272">8</span></span> |
| <span data-ttu-id="b648e-4273">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4273">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4275">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4275">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4277">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4277">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4279">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4279">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4280">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4280">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4281">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4281">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4283">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4283">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4285">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4287">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4289">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4289">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4291">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-4292">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4293">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4294">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4294">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4295">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4296">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4296">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4298">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4298">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4299">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4299">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4301">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4302">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4302">Output Merger Logic Op</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4304">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4305">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4306">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4307">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4307">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4308">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4309">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4310">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4311">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4312">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4313">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4314">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4315">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4316">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4316">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4318">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4318">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4320">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4320">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4322">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4322">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4324">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4324">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4325">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4325">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4327">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4327">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4328">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4328">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4330">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4331">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4332">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4333">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4333">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4335">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4335">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="b648e-4336">DXGI_FORMAT_R8 \_ russo<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="b648e-4336">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="b648e-4337">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4337">Target</span></span> | <span data-ttu-id="b648e-4338">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4338">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4339">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4339">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4340">8</span><span class="sxs-lookup"><span data-stu-id="b648e-4340">8</span></span> |
| <span data-ttu-id="b648e-4341">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4341">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4343">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4343">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4345">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4345">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4347">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4348">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4349">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4351">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4351">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4353">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4355">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4355">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4357">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4357">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4359">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4359">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4361">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4361">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4362">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4362">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4363">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4363">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4365">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4365">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4366">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4366">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4368">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4368">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4370">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4372">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4372">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4374">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4375">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4376">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4377">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4378">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4379">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4380">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4381">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4382">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4383">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4384">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4385">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4386">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4387">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4387">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4389">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4389">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4391">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4391">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4393">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4393">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4395">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4395">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4397">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4397">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4399">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4399">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4400">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4400">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4402">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4402">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4403">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4403">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4404">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4404">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4405">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4405">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4407">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4407">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="b648e-4408">DXGI_FORMAT_R8 \_ Sint<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="b648e-4408">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="b648e-4409">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4409">Target</span></span> | <span data-ttu-id="b648e-4410">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4410">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4411">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4411">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4412">8</span><span class="sxs-lookup"><span data-stu-id="b648e-4412">8</span></span> |
| <span data-ttu-id="b648e-4413">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4413">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4415">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4415">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4417">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4417">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4419">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4419">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4420">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4420">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4421">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4421">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4423">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4425">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4427">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4429">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4429">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4431">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4431">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-4432">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4432">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4433">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4433">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4434">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4434">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4435">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4435">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4436">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4436">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4438">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4438">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4439">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4441">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4441">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4442">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4442">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4443">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4443">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4444">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4444">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4445">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4445">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4446">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4446">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4447">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4447">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4448">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4448">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4449">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4449">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4450">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4450">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4451">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4451">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4452">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4452">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4453">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4453">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4454">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4454">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4455">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4455">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4457">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4457">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4459">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4459">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4461">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4461">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4463">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4463">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4464">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4464">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4466">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4466">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4467">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4467">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4469">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4469">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4470">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4470">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4471">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4471">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4472">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4472">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4474">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4474">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="b648e-4475">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="b648e-4475">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="b648e-4476">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4476">Target</span></span> | <span data-ttu-id="b648e-4477">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4477">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4478">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4478">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4479">8</span><span class="sxs-lookup"><span data-stu-id="b648e-4479">8</span></span> |
| <span data-ttu-id="b648e-4480">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4480">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4482">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4482">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4483">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4483">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4484">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4484">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4485">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4485">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4486">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4486">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4488">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4488">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4490">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4492">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4492">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4494">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4494">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4496">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4496">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4498">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4498">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4499">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4499">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4500">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4500">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4501">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4501">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4502">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4502">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4504">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4504">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4506">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4506">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4508">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4508">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4510">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4510">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4511">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4511">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4512">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4512">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4513">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4513">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4514">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4514">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4515">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4515">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4516">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4516">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4517">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4517">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4518">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4518">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4519">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4519">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4520">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4520">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4521">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4521">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4522">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4522">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4523">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4523">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4525">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4525">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4527">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4527">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4529">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4529">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-4531">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4531">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4533">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4533">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4535">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4536">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-4537">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4538">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4539">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4540">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4540">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4542">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="b648e-4543">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="b648e-4543">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="b648e-4544">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4544">Target</span></span> | <span data-ttu-id="b648e-4545">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4546">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4547">32</span><span class="sxs-lookup"><span data-stu-id="b648e-4547">32</span></span> |
| <span data-ttu-id="b648e-4548">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4548">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4550">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4551">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4552">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4553">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4554">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4556">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4558">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4558">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4560">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4560">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4562">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4562">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4564">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4564">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4566">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4567">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4568">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4569">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4570">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4570">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4572">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4572">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4573">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4573">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4574">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4574">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4575">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4575">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4576">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4576">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4577">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4577">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4578">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4578">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4579">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4579">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4580">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4580">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4581">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4581">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4582">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4582">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4583">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4583">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4584">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4584">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4585">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4585">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4586">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4586">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4587">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4587">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4588">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4588">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4590">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4590">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4591">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4591">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4592">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4592">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-4593">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4593">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4594">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4594">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-4595">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4595">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4596">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4596">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-4597">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4597">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4598">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4598">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4599">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4599">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4600">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4600">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-4601">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4601">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="b648e-4602">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="b648e-4602">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="b648e-4603">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4603">Target</span></span> | <span data-ttu-id="b648e-4604">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4605">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4606">16</span><span class="sxs-lookup"><span data-stu-id="b648e-4606">16</span></span> |
| <span data-ttu-id="b648e-4607">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4607">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4609">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4610">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4610">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4611">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4611">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4612">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4612">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4613">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4613">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4615">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4617">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4617">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4619">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4619">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4621">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4621">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4623">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4623">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4625">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4625">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4626">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4626">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4627">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4627">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4628">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4628">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4629">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4629">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4631">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4631">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4632">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4632">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4633">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4633">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4634">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4634">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4635">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4635">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4636">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4636">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4637">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4637">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4638">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4638">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4639">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4639">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4640">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4640">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4641">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4641">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4642">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4642">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4643">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4643">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4644">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4644">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4645">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4645">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4646">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4646">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4647">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4647">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4649">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4649">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4650">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4650">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4651">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4651">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-4652">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4653">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4653">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-4654">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4654">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4655">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4655">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-4656">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4656">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4657">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4657">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4658">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4658">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4659">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4659">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-4660">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4660">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="b648e-4661">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="b648e-4661">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="b648e-4662">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4662">Target</span></span> | <span data-ttu-id="b648e-4663">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4663">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4664">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4664">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4665">16</span><span class="sxs-lookup"><span data-stu-id="b648e-4665">16</span></span> |
| <span data-ttu-id="b648e-4666">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4666">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4668">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4668">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4669">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4669">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4670">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4670">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4671">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4671">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4672">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4672">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4674">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4674">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4676">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4678">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4678">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4680">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4680">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4682">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4682">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4684">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4685">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4686">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4686">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4687">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4688">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4688">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4690">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4691">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4692">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4693">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4694">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4695">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4696">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4697">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4697">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4698">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4699">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4700">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4701">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4703">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4704">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4705">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4706">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4706">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4708">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4709">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4710">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-4711">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4712">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4712">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-4713">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4714">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4714">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-4715">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4715">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4716">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4716">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4717">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4717">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4718">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4718">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-4719">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4719">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="b648e-4720">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non tipizzato (70)</span><span class="sxs-lookup"><span data-stu-id="b648e-4720">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="b648e-4721">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4721">Target</span></span> | <span data-ttu-id="b648e-4722">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4722">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4723">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4723">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4724">4</span><span class="sxs-lookup"><span data-stu-id="b648e-4724">4</span></span> |
| <span data-ttu-id="b648e-4725">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4725">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4727">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4727">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4728">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4728">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4729">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4729">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4730">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4730">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4731">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4731">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-4732">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4732">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4734">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4734">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4736">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4736">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4738">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4738">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-4739">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4739">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-4740">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4740">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4741">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4741">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4742">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4742">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4743">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4743">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4744">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4744">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4746">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4746">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4747">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4747">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4748">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4748">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4749">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4749">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4750">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4750">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4751">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4751">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4752">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4752">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4753">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4753">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4754">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4754">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4755">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4755">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4756">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4756">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4757">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4757">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4758">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4758">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4759">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4759">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4760">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4760">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4761">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4761">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4762">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4762">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4764">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4764">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4765">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4765">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4766">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4766">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-4767">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4767">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4768">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4768">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-4769">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4769">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4770">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4770">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4772">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4772">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4773">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4773">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4774">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4774">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4775">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4775">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4777">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4777">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="b648e-4778">DXGI_FORMAT_BC1 \_ <sup>FCC</sup> UNORM (71)</span><span class="sxs-lookup"><span data-stu-id="b648e-4778">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="b648e-4779">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4779">Target</span></span> | <span data-ttu-id="b648e-4780">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4780">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4781">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4781">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4782">4</span><span class="sxs-lookup"><span data-stu-id="b648e-4782">4</span></span> |
| <span data-ttu-id="b648e-4783">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4783">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4785">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4785">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4786">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4786">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4787">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4787">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4788">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4788">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4789">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4789">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-4790">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4790">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4792">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4792">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4794">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4794">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4796">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4796">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4798">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4798">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4800">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4800">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4801">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4801">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4802">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4802">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4803">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4803">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4804">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4804">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4806">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4807">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4808">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4809">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4810">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4811">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4812">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4813">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4813">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4814">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4815">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4816">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4817">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4818">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4819">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4820">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4821">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4822">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4822">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4824">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4824">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4825">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4825">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4826">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4826">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-4827">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4827">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4828">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4828">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-4829">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4829">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4830">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4830">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4832">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4832">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4833">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4833">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4834">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4834">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4835">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4835">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4837">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="b648e-4838">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="b648e-4838">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="b648e-4839">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4839">Target</span></span> | <span data-ttu-id="b648e-4840">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4840">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4841">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4842">4</span><span class="sxs-lookup"><span data-stu-id="b648e-4842">4</span></span> |
| <span data-ttu-id="b648e-4843">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4843">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4845">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4845">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4846">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4846">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4847">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4847">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4848">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4848">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4849">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4849">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-4850">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4850">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4852">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4852">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4854">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4854">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4856">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4856">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4858">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4858">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4860">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4860">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4861">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4861">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4862">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4862">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4863">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4863">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4864">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4864">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4866">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4867">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4868">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4869">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4870">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4871">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4872">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4873">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4873">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4874">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4875">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4876">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4877">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4879">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4880">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4881">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4882">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4882">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4884">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4885">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4886">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-4887">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4888">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4888">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-4889">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4890">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4890">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4892">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4892">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4893">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4893">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4894">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4895">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4895">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4897">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4897">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="b648e-4898">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non tipizzato (73)</span><span class="sxs-lookup"><span data-stu-id="b648e-4898">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="b648e-4899">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4899">Target</span></span> | <span data-ttu-id="b648e-4900">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4900">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4901">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4901">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4902">8</span><span class="sxs-lookup"><span data-stu-id="b648e-4902">8</span></span> |
| <span data-ttu-id="b648e-4903">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4903">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4905">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4905">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4906">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4906">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4907">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4907">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4908">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4908">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4909">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4909">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-4910">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4910">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4912">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4912">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4914">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4914">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4916">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4916">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-4917">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4917">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-4918">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4918">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4919">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4919">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4920">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4920">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4921">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4921">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4922">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4922">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4924">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4924">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4925">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4925">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4926">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4926">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4927">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4927">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4928">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4928">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4929">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4929">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4930">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4930">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4931">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4931">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4932">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4932">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4933">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4933">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4934">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4934">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4935">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4935">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4936">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4936">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4937">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4937">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4938">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4938">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4939">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4939">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4940">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-4940">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4942">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-4942">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4943">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-4943">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4944">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-4944">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-4945">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4945">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-4946">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-4946">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-4947">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-4947">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-4948">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-4948">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4950">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4950">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-4951">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4951">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-4952">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-4952">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-4953">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-4953">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4955">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-4955">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="b648e-4956">DXGI_FORMAT_BC2 \_ <sup>FCC</sup> UNORM (74)</span><span class="sxs-lookup"><span data-stu-id="b648e-4956">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="b648e-4957">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4957">Target</span></span> | <span data-ttu-id="b648e-4958">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-4958">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-4959">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-4959">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-4960">8</span><span class="sxs-lookup"><span data-stu-id="b648e-4960">8</span></span> |
| <span data-ttu-id="b648e-4961">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-4961">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4963">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-4963">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4964">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-4964">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4965">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-4965">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4966">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-4966">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-4967">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-4967">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-4968">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-4968">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4970">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-4970">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-4972">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4974">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-4974">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4976">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-4976">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4978">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-4978">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-4979">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-4979">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-4980">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-4980">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-4981">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-4981">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-4982">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4982">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-4984">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-4984">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-4985">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-4985">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4986">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-4986">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-4987">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-4987">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-4988">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-4988">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-4989">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-4989">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4990">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-4990">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-4991">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-4991">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-4992">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4992">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-4993">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4993">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-4994">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4994">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-4995">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4995">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-4996">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-4996">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-4997">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4997">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-4998">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-4998">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-4999">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-4999">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5000">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5000">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5002">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5002">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5003">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5003">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5004">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5004">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5005">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5006">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5006">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5007">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5007">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5008">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5008">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5010">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5011">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5012">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5013">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5013">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5015">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5015">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="b648e-5016">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="b648e-5016">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="b648e-5017">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5017">Target</span></span> | <span data-ttu-id="b648e-5018">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5018">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5019">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5019">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5020">8</span><span class="sxs-lookup"><span data-stu-id="b648e-5020">8</span></span> |
| <span data-ttu-id="b648e-5021">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5021">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5023">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5023">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5024">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5024">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5025">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5025">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5026">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5026">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5027">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5027">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5028">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5028">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5030">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5032">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5032">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5034">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5034">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5036">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5036">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5038">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5038">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5039">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5039">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5040">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5040">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5041">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5041">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5042">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5042">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5044">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5044">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5045">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5045">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5046">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5046">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5047">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5047">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5048">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5048">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5049">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5049">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5050">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5050">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5051">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5051">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5052">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5052">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5053">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5053">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5054">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5054">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5055">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5055">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5056">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5056">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5057">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5057">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5058">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5058">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5059">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5059">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5060">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5060">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5062">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5062">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5063">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5063">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5064">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5064">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5065">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5066">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5067">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5068">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5068">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5070">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5070">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5071">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5071">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5072">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5072">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5073">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5073">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5075">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="b648e-5076">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non tipizzato (76)</span><span class="sxs-lookup"><span data-stu-id="b648e-5076">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="b648e-5077">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5077">Target</span></span> | <span data-ttu-id="b648e-5078">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5078">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5079">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5080">8</span><span class="sxs-lookup"><span data-stu-id="b648e-5080">8</span></span> |
| <span data-ttu-id="b648e-5081">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5081">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5083">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5083">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5084">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5085">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5086">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5087">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5088">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5090">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5090">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5092">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5092">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5094">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5094">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-5095">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5095">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-5096">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5096">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5097">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5097">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5098">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5098">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5099">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5099">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5100">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5100">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5102">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5102">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5103">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5103">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5104">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5104">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5105">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5105">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5106">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5106">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5107">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5107">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5108">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5108">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5109">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5109">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5110">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5110">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5111">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5111">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5112">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5112">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5113">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5113">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5114">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5114">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5115">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5115">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5116">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5116">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5117">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5117">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5118">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5118">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5120">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5120">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5121">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5121">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5122">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5122">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5123">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5123">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5124">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5124">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5125">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5125">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5126">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5126">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5128">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5128">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5129">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5129">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5130">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5130">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5131">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5131">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5133">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5133">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="b648e-5134">DXGI_FORMAT_BC3 \_ <sup>FCC</sup> UNORM (77)</span><span class="sxs-lookup"><span data-stu-id="b648e-5134">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="b648e-5135">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5135">Target</span></span> | <span data-ttu-id="b648e-5136">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5136">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5137">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5137">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5138">8</span><span class="sxs-lookup"><span data-stu-id="b648e-5138">8</span></span> |
| <span data-ttu-id="b648e-5139">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5139">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5141">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5141">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5142">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5142">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5143">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5143">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5144">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5144">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5145">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5145">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5146">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5146">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5148">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5148">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5150">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5150">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5152">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5152">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5154">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5154">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5156">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5156">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5157">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5157">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5158">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5158">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5159">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5159">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5160">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5160">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5162">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5163">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5164">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5165">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5166">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5167">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5168">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5169">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5169">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5170">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5171">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5172">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5173">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5174">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5175">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5176">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5177">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5178">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5178">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5180">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5181">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5182">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5183">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5184">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5184">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5185">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5186">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5186">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5188">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5188">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5189">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5189">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5190">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5190">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5191">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5191">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5193">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5193">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="b648e-5194">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="b648e-5194">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="b648e-5195">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5195">Target</span></span> | <span data-ttu-id="b648e-5196">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5196">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5197">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5197">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5198">8</span><span class="sxs-lookup"><span data-stu-id="b648e-5198">8</span></span> |
| <span data-ttu-id="b648e-5199">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5199">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5201">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5201">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5202">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5202">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5203">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5203">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5204">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5204">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5205">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5205">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5206">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5206">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5208">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5210">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5210">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5212">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5212">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5214">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5214">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5216">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5216">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5217">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5217">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5218">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5218">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5219">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5219">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5220">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5220">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5222">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5224">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5225">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5226">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5227">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5228">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5229">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5230">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5231">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5232">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5233">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5234">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5235">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5236">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5237">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5238">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5238">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5240">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5241">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5242">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5243">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5244">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5245">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5246">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5246">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5248">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5248">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5249">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5249">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5250">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5250">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5251">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5251">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5253">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5253">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="b648e-5254">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non tipizzato (79)</span><span class="sxs-lookup"><span data-stu-id="b648e-5254">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="b648e-5255">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5255">Target</span></span> | <span data-ttu-id="b648e-5256">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5256">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5257">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5257">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5258">4</span><span class="sxs-lookup"><span data-stu-id="b648e-5258">4</span></span> |
| <span data-ttu-id="b648e-5259">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5259">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5261">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5261">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5262">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5262">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5263">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5264">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5265">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5266">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5266">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5268">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5268">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5270">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5272">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5272">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-5273">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5273">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-5274">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5274">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5275">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5275">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5276">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5276">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5277">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5277">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5278">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5278">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5280">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5280">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5281">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5281">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5282">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5282">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5283">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5283">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5284">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5284">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5285">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5285">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5286">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5286">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5287">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5287">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5288">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5288">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5289">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5289">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5290">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5291">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5292">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5292">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5293">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5294">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5294">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5295">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5295">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5296">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5296">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5298">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5298">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5299">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5299">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5300">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5300">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5301">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5302">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5302">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5303">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5303">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5304">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5304">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5306">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5306">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5307">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5307">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5308">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5308">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5309">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-5310">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="b648e-5311">DXGI_FORMAT_BC4 \_ <sup>FCC</sup> UNORM (80)</span><span class="sxs-lookup"><span data-stu-id="b648e-5311">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="b648e-5312">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5312">Target</span></span> | <span data-ttu-id="b648e-5313">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5314">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5315">4</span><span class="sxs-lookup"><span data-stu-id="b648e-5315">4</span></span> |
| <span data-ttu-id="b648e-5316">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5316">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5318">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5319">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5320">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5321">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5323">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5325">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5327">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5329">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5329">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5331">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5331">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5333">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5333">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5334">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5334">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5335">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5335">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5336">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5336">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5337">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5337">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5339">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5341">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5342">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5343">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5344">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5345">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5346">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5347">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5348">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5349">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5350">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5352">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5353">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5354">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5355">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5355">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5357">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5358">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5359">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5360">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5361">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5362">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5363">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5363">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5365">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5365">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5366">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5366">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5367">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5367">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5368">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5368">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-5369">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5369">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="b648e-5370">DXGI_FORMAT_BC4 \_ russare<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="b648e-5370">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="b648e-5371">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5371">Target</span></span> | <span data-ttu-id="b648e-5372">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5372">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5373">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5373">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5374">4</span><span class="sxs-lookup"><span data-stu-id="b648e-5374">4</span></span> |
| <span data-ttu-id="b648e-5375">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5375">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5377">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5377">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5378">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5378">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5379">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5379">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5380">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5380">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5381">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5381">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5382">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5382">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5384">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5384">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5386">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5388">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5388">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5390">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5390">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5392">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5392">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5393">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5393">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5394">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5394">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5395">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5395">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5396">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5396">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5398">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5399">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5400">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5400">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5401">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5401">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5402">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5402">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5403">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5403">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5404">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5404">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5405">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5405">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5406">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5406">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5407">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5407">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5408">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5408">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5409">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5409">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5410">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5410">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5411">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5411">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5412">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5412">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5413">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5413">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5414">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5414">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5416">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5416">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5417">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5417">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5418">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5418">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5419">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5419">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5420">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5420">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5421">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5421">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5422">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5422">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5424">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5424">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5425">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5425">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5426">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5426">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5427">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5427">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-5428">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5428">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="b648e-5429">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non tipizzato (82)</span><span class="sxs-lookup"><span data-stu-id="b648e-5429">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="b648e-5430">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5430">Target</span></span> | <span data-ttu-id="b648e-5431">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5431">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5432">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5432">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5433">8</span><span class="sxs-lookup"><span data-stu-id="b648e-5433">8</span></span> |
| <span data-ttu-id="b648e-5434">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5434">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5436">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5436">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5437">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5437">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5438">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5438">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5439">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5439">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5440">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5440">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5441">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5441">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5443">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5443">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5445">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5445">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5447">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5447">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-5448">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5448">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-5449">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5449">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5450">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5450">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5451">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5451">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5452">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5452">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5453">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5453">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5455">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5455">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5456">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5456">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5457">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5457">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5458">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5458">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5459">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5459">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5460">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5460">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5461">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5461">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5462">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5462">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5463">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5463">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5464">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5464">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5465">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5465">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5466">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5466">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5467">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5467">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5468">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5468">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5469">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5469">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5470">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5470">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5471">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5471">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5473">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5473">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5474">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5474">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5475">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5475">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5476">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5476">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5477">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5477">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5478">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5479">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5479">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5481">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5482">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5483">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5484">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5484">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-5485">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="b648e-5486">DXGI_FORMAT_BC5 \_ <sup>FCC</sup> UNORM (83)</span><span class="sxs-lookup"><span data-stu-id="b648e-5486">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="b648e-5487">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5487">Target</span></span> | <span data-ttu-id="b648e-5488">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5488">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5489">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5490">8</span><span class="sxs-lookup"><span data-stu-id="b648e-5490">8</span></span> |
| <span data-ttu-id="b648e-5491">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5491">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5493">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5493">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5494">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5495">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5496">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5497">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5498">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5500">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5500">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5502">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5502">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5504">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5504">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5506">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5506">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5508">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5509">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5510">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5510">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5511">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5512">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5514">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5515">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5516">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5517">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5518">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5519">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5520">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5521">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5521">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5522">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5523">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5524">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5525">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5526">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5527">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5528">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5529">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5530">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5530">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5532">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5532">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5533">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5533">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5534">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5534">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5535">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5535">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5536">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5536">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5537">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5537">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5538">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5538">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5540">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5541">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5542">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5543">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5543">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-5544">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="b648e-5545">DXGI_FORMAT_BC5 \_ russare<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="b648e-5545">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="b648e-5546">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5546">Target</span></span> | <span data-ttu-id="b648e-5547">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5547">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5548">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5549">8</span><span class="sxs-lookup"><span data-stu-id="b648e-5549">8</span></span> |
| <span data-ttu-id="b648e-5550">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5550">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5552">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5552">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5553">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5553">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5554">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5554">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5555">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5555">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5556">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5556">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-5557">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5557">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5559">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5559">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5561">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5561">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5563">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5563">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5565">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5565">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5567">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5567">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5568">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5568">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5569">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5569">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5570">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5570">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5571">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5571">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5573">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5573">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5574">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5574">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5575">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5575">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5576">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5577">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5578">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5579">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5580">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5580">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5581">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5582">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5583">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5584">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5585">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5586">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5587">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5588">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5589">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5589">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5591">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5591">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5592">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5592">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5593">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5593">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5594">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5594">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5595">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5595">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5596">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5596">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5597">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5597">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5599">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5600">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5601">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5602">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5602">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-5603">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="b648e-5604">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="b648e-5604">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="b648e-5605">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5605">Target</span></span> | <span data-ttu-id="b648e-5606">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5606">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5607">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5608">16</span><span class="sxs-lookup"><span data-stu-id="b648e-5608">16</span></span> |
| <span data-ttu-id="b648e-5609">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5609">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5611">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5611">Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5613">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5613">Input Assembler Vertex Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5615">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5615">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5616">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5616">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5617">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5617">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5619">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5621">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5623">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5623">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5625">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5625">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5627">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5627">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5629">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5629">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5630">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5630">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5631">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5631">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5632">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5632">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5633">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5633">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5635">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5635">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5637">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5637">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5639">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5639">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5641">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5641">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5642">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5642">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5643">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5643">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5644">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5644">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5645">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5645">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5646">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5646">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5647">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5647">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5648">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5648">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5649">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5649">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5650">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5650">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5651">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5651">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5652">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5652">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5653">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5653">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5654">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5654">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5656">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5656">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5658">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5658">8x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5660">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5660">Other Multisample Count RT</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5662">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5662">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5664">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5664">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5666">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5666">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5667">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5667">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-5668">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5669">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5670">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5671">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5671">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-5672">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5672">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="b648e-5673">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="b648e-5673">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="b648e-5674">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5674">Target</span></span> | <span data-ttu-id="b648e-5675">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5675">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5676">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5676">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5677">16</span><span class="sxs-lookup"><span data-stu-id="b648e-5677">16</span></span> |
| <span data-ttu-id="b648e-5678">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5678">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5680">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5680">Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5682">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5682">Input Assembler Vertex Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5684">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5684">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5685">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5685">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5686">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5686">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5688">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5688">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5690">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5690">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5692">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5692">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5694">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5694">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5696">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5696">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5698">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5698">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5699">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5699">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5700">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5700">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5701">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5701">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5702">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5702">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5704">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5704">Mipmap Auto-Generation</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5706">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5706">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5708">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5708">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5710">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5710">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5711">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5711">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5712">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5712">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5713">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5713">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5714">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5714">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5715">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5715">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5716">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5716">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5717">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5717">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5718">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5718">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5719">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5719">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5720">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5720">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5721">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5721">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5722">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5722">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5723">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5723">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5725">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5725">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5727">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5727">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5729">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5729">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5731">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5731">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5733">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5733">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5735">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5735">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5736">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5736">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-5737">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5737">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5738">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5738">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5739">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5739">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5740">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5740">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-5741">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5741">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="b648e-5742">DXGI_FORMAT_B8G8R8A8 \_ <sup>PC</sup> non con tipi (90)</span><span class="sxs-lookup"><span data-stu-id="b648e-5742">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="b648e-5743">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5743">Target</span></span> | <span data-ttu-id="b648e-5744">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5744">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5745">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5745">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5746">32</span><span class="sxs-lookup"><span data-stu-id="b648e-5746">32</span></span> |
| <span data-ttu-id="b648e-5747">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5747">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5749">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5749">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5750">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5750">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5751">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5752">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5753">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5755">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5757">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5759">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5761">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5761">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-5762">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5762">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-5763">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5763">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5764">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5764">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5765">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5765">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5766">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5766">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5767">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5767">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5769">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5769">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5770">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5770">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5771">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5771">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5772">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5772">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5773">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5773">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5774">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5774">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5775">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5775">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5776">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5776">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5777">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5777">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5778">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5778">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5779">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5779">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5780">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5780">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5781">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5781">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5782">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5782">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5783">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5783">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5784">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5784">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5785">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5785">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5787">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5787">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5788">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5788">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5789">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5789">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5790">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5790">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5791">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5791">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5792">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5792">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5793">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5793">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5795">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5795">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5796">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5796">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-5797">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5797">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-5798">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5798">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5800">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="b648e-5801">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="b648e-5801">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="b648e-5802">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5802">Target</span></span> | <span data-ttu-id="b648e-5803">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5803">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5804">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5805">32</span><span class="sxs-lookup"><span data-stu-id="b648e-5805">32</span></span> |
| <span data-ttu-id="b648e-5806">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5806">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5808">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5808">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5810">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5810">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5812">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5812">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5813">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5813">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5814">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5814">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5816">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5816">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5818">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5818">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5820">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5820">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5822">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5822">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5824">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5824">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5826">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5826">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5827">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5827">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5828">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5828">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5829">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5829">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5830">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5830">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5832">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5832">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5834">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5834">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5836">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5836">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5838">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5839">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5840">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5841">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5842">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5843">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5844">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5845">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5846">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5847">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5848">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5849">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5850">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5851">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5851">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5853">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5853">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5855">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5855">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5857">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5857">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5859">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5859">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5861">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5861">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5863">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5863">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5865">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5865">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5867">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5867">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5868">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5868">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5870">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5870">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5872">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5872">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5874">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5874">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="b648e-5875">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="b648e-5875">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="b648e-5876">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5876">Target</span></span> | <span data-ttu-id="b648e-5877">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5877">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5878">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5878">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5879">32</span><span class="sxs-lookup"><span data-stu-id="b648e-5879">32</span></span> |
| <span data-ttu-id="b648e-5880">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5880">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5882">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5882">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5883">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5883">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5884">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5885">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5886">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5888">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5890">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5892">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5894">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5894">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5896">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5896">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5898">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5898">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5899">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5899">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5900">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5900">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5901">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5901">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5902">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5902">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5904">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5904">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5906">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5906">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5908">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5908">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5910">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5910">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5911">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5911">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5912">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5912">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5913">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5913">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5914">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5914">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5915">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5915">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5916">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5916">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5917">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5917">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5918">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5918">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5919">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5919">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5920">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5920">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5921">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5921">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5922">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5922">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5923">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5923">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5925">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5925">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5927">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5927">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5929">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5929">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5931">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5931">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5933">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5933">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5935">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5935">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5937">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5937">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5939">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5939">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-5940">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5940">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5942">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-5942">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-5944">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-5944">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5946">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-5946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="b648e-5947">DXGI_FORMAT_B8G8R8X8 \_ <sup>PC</sup> non con tipi (92)</span><span class="sxs-lookup"><span data-stu-id="b648e-5947">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="b648e-5948">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5948">Target</span></span> | <span data-ttu-id="b648e-5949">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-5949">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-5950">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-5950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-5951">32</span><span class="sxs-lookup"><span data-stu-id="b648e-5951">32</span></span> |
| <span data-ttu-id="b648e-5952">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-5952">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5954">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-5954">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5955">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-5955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5956">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-5956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5957">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-5957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-5958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-5958">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-5960">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-5962">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-5964">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5966">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-5966">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-5967">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-5967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-5968">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-5968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-5969">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-5969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-5970">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-5970">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-5971">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-5971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-5972">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5972">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5974">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-5974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-5975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-5975">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5976">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-5976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5977">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-5977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-5978">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-5978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-5979">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-5979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5980">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-5980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-5981">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-5981">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-5982">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-5983">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-5984">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-5985">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-5986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-5986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-5987">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-5988">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-5988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5989">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-5989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-5990">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-5990">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-5992">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-5992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5993">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-5993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-5994">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-5994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-5995">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-5996">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-5996">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-5997">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-5997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-5998">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-5998">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6000">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-6001">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-6002">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-6003">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6003">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6005">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="b648e-6006">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="b648e-6006">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="b648e-6007">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6007">Target</span></span> | <span data-ttu-id="b648e-6008">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6008">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6009">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6010">32</span><span class="sxs-lookup"><span data-stu-id="b648e-6010">32</span></span> |
| <span data-ttu-id="b648e-6011">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6011">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6013">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6013">Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6015">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6015">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6017">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6018">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6019">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6021">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6023">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6025">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6027">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6027">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6029">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6029">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6031">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6032">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6033">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6033">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-6034">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6035">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6037">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6037">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6039">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6041">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6041">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6043">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6044">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6045">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6046">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6047">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6047">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6048">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6049">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6050">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6051">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6053">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6054">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6055">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6056">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6056">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6058">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6058">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6060">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6060">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6062">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6062">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6064">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6064">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6066">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6066">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6068">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6068">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6069">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6069">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6071">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-6072">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6072">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6074">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6074">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6076">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6076">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6078">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6078">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="b648e-6079">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="b648e-6079">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="b648e-6080">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6080">Target</span></span> | <span data-ttu-id="b648e-6081">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6081">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6082">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6082">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6083">32</span><span class="sxs-lookup"><span data-stu-id="b648e-6083">32</span></span> |
| <span data-ttu-id="b648e-6084">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6084">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6086">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6086">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6087">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6087">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6088">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6088">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6089">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6089">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6090">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6090">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6092">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6092">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6094">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6094">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6096">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6096">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6098">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6098">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6100">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6100">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6102">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6102">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6103">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6103">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6104">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6104">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-6105">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6105">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6106">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6106">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6108">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6108">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6110">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6110">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6112">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6112">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6114">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6115">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6116">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6117">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6118">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6118">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6119">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6120">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6121">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6122">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6124">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6125">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6126">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6127">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6127">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6129">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6129">4x Multisample RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6131">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6131">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6133">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6133">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6135">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6135">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6137">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6137">Multisample Load</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6139">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6139">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6140">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6140">Cast Within Bit Layout</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6142">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6142">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-6143">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6143">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-6144">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6144">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-6145">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6145">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6147">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="b648e-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="b648e-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="b648e-6149">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6149">Target</span></span> | <span data-ttu-id="b648e-6150">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6150">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6151">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6152">32</span><span class="sxs-lookup"><span data-stu-id="b648e-6152">32</span></span> |
| <span data-ttu-id="b648e-6153">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6153">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6155">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6155">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6156">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6157">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6158">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6159">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6160">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6162">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6163">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6164">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6164">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6166">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6166">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6168">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6168">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6169">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6169">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6170">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6170">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6172">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6173">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6173">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6175">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6175">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6177">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6177">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6179">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6179">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6181">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6181">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6182">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6182">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6183">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6183">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6184">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6184">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6185">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6185">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6186">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6186">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6187">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6187">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6188">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6188">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6189">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6189">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6190">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6190">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6191">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6191">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6192">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6192">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6193">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6193">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6194">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6194">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6196">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6196">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6197">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6197">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6198">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6198">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6199">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6199">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6200">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6200">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6201">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6201">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6202">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6202">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6203">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6203">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6205">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6205">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6207">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6207">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6209">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6209">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6211">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6211">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="b648e-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="b648e-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="b648e-6213">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6213">Target</span></span> | <span data-ttu-id="b648e-6214">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6214">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6215">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6215">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6216">32</span><span class="sxs-lookup"><span data-stu-id="b648e-6216">32</span></span> |
| <span data-ttu-id="b648e-6217">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6217">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6219">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6219">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6220">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6220">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6221">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6221">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6222">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6222">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6223">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6223">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6224">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6226">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6227">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6227">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6228">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6228">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6230">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6230">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6232">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6232">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6233">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6233">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6234">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6234">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6236">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6236">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6237">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6237">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6238">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6238">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6239">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6239">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6240">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6240">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6241">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6241">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6242">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6242">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6243">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6243">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6244">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6244">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6245">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6245">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6246">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6246">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6247">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6247">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6248">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6248">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6249">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6249">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6250">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6250">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6251">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6251">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6252">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6252">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6253">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6253">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6254">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6254">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6256">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6256">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6257">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6257">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6258">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6258">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6259">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6259">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6260">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6260">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6261">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6261">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6262">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6262">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6263">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6263">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6265">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6265">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6267">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6267">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6269">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6269">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6271">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="b648e-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="b648e-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="b648e-6273">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6273">Target</span></span> | <span data-ttu-id="b648e-6274">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6274">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6275">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6276">64</span><span class="sxs-lookup"><span data-stu-id="b648e-6276">64</span></span> |
| <span data-ttu-id="b648e-6277">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6277">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6279">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6279">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6280">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6281">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6282">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6283">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6284">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6286">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6286">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6287">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6288">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6288">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6290">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6290">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6292">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6293">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6294">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6294">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6296">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6297">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6297">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6299">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6300">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6301">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6302">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6303">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6304">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6305">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6306">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6306">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6307">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6308">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6309">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6310">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6312">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6313">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6314">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6315">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6315">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6317">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6318">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6319">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6320">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6321">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6321">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6322">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6323">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6324">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6324">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6326">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6326">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6328">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6328">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6330">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6330">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6332">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6332">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="b648e-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="b648e-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="b648e-6334">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6334">Target</span></span> | <span data-ttu-id="b648e-6335">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6335">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6336">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6336">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6337">8</span><span class="sxs-lookup"><span data-stu-id="b648e-6337">8</span></span> |
| <span data-ttu-id="b648e-6338">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6338">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6340">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6340">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6341">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6341">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6342">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6342">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6343">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6343">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6344">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6344">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6345">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6345">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6347">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6348">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6349">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6349">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6351">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6351">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6353">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6353">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6354">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6354">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6355">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6355">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6357">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6357">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6358">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6358">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6359">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6359">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6360">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6360">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6362">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6362">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6364">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6364">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6365">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6365">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6366">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6366">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6367">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6367">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6368">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6368">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6369">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6369">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6370">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6370">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6371">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6371">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6372">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6372">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6373">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6373">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6374">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6374">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6375">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6375">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6376">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6376">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6377">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6377">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6379">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6380">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6381">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6382">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6383">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6383">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6384">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6385">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6386">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6386">Video Decoder Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6388">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6388">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6390">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6390">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6392">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6392">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6394">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6394">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="b648e-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="b648e-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="b648e-6396">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6396">Target</span></span> | <span data-ttu-id="b648e-6397">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6397">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6398">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6398">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6399">16</span><span class="sxs-lookup"><span data-stu-id="b648e-6399">16</span></span> |
| <span data-ttu-id="b648e-6400">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6400">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6402">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6402">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6403">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6403">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6404">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6404">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6405">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6405">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6406">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6406">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6407">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6407">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6409">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6409">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6410">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6411">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6411">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6413">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6413">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6415">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6415">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6416">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6416">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6417">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6417">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6419">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6420">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6420">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6421">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6422">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6424">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6424">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6426">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6427">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6428">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6429">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6430">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6430">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6431">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6432">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6433">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6434">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6436">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6437">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6438">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6439">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6439">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6441">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6441">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6442">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6442">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6443">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6443">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6444">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6444">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6445">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6445">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6446">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6446">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6447">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6447">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6448">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6448">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6450">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6450">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6452">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6452">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6454">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6454">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6456">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="b648e-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="b648e-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="b648e-6458">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6458">Target</span></span> | <span data-ttu-id="b648e-6459">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6459">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6460">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6461">16</span><span class="sxs-lookup"><span data-stu-id="b648e-6461">16</span></span> |
| <span data-ttu-id="b648e-6462">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6462">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6464">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6464">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6465">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6466">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6467">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6468">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6469">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6469">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6471">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6471">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6472">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6472">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6473">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6473">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6475">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6475">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6477">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6477">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6478">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6478">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6479">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6479">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6481">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6481">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6482">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6482">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6483">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6483">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6484">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6484">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6486">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6486">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6488">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6488">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6489">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6489">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6490">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6490">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6491">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6491">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6492">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6492">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6493">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6493">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6494">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6494">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6495">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6495">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6496">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6496">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6497">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6497">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6498">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6498">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6499">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6499">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6500">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6500">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6501">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6501">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6503">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6503">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6504">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6504">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6505">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6505">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6506">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6507">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6507">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6508">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6508">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6509">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6509">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6510">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6510">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6512">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6512">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6514">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6514">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6516">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6516">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6518">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6518">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="b648e-6519">DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="b648e-6519">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="b648e-6520">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6520">Target</span></span> | <span data-ttu-id="b648e-6521">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6521">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6522">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6522">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6523">8</span><span class="sxs-lookup"><span data-stu-id="b648e-6523">8</span></span> |
| <span data-ttu-id="b648e-6524">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6524">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6526">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6526">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6527">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6527">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6528">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6529">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6530">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6531">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6531">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6533">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6533">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6534">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6534">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6535">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6535">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-6536">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6536">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-6537">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6537">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6538">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6538">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6539">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6539">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-6540">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6540">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6541">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6541">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6542">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6542">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6543">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6543">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6544">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6544">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6545">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6545">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6546">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6546">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6547">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6547">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6548">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6548">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6549">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6549">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6550">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6550">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6551">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6551">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6552">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6552">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6553">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6553">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6554">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6554">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6555">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6555">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6556">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6556">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6557">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6557">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6558">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6558">CPU Lockable</span></span> | \- |
| <span data-ttu-id="b648e-6559">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6559">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6560">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6560">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6561">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6561">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6562">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6562">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6563">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6563">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6564">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6564">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6565">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6565">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6566">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6566">Video Decoder Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6568">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6568">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6570">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6570">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6572">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6572">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6574">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6574">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="b648e-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="b648e-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="b648e-6576">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6576">Target</span></span> | <span data-ttu-id="b648e-6577">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6577">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6578">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6578">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6579">16</span><span class="sxs-lookup"><span data-stu-id="b648e-6579">16</span></span> |
| <span data-ttu-id="b648e-6580">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6580">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6582">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6582">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6583">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6583">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6584">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6584">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6585">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6585">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6586">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6586">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6587">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6589">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6590">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6591">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6591">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6593">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6593">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6595">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6595">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6596">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6596">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6597">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6597">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6599">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6600">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6601">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6601">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6602">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6602">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6603">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6603">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6604">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6604">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6605">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6605">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6606">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6606">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6607">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6607">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6608">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6608">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6609">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6609">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6610">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6610">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6611">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6611">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6612">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6612">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6613">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6613">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6614">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6614">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6615">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6615">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6616">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6616">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6617">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6617">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6619">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6619">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6620">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6620">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6621">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6621">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6622">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6622">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6623">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6623">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6624">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6624">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6625">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6625">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6626">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6626">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6628">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6628">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6630">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6630">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6632">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6632">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6634">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6634">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="b648e-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="b648e-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="b648e-6636">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6636">Target</span></span> | <span data-ttu-id="b648e-6637">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6637">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6638">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6638">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6639">32</span><span class="sxs-lookup"><span data-stu-id="b648e-6639">32</span></span> |
| <span data-ttu-id="b648e-6640">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6640">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6642">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6642">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6643">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6643">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6644">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6644">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6645">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6645">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6646">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6646">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6647">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6647">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6649">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6649">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6650">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6650">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6651">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6651">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6653">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6653">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6655">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6655">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6656">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6656">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6657">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6657">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6659">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6659">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6660">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6660">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6661">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6661">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6662">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6662">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6663">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6663">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6664">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6664">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6665">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6665">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6666">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6666">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6667">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6667">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6668">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6668">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6669">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6669">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6670">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6670">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6671">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6671">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6672">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6672">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6673">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6673">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6674">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6674">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6675">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6675">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6676">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6676">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6677">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6677">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6679">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6679">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6680">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6680">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6681">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6681">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6682">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6682">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6683">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6683">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6684">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6684">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6685">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6685">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6686">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6686">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6688">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6688">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6690">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6690">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6692">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6692">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6694">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="b648e-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="b648e-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="b648e-6696">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6696">Target</span></span> | <span data-ttu-id="b648e-6697">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6697">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6698">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6699">32</span><span class="sxs-lookup"><span data-stu-id="b648e-6699">32</span></span> |
| <span data-ttu-id="b648e-6700">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6700">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6702">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6702">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6703">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6703">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6704">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6705">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6706">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6707">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6707">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6709">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6709">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6710">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6710">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6711">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6711">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6713">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6713">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6715">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6715">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6716">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6716">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6717">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6717">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6719">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6719">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6720">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6720">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6721">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6721">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6722">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6722">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6723">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6723">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6724">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6724">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6725">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6725">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6726">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6726">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6727">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6727">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6728">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6728">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6729">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6729">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6730">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6730">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6731">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6731">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6732">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6732">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6733">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6733">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6734">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6734">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6735">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6735">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6736">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6736">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6737">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6737">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6739">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6740">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6741">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6742">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6743">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6743">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6744">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6745">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6746">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6746">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6748">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6748">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6750">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6750">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6752">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6752">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6754">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6754">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="b648e-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="b648e-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="b648e-6756">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6756">Target</span></span> | <span data-ttu-id="b648e-6757">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6757">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6758">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6758">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6759">8</span><span class="sxs-lookup"><span data-stu-id="b648e-6759">8</span></span> |
| <span data-ttu-id="b648e-6760">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6760">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6762">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6762">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6763">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6763">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6764">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6764">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6765">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6765">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6766">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6766">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6767">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6769">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6770">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6771">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6771">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6773">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6773">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6775">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6775">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6776">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6776">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6777">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6777">Shader gather4</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6779">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6780">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6781">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6782">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6784">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6784">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6786">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6787">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6788">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6789">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6790">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6790">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6791">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6792">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6793">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6794">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6795">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6796">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6797">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6798">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6799">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6799">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6801">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6801">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6802">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6802">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6803">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6803">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6804">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6805">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6805">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6806">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6807">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6807">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6808">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6808">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6810">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6810">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6812">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6812">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6814">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6814">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6816">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6816">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="b648e-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="b648e-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="b648e-6818">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6818">Target</span></span> | <span data-ttu-id="b648e-6819">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6819">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6820">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6820">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6821">8</span><span class="sxs-lookup"><span data-stu-id="b648e-6821">8</span></span> |
| <span data-ttu-id="b648e-6822">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6822">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6824">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6824">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6825">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6825">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6826">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6826">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6827">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6827">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6828">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6828">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6829">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6829">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6831">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6831">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6832">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6832">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6833">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6833">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-6834">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6834">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-6835">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6835">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6836">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6836">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6837">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6837">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-6838">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6838">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6839">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6839">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6840">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6840">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6842">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6843">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6844">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6845">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6846">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6847">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6848">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6849">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6850">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6851">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6852">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6852">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6853">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6854">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6854">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6855">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6855">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6856">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6856">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6858">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6859">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6860">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6861">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6862">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6863">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6864">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6864">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6865">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6865">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-6866">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6866">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6868">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-6869">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-6870">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6870">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="b648e-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="b648e-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="b648e-6872">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6872">Target</span></span> | <span data-ttu-id="b648e-6873">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6873">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6874">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6875">8</span><span class="sxs-lookup"><span data-stu-id="b648e-6875">8</span></span> |
| <span data-ttu-id="b648e-6876">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6876">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6878">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6878">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6879">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6880">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6881">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6882">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6883">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6885">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6886">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6886">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6887">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6887">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-6888">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6888">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-6889">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6889">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6890">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6890">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6891">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6891">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-6892">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6892">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6893">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6893">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6894">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6895">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6896">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6897">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6898">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6899">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6900">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6901">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6901">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6902">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6903">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6904">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6905">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6906">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6907">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6908">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6909">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6910">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6910">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6912">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6913">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6914">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6915">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6916">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6916">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6917">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6918">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6919">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-6920">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6920">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6922">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6922">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-6923">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6923">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-6924">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6924">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="b648e-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="b648e-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="b648e-6926">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6926">Target</span></span> | <span data-ttu-id="b648e-6927">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6927">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6928">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6928">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6929">8</span><span class="sxs-lookup"><span data-stu-id="b648e-6929">8</span></span> |
| <span data-ttu-id="b648e-6930">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6930">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6932">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6932">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6933">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6933">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6934">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6934">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6935">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6935">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6936">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6936">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6937">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6937">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6939">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6939">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6940">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6940">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6941">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6941">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-6942">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6942">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-6943">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6943">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6944">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6944">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6945">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6945">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-6946">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-6946">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-6947">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6947">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-6948">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-6948">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-6949">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-6949">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6950">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-6950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6951">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-6951">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-6952">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6952">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-6953">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-6953">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6954">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-6954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-6955">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-6955">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-6956">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-6957">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-6958">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-6959">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-6960">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-6960">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-6961">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-6962">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-6962">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6963">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-6963">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-6964">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-6964">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6966">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-6966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6967">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-6967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-6968">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-6968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-6969">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-6970">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-6970">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-6971">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-6971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-6972">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-6972">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-6973">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6973">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-6974">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6974">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6976">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-6976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-6977">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-6977">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-6978">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-6978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="b648e-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="b648e-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="b648e-6980">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-6980">Target</span></span> | <span data-ttu-id="b648e-6981">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-6981">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-6982">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-6982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-6983">16</span><span class="sxs-lookup"><span data-stu-id="b648e-6983">16</span></span> |
| <span data-ttu-id="b648e-6984">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-6984">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-6986">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-6986">Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6987">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-6987">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6988">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-6988">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6989">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-6989">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-6990">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-6990">Texture1D</span></span> | \- |
| <span data-ttu-id="b648e-6991">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-6991">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-6993">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-6993">Texture3D</span></span> | \- |
| <span data-ttu-id="b648e-6994">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-6994">TextureCube</span></span> | \- |
| <span data-ttu-id="b648e-6995">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-6995">Shader ld</span></span> | \- |
| <span data-ttu-id="b648e-6996">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-6996">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="b648e-6997">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-6997">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-6998">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-6998">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-6999">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-6999">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-7000">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-7000">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-7001">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-7001">Mipmap</span></span> | \- |
| <span data-ttu-id="b648e-7002">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-7002">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="b648e-7003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-7003">RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-7004">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-7004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-7005">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-7005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-7006">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-7006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-7007">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-7007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-7008">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-7008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-7009">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-7009">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-7010">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-7011">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-7012">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-7013">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-7014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-7014">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-7015">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-7016">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-7017">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-7017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-7018">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-7018">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7020">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-7020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-7021">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-7021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="b648e-7022">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-7022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="b648e-7023">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-7023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="b648e-7024">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-7024">Multisample Load</span></span> | \- |
| <span data-ttu-id="b648e-7025">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-7025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-7026">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-7026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-7027">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-7027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-7028">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-7028">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7030">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-7030">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-7031">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-7031">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-7032">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-7032">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="b648e-7033">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="b648e-7033">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="b648e-7034">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-7034">Target</span></span> | <span data-ttu-id="b648e-7035">Supporto</span><span class="sxs-lookup"><span data-stu-id="b648e-7035">Support</span></span> |
| - | - |
| <span data-ttu-id="b648e-7036">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="b648e-7036">Bits Per Element (BPE)</span></span> | <span data-ttu-id="b648e-7037">16</span><span class="sxs-lookup"><span data-stu-id="b648e-7037">16</span></span> |
| <span data-ttu-id="b648e-7038">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="b648e-7038">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7040">Buffer</span><span class="sxs-lookup"><span data-stu-id="b648e-7040">Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-7042">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="b648e-7042">Input Assembler Vertex Buffer</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-7044">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="b648e-7044">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="b648e-7045">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="b648e-7045">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="b648e-7046">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b648e-7046">Texture1D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b648e-7048">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b648e-7050">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b648e-7052">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7054">LD shader</span><span class="sxs-lookup"><span data-stu-id="b648e-7054">Shader ld</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7056">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="b648e-7056">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7058">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="b648e-7058">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="b648e-7059">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="b648e-7059">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="b648e-7060">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="b648e-7060">Shader gather4</span></span> | \- |
| <span data-ttu-id="b648e-7061">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="b648e-7061">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="b648e-7062">Mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-7062">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7064">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="b648e-7064">Mipmap Auto-Generation</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-7066">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="b648e-7066">RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-7068">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="b648e-7068">Blendable RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-7070">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="b648e-7070">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="b648e-7071">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="b648e-7071">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="b648e-7072">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="b648e-7072">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-7073">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="b648e-7073">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="b648e-7074">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-7074">Typed UAV</span></span> | \- |
| <span data-ttu-id="b648e-7075">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7075">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="b648e-7076">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7076">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="b648e-7077">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7077">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="b648e-7078">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7078">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="b648e-7079">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="b648e-7079">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="b648e-7080">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7080">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="b648e-7081">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="b648e-7081">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-7082">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="b648e-7082">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="b648e-7083">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="b648e-7083">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7085">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="b648e-7085">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-7087">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="b648e-7087">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-7089">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="b648e-7089">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-7091">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-7091">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="b648e-7093">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="b648e-7093">Multisample Load</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="b648e-7095">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="b648e-7095">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="b648e-7096">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="b648e-7096">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="b648e-7097">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="b648e-7097">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="b648e-7098">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-7098">Video Processor Input</span></span> | \- |
| <span data-ttu-id="b648e-7099">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="b648e-7099">Video Processor Output</span></span> | \- |
| <span data-ttu-id="b648e-7100">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="b648e-7100">Shared Resource</span></span> | \- |
| <span data-ttu-id="b648e-7101">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="b648e-7101">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="b648e-7102">Note sul formato</span><span class="sxs-lookup"><span data-stu-id="b648e-7102">Format notes</span></span>

<span data-ttu-id="b648e-7103">Lo scopo del formato può variare da un livello di funzionalità hardware a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="b648e-7103">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="b648e-7104"><sup>L</sup> : formato non tipizzato</span><span class="sxs-lookup"><span data-stu-id="b648e-7104"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="b648e-7105"><sup>PC</sup> : layout parzialmente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="b648e-7105"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="b648e-7106"><sup>FCS</sup> : layout completamente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="b648e-7106"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="b648e-7107"><sup>FNS</sup> : layout completamente tipizzato, non ristabile e semplice</span><span class="sxs-lookup"><span data-stu-id="b648e-7107"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="b648e-7108"><sup>PCC</sup> : layout parzialmente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="b648e-7108"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="b648e-7109"><sup>FCC</sup> : layout completamente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="b648e-7109"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="b648e-7110"><sup>FNC</sup> : layout completamente tipizzato, non ristabile e complesso</span><span class="sxs-lookup"><span data-stu-id="b648e-7110"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="b648e-7111"><sup>V</sup> : formato video</span><span class="sxs-lookup"><span data-stu-id="b648e-7111"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="b648e-7112">I buffer indietro e le analisi con il [**formato \_ DXGI \_ R16G16B16A16 \_ float**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) contengono dati gamma con valori lineari.</span><span class="sxs-lookup"><span data-stu-id="b648e-7112">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b648e-7113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b648e-7113">Related topics</span></span>

[<span data-ttu-id="b648e-7114">Livelli di funzionalità hardware D3D12</span><span class="sxs-lookup"><span data-stu-id="b648e-7114">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="b648e-7115">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="b648e-7115">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="b648e-7116">Guida per programmatori per DXGI</span><span class="sxs-lookup"><span data-stu-id="b648e-7116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
