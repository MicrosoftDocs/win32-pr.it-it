---
title: ps_3_0
description: Un pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5aca251b1e8a462b4f2204241680922d76c45ba0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338070"
---
# <a name="ps_3_0"></a>PS \_ 3 \_ 0

Un pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.

-   [le \_ istruzioni di PS 3 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) contengono un elenco delle istruzioni disponibili.
-   [i \_ registri di PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) elencano i diversi tipi di registri usati dal pixel shader Alu.
-   [Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Consentono di modificare la modalità di funzionamento di un'istruzione.
-   La [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quali componenti del registro di destinazione vengono scritti.
-   I [modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   Il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.

## <a name="new-features"></a>Nuove funzioni e caratteristiche

Aggiungere un registro visi. Aggiungere un registro di posizione. I registri colori (v \# ) sono ora completamente a virgola mobile e i registri delle coordinate di trama (t \# ) sono stati consolidati. Le dichiarazioni di input accettano i nomi di utilizzo e sono consentiti più utilizzi per i componenti di un determinato registro.

## <a name="dynamic-flow-control"></a>Controllo dinamico di flusso

Il dispositivo supporta il controllo dinamico del flusso ([se bool-PS](if-bool---ps.md), [break-PS](break---ps.md)e [break \_ comp-PS](break-comp---ps.md)). La profondità dell'annidamento varia da 0 a 24.

## <a name="number-of-temporary-registers"></a>Numero di registri temporanei

Il numero di registri temporanei supportati è 32.

## <a name="static-flow-control-nesting-depth"></a>Profondità di annidamento del controllo di flusso statico

Il Call [-PS](call---ps.md) / [callnz](callnz-bool---ps.md)  / [Call \_ prede](callnz-pred---ps.md) può essere annidato a una profondità massima di 4. In modo indipendente, le istruzioni [loop-PS](loop---ps.md) / [Rep-PS](rep---ps.md) possono essere nidificate a una profondità massima di 4.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrario

Il Swizzle arbitrario è supportato. Vedere il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Istruzioni gradiente

Sono supportate le istruzioni per la sfumatura. Vedere [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)e [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Predicazione

L'istruzione predicazione è supportata. Vedere [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Limite di lettura dipendente

Non sono previsti limiti di lettura dipendenti.

## <a name="texture-instruction-limit"></a>Limite istruzioni trama

Non sono previsti limiti per le istruzioni di trama.

## <a name="instruction-count"></a>Conteggio istruzioni

Ogni pixel shader è consentita da 512 fino al numero di slot in MaxPixelShader30InstructionSlots (non superiore a 32768). Il numero di istruzioni eseguite può essere molto più elevato a causa del supporto del ciclo. MaxPShaderInstructionsExecuted deve essere almeno 2 ^ 16.

## <a name="sampler-count"></a>Numero di campionatori

Il numero di campioni di trama disponibili è 16.

## <a name="device-caps"></a>Tappi dispositivo

Se PS \_ 3 \_ 0 è supportato, i seguenti limiti sono supportati nell'hardware (come minimo):



| Limite                                                                                                          | Valore                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | ogni 4K                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8 K                                                                                                                                                                                                                                                                                                    |
| MaxAnisotropy                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| Vengono impostati i seguenti Caps primitivi:                                                                        | D3DPMISCCAPS \_ BLENDOP, D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS, D3DPMISCCAPS CLIPTLVERTS \_ , D3DPMISCCAPS CULLCCW \_ , \_ \_ \_ \_ D3DPMISCCAPS CULLCW, D3DPMISCCAPS CULLNONE, D3DPMISCCAPS FOGINFVF, D3DPMISCCAPS MASKZ                                                                                               |
| Sono state impostate le seguenti protezioni raster:                                                                           | D3DPRASTERCAPS \_ MIPMAPLODBIAS, D3DPRASTERCAPS \_ anisotropia, D3DPRASTERCAPS \_ COLORPERSPECTIVE, D3DPRASTERCAPS \_ SCISSORTEST in D3DCAPS9                                                                                                                                                                  |
| Supporto completo per la distorsione della profondità, tra cui:                                                                       | D3DPRASTERCAPS \_ SLOPESCALEDEPTHBIAS, D3DPRASTERCAPS \_ DEPTHBIAS                                                                                                                                                                                                                                        |
| Set completo di confronti per test di profondità e Alpha, tra cui:                                                  | Tutti i D3DPCMPCAPS in D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Modalità di combinazione di origine                                                                                        | Tutte le modalità di fusione sono supportate come origine (ad eccezione di D3DPBLENDCAPS \_ SRCALPHASAT, D3DPBLENDCAPS \_ BOTHSRCALPHA e D3DPBLENDCAPS \_ BOTHINVSRCALPHA).                                                                                                                                                    |
| Sono supportati i seguenti Caps di trama:                                                                    | D3DPTEXTURECAPS \_ mappa cubi, D3DPTEXTURECAPS \_ MIPCUBEMAP, D3DPTEXTURECAPS MIPMAP \_ , D3DPTEXTURECAPS MIPVOLUMEMAP, D3DPTEXTURECAPS Perspective, D3DPTEXTURECAPS \_ \_ \_ PROiezioni, D3DPTEXTURECAPS TEXREPEATNOTSCALEDBYSIZE \_ , D3DPTEXTURECAPS \_ VOLUMEMAP                                                        |
| Sono supportate le seguenti opzioni per le protezioni dei filtri di trama, i tappi di filtro della trama del volume e i tappi filtro trama | D3DPTFILTERCAPS \_ MINFPOINT, D3DPTFILTERCAPS \_ MINFLINEAR, D3DPTFILTERCAPS MINFANISOTROPIC \_ (questa operazione non è necessaria per VolumeTextureFilterCaps e CUBETEXTUREFILTERCAPS), D3DPTFILTERCAPS MIPFPOINT \_ , D3DPTFILTERCAPS MIPFLINEAR \_ , \_ \_ D3DPTFILTERCAPS MAGFPOINT, D3DPTFILTERCAPS MAGFLINEAR             |
| Le modalità di indirizzo di trama seguenti sono supportate nelle fasi Vertex e pixel:                                | D3DPTADDRESSCAPS \_ wrap, D3DPTADDRESSCAPS \_ mirror, D3DPTADDRESSCAPS \_ Clamp, D3DPTADDRESSCAPS \_ Border, D3DPTADDRESSCAPS INDEPENDENTUV \_ , D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| Sono supportati tutti i pixel shader Caps.                                                                     | DynamicFlowControlDepth = 24, NumTemps = 32, StaticFlowControlDepth = 4, NumInstructionSlots = 512. Sono supportate le funzionalità seguenti: predicazione, swizzles arbitrarie e istruzioni per la sfumatura. Non esiste alcun limite di lettura dipendente e non è previsto alcun limite per la combinazione di istruzioni matematiche e trama. |
| Sono supportate tutte le operazioni dello stencil. Sono inclusi stencil a due lati.                                   | Vedere [ **D3DSTENCILOP**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Dimensioni del punto di supporto del dispositivo per vertice                                                                         | D3DFVFCAPS \_ PSIZE in D3DCAPS9                                                                                                                                                                                                                                                                         |
| Supporto di trame senza potenza di 2.                                                                              | Supporto completo o supporto non POW-2 condizionale; il dispositivo non deve contenere solo la limitazione della trama quadrata come in D3DPTEXTURECAPS \_ SQUAREONLY.                                                                                                                                                    |
| Se il dispositivo supporta più Rendertargets, sono supportati i seguenti limiti:                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS, D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| Se vs \_ 3 \_ 0 è supportato                                                                                     | MaxUserClipPlanes in D3DCAPS9 è 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 