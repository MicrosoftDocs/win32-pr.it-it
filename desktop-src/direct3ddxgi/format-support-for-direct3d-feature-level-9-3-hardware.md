---
description: Questa sezione specifica i formati ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware 10Level9 9,3 della funzionalità Direct3D.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Supporto del formato per l'hardware a livello di funzionalità 10Level9 9.3 di Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79185ddb360fe9359371671e3722372c3a1615f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048920"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a><span data-ttu-id="73228-103">Supporto del formato per l'hardware a livello di funzionalità 10Level9 9.3 di Direct3D</span><span class="sxs-lookup"><span data-stu-id="73228-103">Format support for Direct3D Feature 10Level9 9.3 hardware</span></span>

<span data-ttu-id="73228-104">Questa sezione specifica i formati ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nella funzionalità Direct3D 10Level9 9,3 hardware.</span><span class="sxs-lookup"><span data-stu-id="73228-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.3 hardware.</span></span>

<span data-ttu-id="73228-105">La tabella riepiloga il supporto della funzionalità, usando la chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="73228-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="73228-106">Simbolo</span><span class="sxs-lookup"><span data-stu-id="73228-106">Symbol</span></span>                            | <span data-ttu-id="73228-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73228-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="73228-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="73228-108">_ *-*\*</span></span>                             | <span data-ttu-id="73228-109">Non consentito o non disponibile.</span><span class="sxs-lookup"><span data-stu-id="73228-109">Disallowed or not available.</span></span>                                                  |
| ![necessario](images/letter-r.jpg)  | <span data-ttu-id="73228-111">Il supporto hardware è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="73228-111">Hardware support is required.</span></span>                                                 |
| ![facoltative](images/letter-o.jpg)  | <span data-ttu-id="73228-113">Supporto hardware facoltativo. il formato potrebbe essere accelerato o meno.</span><span class="sxs-lookup"><span data-stu-id="73228-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dipendenti](images/letter-d.jpg) | <span data-ttu-id="73228-115">Obbligatorio se è supportata la funzionalità facoltativa correlata.</span><span class="sxs-lookup"><span data-stu-id="73228-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="73228-116">Questo argomento contiene una sezione per formato.</span><span class="sxs-lookup"><span data-stu-id="73228-116">This topic contains a section per format.</span></span> <span data-ttu-id="73228-117">Una *destinazione* del formato (le tabelle contengono una riga per destinazione) può essere un tipo di risorsa, una funzione intrinseca HLSL o una particolare funzionalità che dipende da un particolare formato.</span><span class="sxs-lookup"><span data-stu-id="73228-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="73228-118">Per verificare a livello di codice il supporto del formato in D3D11 e D3D12, vedere [controllo della funzionalità hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="73228-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="73228-119">Il numero di formati è prevalentemente, ma non tutti, in ordine numerico crescente &mdash; alcuni sono fuori dall'ordine numerico ed elencati insieme ad altri formati pertinenti.</span><span class="sxs-lookup"><span data-stu-id="73228-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="73228-120">Si noti anche che il *tipo* in un nome di formato può indicare *parzialmente* tipizzato e non esclusivamente senza tipo (fare riferimento alla sezione [Note sul formato](#format-notes) alla fine dell'argomento).</span><span class="sxs-lookup"><span data-stu-id="73228-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="73228-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="73228-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="73228-122">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-122">Target</span></span> | <span data-ttu-id="73228-123">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-123">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-124">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-125">0</span><span class="sxs-lookup"><span data-stu-id="73228-125">0</span></span> |
| <span data-ttu-id="73228-126">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-126">Format Support</span></span> | \- |
| <span data-ttu-id="73228-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-127">Buffer</span></span> | \- |
| <span data-ttu-id="73228-128">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-129">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-130">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-131">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-132">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-133">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-134">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-135">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-136">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-137">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-138">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-139">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-140">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-141">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-142">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-144">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-145">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-146">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-147">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-148">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-149">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-150">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-151">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-152">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-153">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-155">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-156">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-157">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-158">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-159">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-160">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-161">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-162">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-163">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-164">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-165">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-166">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-167">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-168">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-169">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-170">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="73228-171">DXGI_FORMAT_R32G32B32A32 \_ <sup>PC</sup> non con tipi (1)</span><span class="sxs-lookup"><span data-stu-id="73228-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="73228-172">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-172">Target</span></span> | <span data-ttu-id="73228-173">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-173">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-174">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-175">128</span><span class="sxs-lookup"><span data-stu-id="73228-175">128</span></span> |
| <span data-ttu-id="73228-176">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-176">Format Support</span></span> | \- |
| <span data-ttu-id="73228-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-177">Buffer</span></span> | \- |
| <span data-ttu-id="73228-178">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-179">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-180">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-181">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-182">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-183">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-184">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-185">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-186">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-187">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-188">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-189">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-190">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-191">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-191">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-192">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-194">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-195">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-196">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-197">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-198">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-199">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-200">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-201">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-202">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-203">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-205">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-206">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-207">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-208">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-209">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-210">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-211">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-212">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-213">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-214">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-215">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-216">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-217">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-218">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-219">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-220">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="73228-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="73228-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="73228-222">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-222">Target</span></span> | <span data-ttu-id="73228-223">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-223">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-224">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-225">128</span><span class="sxs-lookup"><span data-stu-id="73228-225">128</span></span> |
| <span data-ttu-id="73228-226">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-226">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-228">Buffer</span></span> | \- |
| <span data-ttu-id="73228-229">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-229">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-231">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-232">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-233">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-234">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-236">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-236">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-238">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-238">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-240">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-240">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-242">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-242">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-243">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-243">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-244">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-244">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-245">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-245">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-246">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-246">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-247">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-247">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-249">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-249">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-251">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-253">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-253">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-254">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-254">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-255">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-255">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-256">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-256">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-257">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-257">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-258">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-258">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-259">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-259">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-260">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-260">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-261">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-261">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-262">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-262">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-263">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-263">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-264">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-264">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-265">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-265">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-266">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-266">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-267">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-267">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-269">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-269">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-271">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-271">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-273">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-273">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-275">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-275">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-277">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-277">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-278">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-278">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-279">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-279">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-280">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-281">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-282">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-283">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-283">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-284">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-284">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="73228-285">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="73228-285">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="73228-286">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-286">Target</span></span> | <span data-ttu-id="73228-287">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-287">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-288">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-288">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-289">128</span><span class="sxs-lookup"><span data-stu-id="73228-289">128</span></span> |
| <span data-ttu-id="73228-290">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-290">Format Support</span></span> | \- |
| <span data-ttu-id="73228-291">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-291">Buffer</span></span> | \- |
| <span data-ttu-id="73228-292">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-292">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-293">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-293">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-294">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-294">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-295">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-295">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-296">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-296">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-297">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-297">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-298">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-298">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-299">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-299">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-300">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-300">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-301">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-301">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-302">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-302">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-303">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-303">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-304">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-304">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-305">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-305">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-306">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-306">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-307">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-307">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-308">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-308">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-309">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-309">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-310">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-310">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-311">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-311">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-312">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-312">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-313">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-313">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-314">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-314">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-315">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-315">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-316">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-316">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-317">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-317">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-318">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-318">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-319">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-319">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-320">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-320">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-321">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-321">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-322">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-322">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-323">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-323">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-324">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-324">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-325">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-325">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-326">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-327">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-327">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-328">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-328">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-329">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-329">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-330">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-331">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-332">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-333">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-333">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-334">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-334">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="73228-335">DXGI_FORMAT_R32G32B32A32 \_ Sint<sup>FNS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="73228-335">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="73228-336">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-336">Target</span></span> | <span data-ttu-id="73228-337">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-337">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-338">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-338">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-339">128</span><span class="sxs-lookup"><span data-stu-id="73228-339">128</span></span> |
| <span data-ttu-id="73228-340">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-340">Format Support</span></span> | \- |
| <span data-ttu-id="73228-341">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-341">Buffer</span></span> | \- |
| <span data-ttu-id="73228-342">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-342">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-343">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-343">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-344">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-344">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-345">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-345">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-346">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-346">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-347">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-348">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-349">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-349">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-350">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-350">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-351">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-351">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-352">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-352">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-353">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-353">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-354">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-354">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-355">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-355">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-356">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-356">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-357">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-357">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-358">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-358">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-359">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-360">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-361">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-362">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-363">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-363">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-364">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-365">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-366">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-367">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-369">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-370">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-371">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-372">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-372">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-373">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-373">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-374">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-374">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-375">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-375">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-376">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-377">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-377">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-378">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-378">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-379">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-379">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-380">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-380">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-381">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-381">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-382">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-382">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-383">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-383">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-384">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-384">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="73228-385">DXGI_FORMAT_R32G32B32 i \_ <sup>PC</sup> con tipi (5)</span><span class="sxs-lookup"><span data-stu-id="73228-385">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="73228-386">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-386">Target</span></span> | <span data-ttu-id="73228-387">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-387">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-388">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-388">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-389">96</span><span class="sxs-lookup"><span data-stu-id="73228-389">96</span></span> |
| <span data-ttu-id="73228-390">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-390">Format Support</span></span> | \- |
| <span data-ttu-id="73228-391">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-391">Buffer</span></span> | \- |
| <span data-ttu-id="73228-392">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-392">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-393">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-394">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-394">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-395">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-395">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-396">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-396">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-397">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-397">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-398">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-399">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-399">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-400">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-401">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-402">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-403">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-403">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-404">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-405">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-406">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-407">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-408">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-409">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-410">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-411">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-412">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-413">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-414">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-415">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-416">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-417">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-418">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-419">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-420">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-421">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-422">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-422">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-423">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-424">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-425">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-426">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-427">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-427">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-428">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-429">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-429">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-430">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-430">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-431">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-431">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-432">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-432">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-433">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-433">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-434">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-434">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="73228-435">DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="73228-435">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="73228-436">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-436">Target</span></span> | <span data-ttu-id="73228-437">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-437">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-438">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-439">96</span><span class="sxs-lookup"><span data-stu-id="73228-439">96</span></span> |
| <span data-ttu-id="73228-440">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-440">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-442">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-442">Buffer</span></span> | \- |
| <span data-ttu-id="73228-443">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-443">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-445">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-446">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-447">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-448">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-449">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-450">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-451">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-452">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-453">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-454">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-455">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-455">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-456">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-457">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-458">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-459">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-460">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-460">Blendable RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="73228-462">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-462">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-463">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-463">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-464">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-464">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-465">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-465">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-466">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-466">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-467">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-467">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-468">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-468">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-469">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-469">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-470">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-470">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-471">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-471">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-472">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-472">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-473">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-473">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-474">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-474">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-475">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-475">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-476">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-476">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="73228-478">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-478">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="73228-480">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-481">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-482">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-482">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-483">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-484">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-485">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-486">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-487">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-488">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-488">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-489">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="73228-490">DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="73228-490">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="73228-491">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-491">Target</span></span> | <span data-ttu-id="73228-492">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-492">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-493">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-494">96</span><span class="sxs-lookup"><span data-stu-id="73228-494">96</span></span> |
| <span data-ttu-id="73228-495">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-495">Format Support</span></span> | \- |
| <span data-ttu-id="73228-496">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-496">Buffer</span></span> | \- |
| <span data-ttu-id="73228-497">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-498">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-499">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-500">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-501">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-502">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-503">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-504">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-505">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-506">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-507">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-508">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-508">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-509">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-510">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-511">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-512">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-513">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-514">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-515">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-516">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-517">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-518">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-518">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-519">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-520">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-521">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-522">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-524">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-525">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-526">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-527">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-528">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-528">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="73228-530">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-530">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="73228-532">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-533">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-534">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-534">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-535">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-536">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-537">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-538">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-539">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-540">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-540">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-541">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="73228-542">DXGI_FORMAT_R32G32B32 \_ Sint<sup>FNS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="73228-542">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="73228-543">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-543">Target</span></span> | <span data-ttu-id="73228-544">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-544">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-545">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-546">96</span><span class="sxs-lookup"><span data-stu-id="73228-546">96</span></span> |
| <span data-ttu-id="73228-547">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-547">Format Support</span></span> | \- |
| <span data-ttu-id="73228-548">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-548">Buffer</span></span> | \- |
| <span data-ttu-id="73228-549">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-550">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-551">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-552">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-553">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-554">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-555">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-556">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-557">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-558">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-559">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-560">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-560">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-561">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-562">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-563">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-564">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-565">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-566">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-567">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-568">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-569">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-570">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-570">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-571">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-572">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-573">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-574">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-576">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-577">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-578">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-579">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-580">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-580">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="73228-582">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-582">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="73228-584">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-585">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-586">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-586">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-587">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-588">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-589">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-590">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-591">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-592">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-593">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-593">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="73228-594">DXGI_FORMAT_R16G16B16A16 \_ <sup>PC</sup> non con tipi (9)</span><span class="sxs-lookup"><span data-stu-id="73228-594">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="73228-595">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-595">Target</span></span> | <span data-ttu-id="73228-596">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-596">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-597">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-597">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-598">64</span><span class="sxs-lookup"><span data-stu-id="73228-598">64</span></span> |
| <span data-ttu-id="73228-599">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-599">Format Support</span></span> | \- |
| <span data-ttu-id="73228-600">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-600">Buffer</span></span> | \- |
| <span data-ttu-id="73228-601">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-601">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-602">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-603">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-604">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-605">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-605">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-606">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-606">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-607">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-608">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-608">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-609">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-610">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-611">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-612">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-612">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-613">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-614">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-614">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-615">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-615">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-616">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-616">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-617">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-617">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-618">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-618">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-619">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-619">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-620">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-620">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-621">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-621">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-622">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-622">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-623">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-623">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-624">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-624">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-625">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-625">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-626">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-626">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-627">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-627">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-628">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-628">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-629">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-629">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-630">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-630">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-631">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-631">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-632">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-632">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-633">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-633">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-634">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-634">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-635">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-635">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-636">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-636">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-637">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-637">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-638">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-638">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-639">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-639">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-640">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-640">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-641">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-641">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-642">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-642">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-643">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-643">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="73228-644">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="73228-644">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="73228-645">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-645">Target</span></span> | <span data-ttu-id="73228-646">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-646">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-647">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-647">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-648">64</span><span class="sxs-lookup"><span data-stu-id="73228-648">64</span></span> |
| <span data-ttu-id="73228-649">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-649">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-651">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-651">Buffer</span></span> | \- |
| <span data-ttu-id="73228-652">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-652">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-654">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-654">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-655">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-655">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-656">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-656">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-657">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-657">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-659">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-659">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-661">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-663">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-663">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-665">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-665">Shader sample (any filter)</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-667">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-668">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-669">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-669">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-670">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-671">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-671">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-673">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-673">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-675">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-677">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-677">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-679">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-679">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-680">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-680">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-681">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-681">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-682">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-682">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-683">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-683">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-684">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-684">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-685">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-685">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-686">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-686">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-687">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-687">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-688">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-688">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-689">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-689">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-690">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-690">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-691">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-691">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-692">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-692">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-694">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-694">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-696">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-696">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-698">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-698">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-700">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-700">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-702">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-702">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-703">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-703">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-704">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-704">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-705">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-706">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-707">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-708">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-708">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-710">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="73228-711">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="73228-711">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="73228-712">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-712">Target</span></span> | <span data-ttu-id="73228-713">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-713">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-714">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-715">64</span><span class="sxs-lookup"><span data-stu-id="73228-715">64</span></span> |
| <span data-ttu-id="73228-716">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-716">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-718">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-718">Buffer</span></span> | \- |
| <span data-ttu-id="73228-719">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-719">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-720">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-720">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-721">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-721">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-722">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-722">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-723">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-723">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-725">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-725">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-727">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-727">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-729">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-729">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-731">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-731">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-733">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-733">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-734">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-734">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-735">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-735">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-736">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-736">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-737">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-737">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-739">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-739">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-741">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-741">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-743">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-744">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-745">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-746">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-747">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-748">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-748">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-749">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-750">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-751">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-752">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-754">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-755">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-756">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-757">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-757">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-759">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-759">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-761">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-761">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-763">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-763">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-765">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-765">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-767">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-767">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-768">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-768">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-769">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-769">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-770">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-770">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-771">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-771">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-772">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-772">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-773">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-773">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-774">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-774">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="73228-775">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="73228-775">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="73228-776">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-776">Target</span></span> | <span data-ttu-id="73228-777">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-777">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-778">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-778">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-779">64</span><span class="sxs-lookup"><span data-stu-id="73228-779">64</span></span> |
| <span data-ttu-id="73228-780">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-780">Format Support</span></span> | \- |
| <span data-ttu-id="73228-781">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-781">Buffer</span></span> | \- |
| <span data-ttu-id="73228-782">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-782">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-783">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-783">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-784">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-784">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-785">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-785">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-786">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-786">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-787">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-787">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-788">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-788">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-789">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-789">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-790">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-790">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-791">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-791">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-792">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-792">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-793">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-793">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-794">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-794">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-795">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-795">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-796">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-796">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-797">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-797">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-798">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-798">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-799">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-799">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-800">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-800">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-801">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-801">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-802">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-802">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-803">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-803">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-804">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-804">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-805">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-805">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-806">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-806">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-807">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-807">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-808">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-808">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-809">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-809">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-810">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-810">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-811">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-811">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-812">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-812">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-813">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-813">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-814">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-814">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-815">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-815">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-816">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-816">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-817">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-817">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-818">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-818">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-819">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-819">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-820">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-820">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-821">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-821">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-822">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-822">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-823">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-823">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-824">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-824">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="73228-825">DXGI_FORMAT_R16G16B16A16 \_ russar<sup>FNS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="73228-825">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="73228-826">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-826">Target</span></span> | <span data-ttu-id="73228-827">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-827">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-828">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-829">64</span><span class="sxs-lookup"><span data-stu-id="73228-829">64</span></span> |
| <span data-ttu-id="73228-830">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-830">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-832">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-832">Buffer</span></span> | \- |
| <span data-ttu-id="73228-833">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-833">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-835">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-835">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-836">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-836">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-837">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-837">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-838">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-839">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-839">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-840">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-840">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-841">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-841">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-842">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-842">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-843">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-844">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-845">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-845">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-846">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-847">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-847">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-848">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-849">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-850">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-851">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-852">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-853">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-854">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-855">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-855">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-856">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-857">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-858">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-859">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-860">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-861">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-862">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-863">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-864">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-864">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-865">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-865">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-866">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-866">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-867">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-867">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-868">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-868">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-869">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-869">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-870">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-870">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-871">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-871">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-872">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-872">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-873">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-873">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-874">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-874">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-875">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-875">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-876">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-876">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="73228-877">DXGI_FORMAT_R16G16B16A16 \_ Sint<sup>FNS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="73228-877">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="73228-878">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-878">Target</span></span> | <span data-ttu-id="73228-879">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-879">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-880">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-880">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-881">64</span><span class="sxs-lookup"><span data-stu-id="73228-881">64</span></span> |
| <span data-ttu-id="73228-882">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-882">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-884">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-884">Buffer</span></span> | \- |
| <span data-ttu-id="73228-885">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-885">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-887">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-887">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-888">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-888">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-889">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-889">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-890">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-891">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-892">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-893">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-893">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-894">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-894">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-895">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-895">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-896">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-896">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-897">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-897">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-898">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-898">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-899">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-899">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-900">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-900">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-901">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-902">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-903">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-904">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-905">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-906">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-907">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-907">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-908">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-909">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-910">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-911">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-912">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-913">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-914">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-914">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-915">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-915">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-916">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-916">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-917">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-917">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-918">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-918">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-919">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-919">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-920">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-920">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-921">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-921">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-922">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-922">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-923">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-923">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-924">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-924">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-925">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-925">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-926">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-926">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-927">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-927">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-928">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="73228-929">DXGI_FORMAT_R32G32 \_ <sup>PC</sup> non con tipi (15)</span><span class="sxs-lookup"><span data-stu-id="73228-929">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="73228-930">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-930">Target</span></span> | <span data-ttu-id="73228-931">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-931">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-932">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-933">64</span><span class="sxs-lookup"><span data-stu-id="73228-933">64</span></span> |
| <span data-ttu-id="73228-934">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-934">Format Support</span></span> | \- |
| <span data-ttu-id="73228-935">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-935">Buffer</span></span> | \- |
| <span data-ttu-id="73228-936">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-936">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-937">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-937">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-938">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-938">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-939">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-939">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-940">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-940">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-941">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-941">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-942">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-942">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-943">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-943">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-944">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-944">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-945">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-945">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-946">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-946">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-947">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-947">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-948">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-948">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-949">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-949">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-950">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-950">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-951">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-951">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-952">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-952">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-953">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-953">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-954">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-954">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-955">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-955">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-956">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-956">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-957">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-957">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-958">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-958">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-959">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-959">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-960">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-960">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-961">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-961">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-962">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-962">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-963">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-963">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-964">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-964">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-965">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-965">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-966">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-966">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-967">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-967">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-968">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-968">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-969">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-969">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-970">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-970">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-971">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-971">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-972">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-972">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-973">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-973">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-974">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-975">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-976">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-977">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-977">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-978">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="73228-979">DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="73228-979">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="73228-980">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-980">Target</span></span> | <span data-ttu-id="73228-981">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-981">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-982">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-983">64</span><span class="sxs-lookup"><span data-stu-id="73228-983">64</span></span> |
| <span data-ttu-id="73228-984">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-984">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-986">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-986">Buffer</span></span> | \- |
| <span data-ttu-id="73228-987">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-987">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-989">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-990">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-991">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-992">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-992">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-994">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-994">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-996">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-996">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-998">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-998">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1000">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1000">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1001">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1001">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1002">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1002">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1003">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1003">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1004">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1004">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1005">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1005">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1006">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1006">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1007">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1007">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1009">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1009">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1010">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1010">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1011">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1011">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1012">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1012">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1013">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1013">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1014">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1014">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1015">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1015">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1016">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1016">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1017">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1017">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1018">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1018">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1019">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1019">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1020">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1020">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1021">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1021">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1022">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1022">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1023">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1023">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1025">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1025">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1027">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1027">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1029">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1029">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1031">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1031">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1033">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1033">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1034">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1034">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1035">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1035">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1036">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1036">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1037">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1037">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1038">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1038">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1039">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1039">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1040">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1040">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="73228-1041">DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="73228-1041">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="73228-1042">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1042">Target</span></span> | <span data-ttu-id="73228-1043">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1043">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1044">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1044">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1045">64</span><span class="sxs-lookup"><span data-stu-id="73228-1045">64</span></span> |
| <span data-ttu-id="73228-1046">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1046">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1047">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1047">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1048">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1048">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1049">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1049">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1050">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1050">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1051">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1051">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1052">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1052">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1053">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1053">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1054">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1054">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1055">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1055">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1056">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1056">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1057">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1057">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1058">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1058">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1059">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1059">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1060">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1060">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1061">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1061">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1062">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1062">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1063">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1063">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1064">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1064">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1065">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1065">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1066">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1066">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1067">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1067">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1068">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1068">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1069">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1069">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1070">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1070">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1071">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1071">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1072">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1072">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1073">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1073">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1074">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1074">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1075">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1075">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1076">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1076">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1077">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1077">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1078">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1078">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1079">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1079">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1080">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1080">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1081">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1081">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1082">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1082">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1083">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1083">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1084">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1084">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1085">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1085">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1086">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1087">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1088">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1089">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1089">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1090">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1090">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="73228-1091">DXGI_FORMAT_R32G32 \_ Sint<sup>FNS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="73228-1091">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="73228-1092">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1092">Target</span></span> | <span data-ttu-id="73228-1093">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1093">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1094">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1094">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1095">64</span><span class="sxs-lookup"><span data-stu-id="73228-1095">64</span></span> |
| <span data-ttu-id="73228-1096">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1096">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1097">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1097">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1098">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1098">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1099">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1099">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1100">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1100">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1101">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1101">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1102">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1102">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1103">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1104">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1105">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1105">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1106">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1106">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1107">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1107">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1108">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1108">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1109">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1109">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1110">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1110">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1111">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1111">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1112">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1112">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1113">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1113">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1114">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1114">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1115">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1116">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1117">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1118">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1119">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1119">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1120">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1121">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1122">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1123">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1124">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1125">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1126">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1127">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1128">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1128">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1129">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1130">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1131">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1132">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1133">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1133">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1134">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1135">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1135">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1136">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1137">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1138">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1139">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1139">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1140">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1140">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="73228-1141">DXGI_FORMAT_R32G8X24 i \_ <sup>PC</sup> non con tipi (19)</span><span class="sxs-lookup"><span data-stu-id="73228-1141">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="73228-1142">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1142">Target</span></span> | <span data-ttu-id="73228-1143">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1143">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1144">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1144">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1145">64</span><span class="sxs-lookup"><span data-stu-id="73228-1145">64</span></span> |
| <span data-ttu-id="73228-1146">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1146">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1147">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1147">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1148">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1148">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1149">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1149">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1150">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1150">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1151">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1151">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1152">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1152">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1153">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1153">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1154">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1155">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1155">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1156">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1156">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1157">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1157">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1158">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1158">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1159">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1159">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1160">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1160">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1161">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1161">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1162">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1163">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1164">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1165">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1166">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1167">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1168">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1169">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1169">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1170">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1171">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1172">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1173">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1175">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1176">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1177">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1178">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1178">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1179">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1180">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1181">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1182">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1183">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1183">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1184">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1185">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1185">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1186">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1186">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1187">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1187">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1188">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1188">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1189">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1189">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1190">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1190">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="73228-1191">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="73228-1191">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="73228-1192">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1192">Target</span></span> | <span data-ttu-id="73228-1193">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1193">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1194">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1195">64</span><span class="sxs-lookup"><span data-stu-id="73228-1195">64</span></span> |
| <span data-ttu-id="73228-1196">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1196">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1197">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1197">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1198">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1198">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1199">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1199">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1200">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1200">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1201">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1201">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1202">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1202">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1203">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1203">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1204">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1204">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1205">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1205">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1206">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1206">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1207">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1207">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1208">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1208">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1209">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1209">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1210">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1210">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1211">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1211">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1212">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1213">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1214">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1215">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1216">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1217">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1218">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1219">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1219">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1220">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1221">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1222">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1223">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1225">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1226">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1227">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1228">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1228">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1229">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1229">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1230">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1230">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1231">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1231">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1232">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1232">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1233">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1233">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1234">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1234">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1235">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1235">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1236">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1236">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1237">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1237">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1238">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1238">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1239">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1239">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1240">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1240">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="73228-1241">DXGI_FORMAT_R32 \_ float \_ X8X24 con \_ tipo<sup>FNS</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="73228-1241">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="73228-1242">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1242">Target</span></span> | <span data-ttu-id="73228-1243">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1243">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1244">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1244">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1245">64</span><span class="sxs-lookup"><span data-stu-id="73228-1245">64</span></span> |
| <span data-ttu-id="73228-1246">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1246">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1247">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1247">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1248">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1248">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1249">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1250">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1250">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1251">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1251">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1252">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1252">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1253">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1253">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1254">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1254">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1255">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1255">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1256">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1256">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1257">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1257">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1258">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1258">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1259">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1259">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1260">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1260">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1261">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1261">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1262">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1263">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1264">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1265">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1266">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1267">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1268">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1269">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1269">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1270">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1271">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1272">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1273">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1274">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1275">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1276">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1277">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1278">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1278">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1279">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1280">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1281">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1282">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1283">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1283">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1284">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1285">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1286">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1287">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1288">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1289">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1289">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1290">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="73228-1291">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FNS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="73228-1291">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="73228-1292">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1292">Target</span></span> | <span data-ttu-id="73228-1293">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1293">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1294">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1295">64</span><span class="sxs-lookup"><span data-stu-id="73228-1295">64</span></span> |
| <span data-ttu-id="73228-1296">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1296">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1297">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1297">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1298">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1298">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1299">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1299">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1300">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1300">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1301">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1301">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1302">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1302">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1303">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1304">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1304">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1305">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1305">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1306">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1307">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1307">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1308">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1308">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1309">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1309">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1310">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1310">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1311">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1311">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1312">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1312">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1313">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1313">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1314">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1314">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1315">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1315">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1316">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1316">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1317">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1317">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1318">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1318">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1319">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1319">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1320">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1320">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1321">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1321">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1322">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1322">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1323">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1323">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1324">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1324">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1325">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1325">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1326">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1326">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1327">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1327">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1328">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1328">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1329">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1329">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1330">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1330">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1331">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1331">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1332">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1332">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1333">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1333">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1334">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1334">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1335">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1335">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1336">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1336">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1337">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1337">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1338">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1338">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1339">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1339">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1340">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1340">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="73228-1341">DXGI_FORMAT_R10G10B10A2 \_ <sup>PC</sup> non con tipi (23)</span><span class="sxs-lookup"><span data-stu-id="73228-1341">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="73228-1342">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1342">Target</span></span> | <span data-ttu-id="73228-1343">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1343">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1344">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1344">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1345">32</span><span class="sxs-lookup"><span data-stu-id="73228-1345">32</span></span> |
| <span data-ttu-id="73228-1346">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1346">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1347">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1347">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1348">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1348">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1349">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1349">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1350">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1350">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1351">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1351">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1352">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1352">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1353">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1354">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1354">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1355">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1355">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1356">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1356">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1357">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1357">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1358">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1358">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1359">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1359">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1360">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1360">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1361">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1361">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1362">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1362">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1363">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1363">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1364">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1364">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1365">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1365">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1366">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1366">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1367">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1367">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1368">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1368">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1369">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1369">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1370">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1370">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1371">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1371">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1372">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1372">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1373">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1373">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1374">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1374">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1375">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1375">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1376">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1376">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1377">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1377">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1378">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1378">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1379">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1380">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1381">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1382">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1383">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1383">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1384">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1385">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1386">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1386">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1387">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1387">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1388">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1388">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1389">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1389">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1390">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1390">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="73228-1391">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="73228-1391">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="73228-1392">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1392">Target</span></span> | <span data-ttu-id="73228-1393">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1393">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1394">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1395">32</span><span class="sxs-lookup"><span data-stu-id="73228-1395">32</span></span> |
| <span data-ttu-id="73228-1396">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1396">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1397">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1397">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1398">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1398">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1399">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1399">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1400">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1400">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1401">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1401">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1402">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1402">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1403">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1403">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1404">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1404">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1405">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1405">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1406">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1407">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1407">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1408">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1408">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1409">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1410">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1410">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1411">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1411">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1412">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1412">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1413">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1413">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1414">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1414">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1415">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1415">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1416">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1416">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1417">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1417">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1418">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1418">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1419">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1419">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1420">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1420">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1421">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1421">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1422">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1422">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1423">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1423">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1424">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1424">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1425">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1425">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1426">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1426">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1427">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1427">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1428">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1428">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1429">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1429">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1430">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1430">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1431">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1431">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1432">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1432">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1433">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1433">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1434">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1434">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1435">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1435">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1436">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1437">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1438">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1439">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1439">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1441">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="73228-1442">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="73228-1442">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="73228-1443">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1443">Target</span></span> | <span data-ttu-id="73228-1444">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1444">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1445">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1446">32</span><span class="sxs-lookup"><span data-stu-id="73228-1446">32</span></span> |
| <span data-ttu-id="73228-1447">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1447">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1448">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1448">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1449">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1450">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1451">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1452">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1453">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1454">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1454">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1455">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1455">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1456">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1456">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1457">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1457">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1458">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1458">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1459">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1459">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1460">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1460">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1461">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1461">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1462">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1462">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1463">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1465">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1466">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1467">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1467">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1468">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1469">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1470">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1471">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1472">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1473">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1474">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1475">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1476">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1477">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1478">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1479">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1479">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1480">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1480">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1481">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1481">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1482">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1482">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1483">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1483">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1484">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1484">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1485">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1485">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1486">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1486">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1487">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1487">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1488">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1488">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1489">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1489">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1490">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1490">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1491">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="73228-1492">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FNS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="73228-1492">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="73228-1493">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1493">Target</span></span> | <span data-ttu-id="73228-1494">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1494">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1495">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1496">32</span><span class="sxs-lookup"><span data-stu-id="73228-1496">32</span></span> |
| <span data-ttu-id="73228-1497">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1497">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1498">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1498">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1499">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1500">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1501">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1502">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1503">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1504">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1505">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1506">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1507">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1508">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1509">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1510">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1510">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1511">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1512">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1513">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1514">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1515">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1516">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1517">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1518">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1519">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1520">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1520">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1521">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1522">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1523">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1524">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1526">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1527">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1528">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1529">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1530">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1531">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1532">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1533">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1534">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1534">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1535">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1536">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1537">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1538">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1539">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1540">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1540">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1541">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="73228-1542">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="73228-1542">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="73228-1543">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1543">Target</span></span> | <span data-ttu-id="73228-1544">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1544">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1545">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1546">32</span><span class="sxs-lookup"><span data-stu-id="73228-1546">32</span></span> |
| <span data-ttu-id="73228-1547">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1547">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1548">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1548">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1549">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1550">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1551">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1552">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1553">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1554">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1555">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1556">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1557">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1558">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1559">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1560">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1560">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1561">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1562">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1563">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1564">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1565">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1566">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1567">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1568">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1569">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1570">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1570">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1571">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1572">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1573">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1574">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1576">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1577">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1578">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1579">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1580">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1581">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1582">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1583">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1584">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1584">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1585">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1586">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1587">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1588">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1589">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1590">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1590">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1591">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="73228-1592">DXGI_FORMAT_R8G8B8A8 \_ <sup>PC</sup> non con tipi (27)</span><span class="sxs-lookup"><span data-stu-id="73228-1592">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="73228-1593">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1593">Target</span></span> | <span data-ttu-id="73228-1594">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1594">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1595">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1596">32</span><span class="sxs-lookup"><span data-stu-id="73228-1596">32</span></span> |
| <span data-ttu-id="73228-1597">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1597">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1598">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1598">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1599">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1600">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1601">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1603">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1604">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1605">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1606">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1607">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1608">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1609">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1610">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1610">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1611">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1612">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1613">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1614">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1615">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1616">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1617">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1618">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1619">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1620">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1620">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1621">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1622">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1623">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1624">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1626">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1627">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1628">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1629">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1630">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1631">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1632">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1633">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1634">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1634">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1635">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1636">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1637">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1638">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1639">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1640">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1640">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1641">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="73228-1642">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="73228-1642">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="73228-1643">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1643">Target</span></span> | <span data-ttu-id="73228-1644">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1644">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1645">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1646">32</span><span class="sxs-lookup"><span data-stu-id="73228-1646">32</span></span> |
| <span data-ttu-id="73228-1647">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1647">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1649">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1649">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1650">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1650">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1652">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1653">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1654">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1655">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1657">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1659">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1661">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1661">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1663">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1663">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1665">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1665">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1666">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1666">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1667">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1667">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1668">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1668">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1669">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1669">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1671">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1671">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1673">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1675">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1675">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1677">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1678">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1679">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1680">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1681">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1681">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1682">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1683">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1684">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1685">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1687">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1688">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1689">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1690">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1690">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1692">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1692">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1694">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1694">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1696">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1696">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1698">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1698">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1700">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1700">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1701">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1701">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1703">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1703">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1704">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1704">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1705">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1705">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1707">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1707">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1709">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1709">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1711">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1711">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="73228-1712">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="73228-1712">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="73228-1713">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1713">Target</span></span> | <span data-ttu-id="73228-1714">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1714">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1715">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1715">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1716">32</span><span class="sxs-lookup"><span data-stu-id="73228-1716">32</span></span> |
| <span data-ttu-id="73228-1717">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1717">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1719">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1719">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1720">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1720">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1721">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1721">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1722">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1722">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1723">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1723">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1724">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1724">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1726">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1726">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1728">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1728">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1730">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1730">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1732">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1732">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1734">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1734">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1735">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1735">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1736">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1736">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1737">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1737">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1738">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1738">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1740">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1740">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1742">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1744">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1744">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1746">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1746">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1747">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1747">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1748">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1748">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1749">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1749">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1750">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1750">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1751">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1751">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1752">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1752">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1753">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1753">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1754">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1754">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1755">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1755">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1756">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1756">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1757">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1757">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1758">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1758">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1759">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1759">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1761">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1761">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1763">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1763">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1765">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1765">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1767">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1767">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1769">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1769">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1770">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1770">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1772">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1772">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1773">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1773">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1774">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1774">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-1776">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1776">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1778">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1778">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1780">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="73228-1781">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="73228-1781">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="73228-1782">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1782">Target</span></span> | <span data-ttu-id="73228-1783">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1784">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1785">32</span><span class="sxs-lookup"><span data-stu-id="73228-1785">32</span></span> |
| <span data-ttu-id="73228-1786">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1786">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1788">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1789">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1789">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1791">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1792">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1793">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1794">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1794">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1796">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1797">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1797">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1798">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1798">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1799">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1799">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1800">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1800">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1801">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1801">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1802">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1802">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1803">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1803">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1804">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1804">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1805">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1805">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1806">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1806">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1807">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1807">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1808">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1808">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1809">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1809">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1810">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1810">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1811">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1811">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1812">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1812">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1813">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1813">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1814">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1814">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1815">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1815">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1816">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1816">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1817">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1817">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1818">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1818">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1819">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1819">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1820">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1820">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1821">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1821">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1822">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1822">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1823">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1823">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1824">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1824">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1825">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1825">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1826">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1826">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1827">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1827">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1828">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1828">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1829">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1829">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1830">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1830">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1831">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1831">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1832">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1832">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="73228-1833">DXGI_FORMAT_R8G8B8A8 \_ russar<sup>FNS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="73228-1833">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="73228-1834">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1834">Target</span></span> | <span data-ttu-id="73228-1835">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1835">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1836">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1836">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1837">32</span><span class="sxs-lookup"><span data-stu-id="73228-1837">32</span></span> |
| <span data-ttu-id="73228-1838">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1838">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1840">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1840">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1841">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1841">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1842">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1842">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1843">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1843">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1844">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1844">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1845">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1845">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1847">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1847">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1848">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1848">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1850">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1850">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1852">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1852">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1854">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1855">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1856">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1857">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1858">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1858">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1860">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1860">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1861">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1861">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1862">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1862">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1863">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1863">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1864">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1864">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1865">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1865">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1866">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1866">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1867">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1867">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1868">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1868">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1869">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1869">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1870">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1870">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1871">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1871">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1872">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1872">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1873">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1873">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1874">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1874">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1875">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1875">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1876">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1876">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1878">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1878">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1879">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1879">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1880">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1880">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1881">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1881">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1882">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1882">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1883">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1883">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1884">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1884">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1885">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1885">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1886">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1886">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1887">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1887">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1888">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1888">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1889">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="73228-1890">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup>FNS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="73228-1890">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="73228-1891">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1891">Target</span></span> | <span data-ttu-id="73228-1892">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1892">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1893">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1894">32</span><span class="sxs-lookup"><span data-stu-id="73228-1894">32</span></span> |
| <span data-ttu-id="73228-1895">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1895">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1896">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1896">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1897">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1897">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1898">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1898">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1899">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1899">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1900">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1900">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1901">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1901">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1902">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1903">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1903">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1904">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1904">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1905">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1905">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1906">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1906">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1907">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1907">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1908">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1908">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1909">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1909">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1910">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1910">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1911">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1911">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1912">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1912">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1913">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1913">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1914">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1914">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1915">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1915">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1916">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1916">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1917">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1917">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1918">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1918">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1919">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1919">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1920">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1920">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1921">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1922">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1923">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1924">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1925">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1925">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1926">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1926">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1927">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1927">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1928">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1928">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1929">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1929">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1930">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1930">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1931">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1931">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1932">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1932">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1933">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1933">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1934">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1934">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1935">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1935">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1936">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1936">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1937">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1937">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1938">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1938">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1939">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="73228-1940">DXGI_FORMAT_R16G16 \_ <sup>PC</sup> non con tipi (33)</span><span class="sxs-lookup"><span data-stu-id="73228-1940">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="73228-1941">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1941">Target</span></span> | <span data-ttu-id="73228-1942">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1942">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1943">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1944">32</span><span class="sxs-lookup"><span data-stu-id="73228-1944">32</span></span> |
| <span data-ttu-id="73228-1945">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1945">Format Support</span></span> | \- |
| <span data-ttu-id="73228-1946">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1946">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1947">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1947">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-1948">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-1948">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-1949">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-1949">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-1950">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-1950">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-1951">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-1951">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-1952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-1952">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-1953">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-1953">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-1954">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-1954">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-1955">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-1955">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-1956">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-1956">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-1957">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-1957">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-1958">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-1958">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-1959">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-1959">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-1960">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1960">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-1961">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-1961">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-1962">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-1962">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1963">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-1963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1964">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-1964">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-1965">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1965">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-1966">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-1966">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1967">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-1967">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-1968">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-1968">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-1969">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1969">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-1970">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1970">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-1971">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1971">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-1972">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1972">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-1973">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-1973">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-1974">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1974">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-1975">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-1975">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1976">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-1976">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-1977">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-1977">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-1978">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-1978">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1979">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-1979">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-1980">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-1980">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-1981">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1981">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-1982">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-1982">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-1983">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-1983">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-1984">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-1984">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-1985">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-1985">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-1986">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1986">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-1987">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-1987">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-1988">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-1988">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-1989">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-1989">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="73228-1990">DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="73228-1990">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="73228-1991">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-1991">Target</span></span> | <span data-ttu-id="73228-1992">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-1992">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-1993">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-1993">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-1994">32</span><span class="sxs-lookup"><span data-stu-id="73228-1994">32</span></span> |
| <span data-ttu-id="73228-1995">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-1995">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-1997">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-1997">Buffer</span></span> | \- |
| <span data-ttu-id="73228-1998">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-1998">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2000">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2000">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2001">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2001">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2002">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2002">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2003">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2005">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2007">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2009">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2009">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2011">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2011">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2012">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2012">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2013">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2013">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2014">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2014">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2015">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2015">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2016">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2016">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2018">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2018">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2020">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2020">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2022">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2022">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2023">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2023">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2024">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2024">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2025">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2025">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2026">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2026">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2027">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2027">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2028">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2028">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2029">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2029">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2030">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2030">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2031">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2031">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2032">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2032">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2033">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2033">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2034">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2034">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2035">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2035">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2036">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2036">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2038">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2038">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2040">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2040">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2042">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2042">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2044">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2044">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2046">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2046">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2047">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2047">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2048">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2048">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2049">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2050">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2051">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2052">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2052">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2053">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2053">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="73228-2054">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="73228-2054">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="73228-2055">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2055">Target</span></span> | <span data-ttu-id="73228-2056">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2056">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2057">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2057">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2058">32</span><span class="sxs-lookup"><span data-stu-id="73228-2058">32</span></span> |
| <span data-ttu-id="73228-2059">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2059">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2061">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2061">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2062">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2062">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2063">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2063">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2064">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2064">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2065">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2065">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2066">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2066">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2068">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2068">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2070">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2070">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2072">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2072">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2074">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2074">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2076">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2076">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2077">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2077">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2078">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2078">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2079">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2079">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2080">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2080">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2082">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2082">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2084">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2084">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2086">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2087">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2088">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2089">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2090">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2091">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2091">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2092">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2093">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2094">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2095">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2096">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2097">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2098">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2099">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2100">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2100">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2102">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2102">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2104">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2104">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2106">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2106">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2108">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2108">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2110">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2110">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2111">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2111">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2112">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2112">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2113">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2113">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2114">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2114">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2115">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2115">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2116">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2116">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2117">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2117">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="73228-2118">DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="73228-2118">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="73228-2119">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2119">Target</span></span> | <span data-ttu-id="73228-2120">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2120">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2121">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2121">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2122">32</span><span class="sxs-lookup"><span data-stu-id="73228-2122">32</span></span> |
| <span data-ttu-id="73228-2123">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2123">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2124">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2124">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2125">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2125">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2126">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2126">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2127">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2127">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2128">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2128">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2129">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2130">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2131">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2132">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2132">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2133">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2133">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2134">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2134">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2135">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2135">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2136">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2136">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2137">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2137">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2138">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2138">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2139">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2139">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2140">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2140">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2141">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2141">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2142">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2142">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2143">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2143">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2144">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2145">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2146">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2146">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2147">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2148">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2149">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2150">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2152">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2153">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2154">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2155">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2156">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2156">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2157">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2157">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2158">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2158">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2159">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2159">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2160">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2160">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2161">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2162">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2162">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2163">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2163">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2164">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2164">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2165">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2165">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2166">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2166">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2167">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2167">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="73228-2168">DXGI_FORMAT_R16G16 \_ russar<sup>FNS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="73228-2168">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="73228-2169">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2169">Target</span></span> | <span data-ttu-id="73228-2170">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2170">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2171">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2172">32</span><span class="sxs-lookup"><span data-stu-id="73228-2172">32</span></span> |
| <span data-ttu-id="73228-2173">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2173">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2175">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2175">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2176">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2176">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2178">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2178">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2179">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2179">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2180">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2180">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2181">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2181">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2183">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2185">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2185">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2187">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2187">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2189">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2189">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2191">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2191">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2192">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2192">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2193">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2193">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2194">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2194">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2195">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2195">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2197">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2198">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2199">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2200">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2201">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2202">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2203">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2204">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2204">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2205">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2206">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2207">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2208">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2210">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2211">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2212">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2213">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2213">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2215">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2215">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2216">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2216">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2217">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2217">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2218">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2218">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2219">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2219">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2220">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2220">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2221">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2221">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2222">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2222">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2223">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2223">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2224">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2224">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2225">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2225">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2226">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2226">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="73228-2227">DXGI_FORMAT_R16G16 \_ Sint<sup>FNS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="73228-2227">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="73228-2228">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2228">Target</span></span> | <span data-ttu-id="73228-2229">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2229">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2230">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2230">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2231">32</span><span class="sxs-lookup"><span data-stu-id="73228-2231">32</span></span> |
| <span data-ttu-id="73228-2232">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2232">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2234">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2234">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2235">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2235">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2237">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2237">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2238">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2238">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2239">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2239">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2240">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2240">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2241">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2241">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2242">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2242">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2243">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2243">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2244">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2244">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2245">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2246">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2247">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2248">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2249">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2249">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2250">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2250">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2251">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2252">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2252">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2253">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2253">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2254">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2254">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2255">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2255">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2256">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2256">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2257">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2257">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2258">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2258">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2259">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2259">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2260">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2260">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2261">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2261">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2262">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2262">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2263">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2263">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2264">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2264">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2265">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2265">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2266">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2266">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2267">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2267">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2268">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2268">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2269">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2269">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2270">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2270">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2271">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2271">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2272">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2272">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2273">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2273">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2274">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2274">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2275">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2275">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2276">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2276">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2277">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2277">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2278">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2278">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="73228-2279">DXGI_FORMAT_R32 \_ <sup>PC</sup> non con tipi (39)</span><span class="sxs-lookup"><span data-stu-id="73228-2279">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="73228-2280">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2280">Target</span></span> | <span data-ttu-id="73228-2281">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2281">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2282">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2282">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2283">32</span><span class="sxs-lookup"><span data-stu-id="73228-2283">32</span></span> |
| <span data-ttu-id="73228-2284">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2284">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2285">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2285">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2286">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2286">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2287">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2287">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2288">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2288">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2289">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2289">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2290">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2290">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2291">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2291">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2292">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2292">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2293">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2293">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2294">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2294">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2295">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2295">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2296">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2296">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2297">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2297">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2298">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2298">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2299">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2299">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2300">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2300">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2301">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2301">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2302">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2302">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2303">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2303">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2304">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2305">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2306">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2307">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2307">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2308">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2309">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2310">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2311">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2312">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2313">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2314">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2315">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2316">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2316">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2317">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2318">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2319">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2320">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2321">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2321">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2322">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2323">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2324">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2324">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2325">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2325">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2326">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2326">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2327">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2327">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2328">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2328">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="73228-2329">DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="73228-2329">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="73228-2330">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2330">Target</span></span> | <span data-ttu-id="73228-2331">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2331">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2332">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2332">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2333">32</span><span class="sxs-lookup"><span data-stu-id="73228-2333">32</span></span> |
| <span data-ttu-id="73228-2334">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2334">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2335">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2335">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2336">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2336">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2337">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2337">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2338">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2338">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2339">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2339">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2340">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2340">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2341">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2341">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2342">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2343">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2343">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2344">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2344">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2345">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2346">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2347">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2347">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2348">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2349">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2349">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2350">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2350">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2351">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2351">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2352">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2353">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2354">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2355">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2356">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2357">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2357">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2358">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2358">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2359">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2359">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2360">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2360">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2361">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2361">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2362">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2362">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2363">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2363">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2364">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2364">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2365">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2365">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2366">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2366">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2367">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2367">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2368">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2368">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2369">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2369">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2370">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2370">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2371">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2371">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2372">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2373">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2373">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2374">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2375">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2376">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2377">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2377">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2378">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="73228-2379">DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="73228-2379">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="73228-2380">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2380">Target</span></span> | <span data-ttu-id="73228-2381">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2381">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2382">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2383">32</span><span class="sxs-lookup"><span data-stu-id="73228-2383">32</span></span> |
| <span data-ttu-id="73228-2384">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2384">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2386">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2386">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2387">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2387">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2389">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2390">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2391">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2392">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2394">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2396">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2398">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2398">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2400">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2401">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2402">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2403">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2403">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2404">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2405">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2407">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2407">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2409">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2411">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2411">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2412">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2412">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2413">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2413">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2414">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2414">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2415">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2415">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2416">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2416">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2417">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2417">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2418">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2418">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2419">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2419">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2420">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2420">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2421">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2421">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2422">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2422">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2423">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2423">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2424">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2424">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2425">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2425">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2427">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2427">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2429">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2429">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2431">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2431">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2433">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2433">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2435">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2435">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2436">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2437">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2438">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2439">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2440">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2441">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2441">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2442">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="73228-2443">DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="73228-2443">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="73228-2444">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2444">Target</span></span> | <span data-ttu-id="73228-2445">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2445">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2446">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2447">32</span><span class="sxs-lookup"><span data-stu-id="73228-2447">32</span></span> |
| <span data-ttu-id="73228-2448">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2448">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2450">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2450">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2451">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2451">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2452">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2452">Input Assembler Index Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2454">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2454">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2455">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2455">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2456">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2456">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2457">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2458">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2458">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2459">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2459">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2460">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2460">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2461">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2461">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2462">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2462">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2463">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2463">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2464">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2464">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2465">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2465">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2466">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2466">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2467">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2468">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2468">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2469">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2469">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2470">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2470">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2471">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2471">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2472">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2472">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2473">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2473">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2474">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2474">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2475">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2475">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2476">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2476">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2477">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2477">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2478">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2478">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2479">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2479">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2480">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2480">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2481">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2481">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2482">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2482">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2483">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2483">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2484">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2484">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2485">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2485">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2486">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2486">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2487">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2487">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2488">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2488">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2489">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2489">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2490">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2490">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2491">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2491">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2492">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2492">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2493">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2493">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2494">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="73228-2495">DXGI_FORMAT_R32 \_ Sint<sup>FNS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="73228-2495">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="73228-2496">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2496">Target</span></span> | <span data-ttu-id="73228-2497">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2497">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2498">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2499">32</span><span class="sxs-lookup"><span data-stu-id="73228-2499">32</span></span> |
| <span data-ttu-id="73228-2500">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2500">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2501">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2501">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2502">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2502">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2503">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2503">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2504">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2504">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2505">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2505">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2506">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2506">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2507">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2507">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2508">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2508">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2509">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2509">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2510">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2510">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2511">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2512">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2513">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2514">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2515">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2515">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2516">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2516">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2518">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2519">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2520">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2521">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2522">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2523">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2524">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2525">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2526">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2527">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2528">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2529">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2530">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2530">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2531">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2531">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2532">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2532">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2533">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2533">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2534">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2534">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2535">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2535">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2536">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2536">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2537">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2537">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2538">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2538">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2539">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2539">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2540">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2541">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2542">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2543">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2543">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2544">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="73228-2545">DXGI_FORMAT_R24G8 \_ <sup>PC</sup> non con tipi (44)</span><span class="sxs-lookup"><span data-stu-id="73228-2545">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="73228-2546">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2546">Target</span></span> | <span data-ttu-id="73228-2547">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2547">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2548">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2549">32</span><span class="sxs-lookup"><span data-stu-id="73228-2549">32</span></span> |
| <span data-ttu-id="73228-2550">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2550">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2551">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2551">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2552">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2552">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2553">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2553">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2554">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2554">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2555">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2555">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2556">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2557">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2558">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2559">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2559">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2560">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2560">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2561">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2561">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2562">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2562">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2563">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2563">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2564">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2564">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2565">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2565">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2566">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2566">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2567">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2567">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2568">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2568">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2569">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2569">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2570">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2570">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2571">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2571">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2572">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2572">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2573">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2573">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2574">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2574">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2575">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2575">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2576">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2576">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2577">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2577">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2578">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2578">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2579">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2579">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2580">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2580">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2581">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2581">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2582">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2582">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2583">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2583">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2584">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2584">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2585">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2585">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2586">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2586">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2587">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2587">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2588">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2588">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2589">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2589">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2590">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2590">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2591">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2591">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2592">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2592">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2593">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2593">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2594">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="73228-2595">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="73228-2595">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="73228-2596">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2596">Target</span></span> | <span data-ttu-id="73228-2597">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2597">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2598">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2599">32</span><span class="sxs-lookup"><span data-stu-id="73228-2599">32</span></span> |
| <span data-ttu-id="73228-2600">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2600">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2602">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2602">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2603">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2604">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2605">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2606">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2607">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2609">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2610">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2611">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2612">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2613">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2614">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2615">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2615">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2616">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2617">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2618">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2619">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2620">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2621">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2622">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2622">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2624">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2624">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2625">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2625">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2626">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2626">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2627">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2627">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2628">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2628">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2629">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2629">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2630">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2630">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2631">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2631">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2632">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2632">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2633">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2633">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2634">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2634">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2635">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2635">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2636">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2636">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2638">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2638">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2640">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2640">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-2642">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2642">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2643">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2643">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2644">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2645">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2645">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2646">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2646">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2647">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2647">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2648">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2648">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2649">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2649">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2650">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="73228-2651">DXGI_FORMAT_R24 \_ UNORM \_ X8 di \_ tipo<sup>FNS</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="73228-2651">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="73228-2652">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2652">Target</span></span> | <span data-ttu-id="73228-2653">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2653">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2654">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2655">32</span><span class="sxs-lookup"><span data-stu-id="73228-2655">32</span></span> |
| <span data-ttu-id="73228-2656">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2656">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2657">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2657">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2658">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2659">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2660">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2661">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2662">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2663">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2663">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2664">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2664">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2665">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2665">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2666">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2666">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2667">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2668">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2669">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2669">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2670">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2671">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2671">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2672">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2673">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2674">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2675">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2676">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2677">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2678">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2679">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2679">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2680">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2681">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2682">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2683">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2684">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2685">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2686">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2687">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2688">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2688">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2689">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2690">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2691">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2692">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2693">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2693">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2694">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2695">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2696">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2697">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2698">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2699">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2699">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2700">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2700">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="73228-2701">DXGI_FORMAT_X24 di \_ tipo \_ G8 \_ UINT<sup>FNS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="73228-2701">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="73228-2702">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2702">Target</span></span> | <span data-ttu-id="73228-2703">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2704">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2705">32</span><span class="sxs-lookup"><span data-stu-id="73228-2705">32</span></span> |
| <span data-ttu-id="73228-2706">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2706">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2707">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2707">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2708">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2708">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2709">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2709">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2710">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2710">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2711">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2711">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2712">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2712">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2713">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2714">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2714">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2715">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2715">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2716">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2717">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2718">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2719">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2720">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2721">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2721">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2722">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2722">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2723">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2723">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2724">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2724">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2725">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2725">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2726">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2726">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2727">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2727">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2728">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2728">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2729">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2729">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2730">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2730">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2731">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2731">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2732">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2732">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2733">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2733">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2734">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2734">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2735">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2735">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2736">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2736">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2737">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2737">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2738">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2738">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2739">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2740">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2741">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2742">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2743">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2743">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2744">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2745">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2746">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2746">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2747">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2747">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2748">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2748">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2749">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2749">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2750">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2750">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="73228-2751">DXGI_FORMAT_R8G8 \_ <sup>PC</sup> non con tipi (48)</span><span class="sxs-lookup"><span data-stu-id="73228-2751">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="73228-2752">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2752">Target</span></span> | <span data-ttu-id="73228-2753">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2753">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2754">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2755">16</span><span class="sxs-lookup"><span data-stu-id="73228-2755">16</span></span> |
| <span data-ttu-id="73228-2756">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2756">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2757">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2757">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2758">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2759">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2760">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2761">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2762">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2763">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2764">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2764">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2765">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2765">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2766">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2766">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2767">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2767">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2768">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2768">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2769">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2769">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2770">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2770">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2771">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2771">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2772">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2772">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2773">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2773">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2774">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2774">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2775">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2775">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2776">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2776">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2777">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2777">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2778">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2778">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2779">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2779">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2780">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2780">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2781">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2781">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2782">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2782">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2783">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2783">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2784">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2784">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2785">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2785">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2786">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2786">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2787">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2787">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2788">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2788">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2789">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2789">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2790">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2790">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2791">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2791">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2792">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2792">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2793">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2793">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2794">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2794">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2795">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2795">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2796">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2796">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2797">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2797">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2798">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2798">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2799">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2799">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2800">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="73228-2801">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="73228-2801">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="73228-2802">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2802">Target</span></span> | <span data-ttu-id="73228-2803">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2803">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2804">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2805">16</span><span class="sxs-lookup"><span data-stu-id="73228-2805">16</span></span> |
| <span data-ttu-id="73228-2806">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2806">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2808">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2808">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2809">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2810">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2811">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2812">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2813">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2815">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2815">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2816">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2816">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2817">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2817">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2819">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2819">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2821">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2821">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2822">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2822">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2823">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2823">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2824">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2824">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2825">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2825">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2826">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2826">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2827">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2829">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2829">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2831">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2832">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2833">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2834">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2835">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2835">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2836">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2836">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2837">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2837">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2838">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2838">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2839">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2839">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2840">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2840">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2841">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2841">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2842">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2842">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2843">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2843">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2844">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2844">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2846">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2846">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2847">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2847">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2848">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2848">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2849">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2849">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2850">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2850">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2851">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2851">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2852">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2852">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2853">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2853">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2854">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2854">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2855">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2855">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2856">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2856">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2858">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2858">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="73228-2859">DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="73228-2859">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="73228-2860">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2860">Target</span></span> | <span data-ttu-id="73228-2861">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2861">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2862">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2862">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2863">16</span><span class="sxs-lookup"><span data-stu-id="73228-2863">16</span></span> |
| <span data-ttu-id="73228-2864">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2864">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2865">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2865">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2866">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2866">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2867">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2868">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2869">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2870">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2871">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2871">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2872">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2872">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2873">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2873">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2874">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2874">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2875">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2875">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2876">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2876">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2877">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2877">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2878">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2878">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2879">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2879">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2880">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2881">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2882">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2883">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2884">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2885">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2886">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2887">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2887">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2888">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2889">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2890">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2891">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2893">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2894">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2895">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2896">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2896">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-2897">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2897">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2898">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2898">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2899">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2899">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2900">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2900">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2901">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2901">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2902">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2903">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2903">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2904">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2905">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2906">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2907">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2907">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2908">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2908">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="73228-2909">DXGI_FORMAT_R8G8 \_ russar<sup>FNS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="73228-2909">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="73228-2910">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2910">Target</span></span> | <span data-ttu-id="73228-2911">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2911">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2912">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2912">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2913">16</span><span class="sxs-lookup"><span data-stu-id="73228-2913">16</span></span> |
| <span data-ttu-id="73228-2914">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2914">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2916">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2916">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2917">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2917">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2918">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2918">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2919">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2919">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2920">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2920">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2921">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2921">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2923">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2924">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2925">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2925">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2927">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2927">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2929">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2929">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2930">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2930">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2931">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2931">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2932">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2932">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2933">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2933">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2935">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2935">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2936">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2936">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2937">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2937">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2938">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2938">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2939">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2939">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2940">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2940">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2941">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2941">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2942">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2942">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2943">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2943">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2944">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2944">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2945">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2945">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2946">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2946">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2947">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2947">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2948">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2948">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-2949">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2949">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2950">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-2950">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-2951">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-2951">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-2953">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-2953">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2954">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-2954">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2955">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-2955">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-2956">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2956">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-2957">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-2957">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-2958">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-2958">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-2959">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-2959">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-2960">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-2960">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-2961">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2961">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-2962">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-2962">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-2963">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-2963">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-2964">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-2964">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="73228-2965">DXGI_FORMAT_R8G8 \_ Sint<sup>FNS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="73228-2965">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="73228-2966">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2966">Target</span></span> | <span data-ttu-id="73228-2967">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-2967">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-2968">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-2968">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-2969">16</span><span class="sxs-lookup"><span data-stu-id="73228-2969">16</span></span> |
| <span data-ttu-id="73228-2970">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-2970">Format Support</span></span> | \- |
| <span data-ttu-id="73228-2971">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-2971">Buffer</span></span> | \- |
| <span data-ttu-id="73228-2972">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-2972">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-2973">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-2973">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-2974">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-2974">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-2975">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-2975">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-2976">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-2976">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-2977">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-2977">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-2978">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-2978">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-2979">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-2979">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-2980">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-2980">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-2981">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-2981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-2982">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-2982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-2983">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-2983">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-2984">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-2984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-2985">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2985">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-2986">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-2987">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2988">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-2988">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-2989">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-2989">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-2990">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-2990">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-2991">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-2991">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2992">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-2992">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-2993">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-2993">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-2994">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2994">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-2995">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2995">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-2996">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-2997">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-2998">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-2998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-2999">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-2999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3000">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3000">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3001">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3001">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3002">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3002">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3003">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3003">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3004">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3004">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3005">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3005">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3006">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3006">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3007">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3007">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3008">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3009">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3009">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3010">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3011">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3012">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3013">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3013">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3014">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3014">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="73228-3015">DXGI_FORMAT_R16 \_ <sup>PC</sup> non con tipi (53)</span><span class="sxs-lookup"><span data-stu-id="73228-3015">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="73228-3016">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3016">Target</span></span> | <span data-ttu-id="73228-3017">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3017">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3018">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3018">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3019">16</span><span class="sxs-lookup"><span data-stu-id="73228-3019">16</span></span> |
| <span data-ttu-id="73228-3020">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3020">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3021">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3021">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3022">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3022">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3023">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3023">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3024">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3024">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3025">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3025">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3026">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3026">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3027">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3027">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3028">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3028">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3029">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3029">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3030">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3030">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3031">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3032">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3033">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3033">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3034">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3035">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3036">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3036">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3037">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3037">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3038">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3038">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3039">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3040">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3041">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3042">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3043">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3043">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3044">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3045">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3046">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3047">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3048">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3049">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3050">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3051">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3052">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3052">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3053">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3054">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3055">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3056">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3057">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3057">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3058">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3059">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3059">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3060">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3060">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3061">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3061">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3062">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3062">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3063">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3063">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3064">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3064">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="73228-3065">DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="73228-3065">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="73228-3066">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3066">Target</span></span> | <span data-ttu-id="73228-3067">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3067">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3068">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3068">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3069">16</span><span class="sxs-lookup"><span data-stu-id="73228-3069">16</span></span> |
| <span data-ttu-id="73228-3070">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3070">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3071">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3071">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3072">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3072">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3073">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3073">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3074">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3074">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3075">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3075">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3076">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3076">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3077">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3077">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3078">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3079">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3079">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3080">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3080">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3081">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3081">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3082">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3082">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3083">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3083">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3084">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3084">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3085">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3085">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3086">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3086">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3087">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3087">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3088">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3089">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3090">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3091">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3092">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3093">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3093">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3094">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3095">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3096">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3097">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3098">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3099">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3100">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3101">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3102">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3102">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3103">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3103">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3104">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3104">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3105">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3105">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3106">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3106">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3107">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3107">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3108">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3108">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3109">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3109">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3110">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3111">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3112">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3113">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3113">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3114">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="73228-3115">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="73228-3115">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="73228-3116">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3116">Target</span></span> | <span data-ttu-id="73228-3117">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3117">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3118">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3119">16</span><span class="sxs-lookup"><span data-stu-id="73228-3119">16</span></span> |
| <span data-ttu-id="73228-3120">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3120">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3122">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3122">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3123">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3124">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3125">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3126">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3127">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3127">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3129">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3129">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3130">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3130">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3131">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3131">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3132">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3132">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3133">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3133">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3134">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3134">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3135">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3135">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3136">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3136">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3137">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3137">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3138">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3138">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3139">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3139">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3140">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3140">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3141">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3141">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3142">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3142">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3144">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3145">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3146">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3146">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3147">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3148">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3149">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3150">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3152">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3153">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3154">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3155">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3156">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3156">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-3158">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3158">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-3160">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3160">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-3162">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3163">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3163">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3164">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3165">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3166">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3167">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3168">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3169">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3169">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3170">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="73228-3171">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="73228-3171">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="73228-3172">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3172">Target</span></span> | <span data-ttu-id="73228-3173">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3173">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3174">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3175">16</span><span class="sxs-lookup"><span data-stu-id="73228-3175">16</span></span> |
| <span data-ttu-id="73228-3176">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3176">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3178">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3178">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3179">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3179">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3180">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3180">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3181">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3182">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3183">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3183">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3185">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3185">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3187">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3187">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3189">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3189">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3191">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3191">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3193">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3193">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3194">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3194">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3195">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3195">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3196">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3196">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3197">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3199">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3199">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3200">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3201">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3202">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3203">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3204">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3205">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3206">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3206">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3207">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3208">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3209">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3210">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3211">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3212">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3213">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3213">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3214">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3214">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3215">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3215">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3217">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3218">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3219">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3220">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3221">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3221">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3222">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3223">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3223">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3224">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3224">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3225">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3225">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3226">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3226">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3227">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3227">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3228">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3228">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="73228-3229">DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="73228-3229">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="73228-3230">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3230">Target</span></span> | <span data-ttu-id="73228-3231">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3231">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3232">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3232">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3233">16</span><span class="sxs-lookup"><span data-stu-id="73228-3233">16</span></span> |
| <span data-ttu-id="73228-3234">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3234">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3236">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3236">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3237">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3237">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3238">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3238">Input Assembler Index Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3240">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3240">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3241">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3241">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3242">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3242">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3243">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3243">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3244">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3244">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3245">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3245">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3246">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3246">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3247">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3247">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3248">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3248">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3249">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3249">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3250">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3250">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3251">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3251">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3252">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3252">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3253">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3254">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3254">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3255">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3255">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3256">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3256">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3257">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3257">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3258">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3258">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3259">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3259">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3260">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3260">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3261">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3261">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3262">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3262">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3263">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3263">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3264">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3264">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3265">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3265">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3266">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3266">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3267">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3267">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3268">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3268">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3269">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3269">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3270">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3270">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3271">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3271">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3272">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3272">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3273">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3273">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3274">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3274">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3275">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3275">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3276">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3276">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3277">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3277">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3278">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3278">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3279">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3279">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3280">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3280">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="73228-3281">DXGI_FORMAT_R16 \_ russar<sup>FNS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="73228-3281">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="73228-3282">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3282">Target</span></span> | <span data-ttu-id="73228-3283">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3283">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3284">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3284">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3285">16</span><span class="sxs-lookup"><span data-stu-id="73228-3285">16</span></span> |
| <span data-ttu-id="73228-3286">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3286">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3287">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3287">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3288">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3288">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3289">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3289">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3290">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3290">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3291">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3291">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3292">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3292">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3293">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3293">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3294">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3294">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3295">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3295">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3296">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3296">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3297">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3297">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3298">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3298">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3299">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3299">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3300">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3300">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3301">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3301">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3302">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3302">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3303">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3303">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3304">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3304">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3305">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3305">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3306">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3306">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3307">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3307">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3308">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3308">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3309">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3309">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3310">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3310">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3311">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3311">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3312">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3313">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3314">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3315">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3316">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3316">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3317">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3317">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3318">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3318">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3319">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3319">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3320">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3320">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3321">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3321">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3322">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3322">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3323">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3323">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3324">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3324">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3325">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3325">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3326">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3327">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3328">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3329">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3330">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="73228-3331">DXGI_FORMAT_R16 \_ Sint<sup>FNS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="73228-3331">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="73228-3332">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3332">Target</span></span> | <span data-ttu-id="73228-3333">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3334">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3335">16</span><span class="sxs-lookup"><span data-stu-id="73228-3335">16</span></span> |
| <span data-ttu-id="73228-3336">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3336">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3337">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3337">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3338">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3338">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3339">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3339">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3340">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3340">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3341">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3341">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3342">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3342">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3343">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3343">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3344">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3344">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3345">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3345">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3346">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3346">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3347">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3347">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3348">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3348">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3349">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3349">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3350">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3350">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3351">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3351">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3352">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3352">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3353">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3354">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3354">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3355">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3355">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3356">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3356">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3357">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3357">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3358">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3358">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3359">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3359">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3360">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3360">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3361">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3361">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3362">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3363">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3364">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3365">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3366">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3366">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3367">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3367">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3368">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3368">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3369">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3369">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3370">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3370">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3371">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3371">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3372">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3372">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3373">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3373">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3374">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3374">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3375">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3375">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3376">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3376">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3377">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3377">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3378">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3378">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3379">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3379">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3380">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3380">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="73228-3381">DXGI_FORMAT_R8 \_ <sup>PC</sup> non con tipi (60)</span><span class="sxs-lookup"><span data-stu-id="73228-3381">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="73228-3382">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3382">Target</span></span> | <span data-ttu-id="73228-3383">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3383">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3384">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3385">8</span><span class="sxs-lookup"><span data-stu-id="73228-3385">8</span></span> |
| <span data-ttu-id="73228-3386">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3386">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3387">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3387">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3388">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3389">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3390">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3391">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3392">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3393">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3393">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3394">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3395">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3395">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3396">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3396">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3397">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3397">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3398">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3398">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3399">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3399">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3400">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3400">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3401">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3401">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3402">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3402">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3403">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3403">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3404">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3404">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3405">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3405">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3406">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3406">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3407">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3407">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3408">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3408">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3409">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3409">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3410">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3410">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3411">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3411">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3412">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3412">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3413">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3413">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3414">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3414">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3415">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3415">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3416">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3416">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3417">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3417">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3418">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3418">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3419">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3419">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3420">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3420">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3421">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3421">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3422">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3422">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3423">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3423">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3424">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3424">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3425">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3425">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3426">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3426">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3427">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3427">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3428">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3428">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3429">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3429">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3430">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3430">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="73228-3431">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="73228-3431">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="73228-3432">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3432">Target</span></span> | <span data-ttu-id="73228-3433">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3433">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3434">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3434">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3435">8</span><span class="sxs-lookup"><span data-stu-id="73228-3435">8</span></span> |
| <span data-ttu-id="73228-3436">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3436">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3438">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3438">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3439">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3439">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3440">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3440">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3441">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3441">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3442">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3442">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3443">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3443">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3445">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3445">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3447">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3447">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3449">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3449">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3451">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3451">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3453">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3454">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3455">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3456">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3457">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3459">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3460">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3462">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3462">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3464">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3465">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3466">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3467">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3468">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3468">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3469">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3470">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3471">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3472">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3474">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3475">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3476">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3477">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3477">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3479">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3480">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3481">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3482">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3483">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3483">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3484">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3485">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3486">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3486">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3487">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3487">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3488">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3488">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3489">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3489">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3491">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="73228-3492">DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="73228-3492">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="73228-3493">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3493">Target</span></span> | <span data-ttu-id="73228-3494">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3494">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3495">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3496">8</span><span class="sxs-lookup"><span data-stu-id="73228-3496">8</span></span> |
| <span data-ttu-id="73228-3497">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3497">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3498">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3498">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3499">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3500">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3501">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3502">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3503">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3504">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3505">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3506">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3507">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3508">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3509">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3510">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3510">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3511">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3512">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3513">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3514">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3515">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3516">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3517">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3518">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3519">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3520">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3520">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3521">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3522">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3523">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3524">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3526">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3527">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3528">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3529">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3530">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3531">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3532">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3533">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3534">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3534">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3535">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3536">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3537">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3538">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3539">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3540">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3540">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3541">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="73228-3542">DXGI_FORMAT_R8 \_ russar<sup>FNS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="73228-3542">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="73228-3543">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3543">Target</span></span> | <span data-ttu-id="73228-3544">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3544">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3545">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3546">8</span><span class="sxs-lookup"><span data-stu-id="73228-3546">8</span></span> |
| <span data-ttu-id="73228-3547">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3547">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3548">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3548">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3549">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3550">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3551">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3552">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3553">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3554">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3555">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3556">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3557">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3558">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3559">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3560">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3560">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3561">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3562">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3563">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3564">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3565">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3566">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3567">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3568">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3569">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3570">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3570">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3571">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3572">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3573">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3574">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3576">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3577">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3578">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3579">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3580">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3581">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3582">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3583">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3584">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3584">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3585">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3586">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3587">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3588">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3589">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3590">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3590">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3591">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="73228-3592">DXGI_FORMAT_R8 \_ Sint<sup>FNS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="73228-3592">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="73228-3593">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3593">Target</span></span> | <span data-ttu-id="73228-3594">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3594">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3595">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3596">8</span><span class="sxs-lookup"><span data-stu-id="73228-3596">8</span></span> |
| <span data-ttu-id="73228-3597">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3597">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3598">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3599">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3600">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3601">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3602">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3603">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3604">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3605">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3606">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3607">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3608">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3609">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3610">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3610">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3611">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3612">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3613">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3614">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3615">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3616">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3617">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3618">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3619">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3620">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3620">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3621">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3622">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3623">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3624">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3626">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3627">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3628">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3629">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3630">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3631">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3632">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3633">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3634">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3634">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3635">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3636">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3637">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3638">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3639">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3640">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3640">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3641">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="73228-3642">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="73228-3642">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="73228-3643">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3643">Target</span></span> | <span data-ttu-id="73228-3644">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3644">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3645">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3646">8</span><span class="sxs-lookup"><span data-stu-id="73228-3646">8</span></span> |
| <span data-ttu-id="73228-3647">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3647">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3649">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3649">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3650">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3650">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3651">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3651">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3652">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3652">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3653">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3654">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3654">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3656">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3656">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3658">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3660">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3660">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3662">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3662">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3664">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3665">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3666">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3666">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3667">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3668">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3669">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3670">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3672">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3672">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3674">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3675">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3676">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3677">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3678">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3678">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3679">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3680">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3681">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3682">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3683">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3684">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3685">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3686">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3687">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3687">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3689">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3690">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3691">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3692">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3693">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3693">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3694">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3695">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3696">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3697">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3698">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3699">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3699">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3701">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="73228-3702">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="73228-3702">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="73228-3703">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3703">Target</span></span> | <span data-ttu-id="73228-3704">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3704">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3705">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3706">32</span><span class="sxs-lookup"><span data-stu-id="73228-3706">32</span></span> |
| <span data-ttu-id="73228-3707">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3707">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3708">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3708">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3709">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3709">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3710">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3710">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3711">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3711">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3712">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3712">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3713">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3713">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3714">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3714">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3715">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3716">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3716">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3717">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3717">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3718">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3718">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3719">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3719">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3720">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3720">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3721">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3721">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3722">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3722">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3723">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3724">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3725">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3725">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3726">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3726">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3727">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3727">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3728">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3728">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3729">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3729">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3730">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3730">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3731">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3731">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3732">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3732">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3733">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3733">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3734">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3734">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3735">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3735">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3736">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3736">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3737">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3737">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3738">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3738">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3739">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3739">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3740">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3740">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3741">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3741">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3742">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3742">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3743">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3743">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3744">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3744">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3745">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3746">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3746">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3747">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3747">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3748">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3748">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3749">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3749">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3750">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3750">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3751">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="73228-3752">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="73228-3752">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="73228-3753">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3753">Target</span></span> | <span data-ttu-id="73228-3754">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3754">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3755">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3756">16</span><span class="sxs-lookup"><span data-stu-id="73228-3756">16</span></span> |
| <span data-ttu-id="73228-3757">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3757">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3758">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3758">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3759">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3760">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3761">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3762">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3763">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3764">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3765">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3766">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3766">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3767">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3767">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3768">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3768">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3769">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3769">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3770">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3770">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3771">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3771">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3772">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3772">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3773">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3773">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3774">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3775">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3775">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3776">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3776">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3777">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3777">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3778">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3778">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3779">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3779">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3780">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3780">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3781">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3781">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3782">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3782">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3783">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3783">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3784">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3784">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3785">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3785">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3786">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3786">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3787">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3787">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3788">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3788">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3789">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3789">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3790">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3790">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3791">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3791">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3792">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3792">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3793">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3793">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3794">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3794">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3795">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3795">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3796">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3796">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3797">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3797">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3798">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3798">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3799">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3799">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3800">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3800">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3801">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3801">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="73228-3802">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="73228-3802">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="73228-3803">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3803">Target</span></span> | <span data-ttu-id="73228-3804">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3804">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3805">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3805">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3806">16</span><span class="sxs-lookup"><span data-stu-id="73228-3806">16</span></span> |
| <span data-ttu-id="73228-3807">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3807">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3808">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3808">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3809">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3810">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3811">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3812">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3813">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3814">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3814">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3815">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3815">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3816">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3816">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3817">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3817">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3818">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3818">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3819">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3819">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3820">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3820">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3821">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3821">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3822">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3822">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3823">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3823">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3824">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3824">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3825">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3825">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3826">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3826">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3827">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3827">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3828">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3828">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3829">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3829">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3830">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3830">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3831">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3831">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3832">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3832">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3833">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3833">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3834">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3834">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3835">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3835">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3836">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3836">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3837">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3837">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3838">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3838">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3839">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3839">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3840">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3841">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3842">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3843">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3844">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3845">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3846">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3847">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3848">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3849">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3850">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3850">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3851">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="73228-3852">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non tipizzato (70)</span><span class="sxs-lookup"><span data-stu-id="73228-3852">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="73228-3853">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3853">Target</span></span> | <span data-ttu-id="73228-3854">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3854">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3855">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3856">4</span><span class="sxs-lookup"><span data-stu-id="73228-3856">4</span></span> |
| <span data-ttu-id="73228-3857">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3857">Format Support</span></span> | \- |
| <span data-ttu-id="73228-3858">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3858">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3859">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3860">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3861">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3862">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3863">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-3864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3864">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3865">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-3866">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-3867">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-3868">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3869">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3870">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3870">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3871">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3872">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3872">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-3873">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3874">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3875">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3876">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3877">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3878">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3879">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3880">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3880">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3881">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3882">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3883">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3884">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3886">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3887">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3888">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3889">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-3890">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3891">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3892">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3893">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3894">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3894">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3895">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3896">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3897">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3898">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3899">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3900">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3900">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-3901">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="73228-3902">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="73228-3902">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="73228-3903">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3903">Target</span></span> | <span data-ttu-id="73228-3904">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3904">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3905">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3906">4</span><span class="sxs-lookup"><span data-stu-id="73228-3906">4</span></span> |
| <span data-ttu-id="73228-3907">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3907">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3909">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3909">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3910">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3911">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3912">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3913">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3914">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3916">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3917">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3917">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3919">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3919">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3921">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3921">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3923">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3923">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3924">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3924">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3925">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3925">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3926">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3926">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3927">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3927">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3929">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3929">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3930">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3930">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3931">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3931">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3932">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3932">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3933">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3933">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3934">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3934">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3935">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3935">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3936">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3936">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3937">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3937">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3938">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3938">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3939">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3939">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3940">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3940">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3941">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3941">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-3942">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3942">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-3943">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3943">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3944">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-3944">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-3945">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-3945">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3947">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-3947">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3948">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-3948">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3949">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-3949">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-3950">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3950">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-3951">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-3951">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-3952">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-3952">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-3953">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-3953">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-3954">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-3954">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-3955">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3955">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-3956">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-3956">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-3957">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-3957">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3959">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-3959">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="73228-3960">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FNC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="73228-3960">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="73228-3961">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3961">Target</span></span> | <span data-ttu-id="73228-3962">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-3962">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-3963">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-3963">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-3964">4</span><span class="sxs-lookup"><span data-stu-id="73228-3964">4</span></span> |
| <span data-ttu-id="73228-3965">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-3965">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3967">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-3967">Buffer</span></span> | \- |
| <span data-ttu-id="73228-3968">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-3968">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-3969">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-3969">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-3970">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-3970">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-3971">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-3971">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-3972">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-3972">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3974">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-3974">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-3975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-3975">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3977">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-3977">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3979">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-3979">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3981">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-3981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-3982">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-3982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-3983">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-3983">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-3984">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-3984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-3985">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3985">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-3987">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-3987">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-3988">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-3988">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3989">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-3989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-3990">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-3990">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-3991">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-3991">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-3992">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-3992">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3993">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-3993">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-3994">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-3994">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-3995">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3995">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-3996">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3996">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-3997">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3997">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-3998">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-3998">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-3999">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-3999">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4000">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4000">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4001">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4001">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4002">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4002">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4003">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4003">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4005">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4005">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4006">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4006">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4007">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4007">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4008">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4008">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4009">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4009">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4010">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4010">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4011">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4011">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4012">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4012">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4013">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4013">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4014">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4014">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4015">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4015">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4017">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="73228-4018">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non tipizzato (73)</span><span class="sxs-lookup"><span data-stu-id="73228-4018">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="73228-4019">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4019">Target</span></span> | <span data-ttu-id="73228-4020">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4020">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4021">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4022">8</span><span class="sxs-lookup"><span data-stu-id="73228-4022">8</span></span> |
| <span data-ttu-id="73228-4023">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4023">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4024">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4024">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4025">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4025">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4026">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4026">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4027">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4027">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4028">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4028">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4029">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4029">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4030">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4031">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4031">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4032">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4032">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4033">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4033">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4034">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4034">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4035">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4035">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4036">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4036">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4037">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4037">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4038">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4038">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4039">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4039">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4040">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4040">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4041">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4041">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4042">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4043">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4044">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4045">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4046">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4046">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4047">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4048">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4049">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4050">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4051">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4052">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4053">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4054">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4055">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4055">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4056">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4056">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4057">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4057">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4058">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4058">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4059">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4059">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4060">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4060">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4061">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4062">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4062">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4063">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4063">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4064">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4064">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4065">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4065">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4066">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4066">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4067">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4067">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="73228-4068">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="73228-4068">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="73228-4069">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4069">Target</span></span> | <span data-ttu-id="73228-4070">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4070">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4071">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4071">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4072">8</span><span class="sxs-lookup"><span data-stu-id="73228-4072">8</span></span> |
| <span data-ttu-id="73228-4073">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4073">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4075">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4075">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4076">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4076">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4077">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4077">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4078">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4078">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4079">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4079">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4080">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4080">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4082">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4082">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4083">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4083">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4085">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4085">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4087">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4087">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4089">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4089">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4090">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4090">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4091">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4091">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4092">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4092">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4093">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4093">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4095">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4096">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4097">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4098">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4099">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4100">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4101">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4102">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4102">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4103">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4104">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4105">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4106">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4108">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4109">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4110">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4111">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4111">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4113">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4113">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4114">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4114">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4115">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4115">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4116">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4116">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4117">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4117">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4118">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4118">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4119">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4119">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4120">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4120">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4121">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4121">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4122">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4122">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4123">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4123">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4125">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4125">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="73228-4126">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FNC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="73228-4126">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="73228-4127">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4127">Target</span></span> | <span data-ttu-id="73228-4128">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4128">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4129">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4129">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4130">8</span><span class="sxs-lookup"><span data-stu-id="73228-4130">8</span></span> |
| <span data-ttu-id="73228-4131">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4131">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4133">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4133">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4134">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4134">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4135">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4135">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4136">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4136">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4137">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4137">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4138">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4138">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4140">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4141">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4141">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4143">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4143">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4145">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4145">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4147">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4147">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4148">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4148">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4149">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4149">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4150">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4150">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4151">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4151">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4153">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4153">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4154">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4154">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4155">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4155">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4156">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4156">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4157">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4157">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4158">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4158">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4159">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4159">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4160">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4160">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4161">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4161">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4162">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4162">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4163">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4163">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4164">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4164">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4165">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4165">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4166">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4166">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4167">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4167">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4168">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4168">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4169">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4169">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4171">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4171">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4172">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4172">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4173">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4173">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4174">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4174">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4175">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4175">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4176">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4176">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4177">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4177">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4178">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4178">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4179">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4179">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4180">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4180">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4181">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4181">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4183">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4183">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="73228-4184">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non tipizzato (76)</span><span class="sxs-lookup"><span data-stu-id="73228-4184">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="73228-4185">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4185">Target</span></span> | <span data-ttu-id="73228-4186">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4186">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4187">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4187">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4188">8</span><span class="sxs-lookup"><span data-stu-id="73228-4188">8</span></span> |
| <span data-ttu-id="73228-4189">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4189">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4190">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4190">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4191">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4191">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4192">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4193">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4194">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4195">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4195">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4196">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4196">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4197">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4197">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4198">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4198">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4199">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4199">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4200">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4201">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4202">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4202">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4203">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4204">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4204">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4205">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4205">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4206">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4206">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4207">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4207">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4208">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4208">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4209">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4209">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4210">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4210">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4211">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4211">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4212">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4212">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4213">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4213">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4214">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4214">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4215">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4215">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4216">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4216">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4217">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4217">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4218">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4218">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4219">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4219">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4220">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4220">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4221">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4221">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4222">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4223">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4224">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4225">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4226">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4226">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4227">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4228">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4228">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4229">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4229">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4230">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4230">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4231">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4231">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4232">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4232">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4233">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4233">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="73228-4234">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="73228-4234">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="73228-4235">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4235">Target</span></span> | <span data-ttu-id="73228-4236">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4236">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4237">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4237">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4238">8</span><span class="sxs-lookup"><span data-stu-id="73228-4238">8</span></span> |
| <span data-ttu-id="73228-4239">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4239">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4241">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4241">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4242">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4242">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4243">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4244">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4244">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4245">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4245">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4246">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4246">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4248">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4248">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4249">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4249">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4251">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4251">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4253">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4253">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4255">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4256">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4257">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4257">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4258">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4259">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4259">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4261">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4261">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4262">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4262">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4263">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4263">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4264">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4264">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4265">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4265">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4266">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4266">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4267">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4267">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4268">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4268">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4269">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4269">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4270">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4270">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4271">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4271">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4272">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4272">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4273">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4273">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4274">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4274">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4275">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4275">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4276">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4276">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4277">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4277">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4279">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4280">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4281">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4282">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4283">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4283">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4284">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4285">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4286">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4287">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4288">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4289">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4289">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4291">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4291">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="73228-4292">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FNC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="73228-4292">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="73228-4293">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4293">Target</span></span> | <span data-ttu-id="73228-4294">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4294">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4295">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4295">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4296">8</span><span class="sxs-lookup"><span data-stu-id="73228-4296">8</span></span> |
| <span data-ttu-id="73228-4297">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4297">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4299">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4300">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4301">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4302">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4304">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4306">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4306">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4307">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4307">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4309">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4309">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4311">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4311">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4313">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4313">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4314">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4314">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4315">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4315">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4316">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4316">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4317">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4317">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4319">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4320">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4321">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4322">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4323">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4324">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4325">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4326">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4326">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4327">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4328">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4329">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4330">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4332">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4333">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4334">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4335">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4335">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4337">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4337">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4338">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4338">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4339">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4339">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4340">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4340">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4341">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4341">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4342">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4342">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4343">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4343">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4344">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4344">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4345">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4345">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4346">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4346">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4347">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4347">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4349">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4349">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="73228-4350">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non tipizzato (79)</span><span class="sxs-lookup"><span data-stu-id="73228-4350">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="73228-4351">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4351">Target</span></span> | <span data-ttu-id="73228-4352">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4352">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4353">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4353">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4354">4</span><span class="sxs-lookup"><span data-stu-id="73228-4354">4</span></span> |
| <span data-ttu-id="73228-4355">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4355">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4356">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4356">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4357">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4357">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4358">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4358">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4359">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4359">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4360">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4360">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4361">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4361">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4362">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4362">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4363">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4363">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4364">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4364">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4365">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4365">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4366">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4366">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4367">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4367">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4368">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4368">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4369">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4369">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4370">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4370">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4371">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4371">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4372">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4373">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4374">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4375">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4376">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4377">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4378">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4379">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4380">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4381">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4382">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4383">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4384">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4385">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4386">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4387">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4387">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4388">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4388">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4389">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4389">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4390">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4390">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4391">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4391">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4392">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4392">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4393">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4393">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4394">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4394">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4395">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4395">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4396">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4396">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4397">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4397">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4398">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4398">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4399">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4399">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="73228-4400">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="73228-4400">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="73228-4401">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4401">Target</span></span> | <span data-ttu-id="73228-4402">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4402">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4403">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4403">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4404">4</span><span class="sxs-lookup"><span data-stu-id="73228-4404">4</span></span> |
| <span data-ttu-id="73228-4405">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4405">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4406">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4406">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4407">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4407">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4408">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4408">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4409">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4409">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4410">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4410">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4411">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4411">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4412">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4412">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4413">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4413">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4414">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4414">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4415">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4415">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4416">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4416">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4417">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4417">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4418">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4418">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4419">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4420">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4420">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4421">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4422">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4423">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4424">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4425">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4426">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4427">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4428">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4429">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4430">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4431">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4432">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4433">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4434">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4435">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4436">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4437">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4437">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4438">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4438">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4439">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4439">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4440">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4440">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4441">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4442">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4442">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4443">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4443">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4444">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4444">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4445">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4445">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4446">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4446">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4447">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4447">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4448">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4448">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4449">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="73228-4450">DXGI_FORMAT_BC4 \_ russar<sup>FNC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="73228-4450">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="73228-4451">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4451">Target</span></span> | <span data-ttu-id="73228-4452">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4452">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4453">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4454">4</span><span class="sxs-lookup"><span data-stu-id="73228-4454">4</span></span> |
| <span data-ttu-id="73228-4455">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4455">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4456">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4456">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4457">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4457">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4458">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4458">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4459">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4459">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4460">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4460">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4461">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4461">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4462">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4462">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4463">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4463">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4464">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4464">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4465">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4465">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4466">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4466">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4467">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4467">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4468">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4468">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4469">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4469">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4470">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4470">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4471">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4471">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4472">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4473">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4474">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4475">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4476">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4477">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4478">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4478">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4479">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4479">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4480">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4480">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4481">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4481">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4482">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4482">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4483">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4483">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4484">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4484">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4485">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4485">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4486">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4486">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4487">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4487">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4488">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4489">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4490">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4491">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4492">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4492">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4493">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4494">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4494">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4495">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4496">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4497">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4498">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4498">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4499">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="73228-4500">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non tipizzato (82)</span><span class="sxs-lookup"><span data-stu-id="73228-4500">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="73228-4501">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4501">Target</span></span> | <span data-ttu-id="73228-4502">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4502">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4503">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4504">8</span><span class="sxs-lookup"><span data-stu-id="73228-4504">8</span></span> |
| <span data-ttu-id="73228-4505">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4505">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4506">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4506">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4507">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4507">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4508">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4508">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4509">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4509">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4510">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4510">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4511">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4512">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4513">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4514">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4515">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4516">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4517">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4518">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4518">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4519">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4520">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4520">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4521">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4522">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4523">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4524">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4525">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4525">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4526">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4526">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4527">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4527">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4528">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4528">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4529">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4529">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4530">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4530">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4531">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4531">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4532">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4532">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4533">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4533">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4534">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4534">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4535">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4535">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4536">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4536">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4537">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4537">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4538">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4538">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4539">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4539">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4540">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4540">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4541">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4541">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4542">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4542">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4543">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4544">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4544">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4545">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4545">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4546">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4546">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4547">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4547">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4548">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4548">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4549">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4549">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="73228-4550">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="73228-4550">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="73228-4551">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4551">Target</span></span> | <span data-ttu-id="73228-4552">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4552">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4553">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4553">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4554">8</span><span class="sxs-lookup"><span data-stu-id="73228-4554">8</span></span> |
| <span data-ttu-id="73228-4555">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4555">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4556">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4556">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4557">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4557">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4558">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4558">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4559">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4559">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4560">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4560">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4561">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4561">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4562">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4562">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4563">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4563">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4564">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4564">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4565">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4565">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4566">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4567">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4568">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4569">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4570">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4570">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4571">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4571">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4572">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4573">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4573">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4574">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4574">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4575">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4575">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4576">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4576">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4577">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4577">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4578">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4578">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4579">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4579">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4580">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4580">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4581">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4581">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4582">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4582">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4583">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4583">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4584">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4584">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4585">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4585">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4586">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4586">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4587">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4587">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4588">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4588">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4589">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4589">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4590">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4590">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4591">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4591">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4592">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4592">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4593">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4593">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4594">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4594">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4595">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4595">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4596">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4596">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4597">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4597">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4598">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4598">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4599">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4599">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="73228-4600">DXGI_FORMAT_BC5 \_ russar<sup>FNC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="73228-4600">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="73228-4601">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4601">Target</span></span> | <span data-ttu-id="73228-4602">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4602">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4603">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4603">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4604">8</span><span class="sxs-lookup"><span data-stu-id="73228-4604">8</span></span> |
| <span data-ttu-id="73228-4605">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4605">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4606">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4606">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4607">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4607">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4608">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4609">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4610">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4611">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4612">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4612">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4613">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4613">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4614">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4614">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4615">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4615">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4616">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4616">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4617">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4617">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4618">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4618">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4619">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4619">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4620">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4620">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4621">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4621">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4622">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4622">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4623">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4623">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4624">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4624">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4625">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4625">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4626">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4626">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4627">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4627">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4628">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4628">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4629">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4629">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4630">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4630">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4631">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4631">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4632">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4632">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4633">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4633">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4634">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4634">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4635">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4635">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4636">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4636">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4637">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4637">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4638">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4638">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4639">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4639">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4640">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4640">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4641">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4642">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4642">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4643">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4643">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4644">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4644">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4645">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4645">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4646">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4646">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4647">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4647">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4648">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4648">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4649">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4649">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="73228-4650">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="73228-4650">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="73228-4651">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4651">Target</span></span> | <span data-ttu-id="73228-4652">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4652">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4653">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4653">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4654">16</span><span class="sxs-lookup"><span data-stu-id="73228-4654">16</span></span> |
| <span data-ttu-id="73228-4655">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4655">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4657">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4657">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4658">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4659">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4660">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4661">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4662">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4664">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4664">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4665">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4665">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4667">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4667">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4669">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4669">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4671">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4671">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4672">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4672">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4673">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4673">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4674">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4674">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4675">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4675">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4677">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4677">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4679">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4679">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4681">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4681">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4683">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4683">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4684">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4684">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4685">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4685">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4686">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4686">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4687">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4687">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4688">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4688">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4689">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4689">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4690">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4690">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4691">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4691">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4692">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4692">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4693">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4693">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4694">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4694">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4695">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4695">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4696">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4696">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4698">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4698">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4700">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4700">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4702">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4702">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4704">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4704">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4706">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4707">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4708">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4709">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4710">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4711">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4712">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4713">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="73228-4714">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="73228-4714">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="73228-4715">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4715">Target</span></span> | <span data-ttu-id="73228-4716">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4717">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4718">16</span><span class="sxs-lookup"><span data-stu-id="73228-4718">16</span></span> |
| <span data-ttu-id="73228-4719">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4719">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4721">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4722">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4723">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4724">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4726">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4728">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4729">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4729">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4731">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4731">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4733">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4733">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4735">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4735">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4736">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4736">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4737">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4737">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4738">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4738">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4739">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4739">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4741">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4741">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4742">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4743">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4744">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4745">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4746">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4747">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4748">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4748">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4749">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4750">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4751">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4752">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4754">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4755">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4756">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4757">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4757">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4759">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4759">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4760">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4760">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4761">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4761">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4762">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4762">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4763">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4763">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4764">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4764">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4765">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4765">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4766">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4767">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4768">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4769">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4769">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4770">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4770">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="73228-4771">DXGI_FORMAT_B8G8R8A8 \_ <sup>PC</sup> non con tipi (90)</span><span class="sxs-lookup"><span data-stu-id="73228-4771">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="73228-4772">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4772">Target</span></span> | <span data-ttu-id="73228-4773">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4773">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4774">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4774">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4775">32</span><span class="sxs-lookup"><span data-stu-id="73228-4775">32</span></span> |
| <span data-ttu-id="73228-4776">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4776">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4777">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4777">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4778">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4778">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4779">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4779">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4780">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4780">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4781">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4781">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4782">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4782">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4783">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4783">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4784">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4785">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4785">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4786">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4786">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4787">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4787">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4788">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4788">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4789">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4789">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4790">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4790">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4791">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4791">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4792">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4792">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4793">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4794">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4794">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4795">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4795">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4796">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4796">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4797">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4797">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4798">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4798">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4799">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4799">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4800">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4800">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4801">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4801">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4802">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4802">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4803">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4803">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4804">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4804">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4805">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4805">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4806">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4806">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4807">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4807">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4808">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4808">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4809">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4809">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4810">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4810">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4811">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4811">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-4812">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4812">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-4813">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4813">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4814">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4814">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-4815">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4815">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4816">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4816">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4817">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4817">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-4818">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4818">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-4819">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4819">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-4820">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4820">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="73228-4821">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="73228-4821">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="73228-4822">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4822">Target</span></span> | <span data-ttu-id="73228-4823">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4823">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4824">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4824">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4825">32</span><span class="sxs-lookup"><span data-stu-id="73228-4825">32</span></span> |
| <span data-ttu-id="73228-4826">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4826">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4828">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4828">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4829">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4829">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4830">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4830">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4831">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4831">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4832">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4832">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4833">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4833">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4835">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4835">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4837">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4837">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4839">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4839">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4841">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4841">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4843">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4844">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4845">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4845">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4846">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4847">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4847">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4849">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4849">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4851">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4851">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4853">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4853">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4855">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4855">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4856">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4856">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4857">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4857">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4858">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4858">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4859">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4859">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4860">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4860">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4861">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4861">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4862">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4862">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4863">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4863">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4864">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4864">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4865">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4865">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4866">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4866">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4867">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4867">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4868">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4868">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4870">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4870">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4872">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4872">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4874">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4874">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4876">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4876">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4878">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4878">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4879">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4879">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4881">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4882">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4883">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4883">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4885">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4885">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4887">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4887">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4889">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="73228-4890">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="73228-4890">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="73228-4891">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4891">Target</span></span> | <span data-ttu-id="73228-4892">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4892">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4893">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4894">32</span><span class="sxs-lookup"><span data-stu-id="73228-4894">32</span></span> |
| <span data-ttu-id="73228-4895">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4895">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4897">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4897">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4898">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4898">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4899">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4899">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4900">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4900">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4901">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4901">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4902">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4902">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4904">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4904">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4906">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4906">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4908">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4908">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4910">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4910">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4912">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4912">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4913">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4913">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4914">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4914">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4915">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4915">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4916">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4916">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4918">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4918">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4920">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4920">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4922">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4922">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4924">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4924">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4925">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4925">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4926">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4926">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4927">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4927">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4928">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4928">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4929">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4929">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4930">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4930">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4931">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4931">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4932">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4932">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4933">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4933">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4934">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4934">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4935">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4935">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4936">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4936">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4937">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4937">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4939">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4939">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4941">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4941">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4943">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4943">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4945">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4945">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4947">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-4947">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-4948">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-4948">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4950">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-4950">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-4951">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-4951">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-4952">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4952">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-4954">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-4954">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4956">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-4956">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-4958">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-4958">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="73228-4959">DXGI_FORMAT_B8G8R8X8 \_ <sup>PC</sup> non con tipi (92)</span><span class="sxs-lookup"><span data-stu-id="73228-4959">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="73228-4960">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4960">Target</span></span> | <span data-ttu-id="73228-4961">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-4961">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-4962">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-4962">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-4963">32</span><span class="sxs-lookup"><span data-stu-id="73228-4963">32</span></span> |
| <span data-ttu-id="73228-4964">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-4964">Format Support</span></span> | \- |
| <span data-ttu-id="73228-4965">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-4965">Buffer</span></span> | \- |
| <span data-ttu-id="73228-4966">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-4966">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-4967">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-4967">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-4968">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-4968">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-4969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-4969">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-4970">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-4970">Texture2D</span></span> | \- |
| <span data-ttu-id="73228-4971">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-4971">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-4972">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-4973">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-4973">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-4974">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-4974">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-4975">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-4975">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-4976">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-4976">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-4977">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-4977">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-4978">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-4978">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-4979">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4979">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-4980">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-4980">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-4981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-4981">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4982">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-4982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4983">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-4983">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-4984">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-4984">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-4985">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-4985">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4986">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-4986">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-4987">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-4987">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-4988">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4988">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-4989">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4989">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-4990">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4990">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-4991">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4991">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-4992">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-4992">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-4993">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4993">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-4994">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-4994">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4995">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-4995">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-4996">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-4996">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-4997">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-4997">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4998">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-4998">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-4999">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-4999">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5000">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5000">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5001">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5001">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5002">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5002">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5003">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5003">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5004">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5004">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-5005">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5005">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-5006">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5006">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-5007">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5007">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5008">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="73228-5009">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="73228-5009">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="73228-5010">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5010">Target</span></span> | <span data-ttu-id="73228-5011">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5012">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5013">32</span><span class="sxs-lookup"><span data-stu-id="73228-5013">32</span></span> |
| <span data-ttu-id="73228-5014">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5014">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5016">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5017">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5018">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5019">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5021">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5023">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5025">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5027">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5027">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5029">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5029">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5031">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5032">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5033">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5033">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5034">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5035">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5037">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5037">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5039">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5041">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5041">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5043">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5044">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5045">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5046">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5047">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5047">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5048">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5049">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5050">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5051">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5052">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5053">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5054">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5055">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5056">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5056">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5058">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5058">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5060">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5060">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5062">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5062">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5064">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5064">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5066">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5067">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5068">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5069">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-5070">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5070">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5072">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5072">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5074">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5074">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5076">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="73228-5077">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FNS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="73228-5077">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="73228-5078">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5078">Target</span></span> | <span data-ttu-id="73228-5079">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5079">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5080">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5081">32</span><span class="sxs-lookup"><span data-stu-id="73228-5081">32</span></span> |
| <span data-ttu-id="73228-5082">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5082">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5084">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5084">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5085">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5085">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5086">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5086">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5087">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5087">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5088">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5088">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5089">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5091">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5093">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5095">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5095">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5097">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5097">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5099">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5100">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5101">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5101">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5102">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5103">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5103">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5105">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5105">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5107">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5109">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5109">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5111">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5112">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5113">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5114">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5115">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5115">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5116">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5117">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5118">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5119">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5120">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5121">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5122">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5123">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5124">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5124">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5126">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5126">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5128">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5128">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5130">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5130">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5132">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5132">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5134">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5134">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5135">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5135">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5136">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5136">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5137">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-5138">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-5139">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-5140">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5140">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5142">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5142">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="73228-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="73228-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="73228-5144">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5144">Target</span></span> | <span data-ttu-id="73228-5145">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5145">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5146">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5146">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5147">32</span><span class="sxs-lookup"><span data-stu-id="73228-5147">32</span></span> |
| <span data-ttu-id="73228-5148">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5148">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5150">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5150">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5151">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5151">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5152">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5152">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5153">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5153">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5154">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5154">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5155">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5157">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5158">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5159">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5159">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5160">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5160">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5161">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5161">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5162">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5162">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5163">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5163">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5164">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5164">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5165">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5165">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5166">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5166">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5167">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5167">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5168">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5168">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5169">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5169">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5170">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5170">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5171">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5171">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5172">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5172">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5173">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5173">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5174">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5174">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5175">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5175">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5176">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5176">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5177">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5177">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5178">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5179">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5179">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5180">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5180">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5181">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5181">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5182">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5182">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5184">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5185">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5186">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5187">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5188">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5188">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5189">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5190">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5191">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5191">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5193">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5193">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5195">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5195">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5197">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5197">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5198">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5198">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="73228-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="73228-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="73228-5200">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5200">Target</span></span> | <span data-ttu-id="73228-5201">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5201">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5202">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5202">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5203">32</span><span class="sxs-lookup"><span data-stu-id="73228-5203">32</span></span> |
| <span data-ttu-id="73228-5204">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5204">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5206">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5206">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5207">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5207">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5208">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5208">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5209">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5209">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5210">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5210">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5211">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5213">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5214">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5214">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5215">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5215">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5216">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5216">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5217">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5217">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5218">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5218">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5219">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5219">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5220">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5220">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5221">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5221">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5222">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5224">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5225">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5226">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5227">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5228">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5229">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5230">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5231">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5232">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5233">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5234">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5235">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5236">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5237">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5238">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5238">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5240">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5241">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5242">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5243">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5244">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5245">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5246">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5246">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5247">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5247">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5249">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5249">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5251">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5251">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5253">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5253">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5254">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5254">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="73228-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="73228-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="73228-5256">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5256">Target</span></span> | <span data-ttu-id="73228-5257">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5258">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5259">64</span><span class="sxs-lookup"><span data-stu-id="73228-5259">64</span></span> |
| <span data-ttu-id="73228-5260">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5260">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5262">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5263">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5264">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5265">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5267">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5269">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5270">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5271">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5271">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5272">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5272">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5273">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5273">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5274">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5274">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5275">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5275">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5276">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5276">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5277">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5277">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5278">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5279">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5280">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5281">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5282">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5283">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5284">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5285">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5285">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5286">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5287">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5288">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5289">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5290">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5291">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5292">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5293">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5294">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5294">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5296">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5297">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5298">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5299">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5300">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5300">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5301">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5302">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5303">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5303">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5305">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5305">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5307">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5307">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5309">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5310">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="73228-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="73228-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="73228-5312">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5312">Target</span></span> | <span data-ttu-id="73228-5313">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5314">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5315">8</span><span class="sxs-lookup"><span data-stu-id="73228-5315">8</span></span> |
| <span data-ttu-id="73228-5316">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5316">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5318">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5319">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5320">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5321">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5323">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5325">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5326">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5326">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5327">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5327">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5328">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5328">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5329">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5329">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5330">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5330">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5331">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5331">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5332">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5332">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5333">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5333">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5334">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5334">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5335">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5335">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5336">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5336">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5337">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5337">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5338">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5338">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5339">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5339">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5340">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5340">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5341">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5341">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5342">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5342">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5343">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5343">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5344">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5344">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5345">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5345">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5346">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5346">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5347">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5347">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5348">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5348">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5349">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5349">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5350">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5350">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5352">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5352">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5353">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5353">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5354">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5354">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5355">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5355">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5356">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5356">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5357">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5357">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5358">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5358">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5359">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5359">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5361">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5361">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5363">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5363">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5365">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5365">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5366">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5366">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="73228-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="73228-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="73228-5368">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5368">Target</span></span> | <span data-ttu-id="73228-5369">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5369">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5370">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5370">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5371">16</span><span class="sxs-lookup"><span data-stu-id="73228-5371">16</span></span> |
| <span data-ttu-id="73228-5372">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5372">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5374">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5374">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5375">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5375">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5376">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5376">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5377">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5377">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5378">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5378">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5379">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5379">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5381">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5381">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5382">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5382">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5383">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5383">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5384">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5384">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5385">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5385">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5386">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5386">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5387">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5387">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5388">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5388">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5389">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5389">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5390">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5390">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5391">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5391">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5392">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5392">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5393">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5393">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5394">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5394">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5395">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5395">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5396">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5396">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5397">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5397">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5398">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5398">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5399">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5399">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5400">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5400">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5401">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5401">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5402">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5402">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5403">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5403">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5404">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5404">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5405">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5405">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5406">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5406">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5408">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5408">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5409">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5409">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5410">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5410">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5411">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5411">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5412">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5412">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5413">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5413">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5414">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5414">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5415">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5415">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5417">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5417">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5419">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5419">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5421">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5421">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5422">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="73228-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="73228-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="73228-5424">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5424">Target</span></span> | <span data-ttu-id="73228-5425">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5425">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5426">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5427">16</span><span class="sxs-lookup"><span data-stu-id="73228-5427">16</span></span> |
| <span data-ttu-id="73228-5428">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5428">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5430">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5430">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5431">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5431">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5432">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5432">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5433">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5433">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5434">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5434">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5435">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5435">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5437">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5438">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5439">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5440">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5441">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5442">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5443">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5443">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5444">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5445">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5446">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5447">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5448">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5448">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5449">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5449">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5450">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5450">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5451">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5451">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5452">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5452">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5453">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5453">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5454">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5454">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5455">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5455">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5456">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5456">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5457">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5457">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5458">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5458">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5459">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5459">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5460">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5460">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5461">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5461">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5462">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5462">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5464">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5464">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5465">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5465">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5466">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5466">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5467">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5467">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5468">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5468">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5469">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5469">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5470">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5470">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5471">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5471">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5473">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5473">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5475">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5475">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5477">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5477">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5478">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5478">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="73228-5479">DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="73228-5479">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="73228-5480">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5480">Target</span></span> | <span data-ttu-id="73228-5481">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5481">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5482">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5482">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5483">8</span><span class="sxs-lookup"><span data-stu-id="73228-5483">8</span></span> |
| <span data-ttu-id="73228-5484">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5484">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5486">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5486">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5487">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5487">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5488">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5488">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5489">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5489">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5490">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5490">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5491">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5491">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5493">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5493">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5494">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5494">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5495">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5495">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5496">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5496">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5497">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5497">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5498">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5498">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5499">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5499">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5500">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5500">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5501">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5501">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5502">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5502">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5503">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5503">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5504">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5504">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5505">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5505">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5506">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5506">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5507">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5507">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5508">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5508">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5509">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5509">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5510">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5510">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5511">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5511">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5512">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5512">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5513">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5513">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5514">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5514">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5515">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5515">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5516">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5516">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5517">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5517">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5518">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5518">CPU Lockable</span></span> | \- |
| <span data-ttu-id="73228-5519">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5519">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5520">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5520">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5521">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5521">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5522">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5522">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5523">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5523">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5524">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5524">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5525">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5525">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5526">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5526">Video Decoder Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5528">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5528">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5530">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5530">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5532">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5532">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5533">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5533">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="73228-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="73228-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="73228-5535">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5535">Target</span></span> | <span data-ttu-id="73228-5536">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5536">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5537">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5537">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5538">16</span><span class="sxs-lookup"><span data-stu-id="73228-5538">16</span></span> |
| <span data-ttu-id="73228-5539">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5539">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5541">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5541">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5542">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5542">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5543">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5543">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5544">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5544">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5545">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5545">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5546">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5546">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5548">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5548">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5549">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5549">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5550">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5550">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5551">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5552">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5553">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5554">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5554">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5555">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5556">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5557">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5557">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5558">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5558">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5559">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5559">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5560">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5560">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5561">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5561">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5562">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5562">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5563">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5563">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5564">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5564">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5565">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5565">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5566">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5566">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5567">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5567">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5568">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5568">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5569">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5569">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5570">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5570">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5571">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5571">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5572">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5572">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5573">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5573">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5575">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5575">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5576">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5576">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5577">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5577">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5578">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5578">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5579">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5579">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5580">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5580">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5581">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5581">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5582">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5582">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5584">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5584">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5586">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5586">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5588">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5588">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5589">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="73228-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="73228-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="73228-5591">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5591">Target</span></span> | <span data-ttu-id="73228-5592">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5592">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5593">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5594">32</span><span class="sxs-lookup"><span data-stu-id="73228-5594">32</span></span> |
| <span data-ttu-id="73228-5595">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5595">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5597">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5597">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5598">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5598">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5599">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5599">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5600">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5600">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5601">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5601">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5602">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5602">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5604">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5605">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5606">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5607">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5608">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5609">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5610">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5610">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5611">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5612">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5613">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5614">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5615">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5616">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5617">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5618">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5619">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5620">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5620">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5621">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5622">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5623">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5624">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5626">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5627">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5628">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5629">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5629">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5631">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5632">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5633">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5634">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5635">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5635">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5636">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5637">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5638">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5638">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5640">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5640">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5642">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5642">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5644">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5644">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5645">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5645">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="73228-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="73228-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="73228-5647">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5647">Target</span></span> | <span data-ttu-id="73228-5648">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5648">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5649">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5649">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5650">32</span><span class="sxs-lookup"><span data-stu-id="73228-5650">32</span></span> |
| <span data-ttu-id="73228-5651">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5651">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5653">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5653">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5654">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5654">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5655">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5655">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5656">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5656">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5657">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5657">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5658">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5658">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5660">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5660">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5661">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5662">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5662">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5663">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5664">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5665">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5666">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5666">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5667">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5668">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5669">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5670">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5671">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5671">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5672">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5672">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5673">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5673">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5674">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5674">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5675">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5675">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5676">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5676">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5677">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5677">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5678">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5678">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5679">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5679">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5680">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5680">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5681">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5681">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5682">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5682">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5683">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5683">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5684">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5684">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5685">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5685">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5687">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5687">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5688">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5688">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5689">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5689">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5690">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5690">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5691">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5691">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5692">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5692">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5693">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5693">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5694">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5694">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5696">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5696">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5698">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5698">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5700">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5700">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5701">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="73228-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="73228-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="73228-5703">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5703">Target</span></span> | <span data-ttu-id="73228-5704">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5704">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5705">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5706">8</span><span class="sxs-lookup"><span data-stu-id="73228-5706">8</span></span> |
| <span data-ttu-id="73228-5707">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5707">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5709">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5709">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5710">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5711">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5712">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5713">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5714">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5716">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5717">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5717">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5718">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5718">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5719">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5719">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5720">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5720">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5721">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5721">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5722">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5722">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5723">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5723">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5724">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5724">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5725">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5725">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5726">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5727">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5728">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5729">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5730">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5731">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5732">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5732">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5733">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5734">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5735">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5736">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5737">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5738">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5739">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5739">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5740">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5740">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5741">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5741">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5743">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5744">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5745">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5746">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5747">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5747">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5748">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5749">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5749">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5750">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5750">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5752">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5752">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5754">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5754">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5756">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5756">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5757">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5757">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="73228-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="73228-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="73228-5759">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5759">Target</span></span> | <span data-ttu-id="73228-5760">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5760">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5761">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5761">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5762">8</span><span class="sxs-lookup"><span data-stu-id="73228-5762">8</span></span> |
| <span data-ttu-id="73228-5763">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5763">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5765">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5765">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5766">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5766">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5767">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5767">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5768">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5768">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5769">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5769">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5770">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5770">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5772">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5772">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5773">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5773">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5774">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5774">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5775">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5776">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5777">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5778">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5778">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5779">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5780">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5781">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5782">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5783">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5783">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5784">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5784">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5785">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5785">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5786">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5786">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5787">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5787">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5788">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5788">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5789">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5789">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5790">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5790">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5791">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5791">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5792">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5792">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5793">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5793">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5794">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5794">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5795">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5795">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5796">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5796">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5797">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5797">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5799">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5799">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5800">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5800">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5801">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5801">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5802">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5802">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5803">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5803">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5804">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5804">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5805">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5805">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5806">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-5807">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5807">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5809">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-5810">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5810">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5811">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="73228-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="73228-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="73228-5813">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5813">Target</span></span> | <span data-ttu-id="73228-5814">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5814">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5815">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5816">8</span><span class="sxs-lookup"><span data-stu-id="73228-5816">8</span></span> |
| <span data-ttu-id="73228-5817">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5817">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5819">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5819">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5820">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5821">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5822">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5823">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5824">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5826">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5827">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5828">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5828">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5829">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5829">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5830">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5830">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5831">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5831">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5832">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5832">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5833">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5833">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5834">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5834">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5835">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5835">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5836">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5836">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5837">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5837">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5838">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5839">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5840">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5841">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5842">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5843">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5844">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5845">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5846">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5847">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5848">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5849">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5850">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5851">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5851">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5853">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5853">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5854">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5854">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5855">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5855">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5856">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5856">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5857">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5857">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5858">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5858">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5859">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5859">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5860">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5860">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-5861">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5861">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5863">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5863">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-5864">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5864">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5865">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5865">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="73228-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="73228-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="73228-5867">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5867">Target</span></span> | <span data-ttu-id="73228-5868">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5868">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5869">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5869">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5870">8</span><span class="sxs-lookup"><span data-stu-id="73228-5870">8</span></span> |
| <span data-ttu-id="73228-5871">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5871">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5873">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5873">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5874">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5874">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5875">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5875">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5876">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5876">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5877">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5877">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5878">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5878">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5880">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5881">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5882">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5883">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5884">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5885">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5886">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5886">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5887">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5888">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5888">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5889">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5890">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5891">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5892">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5893">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5894">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5895">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5896">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5897">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5898">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5899">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5900">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5902">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5903">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5904">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5905">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5905">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5907">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5907">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5908">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5908">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5909">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5909">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5910">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5910">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5911">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5911">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5912">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5912">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5913">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5913">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5914">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5914">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-5915">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5915">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5917">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5917">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-5918">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5918">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5919">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5919">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="73228-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="73228-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="73228-5921">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5921">Target</span></span> | <span data-ttu-id="73228-5922">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5922">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5923">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5924">16</span><span class="sxs-lookup"><span data-stu-id="73228-5924">16</span></span> |
| <span data-ttu-id="73228-5925">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5925">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-5927">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5927">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5928">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5929">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5930">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5931">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5932">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5934">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5935">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5935">TextureCube</span></span> | \- |
| <span data-ttu-id="73228-5936">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5936">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="73228-5937">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5937">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="73228-5938">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5938">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5939">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5939">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5940">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5940">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5941">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5941">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5942">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5942">Mipmap</span></span> | \- |
| <span data-ttu-id="73228-5943">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5943">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="73228-5944">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-5944">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5945">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-5945">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5946">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-5946">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-5947">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5947">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-5948">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-5948">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5949">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-5949">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-5950">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-5950">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-5951">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5951">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-5952">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5952">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-5953">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5953">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-5954">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5954">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-5955">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-5955">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-5956">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5956">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-5957">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-5957">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5958">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-5958">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-5959">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-5959">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5961">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-5961">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5962">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-5962">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-5963">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-5963">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-5964">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5964">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-5965">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-5965">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-5966">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-5966">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-5967">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-5967">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-5968">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-5968">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-5969">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5969">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5971">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-5971">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-5972">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-5972">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-5973">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-5973">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="73228-5974">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="73228-5974">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="73228-5975">Destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-5975">Target</span></span> | <span data-ttu-id="73228-5976">Supporto</span><span class="sxs-lookup"><span data-stu-id="73228-5976">Support</span></span> |
| - | - |
| <span data-ttu-id="73228-5977">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="73228-5977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="73228-5978">16</span><span class="sxs-lookup"><span data-stu-id="73228-5978">16</span></span> |
| <span data-ttu-id="73228-5979">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="73228-5979">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5981">Buffer</span><span class="sxs-lookup"><span data-stu-id="73228-5981">Buffer</span></span> | \- |
| <span data-ttu-id="73228-5982">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="73228-5982">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="73228-5983">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="73228-5983">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="73228-5984">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="73228-5984">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="73228-5985">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73228-5985">Texture1D</span></span> | \- |
| <span data-ttu-id="73228-5986">Texture2D</span><span class="sxs-lookup"><span data-stu-id="73228-5986">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5988">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73228-5988">Texture3D</span></span> | \- |
| <span data-ttu-id="73228-5989">TextureCube</span><span class="sxs-lookup"><span data-stu-id="73228-5989">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5991">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="73228-5991">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5993">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="73228-5993">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-5995">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="73228-5995">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="73228-5996">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="73228-5996">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="73228-5997">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="73228-5997">Shader gather4</span></span> | \- |
| <span data-ttu-id="73228-5998">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="73228-5998">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="73228-5999">Mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-5999">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-6001">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="73228-6001">Mipmap Auto-Generation</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="73228-6003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="73228-6003">RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-6004">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="73228-6004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-6005">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="73228-6005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="73228-6006">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="73228-6006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="73228-6007">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="73228-6007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-6008">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="73228-6008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="73228-6009">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-6009">Typed UAV</span></span> | \- |
| <span data-ttu-id="73228-6010">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="73228-6010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="73228-6011">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="73228-6011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="73228-6012">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="73228-6012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="73228-6013">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="73228-6013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="73228-6014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="73228-6014">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="73228-6015">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-6015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="73228-6016">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="73228-6016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="73228-6017">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="73228-6017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="73228-6018">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="73228-6018">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="73228-6020">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="73228-6020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-6021">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="73228-6021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="73228-6022">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="73228-6022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="73228-6023">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-6023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="73228-6024">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="73228-6024">Multisample Load</span></span> | \- |
| <span data-ttu-id="73228-6025">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="73228-6025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="73228-6026">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="73228-6026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="73228-6027">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="73228-6027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="73228-6028">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-6028">Video Processor Input</span></span> | \- |
| <span data-ttu-id="73228-6029">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="73228-6029">Video Processor Output</span></span> | \- |
| <span data-ttu-id="73228-6030">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="73228-6030">Shared Resource</span></span> | \- |
| <span data-ttu-id="73228-6031">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="73228-6031">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="73228-6032">Note sul formato</span><span class="sxs-lookup"><span data-stu-id="73228-6032">Format notes</span></span>

