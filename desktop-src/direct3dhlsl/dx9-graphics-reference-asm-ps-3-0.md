---
title: ps_3_0
description: Informazioni su ps_3_0, un pixel shader programmabile, costituito da un set di istruzioni che operano sui dati pixel.
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19587cbaa79e2b89633560a7b7889219172d0c25
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010864"
---
# <a name="ps_3_0"></a>ps \_ 3 \_ 0

Un'pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento in e all'uscita dall'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.

-   [ps \_ 3 \_ 0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) contiene un elenco delle istruzioni disponibili.
-   [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) elenca i diversi tipi di registri usati dal pixel shader ALU.
-   [Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Vengono usati per modificare il funzionamento di un'istruzione.
-   [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quali componenti del registro di destinazione vengono scritti.
-   [I modificatori del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) pixel shader modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.

## <a name="new-features"></a>Nuove funzioni e caratteristiche

Aggiungere un registro viso. Aggiungere un registro di posizione. I registri colori (v ) sono ora completamente a virgola mobile e i registri delle coordinate della \# trama (t \# ) sono stati consolidati. Le dichiarazioni di input accettano i nomi di utilizzo e sono consentiti più utilizzi per i componenti di un determinato registro.

## <a name="dynamic-flow-control"></a>Controllo dinamico del flusso

Il dispositivo supporta il controllo dinamico del flusso ([if bool - ps](if-bool---ps.md), break - [ps](break---ps.md)e break comp [- \_ ps](break-comp---ps.md)). La profondità di annidamento è compreso tra 0 e 24.

## <a name="number-of-temporary-registers"></a>Numero di registri temporanei

Il numero di registri temporanei supportati è 32.

## <a name="static-flow-control-nesting-depth"></a>Profondità di annidamento del controllo flusso statico

La [chiamata - ps](call---ps.md) / [callnz](callnz-bool---ps.md)call  / [ \_ pred](callnz-pred---ps.md) può essere annidata a una profondità massima di 4. In modo indipendente, [le istruzioni loop - ps](loop---ps.md)rep - / [ps](rep---ps.md) possono essere annidate fino a una profondità massima di 4.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrario

Lo swizzle arbitrario è supportato. Vedere [Swizzling del registro di origine.](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)

## <a name="gradient-instructions"></a>Istruzioni per la sfumatura

Sono supportate le istruzioni per la sfumatura. Vedere [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)e [texldd - ps](texldd---ps.md).

## <a name="predication"></a>Predicazione

La predicazione dell'istruzione è supportata. Vedere [Registro predicati](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Limite di lettura dipendente

Non sono previsti limiti di lettura dipendenti.

## <a name="texture-instruction-limit"></a>Limite istruzioni trama

Non è previsto alcun limite per le istruzioni di trama.

## <a name="instruction-count"></a>Conteggio istruzioni

Ogni pixel shader è consentito da 512 fino al numero di slot in MaxPixelShader30InstructionSlots (non più di 32768). Il numero di istruzioni eseguite può essere molto superiore a causa del supporto del ciclo. MaxPShaderInstructionsExecuted deve essere almeno 2^16.

## <a name="sampler-count"></a>Conteggio campionatore

Il numero di campionatori di trama disponibili è 16.

## <a name="device-caps"></a>Tappi dispositivo

Se ps \_ 3 \_ 0 è supportato, nell'hardware sono supportati almeno i limiti seguenti:



| Cap                                                                                                          | Valore                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | 4.000 ciascuno                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8 K                                                                                                                                                                                                                                                                                                    |
| MaxAnisotropy                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| Vengono impostati i caratteri maiuscoli primitivi seguenti:                                                                        | D3DPMISCCAPS \_ BLENDOP, D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS, D3DPMISCCAPS \_ CLIPTLVERTS, D3DPMISCCAPS \_ CULLCCW, D3DPMISCCAPS \_ CULLCW, D3DPMISCCAPS \_ CULLNONE, D3DPMISCCAPS \_ FOGINFVF, D3DPMISCCAPS \_ MASKZ                                                                                               |
| Vengono impostati i limiti raster seguenti:                                                                           | D3DPRASTERCAPS \_ MIPMAPLODBIAS, D3DPRASTERCAPS \_ ANISOTROPY, D3DPRASTERCAPS \_ COLORPERSPECTIVE, D3DPRASTERCAPS \_ SCISSORTEST in D3DCAPS9                                                                                                                                                                  |
| Supporto completo per la distorsione della profondità, tra cui:                                                                       | D3DPRASTERCAPS \_ SLOPESCALEDEPTHBIAS, D3DPRASTERCAPS \_ DEPTHBIAS                                                                                                                                                                                                                                        |
| Set completo di confronti per il test di profondità e alfa, tra cui:                                                  | Tutti i D3DPCMPCAPS in D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Modalità di fusione dell'origine                                                                                        | Tutte le modalità di fusione sono supportate come origine (ad eccezione di D3DPBLENDCAPS \_ SRCALPHASAT, D3DPBLENDCAPS \_ BOTHSRCALPHA e D3DPBLENDCAPS \_ BOTHINVSRCALPHA).                                                                                                                                                    |
| Sono supportati i limiti di trama seguenti:                                                                    | D3DPTEXTURECAPS \_ CUBEMAP, D3DPTEXTURECAPS \_ MIPCUBEMAP, D3DPTEXTURECAPS \_ MIPMAP, D3DPTEXTURECAPS \_ MIPVOLUMEMAP, D3DPTEXTURECAPS \_ PERSPECTIVE, D3DPTEXTURECAPS \_ PROJECTED, D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE, D3DPTEXTURECAPS \_ VOLUMEMAP                                                        |
| I valori seguenti sono supportati per i limiti del filtro trame, i limiti del filtro trame del volume e i limiti del filtro trame del cubo: | D3DPTFILTERCAPS \_ MINFPOINT, D3DPTFILTERCAPS \_ MINFLINEAR, D3DPTFILTERCAPS \_ MINFANISOTROP (non obbligatorio per VolumeTextureFilterCaps e CubeTextureFilterCaps), D3DPTFILTERCAPS \_ MIPFPOINT, D3DPTFILTERCAPS \_ MIPFLINEAR, D3DPTFILTERCAPS \_ MAGFPOINT, D3DPTFILTERCAPS \_ MAGFLINEAR             |
| Le modalità di indirizzo trame seguenti sono supportate nelle fasi vertice e pixel:                                | D3DPTADDRESSCAPS \_ WRAP, D3DPTADDRESSCAPS \_ MIRROR, D3DPTADDRESSCAPS \_ CLAMP, D3DPTADDRESSCAPS \_ BORDER, D3DPTADDRESSCAPS \_ INDEPENDENTUV, D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| Tutti i pixel shader sono supportati.                                                                     | DynamicFlowControlDepth = 24, NumTemps = 32, StaticFlowControlDepth = 4, NumInstructionSlots = 512. Sono supportate le funzionalità seguenti: predicazione, swizzle arbitrari e istruzioni di sfumatura. Non esiste alcun limite di lettura dipendente e nessun limite alla combinazione di istruzioni matematiche e trame. |
| Tutte le operazioni di stencil sono supportate. Include uno stencil a due lati.                                   | Vedere [ **D3DSTENCILOP**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Dimensioni del punto di supporto del dispositivo per vertice                                                                         | D3DFVFCAPS \_ PSIZE in D3DCAPS9                                                                                                                                                                                                                                                                         |
| Supporto non a potenza di 2 trame.                                                                              | Supporto completo o supporto condizionale non-pow-2; il dispositivo non deve avere solo la limitazione della trama quadrata, come in D3DPTEXTURECAPS \_ SQUAREONLY.                                                                                                                                                    |
| Se il dispositivo supporta più rendertarget, sono supportati i limiti seguenti:                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS, D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| Se rispetto \_ a 3 \_ 0 è supportato                                                                                     | MaxUserClipPlanes in D3DCAPS9 è 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 