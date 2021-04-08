---
description: Questa sezione specifica i formati ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware 10Level9 9,1 della funzionalità Direct3D.
ms.assetid: 770A5396-C5D9-442B-99FE-3D220C54E8EB
title: Supporto del formato per l'hardware a livello di funzionalità 10Level9 9.1 di Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56653fd2fb504e3f23cfac13b432530ebaa7219b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876270"
---
# <a name="format-support-for-direct3d-feature-10level9-91-hardware"></a><span data-ttu-id="7fbf0-103">Supporto del formato per l'hardware a livello di funzionalità 10Level9 9.1 di Direct3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-103">Format support for Direct3D Feature 10Level9 9.1 hardware</span></span>

<span data-ttu-id="7fbf0-104">Questa sezione specifica i formati ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nella funzionalità Direct3D 10Level9 9,1 hardware.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.1 hardware.</span></span>

<span data-ttu-id="7fbf0-105">La tabella riepiloga il supporto della funzionalità, usando la chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="7fbf0-106">Simbolo</span><span class="sxs-lookup"><span data-stu-id="7fbf0-106">Symbol</span></span>                            | <span data-ttu-id="7fbf0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="7fbf0-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="7fbf0-108">_ *-*\*</span></span>                             | <span data-ttu-id="7fbf0-109">Non consentito o non disponibile.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-109">Disallowed or not available.</span></span>                                                  |
| ![necessario](images/letter-r.jpg)  | <span data-ttu-id="7fbf0-111">Il supporto hardware è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-111">Hardware support is required.</span></span>                                                 |
| ![facoltative](images/letter-o.jpg)  | <span data-ttu-id="7fbf0-113">Supporto hardware facoltativo. il formato potrebbe essere accelerato o meno.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dipendenti](images/letter-d.jpg) | <span data-ttu-id="7fbf0-115">Obbligatorio se è supportata la funzionalità facoltativa correlata.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="7fbf0-116">Questo argomento contiene una sezione per formato.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-116">This topic contains a section per format.</span></span> <span data-ttu-id="7fbf0-117">Una *destinazione* del formato (le tabelle contengono una riga per destinazione) può essere un tipo di risorsa, una funzione intrinseca HLSL o una particolare funzionalità che dipende da un particolare formato.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="7fbf0-118">Per verificare a livello di codice il supporto del formato in D3D11 e D3D12, vedere [controllo della funzionalità hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="7fbf0-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="7fbf0-119">Il numero di formati è prevalentemente, ma non tutti, in ordine numerico crescente &mdash; alcuni sono fuori dall'ordine numerico ed elencati insieme ad altri formati pertinenti.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="7fbf0-120">Si noti anche che il *tipo* in un nome di formato può indicare *parzialmente* tipizzato e non esclusivamente senza tipo (fare riferimento alla sezione [Note sul formato](#format-notes) alla fine dell'argomento).</span><span class="sxs-lookup"><span data-stu-id="7fbf0-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