<span data-ttu-id="73228-6033">Lo scopo del formato può variare da un livello di funzionalità hardware a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="73228-6033">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="73228-6034"><sup>L</sup> : formato non tipizzato</span><span class="sxs-lookup"><span data-stu-id="73228-6034"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="73228-6035"><sup>PC</sup> : layout parzialmente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="73228-6035"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="73228-6036"><sup>FCS</sup> : layout completamente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="73228-6036"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="73228-6037"><sup>FNS</sup> : layout completamente tipizzato, non ristabile e semplice</span><span class="sxs-lookup"><span data-stu-id="73228-6037"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="73228-6038"><sup>PCC</sup> : layout parzialmente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="73228-6038"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="73228-6039"><sup>FCC</sup> : layout completamente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="73228-6039"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="73228-6040"><sup>FNC</sup> : layout completamente tipizzato, non ristabile e complesso</span><span class="sxs-lookup"><span data-stu-id="73228-6040"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="73228-6041"><sup>V</sup> : formato video</span><span class="sxs-lookup"><span data-stu-id="73228-6041"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="73228-6042">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73228-6042">Related topics</span></span>

[<span data-ttu-id="73228-6043">Livelli di funzionalità hardware D3D12</span><span class="sxs-lookup"><span data-stu-id="73228-6043">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="73228-6044">[Implementazione dei buffer shadow per il livello di funzionalità Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="73228-6044">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="73228-6045">Mapping di formati legacy</span><span class="sxs-lookup"><span data-stu-id="73228-6045">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="73228-6046">Guida per programmatori per DXGI</span><span class="sxs-lookup"><span data-stu-id="73228-6046">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