// 

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="7fbf0-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="7fbf0-122">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-122">Target</span></span> | <span data-ttu-id="7fbf0-123">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-123">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-124">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-125">0</span><span class="sxs-lookup"><span data-stu-id="7fbf0-125">0</span></span> |
| <span data-ttu-id="7fbf0-126">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-126">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-127">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-128">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-129">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-130">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-131">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-132">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-133">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-134">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-135">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-136">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-137">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-138">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-139">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-140">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-141">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-142">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-144">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-145">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-146">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-147">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-148">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-149">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-150">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-151">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-152">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-153">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-155">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-156">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-157">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-158">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-159">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-160">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-161">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-162">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-163">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-164">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-165">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-166">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-167">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-168">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-169">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-170">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="7fbf0-171">DXGI_FORMAT_R32G32B32A32 \_ <sup>PC</sup> non con tipi (1)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="7fbf0-172">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-172">Target</span></span> | <span data-ttu-id="7fbf0-173">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-173">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-174">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-175">128</span><span class="sxs-lookup"><span data-stu-id="7fbf0-175">128</span></span> |
| <span data-ttu-id="7fbf0-176">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-176">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-177">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-178">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-179">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-180">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-181">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-182">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-183">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-184">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-185">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-186">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-187">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-188">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-189">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-190">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-191">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-191">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-192">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-194">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-195">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-196">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-197">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-198">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-199">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-200">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-201">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-202">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-203">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-205">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-206">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-207">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-208">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-209">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-210">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-211">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-212">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-213">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-214">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-215">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-216">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-217">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-218">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-219">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-220">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="7fbf0-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="7fbf0-222">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-222">Target</span></span> | <span data-ttu-id="7fbf0-223">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-223">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-224">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-225">128</span><span class="sxs-lookup"><span data-stu-id="7fbf0-225">128</span></span> |
| <span data-ttu-id="7fbf0-226">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-226">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-228">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-229">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-229">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-231">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-232">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-233">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-234">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-235">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-235">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-236">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-236">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-237">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-237">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-238">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-238">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-239">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-239">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-240">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-240">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-241">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-241">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-242">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-242">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-243">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-243">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-244">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-244">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-245">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-245">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-246">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-246">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-247">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-247">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-248">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-248">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-249">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-249">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-250">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-250">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-251">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-251">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-252">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-252">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-253">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-253">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-254">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-254">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-255">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-255">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-256">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-256">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-257">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-257">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-258">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-258">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-259">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-259">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-260">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-260">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-261">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-261">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-262">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-262">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-263">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-263">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-264">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-264">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-265">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-265">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-266">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-266">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-267">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-267">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-268">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-268">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-269">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-269">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-270">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-270">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-271">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-271">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-272">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-272">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="7fbf0-273">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-273">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="7fbf0-274">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-274">Target</span></span> | <span data-ttu-id="7fbf0-275">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-275">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-276">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-276">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-277">128</span><span class="sxs-lookup"><span data-stu-id="7fbf0-277">128</span></span> |
| <span data-ttu-id="7fbf0-278">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-278">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-279">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-279">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-280">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-281">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-282">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-283">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-284">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-285">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-286">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-287">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-287">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-288">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-288">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-289">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-289">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-290">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-290">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-291">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-291">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-292">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-292">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-293">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-293">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-294">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-294">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-295">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-295">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-296">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-296">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-297">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-297">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-298">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-298">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-299">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-299">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-300">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-300">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-301">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-301">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-302">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-302">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-303">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-303">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-304">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-304">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-305">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-305">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-306">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-306">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-307">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-307">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-308">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-308">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-309">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-309">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-310">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-310">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-311">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-311">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-312">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-312">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-313">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-313">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-314">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-314">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-315">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-315">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-316">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-316">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-317">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-317">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-318">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-318">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-319">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-319">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-320">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-320">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-321">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-321">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-322">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-322">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="7fbf0-323">DXGI_FORMAT_R32G32B32A32 \_ Sint<sup>FNS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-323">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="7fbf0-324">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-324">Target</span></span> | <span data-ttu-id="7fbf0-325">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-325">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-326">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-326">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-327">128</span><span class="sxs-lookup"><span data-stu-id="7fbf0-327">128</span></span> |
| <span data-ttu-id="7fbf0-328">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-328">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-329">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-329">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-330">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-330">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-331">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-332">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-333">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-334">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-335">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-335">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-336">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-337">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-337">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-338">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-338">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-339">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-339">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-340">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-340">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-341">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-341">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-342">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-342">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-343">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-343">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-344">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-345">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-346">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-347">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-348">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-349">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-350">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-351">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-351">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-352">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-353">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-354">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-355">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-356">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-357">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-358">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-359">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-360">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-360">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-361">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-361">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-362">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-362">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-363">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-363">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-364">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-364">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-365">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-365">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-366">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-366">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-367">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-367">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-368">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-369">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-370">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-371">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-371">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-372">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="7fbf0-373">DXGI_FORMAT_R32G32B32 i \_ <sup>PC</sup> con tipi (5)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-373">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="7fbf0-374">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-374">Target</span></span> | <span data-ttu-id="7fbf0-375">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-375">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-376">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-377">96</span><span class="sxs-lookup"><span data-stu-id="7fbf0-377">96</span></span> |
| <span data-ttu-id="7fbf0-378">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-378">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-379">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-379">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-380">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-381">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-382">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-383">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-384">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-385">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-385">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-386">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-387">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-387">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-388">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-388">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-389">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-389">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-390">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-390">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-391">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-391">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-392">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-392">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-393">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-393">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-394">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-394">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-395">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-395">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-396">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-396">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-397">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-398">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-399">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-400">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-401">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-401">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-402">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-403">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-404">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-405">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-406">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-407">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-408">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-408">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-409">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-409">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-410">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-410">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-411">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-411">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-412">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-412">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-413">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-413">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-414">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-414">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-415">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-415">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-416">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-416">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-417">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-417">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-418">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-418">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-419">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-419">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-420">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-420">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-421">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-421">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-422">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="7fbf0-423">DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-423">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="7fbf0-424">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-424">Target</span></span> | <span data-ttu-id="7fbf0-425">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-425">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-426">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-427">96</span><span class="sxs-lookup"><span data-stu-id="7fbf0-427">96</span></span> |
| <span data-ttu-id="7fbf0-428">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-428">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-430">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-430">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-431">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-431">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-433">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-433">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-434">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-434">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-435">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-435">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-436">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-436">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-437">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-438">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-439">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-440">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-441">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-442">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-443">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-443">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-444">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-445">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-446">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-447">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-448">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-448">Blendable RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="7fbf0-450">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-450">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-451">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-451">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-452">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-452">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-453">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-453">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-454">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-454">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-455">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-455">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-456">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-456">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-457">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-457">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-458">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-458">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-459">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-459">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-460">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-460">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-461">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-461">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-462">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-462">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-463">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-463">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-464">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-464">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="7fbf0-466">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-466">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="7fbf0-468">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-468">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-469">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-469">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-470">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-470">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-471">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-471">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-472">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-472">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-473">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-473">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-474">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-474">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-475">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-475">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-476">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-476">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-477">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-477">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="7fbf0-478">DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-478">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="7fbf0-479">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-479">Target</span></span> | <span data-ttu-id="7fbf0-480">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-480">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-481">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-481">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-482">96</span><span class="sxs-lookup"><span data-stu-id="7fbf0-482">96</span></span> |
| <span data-ttu-id="7fbf0-483">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-483">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-484">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-484">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-485">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-485">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-486">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-486">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-487">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-487">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-488">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-488">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-489">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-489">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-490">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-491">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-491">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-492">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-492">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-493">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-493">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-494">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-494">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-495">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-495">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-496">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-496">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-497">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-497">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-498">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-498">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-499">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-499">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-500">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-500">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-501">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-501">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-502">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-502">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-503">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-503">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-504">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-504">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-505">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-505">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-506">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-506">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-507">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-507">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-508">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-508">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-509">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-509">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-510">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-510">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-511">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-511">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-512">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-512">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-513">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-513">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-514">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-514">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-515">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-515">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-516">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-516">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="7fbf0-518">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-518">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="7fbf0-520">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-520">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-521">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-521">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-522">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-522">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-523">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-523">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-524">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-524">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-525">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-526">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-527">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-528">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-528">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-529">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-529">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="7fbf0-530">DXGI_FORMAT_R32G32B32 \_ Sint<sup>FNS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-530">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="7fbf0-531">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-531">Target</span></span> | <span data-ttu-id="7fbf0-532">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-532">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-533">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-533">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-534">96</span><span class="sxs-lookup"><span data-stu-id="7fbf0-534">96</span></span> |
| <span data-ttu-id="7fbf0-535">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-535">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-536">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-536">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-537">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-537">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-538">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-539">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-540">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-541">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-541">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-542">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-542">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-543">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-544">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-544">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-545">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-545">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-546">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-546">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-547">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-547">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-548">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-548">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-549">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-549">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-550">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-550">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-551">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-551">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-552">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-552">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-553">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-553">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-554">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-554">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-555">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-555">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-556">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-556">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-557">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-557">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-558">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-558">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-559">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-559">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-560">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-560">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-561">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-561">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-562">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-562">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-563">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-563">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-564">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-564">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-565">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-565">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-566">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-566">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-567">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-567">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-568">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-568">4x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="7fbf0-570">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-570">8x Multisample RenderTarget</span></span> | ![dipendenti](images/letter-d.jpg) |
| <span data-ttu-id="7fbf0-572">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-572">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-573">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-573">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-574">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-574">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-575">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-575">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-576">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-576">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-577">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-577">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-578">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-578">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-579">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-579">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-580">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-580">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-581">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-581">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="7fbf0-582">DXGI_FORMAT_R16G16B16A16 \_ <sup>PC</sup> non con tipi (9)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-582">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="7fbf0-583">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-583">Target</span></span> | <span data-ttu-id="7fbf0-584">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-584">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-585">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-585">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-586">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-586">64</span></span> |
| <span data-ttu-id="7fbf0-587">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-587">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-588">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-588">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-589">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-589">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-590">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-590">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-591">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-591">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-592">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-592">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-593">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-593">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-594">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-594">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-595">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-595">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-596">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-596">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-597">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-597">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-598">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-598">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-599">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-599">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-600">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-600">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-601">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-601">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-602">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-602">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-603">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-603">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-604">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-604">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-605">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-606">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-606">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-607">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-607">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-608">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-608">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-609">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-609">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-610">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-610">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-611">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-611">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-612">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-612">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-613">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-613">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-614">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-614">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-615">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-615">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-616">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-616">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-617">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-617">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-618">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-618">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-619">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-619">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-620">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-620">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-621">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-621">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-622">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-622">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-623">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-623">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-624">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-624">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-625">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-625">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-626">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-626">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-627">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-627">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-628">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-628">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-629">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-629">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-630">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-630">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-631">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-631">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="7fbf0-632">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-632">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="7fbf0-633">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-633">Target</span></span> | <span data-ttu-id="7fbf0-634">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-634">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-635">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-635">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-636">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-636">64</span></span> |
| <span data-ttu-id="7fbf0-637">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-637">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-638">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-638">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-639">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-639">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-640">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-640">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-641">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-641">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-642">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-642">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-643">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-643">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-644">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-644">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-645">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-645">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-646">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-646">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-647">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-647">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-648">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-649">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-650">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-650">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-651">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-652">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-652">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-653">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-653">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-654">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-654">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-655">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-655">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-656">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-656">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-657">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-657">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-658">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-658">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-659">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-659">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-660">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-660">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-661">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-661">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-662">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-662">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-663">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-663">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-664">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-664">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-665">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-665">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-666">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-666">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-667">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-667">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-668">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-668">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-669">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-669">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-670">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-670">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-671">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-671">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-672">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-672">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-673">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-673">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-674">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-674">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-675">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-675">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-676">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-676">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-677">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-677">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-678">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-678">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-679">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-680">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-680">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-682">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="7fbf0-683">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-683">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="7fbf0-684">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-684">Target</span></span> | <span data-ttu-id="7fbf0-685">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-685">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-686">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-687">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-687">64</span></span> |
| <span data-ttu-id="7fbf0-688">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-688">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-689">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-689">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-690">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-690">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-691">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-691">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-692">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-692">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-693">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-693">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-694">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-695">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-696">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-696">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-697">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-697">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-698">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-698">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-699">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-700">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-701">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-701">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-702">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-703">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-703">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-704">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-704">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-705">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-705">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-706">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-706">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-707">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-707">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-708">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-708">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-709">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-709">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-710">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-710">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-711">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-711">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-712">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-712">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-713">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-713">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-714">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-714">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-715">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-715">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-716">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-716">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-717">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-717">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-718">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-718">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-719">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-719">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-720">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-720">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-721">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-721">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-722">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-722">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-723">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-723">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-724">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-724">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-725">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-725">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-726">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-726">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-727">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-727">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-728">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-728">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-729">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-729">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-730">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-730">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-731">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-731">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-732">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-732">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="7fbf0-733">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-733">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="7fbf0-734">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-734">Target</span></span> | <span data-ttu-id="7fbf0-735">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-735">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-736">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-736">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-737">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-737">64</span></span> |
| <span data-ttu-id="7fbf0-738">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-738">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-739">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-740">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-741">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-742">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-743">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-744">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-744">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-745">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-745">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-746">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-746">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-747">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-747">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-748">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-748">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-749">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-749">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-750">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-750">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-751">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-751">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-752">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-752">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-753">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-753">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-754">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-754">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-755">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-755">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-756">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-756">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-757">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-757">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-758">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-758">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-759">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-759">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-760">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-760">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-761">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-761">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-762">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-762">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-763">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-763">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-764">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-764">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-765">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-765">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-766">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-766">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-767">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-767">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-768">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-768">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-769">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-769">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-770">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-770">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-771">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-771">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-772">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-772">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-773">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-773">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-774">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-774">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-775">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-775">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-776">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-776">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-777">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-777">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-778">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-778">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-779">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-779">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-780">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-780">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-781">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-781">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-782">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="7fbf0-783">DXGI_FORMAT_R16G16B16A16 \_ russar<sup>FNS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-783">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="7fbf0-784">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-784">Target</span></span> | <span data-ttu-id="7fbf0-785">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-785">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-786">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-787">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-787">64</span></span> |
| <span data-ttu-id="7fbf0-788">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-788">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-790">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-790">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-791">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-791">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-793">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-793">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-794">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-794">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-795">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-795">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-796">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-796">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-797">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-798">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-799">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-799">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-800">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-800">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-801">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-801">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-802">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-802">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-803">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-803">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-804">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-804">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-805">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-805">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-806">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-807">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-808">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-809">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-810">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-811">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-812">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-813">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-813">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-814">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-815">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-816">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-817">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-818">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-819">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-820">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-821">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-822">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-822">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-823">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-823">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-824">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-824">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-825">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-825">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-826">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-826">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-827">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-827">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-828">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-828">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-829">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-829">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-830">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-830">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-831">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-831">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-832">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-832">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-833">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-833">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-834">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-834">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="7fbf0-835">DXGI_FORMAT_R16G16B16A16 \_ Sint<sup>FNS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-835">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="7fbf0-836">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-836">Target</span></span> | <span data-ttu-id="7fbf0-837">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-837">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-838">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-838">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-839">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-839">64</span></span> |
| <span data-ttu-id="7fbf0-840">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-840">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-842">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-842">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-843">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-843">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-845">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-845">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-846">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-846">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-847">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-847">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-848">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-848">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-849">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-849">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-850">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-850">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-851">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-851">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-852">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-852">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-853">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-853">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-854">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-854">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-855">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-855">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-856">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-856">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-857">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-857">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-858">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-858">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-859">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-859">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-860">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-860">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-861">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-861">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-862">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-862">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-863">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-863">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-864">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-864">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-865">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-865">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-866">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-866">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-867">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-867">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-868">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-868">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-869">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-869">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-870">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-870">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-871">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-871">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-872">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-872">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-873">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-873">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-874">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-874">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-875">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-875">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-876">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-876">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-877">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-877">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-878">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-878">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-879">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-879">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-880">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-880">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-881">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-882">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-883">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-883">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-884">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-884">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-885">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-885">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-886">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-886">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="7fbf0-887">DXGI_FORMAT_R32G32 \_ <sup>PC</sup> non con tipi (15)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-887">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="7fbf0-888">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-888">Target</span></span> | <span data-ttu-id="7fbf0-889">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-889">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-890">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-891">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-891">64</span></span> |
| <span data-ttu-id="7fbf0-892">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-892">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-893">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-893">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-894">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-894">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-895">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-895">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-896">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-896">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-897">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-897">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-898">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-898">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-899">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-899">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-900">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-901">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-901">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-902">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-902">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-903">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-904">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-905">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-905">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-906">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-907">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-907">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-908">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-908">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-909">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-910">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-910">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-911">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-912">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-913">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-914">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-915">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-915">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-916">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-917">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-918">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-919">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-920">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-921">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-922">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-923">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-924">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-924">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-925">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-925">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-926">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-926">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-927">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-927">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-928">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-928">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-929">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-929">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-930">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-930">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-931">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-931">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-932">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-933">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-934">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-935">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-935">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-936">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-936">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="7fbf0-937">DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-937">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="7fbf0-938">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-938">Target</span></span> | <span data-ttu-id="7fbf0-939">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-939">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-940">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-940">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-941">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-941">64</span></span> |
| <span data-ttu-id="7fbf0-942">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-942">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-944">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-944">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-945">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-945">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-947">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-948">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-949">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-950">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-951">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-951">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-952">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-953">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-953">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-954">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-954">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-955">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-955">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-956">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-956">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-957">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-957">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-958">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-958">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-959">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-959">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-960">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-961">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-962">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-962">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-963">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-963">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-964">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-964">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-965">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-965">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-966">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-966">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-967">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-967">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-968">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-968">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-969">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-969">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-970">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-970">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-971">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-971">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-972">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-972">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-973">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-973">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-974">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-974">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-975">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-975">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-976">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-976">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-977">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-977">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-978">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-978">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-979">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-979">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-980">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-980">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-981">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-981">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-982">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-982">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-983">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-983">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-984">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-984">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-985">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-985">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-986">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-986">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-987">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-987">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-988">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-988">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="7fbf0-989">DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-989">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="7fbf0-990">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-990">Target</span></span> | <span data-ttu-id="7fbf0-991">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-991">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-992">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-992">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-993">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-993">64</span></span> |
| <span data-ttu-id="7fbf0-994">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-994">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-995">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-995">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-996">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-996">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-997">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-997">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-998">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-998">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-999">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-999">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1000">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1001">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1001">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1002">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1002">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1003">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1003">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1004">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1004">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1005">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1005">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1006">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1006">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1007">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1007">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1008">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1008">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1009">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1009">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1010">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1010">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1011">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1012">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1012">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1013">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1013">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1014">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1014">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1015">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1015">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1016">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1016">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1017">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1017">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1018">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1018">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1019">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1019">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1020">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1020">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1021">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1021">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1022">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1022">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1023">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1023">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1024">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1024">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1025">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1025">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1026">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1026">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1027">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1027">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1028">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1028">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1029">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1029">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1030">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1030">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1031">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1031">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1032">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1032">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1033">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1033">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1034">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1034">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1035">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1035">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1036">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1036">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1037">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1037">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1038">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1038">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="7fbf0-1039">DXGI_FORMAT_R32G32 \_ Sint<sup>FNS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1039">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="7fbf0-1040">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1040">Target</span></span> | <span data-ttu-id="7fbf0-1041">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1041">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1042">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1042">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1043">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1043">64</span></span> |
| <span data-ttu-id="7fbf0-1044">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1044">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1045">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1045">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1046">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1046">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1047">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1047">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1048">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1048">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1049">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1049">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1050">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1050">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1051">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1051">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1052">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1053">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1053">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1054">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1054">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1055">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1055">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1056">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1056">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1057">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1057">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1058">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1058">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1059">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1059">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1060">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1060">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1061">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1061">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1062">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1062">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1063">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1063">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1064">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1064">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1065">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1065">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1066">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1066">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1067">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1067">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1068">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1068">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1069">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1069">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1070">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1070">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1071">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1071">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1072">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1072">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1073">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1073">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1074">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1074">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1075">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1075">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1076">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1076">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1077">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1078">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1079">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1080">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1081">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1081">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1082">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1083">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1084">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1084">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1085">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1085">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1086">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1086">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1087">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1087">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1088">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1088">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="7fbf0-1089">DXGI_FORMAT_R32G8X24 i \_ <sup>PC</sup> non con tipi (19)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1089">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="7fbf0-1090">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1090">Target</span></span> | <span data-ttu-id="7fbf0-1091">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1091">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1092">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1093">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1093">64</span></span> |
| <span data-ttu-id="7fbf0-1094">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1094">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1095">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1095">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1096">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1096">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1097">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1097">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1098">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1098">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1099">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1099">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1100">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1100">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1101">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1101">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1102">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1102">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1103">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1103">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1104">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1105">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1106">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1107">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1107">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1108">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1109">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1109">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1110">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1110">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1111">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1112">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1113">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1114">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1115">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1116">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1117">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1117">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1118">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1119">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1120">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1121">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1122">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1123">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1124">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1124">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1125">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1125">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1126">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1126">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1127">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1127">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1128">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1128">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1129">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1129">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1130">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1130">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1131">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1131">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1132">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1132">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1133">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1133">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1134">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1134">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1135">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1135">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1136">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1136">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1137">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1137">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1138">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1138">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="7fbf0-1139">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1139">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="7fbf0-1140">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1140">Target</span></span> | <span data-ttu-id="7fbf0-1141">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1141">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1142">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1142">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1143">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1143">64</span></span> |
| <span data-ttu-id="7fbf0-1144">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1144">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1145">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1145">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1146">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1146">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1147">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1147">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1148">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1148">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1149">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1149">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1150">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1151">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1151">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1152">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1152">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1153">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1153">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1154">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1154">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1155">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1155">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1156">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1156">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1157">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1157">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1158">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1158">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1159">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1159">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1160">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1160">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1161">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1161">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1162">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1163">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1164">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1165">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1166">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1167">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1167">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1168">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1168">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1169">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1169">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1170">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1170">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1171">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1171">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1172">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1172">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1173">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1173">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1174">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1174">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1175">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1175">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1176">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1176">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1177">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1178">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1179">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1180">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1181">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1181">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1182">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1183">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1184">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1184">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1185">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1185">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1186">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1186">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1187">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1187">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1188">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1188">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="7fbf0-1189">DXGI_FORMAT_R32 \_ float \_ X8X24 con \_ tipo<sup>FNS</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1189">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="7fbf0-1190">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1190">Target</span></span> | <span data-ttu-id="7fbf0-1191">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1191">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1192">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1192">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1193">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1193">64</span></span> |
| <span data-ttu-id="7fbf0-1194">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1194">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1195">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1195">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1196">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1196">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1197">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1197">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1198">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1198">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1199">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1199">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1200">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1200">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1201">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1201">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1202">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1202">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1203">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1203">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1204">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1204">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1205">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1205">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1206">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1206">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1207">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1207">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1208">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1208">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1209">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1209">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1210">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1210">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1211">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1211">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1212">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1212">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1213">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1213">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1214">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1214">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1215">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1215">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1216">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1216">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1217">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1217">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1218">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1218">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1219">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1219">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1220">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1220">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1221">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1221">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1222">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1222">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1223">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1223">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1224">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1224">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1225">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1225">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1226">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1226">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1227">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1227">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1228">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1228">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1229">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1229">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1230">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1230">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1231">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1231">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1232">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1232">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1233">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1233">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1234">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1235">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1236">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1237">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1237">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1238">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1238">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="7fbf0-1239">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FNS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1239">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="7fbf0-1240">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1240">Target</span></span> | <span data-ttu-id="7fbf0-1241">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1241">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1242">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1242">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1243">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1243">64</span></span> |
| <span data-ttu-id="7fbf0-1244">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1244">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1245">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1245">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1246">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1246">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1247">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1247">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1248">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1248">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1249">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1249">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1250">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1250">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1251">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1252">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1253">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1253">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1254">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1254">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1255">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1256">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1257">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1257">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1258">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1259">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1259">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1260">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1260">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1261">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1261">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1262">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1262">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1263">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1263">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1264">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1264">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1265">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1265">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1266">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1266">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1267">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1267">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1268">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1268">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1269">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1269">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1270">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1270">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1271">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1271">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1272">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1272">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1273">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1273">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1274">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1274">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1275">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1275">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1276">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1276">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1277">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1277">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1278">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1278">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1279">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1279">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1280">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1280">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1281">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1281">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1282">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1283">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1283">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1284">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1284">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1285">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1285">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1286">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1286">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1287">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1287">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1288">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1288">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="7fbf0-1289">DXGI_FORMAT_R10G10B10A2 \_ <sup>PC</sup> non con tipi (23)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1289">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="7fbf0-1290">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1290">Target</span></span> | <span data-ttu-id="7fbf0-1291">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1291">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1292">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1292">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1293">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1293">32</span></span> |
| <span data-ttu-id="7fbf0-1294">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1294">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1295">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1295">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1296">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1296">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1297">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1298">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1299">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1300">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1301">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1301">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1302">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1302">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1303">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1303">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1304">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1304">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1305">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1305">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1306">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1306">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1307">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1307">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1308">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1308">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1309">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1309">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1310">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1310">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1311">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1311">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1312">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1312">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1313">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1313">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1314">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1314">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1315">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1315">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1316">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1316">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1317">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1317">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1318">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1318">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1319">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1319">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1320">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1320">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1321">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1321">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1322">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1322">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1323">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1323">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1324">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1324">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1325">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1325">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1326">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1326">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1327">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1327">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1328">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1328">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1329">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1329">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1330">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1330">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1331">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1331">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1332">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1332">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1333">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1333">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1334">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1334">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1335">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1335">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1336">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1336">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1337">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1337">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1338">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1338">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="7fbf0-1339">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1339">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="7fbf0-1340">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1340">Target</span></span> | <span data-ttu-id="7fbf0-1341">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1341">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1342">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1342">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1343">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1343">32</span></span> |
| <span data-ttu-id="7fbf0-1344">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1344">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1345">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1345">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1346">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1346">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1347">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1348">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1349">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1350">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1350">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1351">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1351">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1352">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1352">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1353">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1353">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1354">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1354">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1355">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1355">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1356">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1356">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1357">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1357">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1358">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1358">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1359">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1359">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1360">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1360">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1361">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1361">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1362">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1362">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1363">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1363">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1364">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1364">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1365">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1365">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1366">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1366">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1367">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1367">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1368">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1368">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1369">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1369">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1370">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1370">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1371">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1371">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1372">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1372">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1373">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1373">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1374">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1374">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1375">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1375">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1376">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1376">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1377">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1377">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1378">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1378">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1379">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1379">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1380">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1380">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1381">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1381">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1382">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1382">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1383">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1383">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1384">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1385">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1386">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1387">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1387">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1389">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="7fbf0-1390">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1390">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="7fbf0-1391">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1391">Target</span></span> | <span data-ttu-id="7fbf0-1392">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1392">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1393">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1394">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1394">32</span></span> |
| <span data-ttu-id="7fbf0-1395">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1395">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1396">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1396">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1397">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1397">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1398">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1398">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1399">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1399">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1400">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1400">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1401">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1401">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1402">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1402">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1403">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1403">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1404">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1404">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1405">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1405">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1406">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1406">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1407">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1407">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1408">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1408">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1409">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1409">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1410">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1410">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1411">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1411">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1412">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1413">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1413">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1414">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1414">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1415">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1415">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1416">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1416">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1417">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1417">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1418">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1418">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1419">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1419">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1420">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1420">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1421">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1421">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1422">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1422">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1423">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1423">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1424">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1424">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1425">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1425">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1426">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1426">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1427">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1427">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1428">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1429">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1430">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1431">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1432">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1432">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1433">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1434">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1435">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1435">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1436">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1436">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1437">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1437">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1438">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1438">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1439">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1439">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="7fbf0-1440">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FNS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1440">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="7fbf0-1441">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1441">Target</span></span> | <span data-ttu-id="7fbf0-1442">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1442">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1443">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1443">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1444">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1444">32</span></span> |
| <span data-ttu-id="7fbf0-1445">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1445">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1446">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1446">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1447">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1447">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1448">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1448">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1449">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1449">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1450">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1450">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1451">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1451">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1453">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1454">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1454">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1455">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1456">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1457">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1458">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1459">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1460">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1460">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1461">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1461">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1462">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1462">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1463">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1463">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1464">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1465">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1466">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1467">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1468">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1468">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1469">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1470">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1471">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1472">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1474">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1475">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1476">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1477">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1477">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1478">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1478">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1479">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1479">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1480">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1481">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1482">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1482">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1483">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1484">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1485">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1486">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1487">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1488">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1488">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1489">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="7fbf0-1490">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1490">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="7fbf0-1491">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1491">Target</span></span> | <span data-ttu-id="7fbf0-1492">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1492">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1493">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1494">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1494">32</span></span> |
| <span data-ttu-id="7fbf0-1495">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1495">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1496">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1496">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1497">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1498">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1499">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1500">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1501">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1502">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1503">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1504">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1505">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1506">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1507">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1508">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1508">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1509">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1510">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1511">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1512">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1513">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1514">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1515">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1516">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1517">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1518">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1518">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1519">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1520">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1521">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1522">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1524">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1525">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1526">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1527">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1528">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1528">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1529">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1529">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1530">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1530">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1531">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1531">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1532">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1532">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1533">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1533">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1534">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1534">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1535">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1535">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1536">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1536">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1537">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1537">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1538">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1538">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1539">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1539">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="7fbf0-1540">DXGI_FORMAT_R8G8B8A8 \_ <sup>PC</sup> non con tipi (27)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1540">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="7fbf0-1541">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1541">Target</span></span> | <span data-ttu-id="7fbf0-1542">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1542">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1543">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1543">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1544">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1544">32</span></span> |
| <span data-ttu-id="7fbf0-1545">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1545">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1546">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1546">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1547">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1548">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1549">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1550">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1551">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1552">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1552">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1553">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1553">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1554">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1554">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1555">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1555">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1556">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1556">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1557">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1557">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1558">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1558">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1559">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1559">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1560">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1560">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1561">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1561">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1562">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1562">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1563">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1563">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1564">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1565">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1566">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1567">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1568">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1568">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1569">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1570">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1571">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1572">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1573">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1574">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1575">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1576">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1577">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1577">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1578">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1578">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1579">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1579">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1580">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1580">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1581">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1581">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1582">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1582">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1583">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1583">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1584">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1584">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1585">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1585">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1586">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1586">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1587">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1587">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1588">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1588">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1589">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="7fbf0-1590">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1590">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="7fbf0-1591">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1591">Target</span></span> | <span data-ttu-id="7fbf0-1592">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1592">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1593">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1594">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1594">32</span></span> |
| <span data-ttu-id="7fbf0-1595">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1595">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1597">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1597">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1598">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1598">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1600">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1601">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1603">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1605">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1605">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1607">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1609">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1609">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1611">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1611">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1613">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1614">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1615">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1615">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1616">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1617">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1619">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1619">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1621">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1621">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1623">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1623">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1625">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1625">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1626">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1626">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1627">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1627">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1628">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1628">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1629">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1629">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1630">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1630">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1631">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1631">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1632">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1632">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1633">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1633">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1634">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1634">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1635">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1635">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1636">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1636">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1637">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1637">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1638">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1638">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1640">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1640">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-1642">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1642">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-1644">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1644">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-1646">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1646">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1648">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1648">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1649">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1649">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1651">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1651">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1652">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1652">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1653">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1653">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-1655">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1655">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1657">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1657">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1659">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1659">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="7fbf0-1660">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1660">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="7fbf0-1661">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1661">Target</span></span> | <span data-ttu-id="7fbf0-1662">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1662">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1663">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1663">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1664">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1664">32</span></span> |
| <span data-ttu-id="7fbf0-1665">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1665">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1667">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1667">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1668">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1668">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1669">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1669">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1670">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1670">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1671">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1671">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1672">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1672">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1674">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1674">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1676">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1676">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1678">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1678">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1680">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1680">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1682">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1682">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1683">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1683">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1684">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1684">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1685">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1685">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1686">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1686">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1688">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1688">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1690">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1690">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1692">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1692">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1694">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1694">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1695">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1695">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1696">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1696">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1697">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1697">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1698">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1698">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1699">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1699">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1700">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1700">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1701">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1701">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1702">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1702">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1703">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1703">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1704">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1704">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1705">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1705">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1706">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1706">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1707">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1707">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1709">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1709">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-1711">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1711">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-1713">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1713">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-1715">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1715">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1717">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1717">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1718">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1718">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1720">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1720">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1721">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1721">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1722">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1722">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-1724">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1724">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1726">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1726">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1728">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1728">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="7fbf0-1729">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1729">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="7fbf0-1730">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1730">Target</span></span> | <span data-ttu-id="7fbf0-1731">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1731">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1732">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1732">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1733">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1733">32</span></span> |
| <span data-ttu-id="7fbf0-1734">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1734">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1736">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1736">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1737">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1737">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1739">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1739">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1740">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1740">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1741">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1741">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1742">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1742">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1743">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1743">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1744">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1744">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1745">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1745">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1746">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1746">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1747">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1748">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1749">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1749">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1750">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1750">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1751">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1751">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1752">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1752">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1753">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1753">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1754">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1754">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1755">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1755">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1756">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1756">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1757">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1757">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1758">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1758">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1759">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1759">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1760">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1760">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1761">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1761">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1762">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1762">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1763">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1763">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1764">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1764">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1765">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1765">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1766">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1766">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1767">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1767">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1768">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1768">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1769">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1770">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1771">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1772">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1773">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1773">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1774">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1775">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1775">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1776">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1777">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1778">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1779">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1779">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1780">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="7fbf0-1781">DXGI_FORMAT_R8G8B8A8 \_ russar<sup>FNS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1781">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="7fbf0-1782">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1782">Target</span></span> | <span data-ttu-id="7fbf0-1783">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1784">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1785">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1785">32</span></span> |
| <span data-ttu-id="7fbf0-1786">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1786">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1788">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1789">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1789">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1790">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1790">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1791">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1791">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1792">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1792">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1793">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1793">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1796">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1798">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1798">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1800">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1800">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1802">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1803">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1804">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1804">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1805">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1806">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1806">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1808">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1809">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1810">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1811">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1812">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1813">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1814">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1815">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1815">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1816">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1816">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1817">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1817">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1818">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1818">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1819">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1819">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1820">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1820">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1821">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1821">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1822">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1822">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1823">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1823">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1824">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1824">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-1826">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1826">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1827">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1827">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1828">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1828">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1829">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1829">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1830">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1830">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1831">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1831">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1832">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1832">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1833">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1833">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1834">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1834">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1835">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1835">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1836">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1836">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1837">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="7fbf0-1838">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup>FNS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1838">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="7fbf0-1839">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1839">Target</span></span> | <span data-ttu-id="7fbf0-1840">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1840">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1841">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1842">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1842">32</span></span> |
| <span data-ttu-id="7fbf0-1843">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1843">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1844">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1844">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1845">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1845">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1846">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1846">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1847">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1847">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1848">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1848">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1849">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1849">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1850">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1850">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1851">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1851">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1852">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1852">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1853">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1853">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1854">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1855">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1856">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1857">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1858">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1858">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1859">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1859">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1860">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1860">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1861">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1861">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1862">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1862">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1863">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1863">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1864">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1864">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1865">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1865">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1866">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1866">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1867">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1867">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1868">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1868">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1869">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1869">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1870">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1870">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1871">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1871">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1872">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1872">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1873">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1873">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1874">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1874">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1875">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1875">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1876">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1876">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1877">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1877">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1878">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1878">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1879">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1879">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1880">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1880">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1881">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1881">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1882">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1882">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1883">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1883">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1884">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1884">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1885">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1885">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1886">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1886">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1887">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1887">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="7fbf0-1888">DXGI_FORMAT_R16G16 \_ <sup>PC</sup> non con tipi (33)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1888">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="7fbf0-1889">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1889">Target</span></span> | <span data-ttu-id="7fbf0-1890">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1890">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1891">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1891">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1892">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1892">32</span></span> |
| <span data-ttu-id="7fbf0-1893">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1893">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1894">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1894">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1895">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1896">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1897">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1898">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1899">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1899">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1900">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1900">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1901">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1901">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1902">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1902">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1903">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1903">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1904">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1904">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1905">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1905">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1906">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1906">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1907">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1907">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1908">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1908">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1909">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1909">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1910">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1910">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1911">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1911">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1912">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1912">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1913">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1913">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1914">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1914">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1915">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1915">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1916">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1916">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1917">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1917">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1918">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1918">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1919">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1919">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1920">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1920">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1921">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1921">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1922">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1922">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1923">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1923">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1924">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1924">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1925">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1925">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1926">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1926">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1927">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1927">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1928">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1928">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1929">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1929">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1930">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1930">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1931">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1931">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1932">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1932">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1933">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1933">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1934">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1934">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1935">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1935">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1936">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1936">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1937">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="7fbf0-1938">DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1938">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="7fbf0-1939">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1939">Target</span></span> | <span data-ttu-id="7fbf0-1940">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1940">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1941">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1942">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1942">32</span></span> |
| <span data-ttu-id="7fbf0-1943">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1943">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1944">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1944">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1945">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1945">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1946">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1946">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1947">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1947">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1948">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1948">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1949">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1949">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-1950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1950">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-1951">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1951">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-1952">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1952">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-1953">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1954">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1955">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-1956">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1956">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-1957">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-1958">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1958">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-1959">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1959">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-1960">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1960">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1961">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1961">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1962">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1962">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-1963">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1963">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-1964">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1964">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1965">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1965">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-1966">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1966">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-1967">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1967">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-1968">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1968">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1969">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1969">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-1970">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1970">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-1971">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1971">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-1972">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1972">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-1973">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1973">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1974">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1974">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-1975">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1975">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-1976">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1976">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1977">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1977">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-1978">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1978">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-1979">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1979">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-1980">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1980">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-1981">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1981">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-1982">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1982">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-1983">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1983">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1984">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1984">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-1985">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1985">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-1986">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1986">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-1987">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="7fbf0-1988">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1988">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="7fbf0-1989">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1989">Target</span></span> | <span data-ttu-id="7fbf0-1990">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1990">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-1991">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-1992">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1992">32</span></span> |
| <span data-ttu-id="7fbf0-1993">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1993">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-1994">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1994">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1995">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1995">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1996">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1997">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-1998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1998">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-1999">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-1999">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2000">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2000">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2001">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2001">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2002">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2002">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2003">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2003">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2004">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2004">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2005">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2005">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2006">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2006">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2007">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2007">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2008">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2008">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2009">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2009">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2010">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2010">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2011">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2011">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2012">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2013">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2014">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2015">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2016">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2016">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2017">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2018">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2019">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2020">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2021">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2022">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2023">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2023">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2024">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2024">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2025">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2025">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2026">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2026">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2027">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2027">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2028">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2028">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2029">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2029">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2030">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2030">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2031">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2031">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2032">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2032">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2033">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2033">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2034">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2034">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2035">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2035">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2036">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2036">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2037">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2037">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="7fbf0-2038">DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2038">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="7fbf0-2039">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2039">Target</span></span> | <span data-ttu-id="7fbf0-2040">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2040">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2041">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2041">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2042">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2042">32</span></span> |
| <span data-ttu-id="7fbf0-2043">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2043">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2044">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2044">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2045">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2045">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2046">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2046">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2047">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2047">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2048">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2048">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2049">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2049">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2050">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2051">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2052">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2053">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2054">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2055">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2056">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2056">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2057">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2058">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2059">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2060">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2061">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2062">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2063">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2064">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2065">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2066">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2066">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2067">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2068">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2069">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2070">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2072">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2073">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2074">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2075">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2075">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2076">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2076">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2077">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2077">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2078">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2078">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2079">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2079">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2080">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2080">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2081">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2081">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2082">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2082">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2083">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2083">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2084">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2084">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2085">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2085">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2086">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2086">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2087">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2087">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="7fbf0-2088">DXGI_FORMAT_R16G16 \_ russar<sup>FNS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2088">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="7fbf0-2089">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2089">Target</span></span> | <span data-ttu-id="7fbf0-2090">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2090">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2091">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2091">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2092">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2092">32</span></span> |
| <span data-ttu-id="7fbf0-2093">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2093">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2095">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2095">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2096">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2096">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2098">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2098">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2099">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2099">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2100">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2100">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2101">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2101">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2103">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2104">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2105">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2105">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2107">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2107">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2108">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2108">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2109">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2109">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2110">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2110">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2111">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2111">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2112">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2112">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2114">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2114">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2115">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2115">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2116">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2116">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2117">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2117">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2118">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2118">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2119">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2119">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2120">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2120">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2121">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2121">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2122">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2122">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2123">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2123">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2124">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2124">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2125">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2125">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2126">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2126">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2127">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2127">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2128">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2128">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2129">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2129">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2130">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2130">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2132">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2132">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2133">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2133">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2134">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2134">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2135">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2135">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2136">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2136">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2137">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2137">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2138">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2138">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2139">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2139">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2140">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2140">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2141">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2141">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2142">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2142">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2143">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2143">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="7fbf0-2144">DXGI_FORMAT_R16G16 \_ Sint<sup>FNS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2144">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="7fbf0-2145">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2145">Target</span></span> | <span data-ttu-id="7fbf0-2146">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2146">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2147">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2148">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2148">32</span></span> |
| <span data-ttu-id="7fbf0-2149">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2149">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2151">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2151">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2152">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2152">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2154">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2154">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2155">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2155">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2156">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2156">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2157">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2157">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2158">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2158">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2159">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2159">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2160">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2160">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2161">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2162">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2163">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2164">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2164">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2165">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2166">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2166">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2167">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2167">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2168">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2168">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2169">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2169">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2170">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2170">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2171">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2171">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2172">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2172">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2173">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2173">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2174">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2174">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2175">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2175">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2176">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2176">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2177">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2177">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2178">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2178">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2179">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2179">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2180">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2180">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2181">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2181">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2182">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2182">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2183">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2183">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2184">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2185">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2186">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2187">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2188">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2188">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2189">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2190">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2191">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2191">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2192">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2192">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2193">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2193">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2194">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2194">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2195">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="7fbf0-2196">DXGI_FORMAT_R32 \_ <sup>PC</sup> non con tipi (39)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2196">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="7fbf0-2197">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2197">Target</span></span> | <span data-ttu-id="7fbf0-2198">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2198">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2199">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2200">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2200">32</span></span> |
| <span data-ttu-id="7fbf0-2201">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2201">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2202">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2202">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2203">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2204">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2205">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2206">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2207">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2208">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2209">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2209">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2210">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2210">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2211">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2211">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2212">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2212">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2213">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2213">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2214">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2214">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2215">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2215">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2216">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2216">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2217">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2217">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2218">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2218">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2219">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2219">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2220">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2220">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2221">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2221">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2222">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2222">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2223">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2223">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2224">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2224">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2225">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2225">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2226">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2226">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2227">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2227">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2228">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2228">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2229">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2229">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2230">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2230">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2231">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2231">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2232">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2232">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2233">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2233">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2234">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2234">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2235">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2235">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2236">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2236">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2237">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2237">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2238">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2238">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2239">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2239">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2240">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2240">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2241">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2241">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2242">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2242">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2243">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2243">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2244">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2244">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2245">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2245">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="7fbf0-2246">DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2246">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="7fbf0-2247">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2247">Target</span></span> | <span data-ttu-id="7fbf0-2248">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2248">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2249">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2249">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2250">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2250">32</span></span> |
| <span data-ttu-id="7fbf0-2251">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2251">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2252">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2252">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2253">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2253">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2254">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2254">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2255">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2255">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2256">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2256">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2257">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2258">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2258">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2259">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2259">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2260">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2260">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2261">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2261">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2262">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2262">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2263">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2263">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2264">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2264">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2265">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2265">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2266">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2266">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2267">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2267">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2268">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2268">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2269">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2269">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2270">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2270">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2271">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2271">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2272">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2272">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2273">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2273">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2274">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2274">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2275">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2275">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2276">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2276">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2277">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2277">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2278">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2278">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2279">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2279">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2280">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2280">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2281">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2281">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2282">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2282">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2283">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2283">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2284">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2284">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2285">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2285">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2286">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2286">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2287">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2287">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2288">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2288">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2289">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2289">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2290">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2290">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2291">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2291">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2292">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2292">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2293">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2293">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2294">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2294">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2295">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2295">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="7fbf0-2296">DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2296">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="7fbf0-2297">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2297">Target</span></span> | <span data-ttu-id="7fbf0-2298">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2298">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2299">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2299">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2300">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2300">32</span></span> |
| <span data-ttu-id="7fbf0-2301">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2301">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2303">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2303">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2304">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2304">Input Assembler Vertex Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2306">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2306">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2307">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2307">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2308">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2308">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2309">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2309">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2310">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2310">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2311">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2311">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2312">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2312">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2313">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2313">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2314">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2314">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2315">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2315">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2316">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2316">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2317">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2317">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2318">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2318">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2319">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2320">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2321">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2322">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2323">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2324">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2325">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2326">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2326">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2327">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2328">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2329">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2330">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2332">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2333">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2334">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2335">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2335">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2336">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2336">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2337">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2337">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2338">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2338">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2339">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2339">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2340">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2340">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2341">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2341">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2342">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2342">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2343">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2343">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2344">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2344">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2345">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2345">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2346">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2346">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2347">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2347">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="7fbf0-2348">DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2348">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="7fbf0-2349">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2349">Target</span></span> | <span data-ttu-id="7fbf0-2350">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2350">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2351">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2351">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2352">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2352">32</span></span> |
| <span data-ttu-id="7fbf0-2353">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2353">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2354">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2354">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2355">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2355">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2356">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2356">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2357">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2357">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2358">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2358">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2359">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2359">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2360">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2361">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2362">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2362">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2363">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2363">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2364">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2364">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2365">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2365">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2366">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2366">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2367">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2367">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2368">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2368">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2369">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2369">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2370">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2371">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2371">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2372">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2372">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2373">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2373">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2374">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2374">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2375">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2375">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2376">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2376">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2377">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2377">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2378">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2378">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2379">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2379">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2380">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2380">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2381">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2381">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2382">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2382">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2383">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2383">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2384">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2384">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2385">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2385">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2386">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2386">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2387">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2387">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2388">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2388">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2389">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2389">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2390">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2390">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2391">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2391">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2392">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2392">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2393">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2393">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2394">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2394">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2395">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2395">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2396">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2396">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2397">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2397">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="7fbf0-2398">DXGI_FORMAT_R32 \_ Sint<sup>FNS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2398">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="7fbf0-2399">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2399">Target</span></span> | <span data-ttu-id="7fbf0-2400">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2400">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2401">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2401">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2402">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2402">32</span></span> |
| <span data-ttu-id="7fbf0-2403">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2403">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2404">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2404">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2405">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2405">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2406">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2406">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2407">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2407">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2408">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2408">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2409">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2409">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2410">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2410">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2411">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2411">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2412">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2412">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2413">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2414">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2415">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2416">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2416">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2417">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2418">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2419">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2419">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2420">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2420">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2421">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2421">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2422">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2422">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2423">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2423">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2424">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2424">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2425">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2425">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2426">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2426">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2427">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2427">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2428">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2428">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2429">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2429">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2430">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2430">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2431">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2431">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2432">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2432">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2433">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2433">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2434">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2434">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2435">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2435">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2436">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2437">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2438">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2439">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2440">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2440">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2441">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2442">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2442">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2443">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2443">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2444">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2444">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2445">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2445">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2446">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2446">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2447">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2447">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="7fbf0-2448">DXGI_FORMAT_R24G8 \_ <sup>PC</sup> non con tipi (44)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2448">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="7fbf0-2449">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2449">Target</span></span> | <span data-ttu-id="7fbf0-2450">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2450">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2451">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2451">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2452">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2452">32</span></span> |
| <span data-ttu-id="7fbf0-2453">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2453">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2454">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2454">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2455">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2455">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2456">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2456">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2457">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2457">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2458">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2458">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2459">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2459">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2460">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2460">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2461">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2461">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2462">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2462">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2463">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2463">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2464">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2464">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2465">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2465">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2466">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2466">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2467">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2467">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2468">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2468">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2469">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2470">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2471">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2472">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2473">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2474">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2475">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2476">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2476">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2477">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2478">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2479">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2480">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2481">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2482">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2483">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2484">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2485">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2485">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2486">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2486">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2487">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2487">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2488">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2488">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2489">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2489">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2490">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2490">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2491">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2491">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2492">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2492">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2493">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2494">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2495">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2496">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2496">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2497">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="7fbf0-2498">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2498">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="7fbf0-2499">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2499">Target</span></span> | <span data-ttu-id="7fbf0-2500">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2500">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2501">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2502">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2502">32</span></span> |
| <span data-ttu-id="7fbf0-2503">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2503">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2505">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2505">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2506">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2507">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2508">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2509">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2510">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2512">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2513">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2514">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2515">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2516">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2517">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2518">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2518">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2519">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2520">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2520">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2521">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2522">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2523">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2524">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2525">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2525">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2527">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2527">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2528">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2528">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2529">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2529">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2530">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2530">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2531">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2531">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2532">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2532">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2533">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2533">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2534">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2534">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2535">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2535">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2536">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2536">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2537">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2537">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2538">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2538">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2539">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2539">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-2541">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2541">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-2543">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2543">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-2545">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2545">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2546">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2546">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2547">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2547">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2548">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2548">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2549">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2549">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2550">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2550">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2551">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2551">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2552">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2552">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2553">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2553">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="7fbf0-2554">DXGI_FORMAT_R24 \_ UNORM \_ X8 di \_ tipo<sup>FNS</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2554">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="7fbf0-2555">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2555">Target</span></span> | <span data-ttu-id="7fbf0-2556">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2556">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2557">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2557">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2558">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2558">32</span></span> |
| <span data-ttu-id="7fbf0-2559">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2559">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2560">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2560">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2561">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2561">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2562">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2563">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2564">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2565">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2565">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2566">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2567">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2567">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2568">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2568">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2569">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2569">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2570">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2570">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2571">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2571">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2572">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2572">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2573">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2573">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2574">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2574">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2575">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2575">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2576">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2576">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2577">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2577">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2578">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2578">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2579">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2579">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2580">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2580">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2581">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2581">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2582">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2582">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2583">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2583">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2584">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2584">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2585">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2585">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2586">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2586">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2587">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2587">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2588">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2588">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2589">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2589">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2590">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2590">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2591">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2591">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2592">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2592">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2593">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2593">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2594">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2594">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2595">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2595">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2596">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2596">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2597">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2597">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2598">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2598">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2599">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2600">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2601">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2602">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2602">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2603">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="7fbf0-2604">DXGI_FORMAT_X24 di \_ tipo \_ G8 \_ UINT<sup>FNS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2604">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="7fbf0-2605">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2605">Target</span></span> | <span data-ttu-id="7fbf0-2606">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2606">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2607">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2608">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2608">32</span></span> |
| <span data-ttu-id="7fbf0-2609">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2609">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2610">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2610">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2611">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2611">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2612">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2612">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2613">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2613">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2614">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2614">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2615">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2616">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2616">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2617">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2617">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2618">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2618">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2619">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2620">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2620">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2621">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2621">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2622">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2622">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2623">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2623">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2624">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2624">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2625">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2625">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2626">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2626">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2627">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2627">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2628">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2628">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2629">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2629">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2630">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2630">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2631">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2631">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2632">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2632">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2633">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2633">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2634">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2634">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2635">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2635">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2636">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2636">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2637">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2637">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2638">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2638">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2639">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2639">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2640">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2640">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2641">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2641">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2642">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2642">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2643">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2643">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2644">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2644">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2645">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2645">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2646">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2646">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2647">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2647">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2648">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2648">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2649">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2649">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2650">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2650">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2651">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2651">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2652">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2652">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2653">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2653">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="7fbf0-2654">DXGI_FORMAT_R8G8 \_ <sup>PC</sup> non con tipi (48)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2654">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="7fbf0-2655">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2655">Target</span></span> | <span data-ttu-id="7fbf0-2656">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2656">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2657">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2657">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2658">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2658">16</span></span> |
| <span data-ttu-id="7fbf0-2659">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2659">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2660">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2660">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2661">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2661">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2662">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2662">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2663">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2663">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2664">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2664">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2665">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2666">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2666">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2667">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2667">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2668">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2668">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2669">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2669">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2670">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2670">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2671">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2671">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2672">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2672">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2673">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2673">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2674">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2674">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2675">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2675">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2676">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2676">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2677">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2677">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2678">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2678">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2679">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2679">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2680">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2680">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2681">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2681">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2682">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2682">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2683">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2683">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2684">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2684">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2685">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2685">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2686">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2686">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2687">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2687">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2688">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2688">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2689">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2689">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2690">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2690">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2691">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2691">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2692">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2693">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2694">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2695">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2696">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2696">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2697">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2698">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2699">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2700">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2700">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2701">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2701">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2702">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2702">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2703">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2703">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="7fbf0-2704">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2704">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="7fbf0-2705">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2705">Target</span></span> | <span data-ttu-id="7fbf0-2706">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2706">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2707">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2707">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2708">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2708">16</span></span> |
| <span data-ttu-id="7fbf0-2709">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2709">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2711">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2711">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2712">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2712">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2713">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2713">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2714">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2714">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2715">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2715">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2716">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2718">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2719">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2719">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2720">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2720">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2722">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2722">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2724">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2724">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2725">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2725">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2726">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2726">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2727">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2727">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2728">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2728">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2729">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2729">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2730">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2730">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2732">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2732">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2734">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2734">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2735">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2735">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2736">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2736">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2737">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2737">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2738">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2738">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2739">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2739">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2740">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2740">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2741">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2741">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2742">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2742">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2743">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2743">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2744">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2744">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2745">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2745">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2746">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2746">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2747">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2747">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2749">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2749">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2750">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2750">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2751">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2751">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2752">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2752">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2753">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2753">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2754">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2754">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2755">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2755">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2756">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2756">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2757">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2757">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2758">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2758">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2759">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2759">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2761">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2761">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="7fbf0-2762">DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2762">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="7fbf0-2763">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2763">Target</span></span> | <span data-ttu-id="7fbf0-2764">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2764">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2765">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2765">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2766">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2766">16</span></span> |
| <span data-ttu-id="7fbf0-2767">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2767">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2768">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2768">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2769">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2769">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2770">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2771">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2772">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2773">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2773">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2774">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2775">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2775">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2776">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2776">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2777">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2777">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2778">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2778">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2779">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2779">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2780">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2780">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2781">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2781">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2782">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2782">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2783">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2783">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2784">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2784">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2785">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2786">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2787">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2788">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2789">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2790">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2790">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2791">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2792">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2793">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2794">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2795">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2796">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2797">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2798">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2799">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2799">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2800">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2801">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2802">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2803">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2804">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2804">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2805">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2806">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2807">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2808">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2808">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2809">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2810">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2810">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2811">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="7fbf0-2812">DXGI_FORMAT_R8G8 \_ russar<sup>FNS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2812">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="7fbf0-2813">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2813">Target</span></span> | <span data-ttu-id="7fbf0-2814">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2815">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2816">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2816">16</span></span> |
| <span data-ttu-id="7fbf0-2817">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2817">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2819">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2820">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2821">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2822">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2823">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2824">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2826">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2827">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2828">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2828">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2830">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2830">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2832">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2833">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2834">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2835">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2836">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2838">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2840">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2841">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2842">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2843">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2844">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2845">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2845">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2846">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2847">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2848">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2849">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2850">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2851">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2852">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2852">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2853">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2853">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2854">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2854">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-2856">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2857">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2858">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2859">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2860">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2860">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2861">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2862">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2862">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2863">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2864">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2864">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2865">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2865">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2866">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2866">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2867">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2867">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="7fbf0-2868">DXGI_FORMAT_R8G8 \_ Sint<sup>FNS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2868">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="7fbf0-2869">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2869">Target</span></span> | <span data-ttu-id="7fbf0-2870">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2870">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2871">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2871">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2872">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2872">16</span></span> |
| <span data-ttu-id="7fbf0-2873">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2873">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2874">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2874">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2875">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2876">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2877">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2878">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2879">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2880">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2881">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2882">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2883">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2884">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2885">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2886">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2886">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2887">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2888">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2888">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2889">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2890">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2891">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2892">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2893">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2894">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2895">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2896">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2896">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2897">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2898">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2899">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2900">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2902">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2903">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2904">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2905">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2905">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2906">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2906">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2907">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2907">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2908">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2908">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2909">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2909">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2910">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2910">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2911">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2911">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2912">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2912">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2913">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2914">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2915">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2916">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2917">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2917">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="7fbf0-2918">DXGI_FORMAT_R16 \_ <sup>PC</sup> non con tipi (53)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2918">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="7fbf0-2919">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2919">Target</span></span> | <span data-ttu-id="7fbf0-2920">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2920">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2921">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2921">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2922">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2922">16</span></span> |
| <span data-ttu-id="7fbf0-2923">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2923">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2924">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2924">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2925">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2925">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2926">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2926">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2927">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2927">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2928">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2928">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2929">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2929">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2930">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2930">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2931">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2931">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2932">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2932">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2933">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2934">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2935">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2936">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2936">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2937">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2938">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2939">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2939">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2940">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2940">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2941">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2941">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2942">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2942">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2943">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2943">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2944">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2944">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2945">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2945">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2946">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2946">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2947">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2947">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2948">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2948">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2949">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2949">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-2950">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2950">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-2951">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2951">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-2952">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2952">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-2953">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2953">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2954">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2954">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-2955">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2955">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-2956">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2956">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2957">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2957">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2958">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2958">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-2959">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2959">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-2960">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2960">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2961">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2961">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-2962">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2962">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-2963">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2964">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2964">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-2965">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2965">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-2966">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2966">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-2967">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2967">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="7fbf0-2968">DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2968">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="7fbf0-2969">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2969">Target</span></span> | <span data-ttu-id="7fbf0-2970">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2970">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-2971">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2971">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-2972">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2972">16</span></span> |
| <span data-ttu-id="7fbf0-2973">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2973">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-2974">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2974">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2975">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2975">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2976">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2976">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2977">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2977">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-2978">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2978">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-2979">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2979">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-2980">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2980">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-2981">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2981">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-2982">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2982">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-2983">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2983">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2984">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2984">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2985">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2985">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-2986">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2986">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-2987">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2987">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-2988">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2988">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-2989">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2989">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-2990">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2990">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2991">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2991">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-2992">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2992">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-2993">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2993">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-2994">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2994">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2995">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2995">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-2996">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2996">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-2997">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2997">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-2998">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2998">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-2999">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-2999">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3000">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3000">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3001">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3001">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3002">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3002">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3003">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3003">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3004">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3004">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3005">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3005">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3006">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3007">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3008">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3009">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3010">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3010">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3011">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3012">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3013">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3014">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3015">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3016">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3016">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3017">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="7fbf0-3018">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3018">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="7fbf0-3019">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3019">Target</span></span> | <span data-ttu-id="7fbf0-3020">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3020">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3021">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3022">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3022">16</span></span> |
| <span data-ttu-id="7fbf0-3023">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3023">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3025">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3025">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3026">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3026">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3027">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3027">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3028">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3028">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3029">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3029">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3030">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3030">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3032">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3032">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3033">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3033">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3034">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3034">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3035">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3035">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3036">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3036">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3037">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3037">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3038">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3038">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3039">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3039">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3040">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3040">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3041">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3041">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3042">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3043">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3043">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3044">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3044">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3045">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3045">Depth/Stencil Target</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3047">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3047">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3048">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3048">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3049">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3049">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3050">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3050">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3051">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3051">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3052">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3052">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3053">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3053">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3054">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3054">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3055">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3055">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3056">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3056">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3057">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3057">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3058">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3058">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3059">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3059">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-3061">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3061">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-3063">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3063">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-3065">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3066">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3066">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3067">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3068">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3069">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3070">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3071">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3072">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3072">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3073">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3073">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="7fbf0-3074">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3074">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="7fbf0-3075">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3075">Target</span></span> | <span data-ttu-id="7fbf0-3076">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3076">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3077">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3077">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3078">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3078">16</span></span> |
| <span data-ttu-id="7fbf0-3079">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3079">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3080">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3080">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3081">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3081">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3082">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3082">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3083">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3083">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3084">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3084">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3085">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3086">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3086">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3087">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3087">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3088">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3088">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3089">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3089">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3090">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3090">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3091">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3091">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3092">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3092">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3093">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3093">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3094">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3094">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3095">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3096">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3097">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3098">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3099">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3100">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3101">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3102">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3102">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3103">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3104">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3105">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3106">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3108">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3109">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3110">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3111">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3111">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3112">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3112">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3113">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3113">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3114">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3114">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3115">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3115">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3116">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3116">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3117">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3117">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3118">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3118">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3119">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3120">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3121">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3122">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3122">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3123">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3123">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="7fbf0-3124">DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3124">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="7fbf0-3125">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3125">Target</span></span> | <span data-ttu-id="7fbf0-3126">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3126">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3127">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3127">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3128">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3128">16</span></span> |
| <span data-ttu-id="7fbf0-3129">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3129">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3131">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3131">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3132">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3132">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3133">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3133">Input Assembler Index Buffer</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3135">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3135">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3136">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3136">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3137">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3137">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3138">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3138">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3139">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3140">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3140">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3141">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3141">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3142">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3142">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3143">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3143">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3144">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3144">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3145">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3145">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3146">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3146">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3147">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3147">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3148">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3148">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3149">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3149">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3150">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3150">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3151">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3151">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3152">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3152">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3153">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3153">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3154">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3154">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3155">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3155">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3156">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3156">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3157">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3157">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3158">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3158">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3159">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3159">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3160">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3160">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3161">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3161">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3162">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3162">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3163">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3163">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3164">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3164">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3165">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3165">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3166">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3166">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3167">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3167">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3168">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3168">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3169">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3169">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3170">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3170">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3171">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3171">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3172">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3172">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3173">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3173">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3174">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3174">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3175">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="7fbf0-3176">DXGI_FORMAT_R16 \_ russar<sup>FNS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3176">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="7fbf0-3177">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3177">Target</span></span> | <span data-ttu-id="7fbf0-3178">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3178">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3179">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3180">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3180">16</span></span> |
| <span data-ttu-id="7fbf0-3181">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3181">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3182">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3182">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3183">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3183">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3184">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3185">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3185">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3186">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3186">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3187">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3188">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3188">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3189">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3190">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3190">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3191">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3191">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3192">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3192">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3193">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3193">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3194">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3194">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3195">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3195">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3196">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3196">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3197">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3198">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3199">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3200">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3201">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3202">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3203">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3204">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3204">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3205">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3206">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3207">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3208">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3210">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3211">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3212">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3213">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3213">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3214">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3214">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3215">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3215">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3216">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3216">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3217">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3217">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3218">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3218">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3219">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3219">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3220">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3220">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3221">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3221">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3222">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3222">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3223">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3223">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3224">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3224">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3225">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3225">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="7fbf0-3226">DXGI_FORMAT_R16 \_ Sint<sup>FNS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3226">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="7fbf0-3227">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3227">Target</span></span> | <span data-ttu-id="7fbf0-3228">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3228">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3229">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3229">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3230">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3230">16</span></span> |
| <span data-ttu-id="7fbf0-3231">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3231">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3232">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3232">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3233">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3233">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3234">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3234">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3235">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3235">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3236">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3236">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3237">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3237">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3238">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3238">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3239">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3240">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3240">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3241">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3241">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3242">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3242">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3243">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3243">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3244">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3244">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3245">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3245">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3246">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3246">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3247">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3247">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3248">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3248">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3249">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3249">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3250">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3250">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3251">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3251">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3252">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3252">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3253">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3253">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3254">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3254">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3255">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3255">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3256">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3256">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3257">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3257">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3258">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3258">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3259">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3259">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3260">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3260">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3261">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3261">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3262">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3262">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3263">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3263">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3264">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3264">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3265">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3265">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3266">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3266">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3267">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3267">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3268">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3268">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3269">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3269">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3270">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3270">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3271">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3271">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3272">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3272">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3273">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3273">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3274">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3274">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3275">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3275">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="7fbf0-3276">DXGI_FORMAT_R8 \_ <sup>PC</sup> non con tipi (60)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3276">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="7fbf0-3277">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3277">Target</span></span> | <span data-ttu-id="7fbf0-3278">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3278">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3279">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3279">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3280">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3280">8</span></span> |
| <span data-ttu-id="7fbf0-3281">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3281">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3282">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3282">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3283">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3283">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3284">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3284">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3285">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3285">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3286">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3286">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3287">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3287">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3288">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3288">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3289">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3289">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3290">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3290">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3291">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3292">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3293">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3294">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3294">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3295">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3296">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3296">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3297">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3297">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3298">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3299">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3299">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3300">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3300">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3301">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3301">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3302">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3302">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3303">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3303">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3304">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3304">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3305">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3305">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3306">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3306">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3307">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3307">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3308">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3308">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3309">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3309">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3310">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3310">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3311">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3311">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3312">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3312">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3313">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3313">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3314">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3314">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3315">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3315">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3316">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3316">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3317">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3317">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3318">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3318">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3319">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3319">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3320">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3320">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3321">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3321">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3322">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3322">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3323">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3323">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3324">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3324">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3325">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3325">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="7fbf0-3326">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3326">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="7fbf0-3327">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3327">Target</span></span> | <span data-ttu-id="7fbf0-3328">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3328">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3329">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3329">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3330">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3330">8</span></span> |
| <span data-ttu-id="7fbf0-3331">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3331">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3333">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3333">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3334">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3334">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3335">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3335">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3336">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3336">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3337">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3337">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3338">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3338">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3340">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3340">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3342">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3344">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3344">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3346">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3346">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3348">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3348">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3349">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3349">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3350">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3350">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3351">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3351">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3352">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3352">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3354">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3354">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3355">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3355">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3357">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3357">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3359">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3360">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3361">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3362">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3363">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3363">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3364">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3365">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3366">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3367">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3369">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3370">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3371">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3372">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3372">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3374">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3374">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3375">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3375">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3376">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3376">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3377">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3378">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3378">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3379">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3380">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3380">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3381">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3381">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3382">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3382">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3383">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3383">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3384">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3384">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3386">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3386">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="7fbf0-3387">DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3387">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="7fbf0-3388">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3388">Target</span></span> | <span data-ttu-id="7fbf0-3389">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3389">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3390">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3390">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3391">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3391">8</span></span> |
| <span data-ttu-id="7fbf0-3392">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3392">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3393">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3393">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3394">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3394">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3395">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3395">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3396">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3396">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3397">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3397">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3398">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3399">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3399">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3400">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3400">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3401">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3401">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3402">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3402">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3403">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3403">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3404">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3404">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3405">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3405">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3406">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3406">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3407">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3407">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3408">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3408">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3409">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3410">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3411">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3412">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3413">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3414">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3415">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3415">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3416">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3416">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3417">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3417">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3418">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3418">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3419">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3419">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3420">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3420">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3421">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3421">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3422">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3422">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3423">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3423">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3424">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3424">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3425">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3426">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3427">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3428">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3429">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3429">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3430">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3431">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3431">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3432">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3433">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3434">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3435">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3435">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3436">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="7fbf0-3437">DXGI_FORMAT_R8 \_ russar<sup>FNS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3437">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="7fbf0-3438">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3438">Target</span></span> | <span data-ttu-id="7fbf0-3439">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3439">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3440">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3441">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3441">8</span></span> |
| <span data-ttu-id="7fbf0-3442">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3442">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3443">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3443">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3444">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3445">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3446">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3447">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3448">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3449">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3450">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3451">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3452">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3453">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3454">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3455">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3456">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3457">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3458">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3459">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3460">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3460">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3461">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3461">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3462">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3462">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3463">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3463">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3464">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3464">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3465">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3465">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3466">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3466">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3467">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3467">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3468">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3468">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3469">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3469">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3470">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3470">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3471">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3471">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3472">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3472">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3473">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3473">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3474">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3474">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3475">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3475">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3476">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3476">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3477">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3477">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3478">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3478">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3479">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3479">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3480">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3480">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3481">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3481">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3482">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3482">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3483">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3483">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3484">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3484">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3485">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3485">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3486">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3486">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="7fbf0-3487">DXGI_FORMAT_R8 \_ Sint<sup>FNS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3487">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="7fbf0-3488">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3488">Target</span></span> | <span data-ttu-id="7fbf0-3489">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3489">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3490">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3490">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3491">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3491">8</span></span> |
| <span data-ttu-id="7fbf0-3492">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3492">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3493">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3493">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3494">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3495">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3496">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3497">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3498">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3499">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3499">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3500">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3501">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3501">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3502">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3502">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3503">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3503">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3504">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3504">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3505">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3505">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3506">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3506">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3507">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3507">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3508">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3508">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3509">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3509">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3510">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3510">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3511">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3511">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3512">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3512">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3513">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3513">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3514">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3514">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3515">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3515">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3516">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3516">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3517">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3517">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3518">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3518">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3519">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3519">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3520">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3520">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3521">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3521">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3522">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3522">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3523">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3523">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3524">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3524">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3525">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3525">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3526">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3526">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3527">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3527">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3528">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3528">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3529">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3529">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3530">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3530">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3531">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3531">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3532">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3532">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3533">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3533">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3534">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3534">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3535">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3535">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3536">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3536">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="7fbf0-3537">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3537">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="7fbf0-3538">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3538">Target</span></span> | <span data-ttu-id="7fbf0-3539">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3539">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3540">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3540">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3541">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3541">8</span></span> |
| <span data-ttu-id="7fbf0-3542">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3542">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3544">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3544">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3545">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3545">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3546">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3546">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3547">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3547">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3548">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3548">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3549">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3549">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3551">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3551">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3552">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3552">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3553">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3553">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3555">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3555">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3557">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3558">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3559">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3559">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3560">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3561">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3562">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3563">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3565">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3565">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3567">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3567">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3568">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3568">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3569">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3569">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3570">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3570">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3571">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3571">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3572">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3572">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3573">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3573">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3574">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3575">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3576">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3577">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3578">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3578">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3579">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3579">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3580">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3580">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3582">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3582">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3583">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3583">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3584">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3585">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3586">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3586">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3587">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3588">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3589">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3590">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3591">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3592">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3592">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3594">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="7fbf0-3595">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3595">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="7fbf0-3596">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3596">Target</span></span> | <span data-ttu-id="7fbf0-3597">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3597">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3598">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3599">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3599">32</span></span> |
| <span data-ttu-id="7fbf0-3600">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3600">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3601">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3601">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3602">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3602">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3603">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3603">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3604">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3604">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3605">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3605">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3606">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3607">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3607">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3608">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3608">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3609">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3609">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3610">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3610">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3611">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3612">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3613">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3613">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3614">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3615">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3615">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3616">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3617">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3618">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3618">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3619">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3619">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3620">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3620">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3621">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3621">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3622">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3622">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3623">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3623">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3624">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3624">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3625">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3625">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3626">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3626">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3627">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3627">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3628">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3628">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3629">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3629">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3630">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3630">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3631">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3631">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3632">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3632">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3633">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3633">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3634">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3634">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3635">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3635">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3636">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3636">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3637">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3637">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3638">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3638">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3639">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3639">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3640">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3640">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3641">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3641">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3642">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3642">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3643">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3643">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3644">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3644">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="7fbf0-3645">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3645">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="7fbf0-3646">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3646">Target</span></span> | <span data-ttu-id="7fbf0-3647">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3647">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3648">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3648">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3649">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3649">16</span></span> |
| <span data-ttu-id="7fbf0-3650">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3650">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3651">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3651">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3652">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3652">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3653">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3653">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3654">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3654">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3655">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3655">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3656">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3657">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3658">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3659">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3659">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3660">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3660">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3661">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3661">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3662">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3662">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3663">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3663">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3664">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3664">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3665">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3665">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3666">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3666">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3667">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3667">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3668">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3668">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3669">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3669">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3670">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3670">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3671">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3671">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3672">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3672">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3673">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3673">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3674">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3674">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3675">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3675">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3676">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3676">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3677">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3677">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3678">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3678">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3679">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3679">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3680">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3680">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3681">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3681">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3682">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3682">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3683">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3684">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3685">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3686">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3687">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3687">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3688">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3688">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3689">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3689">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3690">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3690">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3691">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3691">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3692">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3692">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3693">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3693">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3694">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="7fbf0-3695">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3695">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="7fbf0-3696">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3696">Target</span></span> | <span data-ttu-id="7fbf0-3697">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3697">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3698">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3699">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3699">16</span></span> |
| <span data-ttu-id="7fbf0-3700">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3700">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3701">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3701">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3702">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3702">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3703">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3703">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3704">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3704">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3705">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3705">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3706">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3706">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3707">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3707">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3708">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3708">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3709">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3709">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3710">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3711">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3712">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3713">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3713">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3714">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3715">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3716">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3716">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3717">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3718">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3719">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3720">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3721">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3722">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3723">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3723">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3724">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3725">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3726">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3727">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3728">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3729">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3730">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3730">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3731">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3731">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3732">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3732">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3733">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3733">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3734">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3734">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3735">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3735">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3736">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3736">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3737">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3737">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3738">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3738">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3739">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3739">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3740">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3741">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3741">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3742">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3742">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3743">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3743">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3744">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3744">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="7fbf0-3745">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non tipizzato (70)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3745">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="7fbf0-3746">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3746">Target</span></span> | <span data-ttu-id="7fbf0-3747">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3747">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3748">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3748">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3749">4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3749">4</span></span> |
| <span data-ttu-id="7fbf0-3750">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3750">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3751">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3751">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3752">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3752">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3753">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3753">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3754">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3754">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3755">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3755">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3756">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3756">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3757">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3758">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3758">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3759">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3759">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3760">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3760">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3761">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3761">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3762">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3762">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3763">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3763">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3764">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3764">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3765">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3765">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3766">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3766">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3767">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3767">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3768">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3768">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3769">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3769">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3770">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3770">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3771">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3771">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3772">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3772">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3773">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3773">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3774">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3774">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3775">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3775">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3776">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3776">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3777">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3777">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3778">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3778">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3779">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3779">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3780">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3780">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3781">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3781">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3782">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3782">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3783">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3783">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3784">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3784">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3785">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3785">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3786">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3786">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3787">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3787">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3788">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3788">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3789">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3789">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3790">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3790">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3791">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3791">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3792">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3792">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3793">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3793">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3794">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3794">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="7fbf0-3795">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3795">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="7fbf0-3796">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3796">Target</span></span> | <span data-ttu-id="7fbf0-3797">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3797">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3798">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3798">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3799">4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3799">4</span></span> |
| <span data-ttu-id="7fbf0-3800">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3800">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3802">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3802">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3803">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3803">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3804">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3805">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3806">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3807">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3810">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3812">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3812">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3814">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3814">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3816">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3816">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3817">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3817">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3818">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3818">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3819">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3819">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3820">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3820">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3822">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3822">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3823">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3823">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3824">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3824">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3825">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3825">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3826">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3826">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3827">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3827">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3828">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3828">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3829">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3829">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3830">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3830">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3831">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3831">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3832">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3832">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3833">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3833">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3834">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3834">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3835">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3835">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3836">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3836">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3837">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3837">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3838">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3838">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3840">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3841">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3842">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3843">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3844">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3845">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3846">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3847">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3848">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3849">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3850">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3850">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3852">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3852">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="7fbf0-3853">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FNC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3853">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="7fbf0-3854">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3854">Target</span></span> | <span data-ttu-id="7fbf0-3855">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3855">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3856">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3856">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3857">4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3857">4</span></span> |
| <span data-ttu-id="7fbf0-3858">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3858">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3860">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3860">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3861">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3861">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3862">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3862">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3863">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3863">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3864">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3864">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3865">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3865">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3867">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3867">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3868">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3870">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3870">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3872">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3872">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3874">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3874">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3875">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3875">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3876">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3876">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3877">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3877">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3878">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3878">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3880">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3881">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3882">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3883">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3884">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3885">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3886">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3887">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3887">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3888">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3889">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3890">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3891">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3893">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3894">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3895">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3896">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3896">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3898">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3898">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3899">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3899">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3900">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3900">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3901">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3901">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3902">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3902">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3903">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3903">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3904">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3904">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3905">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3906">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3907">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3908">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3908">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3910">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3910">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="7fbf0-3911">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non tipizzato (73)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3911">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="7fbf0-3912">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3912">Target</span></span> | <span data-ttu-id="7fbf0-3913">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3913">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3914">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3914">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3915">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3915">8</span></span> |
| <span data-ttu-id="7fbf0-3916">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3916">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3917">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3917">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3918">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3918">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3919">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3919">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3920">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3920">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3921">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3921">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3922">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3922">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-3923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3923">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3924">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-3925">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3925">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-3926">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3926">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3927">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3927">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3928">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3928">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3929">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3929">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3930">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3930">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3931">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3931">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-3932">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3932">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3933">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3933">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3934">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3934">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3935">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3935">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3936">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3936">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3937">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3937">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3938">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3938">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3939">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3939">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3940">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3940">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3941">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3941">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3942">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3942">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3943">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3943">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-3944">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3944">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-3945">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3945">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-3946">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3946">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3947">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3947">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-3948">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3948">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-3949">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3949">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3950">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3950">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3951">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3951">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-3952">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3952">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-3953">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3953">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3954">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3954">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-3955">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3955">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-3956">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3956">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-3957">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3957">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-3958">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3958">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-3959">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3959">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-3960">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3960">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="7fbf0-3961">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3961">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="7fbf0-3962">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3962">Target</span></span> | <span data-ttu-id="7fbf0-3963">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3963">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-3964">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3964">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-3965">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3965">8</span></span> |
| <span data-ttu-id="7fbf0-3966">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3966">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3968">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3968">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3969">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3969">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3970">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3970">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3971">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3971">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-3972">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3972">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-3973">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3973">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3975">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3975">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-3976">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3976">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3978">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3978">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3980">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3980">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3982">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3982">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3983">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3983">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-3984">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3984">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-3985">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3985">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-3986">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3986">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-3988">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3988">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-3989">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3989">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3990">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3990">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-3991">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3991">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-3992">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-3993">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3994">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-3995">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3995">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-3996">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-3997">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-3998">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-3999">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-3999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4000">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4001">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4002">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4003">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4004">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4004">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4006">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4007">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4008">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4009">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4010">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4010">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4011">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4012">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4013">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4014">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4015">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4016">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4016">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4018">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4018">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="7fbf0-4019">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FNC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4019">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="7fbf0-4020">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4020">Target</span></span> | <span data-ttu-id="7fbf0-4021">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4021">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4022">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4022">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4023">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4023">8</span></span> |
| <span data-ttu-id="7fbf0-4024">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4024">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4026">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4026">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4027">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4027">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4028">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4029">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4029">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4030">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4030">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4031">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4031">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4033">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4033">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4034">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4034">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4036">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4036">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4038">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4038">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4040">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4040">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4041">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4041">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4042">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4042">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4043">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4043">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4044">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4044">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4046">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4046">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4047">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4047">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4048">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4048">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4049">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4049">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4050">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4050">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4051">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4051">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4052">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4052">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4053">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4053">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4054">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4054">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4055">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4055">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4056">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4057">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4058">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4059">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4060">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4060">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4061">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4061">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4062">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4062">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4064">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4064">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4065">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4065">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4066">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4066">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4067">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4067">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4068">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4068">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4069">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4069">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4070">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4070">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4071">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4072">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4072">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4073">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4073">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4074">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4074">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4076">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="7fbf0-4077">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non tipizzato (76)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4077">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="7fbf0-4078">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4078">Target</span></span> | <span data-ttu-id="7fbf0-4079">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4079">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4080">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4081">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4081">8</span></span> |
| <span data-ttu-id="7fbf0-4082">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4082">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4083">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4083">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4084">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4085">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4086">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4087">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4088">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-4089">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4089">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4090">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4090">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-4091">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4091">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-4092">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4092">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4093">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4093">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4094">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4094">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4095">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4095">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4096">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4096">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4097">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4097">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-4098">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4098">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4099">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4100">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4101">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4102">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4103">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4104">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4105">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4105">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4106">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4107">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4108">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4109">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4110">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4111">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4112">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4112">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4113">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4113">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4114">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4114">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-4115">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4116">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4117">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4118">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4119">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4119">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4120">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4121">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4122">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4122">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4123">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4123">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4124">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4124">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4125">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4125">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4126">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4126">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="7fbf0-4127">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4127">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="7fbf0-4128">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4128">Target</span></span> | <span data-ttu-id="7fbf0-4129">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4129">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4130">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4131">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4131">8</span></span> |
| <span data-ttu-id="7fbf0-4132">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4132">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4134">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4134">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4135">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4135">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4136">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4136">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4137">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4137">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4138">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4139">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4139">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4141">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4142">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4142">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4144">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4144">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4146">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4146">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4148">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4148">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4149">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4149">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4150">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4150">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4151">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4151">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4152">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4152">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4154">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4154">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4155">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4155">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4156">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4156">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4157">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4157">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4158">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4158">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4159">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4159">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4160">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4160">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4161">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4161">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4162">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4162">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4163">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4163">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4164">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4164">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4165">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4165">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4166">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4166">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4167">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4167">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4168">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4168">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4169">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4169">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4170">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4170">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4172">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4172">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4173">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4173">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4174">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4174">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4175">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4175">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4176">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4176">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4177">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4177">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4178">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4178">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4179">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4179">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4180">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4180">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4181">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4181">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4182">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4182">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4184">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4184">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="7fbf0-4185">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FNC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4185">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="7fbf0-4186">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4186">Target</span></span> | <span data-ttu-id="7fbf0-4187">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4187">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4188">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4188">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4189">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4189">8</span></span> |
| <span data-ttu-id="7fbf0-4190">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4190">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4192">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4192">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4193">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4193">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4194">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4194">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4195">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4195">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4196">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4196">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4197">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4197">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4199">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4199">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4200">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4202">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4202">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4204">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4204">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4206">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4207">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4208">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4209">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4210">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4210">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4212">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4213">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4214">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4215">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4216">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4217">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4218">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4219">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4219">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4220">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4221">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4222">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4223">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4225">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4226">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4227">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4228">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4228">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4230">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4230">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4231">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4231">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4232">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4232">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4233">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4233">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4234">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4234">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4235">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4235">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4236">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4236">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4237">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4237">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4238">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4238">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4239">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4239">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4240">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4240">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4242">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4242">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="7fbf0-4243">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non tipizzato (79)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4243">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="7fbf0-4244">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4244">Target</span></span> | <span data-ttu-id="7fbf0-4245">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4245">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4246">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4246">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4247">4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4247">4</span></span> |
| <span data-ttu-id="7fbf0-4248">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4248">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4249">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4250">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4250">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4251">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4251">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4252">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4252">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4253">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4253">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4254">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-4255">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4255">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4256">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4256">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-4257">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4257">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-4258">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4258">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4259">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4260">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4261">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4261">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4262">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4263">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-4264">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4264">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4265">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4265">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4266">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4266">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4267">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4267">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4268">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4268">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4269">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4269">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4270">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4270">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4271">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4271">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4272">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4272">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4273">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4273">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4274">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4274">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4275">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4275">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4276">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4276">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4277">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4277">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4278">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4278">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4279">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4279">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4280">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4280">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-4281">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4281">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4282">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4282">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4283">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4283">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4284">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4284">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4285">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4285">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4286">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4286">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4287">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4287">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4288">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4289">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4290">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4291">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4291">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4292">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="7fbf0-4293">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4293">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="7fbf0-4294">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4294">Target</span></span> | <span data-ttu-id="7fbf0-4295">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4295">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4296">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4297">4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4297">4</span></span> |
| <span data-ttu-id="7fbf0-4298">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4298">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4299">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4300">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4301">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4302">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4304">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-4305">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4305">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4306">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4306">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-4307">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4307">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-4308">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4308">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4309">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4309">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4310">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4310">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4311">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4311">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4312">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4312">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4313">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4313">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-4314">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4314">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4315">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4315">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4316">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4316">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4317">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4317">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4318">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4318">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4319">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4319">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4320">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4320">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4321">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4321">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4322">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4322">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4323">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4323">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4324">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4324">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4325">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4325">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4326">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4326">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4327">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4327">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4328">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4328">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4329">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4329">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4330">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4330">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-4331">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4332">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4333">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4334">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4335">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4335">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4336">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4337">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4337">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4338">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4338">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4339">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4339">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4340">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4340">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4341">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4341">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4342">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4342">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="7fbf0-4343">DXGI_FORMAT_BC4 \_ russar<sup>FNC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4343">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="7fbf0-4344">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4344">Target</span></span> | <span data-ttu-id="7fbf0-4345">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4345">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4346">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4346">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4347">4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4347">4</span></span> |
| <span data-ttu-id="7fbf0-4348">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4348">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4349">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4349">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4350">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4350">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4351">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4352">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4353">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4354">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4354">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-4355">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4355">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4356">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4356">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-4357">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4357">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-4358">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4358">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4359">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4359">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4360">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4360">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4361">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4361">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4362">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4362">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4363">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4363">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-4364">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4364">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4365">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4365">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4366">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4366">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4367">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4367">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4368">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4368">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4369">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4369">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4370">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4370">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4371">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4371">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4372">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4372">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4373">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4373">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4374">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4374">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4375">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4375">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4376">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4376">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4377">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4377">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4378">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4378">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4379">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4379">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4380">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4380">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-4381">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4381">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4382">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4382">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4383">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4383">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4384">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4384">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4385">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4385">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4386">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4386">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4387">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4387">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4388">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4388">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4389">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4389">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4390">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4390">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4391">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4391">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4392">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4392">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="7fbf0-4393">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non tipizzato (82)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4393">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="7fbf0-4394">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4394">Target</span></span> | <span data-ttu-id="7fbf0-4395">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4395">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4396">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4396">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4397">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4397">8</span></span> |
| <span data-ttu-id="7fbf0-4398">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4398">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4399">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4399">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4400">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4400">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4401">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4402">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4403">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4404">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-4405">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4405">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4406">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4406">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-4407">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4407">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-4408">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4408">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4409">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4409">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4410">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4410">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4411">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4411">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4412">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4412">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4413">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4413">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-4414">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4414">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4415">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4415">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4416">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4417">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4418">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4419">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4420">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4421">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4421">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4422">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4422">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4423">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4423">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4424">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4424">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4425">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4425">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4426">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4426">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4427">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4427">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4428">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4428">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4429">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4429">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4430">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4430">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-4431">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4431">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4432">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4432">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4433">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4433">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4434">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4434">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4435">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4435">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4436">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4437">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4438">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4439">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4440">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4441">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4441">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4442">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="7fbf0-4443">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4443">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="7fbf0-4444">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4444">Target</span></span> | <span data-ttu-id="7fbf0-4445">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4445">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4446">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4447">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4447">8</span></span> |
| <span data-ttu-id="7fbf0-4448">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4448">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4449">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4449">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4450">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4451">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4452">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4453">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4454">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4454">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-4455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4455">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4456">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4456">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-4457">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4457">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-4458">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4458">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4459">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4459">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4460">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4460">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4461">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4461">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4462">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4462">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4463">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4463">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-4464">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4464">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4465">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4465">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4466">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4466">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4467">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4467">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4468">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4468">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4469">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4470">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4471">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4471">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4472">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4473">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4474">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4475">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4476">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4477">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4478">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4479">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4480">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4480">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-4481">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4481">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4482">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4482">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4483">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4483">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4484">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4484">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4485">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4485">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4486">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4486">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4487">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4487">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4488">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4488">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4489">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4489">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4490">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4490">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4491">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4491">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4492">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4492">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="7fbf0-4493">DXGI_FORMAT_BC5 \_ russar<sup>FNC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4493">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="7fbf0-4494">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4494">Target</span></span> | <span data-ttu-id="7fbf0-4495">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4495">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4496">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4496">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4497">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4497">8</span></span> |
| <span data-ttu-id="7fbf0-4498">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4498">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4499">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4499">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4500">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4500">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4501">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4501">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4502">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4502">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4503">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4503">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4504">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4504">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-4505">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4505">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4506">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-4507">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4507">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-4508">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4508">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4509">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4509">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4510">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4510">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4511">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4511">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4512">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4512">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4513">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4513">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-4514">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4515">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4516">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4517">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4518">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4519">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4520">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4521">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4521">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4522">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4523">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4524">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4525">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4526">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4527">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4528">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4529">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4530">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4530">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-4531">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4531">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4532">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4532">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4533">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4533">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4534">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4534">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4535">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4535">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4536">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4536">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4537">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4537">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4538">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4538">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4539">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4539">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4540">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4540">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4541">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4541">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4542">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="7fbf0-4543">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4543">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="7fbf0-4544">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4544">Target</span></span> | <span data-ttu-id="7fbf0-4545">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4546">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4547">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4547">16</span></span> |
| <span data-ttu-id="7fbf0-4548">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4548">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4550">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4551">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4552">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4553">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4554">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4555">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4555">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4557">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4558">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4560">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4560">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4562">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4562">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4564">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4564">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4565">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4565">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4566">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4566">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4567">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4567">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4568">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4568">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4570">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4570">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4572">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4574">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4574">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4576">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4577">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4578">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4579">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4580">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4580">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4581">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4582">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4583">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4584">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4585">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4586">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4587">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4588">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4589">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4589">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4591">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4591">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4593">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4593">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4595">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4595">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4597">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4597">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4599">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4599">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4600">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4600">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4601">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4601">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4602">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4602">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4603">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4603">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4604">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4604">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4605">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4605">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4606">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4606">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="7fbf0-4607">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4607">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="7fbf0-4608">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4608">Target</span></span> | <span data-ttu-id="7fbf0-4609">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4609">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4610">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4610">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4611">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4611">16</span></span> |
| <span data-ttu-id="7fbf0-4612">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4612">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4614">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4614">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4615">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4615">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4616">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4616">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4617">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4617">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4618">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4618">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4619">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4621">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4622">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4622">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4624">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4624">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4626">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4626">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4628">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4628">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4629">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4629">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4630">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4630">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4631">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4631">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4632">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4632">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4634">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4634">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4635">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4635">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4636">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4636">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4637">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4637">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4638">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4638">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4639">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4639">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4640">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4640">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4641">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4641">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4642">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4642">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4643">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4643">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4644">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4644">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4645">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4645">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4646">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4646">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4647">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4647">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4648">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4648">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4649">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4649">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4650">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4650">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4652">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4652">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4653">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4653">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4654">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4654">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4655">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4655">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4656">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4656">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4657">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4658">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4658">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4659">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4659">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4660">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4660">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4661">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4661">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4662">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4662">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4663">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="7fbf0-4664">DXGI_FORMAT_B8G8R8A8 \_ <sup>PC</sup> non con tipi (90)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4664">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="7fbf0-4665">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4665">Target</span></span> | <span data-ttu-id="7fbf0-4666">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4666">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4667">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4668">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4668">32</span></span> |
| <span data-ttu-id="7fbf0-4669">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4669">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4670">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4670">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4671">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4672">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4673">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4674">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4675">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4675">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4676">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4677">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4677">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-4678">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4678">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-4679">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4679">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4680">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4681">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4682">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4682">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4683">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4684">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4684">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-4685">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4685">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4686">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4686">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4687">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4687">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4688">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4688">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4689">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4689">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4690">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4690">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4691">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4691">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4692">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4692">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4693">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4693">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4694">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4694">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4695">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4695">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4696">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4696">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4697">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4697">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4698">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4698">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4699">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4699">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4700">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4700">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4701">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4701">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-4702">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4702">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4703">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4703">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4704">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4704">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4705">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4705">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4706">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4707">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4708">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4709">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4710">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4711">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4712">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4713">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="7fbf0-4714">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4714">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="7fbf0-4715">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4715">Target</span></span> | <span data-ttu-id="7fbf0-4716">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4717">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4718">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4718">32</span></span> |
| <span data-ttu-id="7fbf0-4719">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4719">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4721">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4722">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4723">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4724">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4726">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4728">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4730">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4732">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4732">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4734">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4734">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4736">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4737">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4738">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4738">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4739">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4740">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4740">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4742">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4742">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4744">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4746">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4746">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4748">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4749">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4750">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4751">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4752">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4752">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4753">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4754">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4755">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4756">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4757">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4758">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4759">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4760">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4761">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4761">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4763">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4763">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4765">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4765">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4767">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4767">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4769">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4769">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4771">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4771">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4772">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4772">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4774">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4774">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4775">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4775">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4776">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4776">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4778">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4778">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4780">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4780">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4782">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="7fbf0-4783">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4783">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="7fbf0-4784">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4784">Target</span></span> | <span data-ttu-id="7fbf0-4785">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4785">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4786">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4787">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4787">32</span></span> |
| <span data-ttu-id="7fbf0-4788">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4788">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4790">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4790">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4791">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4791">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4792">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4792">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4793">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4793">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4794">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4794">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4795">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4797">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4799">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4799">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4801">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4801">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4803">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4803">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4805">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4805">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4806">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4806">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4807">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4807">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4808">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4808">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4809">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4809">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4811">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4811">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4813">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4815">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4815">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4817">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4817">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4818">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4818">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4819">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4819">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4820">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4820">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4821">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4821">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4822">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4822">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4823">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4823">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4824">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4824">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4825">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4825">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4826">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4826">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4827">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4827">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4828">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4828">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4829">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4829">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4830">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4830">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4832">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4832">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4834">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4834">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4836">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4836">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4838">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4838">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4840">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4840">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4841">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4841">Display Scan-Out</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4843">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4843">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4844">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4844">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4845">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4845">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4847">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4847">Video Processor Output</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4849">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4849">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4851">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="7fbf0-4852">DXGI_FORMAT_B8G8R8X8 \_ <sup>PC</sup> non con tipi (92)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4852">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="7fbf0-4853">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4853">Target</span></span> | <span data-ttu-id="7fbf0-4854">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4854">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4855">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4856">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4856">32</span></span> |
| <span data-ttu-id="7fbf0-4857">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4857">Format Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4858">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4858">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4859">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4860">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4861">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4862">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4863">Texture2D</span></span> | \- |
| <span data-ttu-id="7fbf0-4864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4864">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-4865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4865">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-4866">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-4867">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4868">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4869">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4870">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4870">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4871">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4872">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4872">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-4873">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-4874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4874">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4875">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4876">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4877">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4878">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4879">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4880">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4880">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4881">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4882">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4883">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4884">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4886">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4887">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4888">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4889">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-4890">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4891">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-4892">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-4893">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-4894">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4894">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4895">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4896">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4897">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4898">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-4899">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-4900">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4900">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-4901">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="7fbf0-4902">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4902">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="7fbf0-4903">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4903">Target</span></span> | <span data-ttu-id="7fbf0-4904">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4904">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4905">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4906">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4906">32</span></span> |
| <span data-ttu-id="7fbf0-4907">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4907">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4909">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4909">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4910">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4911">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4912">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4913">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4914">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4916">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4918">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4918">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4920">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4920">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4922">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4922">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4924">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4924">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4925">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4925">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4926">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4926">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4927">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4927">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4928">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4928">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4930">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4930">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4932">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4932">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4934">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4934">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4936">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4936">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-4937">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4937">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-4938">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4938">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4939">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4939">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-4940">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4940">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-4941">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4941">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-4942">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4942">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4943">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4943">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-4944">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4944">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-4945">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4945">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-4946">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4946">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-4947">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4947">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4948">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4948">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-4949">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4949">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4951">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4951">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4953">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4953">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4955">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4955">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4957">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4957">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4959">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4959">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-4960">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4960">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-4961">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4961">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-4962">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4962">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-4963">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4963">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4965">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4965">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-4967">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4967">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4969">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4969">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="7fbf0-4970">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FNS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4970">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="7fbf0-4971">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4971">Target</span></span> | <span data-ttu-id="7fbf0-4972">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4972">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-4973">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4973">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-4974">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4974">32</span></span> |
| <span data-ttu-id="7fbf0-4975">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4975">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4977">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4977">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4978">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4978">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4979">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4979">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4980">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4980">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-4981">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4981">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-4982">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4982">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4984">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4984">Texture3D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4986">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4986">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4988">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4988">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4990">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4990">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4992">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4992">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4993">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4993">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-4994">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4994">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-4995">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4995">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-4996">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4996">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-4998">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-4998">Mipmap Auto-Generation</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5000">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5000">RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5002">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5002">Blendable RenderTarget</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5004">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5004">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5005">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5005">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5006">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5006">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5007">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5007">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5008">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5008">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5009">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5009">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5010">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5010">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5011">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5011">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5012">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5012">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5013">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5013">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5014">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5014">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5015">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5015">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5016">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5016">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5017">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5017">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5019">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5019">4x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5021">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5021">8x Multisample RenderTarget</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5023">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5023">Other Multisample Count RT</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5025">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5025">Multisample Resolve</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5027">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5027">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5028">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5028">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5029">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5029">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5030">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5030">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-5031">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5031">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-5032">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5032">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-5033">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5033">Shared Resource</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5035">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5035">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="7fbf0-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="7fbf0-5037">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5037">Target</span></span> | <span data-ttu-id="7fbf0-5038">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5038">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5039">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5039">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5040">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5040">32</span></span> |
| <span data-ttu-id="7fbf0-5041">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5041">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5043">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5043">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5044">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5044">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5045">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5045">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5046">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5046">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5047">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5047">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5048">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5050">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5051">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5052">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5053">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5054">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5055">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5056">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5056">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5057">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5058">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5059">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5060">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5061">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5062">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5063">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5064">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5065">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5066">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5066">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5067">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5068">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5069">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5070">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5072">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5073">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5074">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5075">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5075">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5077">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5078">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5079">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5080">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5081">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5081">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5082">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5083">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5084">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5084">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5086">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5086">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5088">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5088">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5090">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5090">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5091">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="7fbf0-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="7fbf0-5093">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5093">Target</span></span> | <span data-ttu-id="7fbf0-5094">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5094">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5095">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5096">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5096">32</span></span> |
| <span data-ttu-id="7fbf0-5097">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5097">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5099">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5099">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5100">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5101">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5102">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5103">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5104">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5106">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5107">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5107">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5108">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5108">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5109">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5109">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5110">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5110">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5111">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5111">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5112">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5112">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5113">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5113">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5114">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5114">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5115">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5115">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5116">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5116">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5117">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5117">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5118">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5118">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5119">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5119">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5120">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5120">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5121">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5121">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5122">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5122">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5123">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5123">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5124">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5124">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5125">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5125">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5126">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5126">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5127">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5127">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5128">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5128">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5129">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5129">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5130">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5130">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5131">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5131">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5133">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5133">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5134">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5134">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5135">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5135">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5136">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5136">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5137">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5137">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5138">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5138">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5139">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5139">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5140">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5140">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5142">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5142">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5144">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5144">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5146">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5146">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5147">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="7fbf0-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="7fbf0-5149">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5149">Target</span></span> | <span data-ttu-id="7fbf0-5150">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5150">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5151">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5152">64</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5152">64</span></span> |
| <span data-ttu-id="7fbf0-5153">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5153">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5155">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5155">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5156">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5157">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5158">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5159">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5160">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5162">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5163">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5164">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5164">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5165">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5165">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5166">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5166">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5167">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5167">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5168">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5168">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5169">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5169">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5170">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5170">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5171">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5171">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5172">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5172">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5173">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5173">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5174">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5174">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5175">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5175">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5176">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5176">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5177">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5177">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5178">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5178">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5179">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5179">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5180">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5180">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5181">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5181">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5182">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5182">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5183">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5183">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5184">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5184">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5185">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5185">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5186">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5186">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5187">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5187">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5189">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5189">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5190">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5190">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5191">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5191">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5192">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5192">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5193">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5193">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5194">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5194">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5195">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5195">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5196">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5196">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5198">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5198">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5200">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5200">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5202">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5202">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5203">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5203">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="7fbf0-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="7fbf0-5205">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5205">Target</span></span> | <span data-ttu-id="7fbf0-5206">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5206">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5207">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5207">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5208">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5208">8</span></span> |
| <span data-ttu-id="7fbf0-5209">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5209">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5211">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5211">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5212">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5212">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5213">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5213">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5214">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5214">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5215">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5215">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5216">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5218">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5219">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5220">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5220">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5221">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5221">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5222">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5222">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5223">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5223">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5224">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5224">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5225">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5226">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5226">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5227">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5227">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5228">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5228">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5229">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5229">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5230">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5230">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5231">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5231">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5232">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5232">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5233">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5233">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5234">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5234">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5235">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5235">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5236">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5237">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5238">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5239">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5240">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5241">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5241">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5242">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5242">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5243">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5243">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5245">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5246">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5247">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5248">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5249">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5249">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5250">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5251">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5252">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5252">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5254">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5254">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5256">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5256">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5258">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5258">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5259">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5259">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="7fbf0-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="7fbf0-5261">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5261">Target</span></span> | <span data-ttu-id="7fbf0-5262">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5262">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5263">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5263">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5264">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5264">16</span></span> |
| <span data-ttu-id="7fbf0-5265">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5265">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5267">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5267">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5268">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5268">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5269">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5269">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5270">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5270">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5271">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5271">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5272">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5272">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5274">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5274">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5275">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5275">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5276">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5276">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5277">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5277">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5278">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5278">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5279">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5279">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5280">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5280">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5281">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5281">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5282">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5282">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5283">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5283">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5284">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5284">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5285">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5286">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5286">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5287">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5287">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5288">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5288">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5289">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5289">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5290">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5290">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5291">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5291">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5292">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5292">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5293">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5293">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5294">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5294">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5295">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5295">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5296">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5296">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5297">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5297">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5298">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5298">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5299">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5299">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5301">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5301">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5302">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5302">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5303">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5303">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5304">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5304">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5305">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5305">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5306">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5306">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5307">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5307">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5308">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5308">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5310">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5310">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5312">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5312">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5314">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5314">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5315">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5315">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="7fbf0-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="7fbf0-5317">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5317">Target</span></span> | <span data-ttu-id="7fbf0-5318">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5318">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5319">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5320">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5320">16</span></span> |
| <span data-ttu-id="7fbf0-5321">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5321">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5323">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5323">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5324">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5324">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5325">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5325">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5326">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5326">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5327">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5328">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5330">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5331">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5331">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5332">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5332">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5333">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5334">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5334">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5335">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5335">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5336">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5336">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5337">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5337">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5338">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5338">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5339">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5341">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5342">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5343">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5344">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5345">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5346">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5347">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5348">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5349">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5350">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5351">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5352">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5353">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5354">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5355">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5355">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5357">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5358">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5359">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5360">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5361">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5362">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5363">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5364">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5364">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5366">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5366">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5368">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5368">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5370">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5370">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5371">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5371">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="7fbf0-5372">DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5372">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="7fbf0-5373">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5373">Target</span></span> | <span data-ttu-id="7fbf0-5374">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5374">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5375">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5375">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5376">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5376">8</span></span> |
| <span data-ttu-id="7fbf0-5377">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5377">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5379">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5379">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5380">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5381">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5382">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5383">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5384">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5386">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5386">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5387">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5387">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5388">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5388">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5389">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5389">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5390">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5390">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5391">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5391">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5392">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5392">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5393">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5393">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5394">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5394">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5395">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5395">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5396">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5396">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5397">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5397">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5398">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5398">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5399">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5399">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5400">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5400">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5401">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5401">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5402">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5402">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5403">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5403">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5404">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5404">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5405">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5405">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5406">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5406">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5407">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5407">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5408">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5408">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5409">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5409">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5410">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5410">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5411">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5411">CPU Lockable</span></span> | \- |
| <span data-ttu-id="7fbf0-5412">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5412">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5413">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5413">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5414">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5414">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5415">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5415">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5416">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5416">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5417">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5417">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5418">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5418">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5419">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5419">Video Decoder Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5421">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5421">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5423">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5423">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5425">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5425">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5426">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5426">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="7fbf0-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="7fbf0-5428">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5428">Target</span></span> | <span data-ttu-id="7fbf0-5429">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5429">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5430">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5430">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5431">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5431">16</span></span> |
| <span data-ttu-id="7fbf0-5432">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5432">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5434">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5434">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5435">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5435">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5436">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5436">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5437">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5437">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5438">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5438">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5439">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5439">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5441">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5441">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5442">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5442">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5443">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5443">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5444">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5444">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5445">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5445">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5446">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5446">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5447">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5447">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5448">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5448">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5449">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5449">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5450">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5450">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5451">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5451">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5452">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5452">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5453">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5454">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5455">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5456">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5457">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5457">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5458">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5459">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5460">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5461">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5462">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5463">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5464">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5465">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5466">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5466">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5468">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5468">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5469">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5469">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5470">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5470">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5471">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5471">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5472">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5472">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5473">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5474">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5474">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5475">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5475">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5477">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5477">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5479">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5479">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5481">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5481">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5482">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5482">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="7fbf0-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="7fbf0-5484">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5484">Target</span></span> | <span data-ttu-id="7fbf0-5485">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5485">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5486">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5486">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5487">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5487">32</span></span> |
| <span data-ttu-id="7fbf0-5488">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5488">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5490">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5490">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5491">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5491">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5492">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5493">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5494">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5495">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5495">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5497">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5497">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5498">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5498">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5499">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5499">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5500">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5500">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5501">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5501">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5502">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5502">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5503">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5503">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5504">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5504">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5505">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5505">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5506">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5506">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5507">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5507">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5508">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5508">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5509">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5509">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5510">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5510">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5511">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5511">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5512">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5512">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5513">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5513">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5514">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5514">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5515">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5515">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5516">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5516">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5517">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5517">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5518">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5518">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5519">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5519">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5520">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5520">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5521">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5521">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5522">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5522">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5524">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5524">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5525">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5525">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5526">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5526">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5527">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5527">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5528">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5528">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5529">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5529">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5530">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5530">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5531">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5531">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5533">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5533">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5535">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5535">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5537">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5537">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5538">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5538">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="7fbf0-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="7fbf0-5540">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5540">Target</span></span> | <span data-ttu-id="7fbf0-5541">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5541">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5542">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5542">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5543">32</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5543">32</span></span> |
| <span data-ttu-id="7fbf0-5544">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5544">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5546">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5546">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5547">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5548">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5549">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5550">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5551">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5553">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5553">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5554">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5554">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5555">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5555">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5556">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5556">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5557">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5558">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5559">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5559">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5560">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5561">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5562">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5563">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5564">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5564">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5565">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5565">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5566">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5566">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5567">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5567">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5568">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5568">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5569">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5569">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5570">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5570">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5571">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5571">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5572">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5572">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5573">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5573">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5574">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5574">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5575">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5575">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5576">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5576">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5577">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5577">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5578">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5578">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5580">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5581">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5582">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5583">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5584">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5584">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5585">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5586">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5587">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5587">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5589">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5589">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5591">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5591">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5593">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5593">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5594">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="7fbf0-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="7fbf0-5596">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5596">Target</span></span> | <span data-ttu-id="7fbf0-5597">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5597">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5598">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5599">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5599">8</span></span> |
| <span data-ttu-id="7fbf0-5600">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5600">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5602">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5602">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5603">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5604">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5605">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5606">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5607">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5609">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5610">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5611">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5612">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5613">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5614">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5615">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5615">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5616">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5617">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5618">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5619">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5620">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5621">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5622">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5622">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5623">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5623">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5624">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5624">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5625">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5625">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5626">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5626">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5627">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5627">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5628">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5628">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5629">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5629">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5630">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5630">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5631">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5631">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5632">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5632">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5633">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5633">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5634">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5634">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5636">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5636">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5637">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5637">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5638">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5638">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5639">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5639">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5640">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5640">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5641">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5641">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5642">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5642">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5643">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5643">Video Decoder Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5645">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5645">Video Processor Input</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5647">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5647">Video Processor Output</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5649">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5649">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5650">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="7fbf0-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="7fbf0-5652">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5652">Target</span></span> | <span data-ttu-id="7fbf0-5653">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5653">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5654">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5655">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5655">8</span></span> |
| <span data-ttu-id="7fbf0-5656">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5656">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5658">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5658">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5659">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5659">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5660">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5660">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5661">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5661">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5662">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5662">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5663">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5663">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5665">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5665">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5666">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5666">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5667">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5667">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5668">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5668">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5669">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5669">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5670">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5670">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5671">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5671">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5672">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5672">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5673">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5673">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5674">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5674">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5675">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5676">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5676">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5677">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5678">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5679">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5680">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5681">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5681">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5682">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5683">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5684">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5685">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5687">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5688">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5689">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5690">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5690">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5692">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5693">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5694">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5695">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5696">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5696">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5697">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5698">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5699">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-5700">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5700">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5702">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5702">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-5703">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5703">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5704">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5704">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="7fbf0-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="7fbf0-5706">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5706">Target</span></span> | <span data-ttu-id="7fbf0-5707">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5707">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5708">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5708">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5709">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5709">8</span></span> |
| <span data-ttu-id="7fbf0-5710">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5710">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5712">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5712">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5713">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5713">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5714">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5714">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5715">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5715">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5716">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5716">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5717">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5717">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5719">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5719">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5720">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5721">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5721">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5722">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5722">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5723">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5723">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5724">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5724">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5725">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5725">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5726">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5726">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5727">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5727">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5728">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5729">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5730">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5731">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5732">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5733">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5734">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5735">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5735">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5736">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5737">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5738">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5739">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5740">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5741">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5742">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5743">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5744">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5744">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5746">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5747">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5748">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5749">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5750">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5750">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5751">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5752">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5752">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5753">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5753">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-5754">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5754">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5756">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-5757">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5757">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5758">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="7fbf0-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="7fbf0-5760">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5760">Target</span></span> | <span data-ttu-id="7fbf0-5761">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5761">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5762">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5763">8</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5763">8</span></span> |
| <span data-ttu-id="7fbf0-5764">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5764">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5766">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5766">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5767">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5768">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5769">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5770">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5771">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5771">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5773">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5773">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5774">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5774">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5775">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5775">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5776">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5776">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5777">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5777">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5778">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5778">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5779">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5779">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5780">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5780">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5781">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5781">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5782">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5783">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5784">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5784">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5785">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5785">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5786">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5786">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5787">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5787">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5788">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5788">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5789">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5789">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5790">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5790">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5791">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5791">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5792">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5792">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5793">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5793">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5794">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5794">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5795">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5795">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5796">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5796">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5797">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5797">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5798">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5798">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5800">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5801">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5802">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5803">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5804">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5804">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5805">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5806">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5807">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-5808">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5808">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5810">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5810">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-5811">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5811">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5812">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5812">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="7fbf0-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="7fbf0-5814">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5814">Target</span></span> | <span data-ttu-id="7fbf0-5815">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5815">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5816">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5816">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5817">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5817">16</span></span> |
| <span data-ttu-id="7fbf0-5818">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5818">Format Support</span></span> | ![facoltative](images/letter-o.jpg) |
| <span data-ttu-id="7fbf0-5820">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5820">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5821">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5821">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5822">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5822">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5823">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5823">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5824">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5824">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5825">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5827">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5828">TextureCube</span></span> | \- |
| <span data-ttu-id="7fbf0-5829">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5829">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="7fbf0-5830">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5830">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5831">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5831">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5832">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5832">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5833">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5833">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5834">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5834">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5835">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5835">Mipmap</span></span> | \- |
| <span data-ttu-id="7fbf0-5836">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5836">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5837">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5837">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5838">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5838">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5839">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5839">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5840">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5840">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5841">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5841">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5842">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5842">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5843">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5843">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5844">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5844">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5845">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5845">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5846">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5846">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5847">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5847">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5848">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5848">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5849">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5849">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5850">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5850">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5851">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5851">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5852">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5852">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5854">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5854">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5855">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5855">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5856">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5856">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5857">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5857">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5858">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5858">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5859">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5859">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5860">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5860">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5861">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5861">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-5862">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5862">Video Processor Input</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5864">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5864">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-5865">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5865">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5866">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5866">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="7fbf0-5867">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5867">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="7fbf0-5868">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5868">Target</span></span> | <span data-ttu-id="7fbf0-5869">Supporto</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5869">Support</span></span> |
| - | - |
| <span data-ttu-id="7fbf0-5870">Bit per elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5870">Bits Per Element (BPE)</span></span> | <span data-ttu-id="7fbf0-5871">16</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5871">16</span></span> |
| <span data-ttu-id="7fbf0-5872">Supporto del formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5872">Format Support</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5874">Buffer</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5874">Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5875">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5876">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5877">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="7fbf0-5878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5878">Texture1D</span></span> | \- |
| <span data-ttu-id="7fbf0-5879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5879">Texture2D</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5881">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5881">Texture3D</span></span> | \- |
| <span data-ttu-id="7fbf0-5882">TextureCube</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5882">TextureCube</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5884">Esempio di shader (solo esempio di punto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5884">Shader sample (point sample only)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5886">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5886">Shader sample (any filter)</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5888">Esempio shader \_ c (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5888">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5889">Esempio di shader (filtro mono a 1 bit)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5889">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="7fbf0-5890">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5890">Shader gather4</span></span> | \- |
| <span data-ttu-id="7fbf0-5891">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5891">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="7fbf0-5892">Mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5892">Mipmap</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5894">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="7fbf0-5895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5895">RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5896">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5897">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="7fbf0-5898">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="7fbf0-5899">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5900">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="7fbf0-5901">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5901">Typed UAV</span></span> | \- |
| <span data-ttu-id="7fbf0-5902">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="7fbf0-5903">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5904">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="7fbf0-5905">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="7fbf0-5906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5906">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="7fbf0-5907">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="7fbf0-5908">Min o max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5909">UAV atomico senza segno min o Max</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="7fbf0-5910">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5910">CPU Lockable</span></span> | ![necessario](images/letter-r.jpg) |
| <span data-ttu-id="7fbf0-5912">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5913">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="7fbf0-5914">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="7fbf0-5915">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="7fbf0-5916">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5916">Multisample Load</span></span> | \- |
| <span data-ttu-id="7fbf0-5917">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="7fbf0-5918">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="7fbf0-5919">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="7fbf0-5920">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5920">Video Processor Input</span></span> | \- |
| <span data-ttu-id="7fbf0-5921">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5921">Video Processor Output</span></span> | \- |
| <span data-ttu-id="7fbf0-5922">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5922">Shared Resource</span></span> | \- |
| <span data-ttu-id="7fbf0-5923">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5923">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="7fbf0-5924">Note sul formato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5924">Format notes</span></span>

<span data-ttu-id="7fbf0-5925">Lo scopo del formato può variare da un livello di funzionalità hardware a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5925">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="7fbf0-5926"><sup>L</sup> : formato non tipizzato</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5926"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="7fbf0-5927"><sup>PC</sup> : layout parzialmente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5927"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="7fbf0-5928"><sup>FCS</sup> : layout completamente tipizzato, castabile e semplice</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5928"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="7fbf0-5929"><sup>FNS</sup> : layout completamente tipizzato, non ristabile e semplice</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5929"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="7fbf0-5930"><sup>PCC</sup> : layout parzialmente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5930"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="7fbf0-5931"><sup>FCC</sup> : layout completamente tipizzato, castabile e complesso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5931"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="7fbf0-5932"><sup>FNC</sup> : layout completamente tipizzato, non ristabile e complesso</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5932"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="7fbf0-5933"><sup>V</sup> : formato video</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5933"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="7fbf0-5934">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5934">Related topics</span></span>

[<span data-ttu-id="7fbf0-5935">Livelli di funzionalità hardware D3D12</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5935">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="7fbf0-5936">[Implementazione dei buffer shadow per il livello di funzionalità Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5936">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="7fbf0-5937">Mapping di formati legacy</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5937">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="7fbf0-5938">Guida per programmatori per DXGI</span><span class="sxs-lookup"><span data-stu-id="7fbf0-5938">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
