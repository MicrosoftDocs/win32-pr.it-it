---
title: Specifica delle destinazioni del compilatore
description: Qui sono elencate le destinazioni per i vari profili supportati da D3DCompile \ functions e dal compilatore HLSL.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399660"
---
# <a name="specifying-compiler-targets"></a>Specifica delle destinazioni del compilatore

È necessario specificare la destinazione dello shader, ovvero il set di funzionalità shader, per la compilazione quando si chiama la funzione [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)o [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) . Qui sono elencate le destinazioni per i vari profili supportati dalle funzioni **D3DCompile \*** e dal compilatore HLSL.

-   [Livelli di funzionalità Direct3D 11,0 e 11,1](#direct3d-110-and-111-feature-levels)
-   [Livello funzionalità Direct3D 10,1](#direct3d-101-feature-level)
-   [Livello funzionalità Direct3D 10,0](#direct3d-100-feature-level)
-   [Livelli di funzionalità Direct3D 9,1, 9,2 e 9,3](#direct3d-91-92-and-93-feature-levels)
-   [Modello di shader Direct3D 9 Legacy 3,0](#legacy-direct3d-9-shader-model-30)
-   [Modello di shader Direct3D 9 Legacy 2,0](#legacy-direct3d-9-shader-model-20)
-   [Modello 1. x legacy Direct3D 9 shader](#legacy-direct3d-9-shader-model-1x)
-   [Effetti legacy](#legacy-effects)
-   [Note](#notes)
-   [Argomenti correlati](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Livelli di funzionalità Direct3D 11,0 e 11,1

Di seguito sono riportate le destinazioni dello shader supportate dai [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 11,0 e 11,1.



| Destinazione   | Descrizione                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 5 \_ 0 | DirectCompute 5,0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))                              |
| DS \_ 5 \_ 0 | [Domain shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| GS \_ 5 \_ 0 | [Geometria Shader](/previous-versions//bb205146(v=vs.85)) |
| HS \_ 5 \_ 0 | [Hull shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| PS \_ 5 \_ 0 | [Pixel shader](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 5 \_ 0 | [Vertex shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Livello funzionalità Direct3D 10,1

Di seguito sono riportate le destinazioni dello shader supportate dal [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,1.



| Destinazione   | Descrizione                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 1 | DirectCompute 4,1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 1 | [Geometria Shader](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 1 | [Pixel shader](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 1 | [Vertex shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Livello funzionalità Direct3D 10,0

Di seguito sono riportate le destinazioni dello shader supportate dal [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,0.



| Destinazione   | Descrizione                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 0 | DirectCompute 4,0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 0 | [Geometria Shader](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 0 | [Pixel shader](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 0 | [Vertex shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Livelli di funzionalità Direct3D 9,1, 9,2 e 9,3

Di seguito sono riportate le destinazioni dello shader supportate dai [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 9,1, 9,2 e 9,3.

> [!Note]  
> Quando si usano i \* \_ \_ profili dello \_ shader HLSL a 4 0 di livello \_ 9 \_ , si usano in modo implicito i profili [Shader Model 2. x](dx-graphics-hlsl-sm2.md) per supportare l'hardware compatibile con Direct3D 9. I profili Shader Model 2. x supportano un comportamento di controllo di flusso più limitato rispetto ai profili [4. x](dx-graphics-hlsl-sm4.md) e successivi del modello shader.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Destinazione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ps_4_0_level_9_1</td>
<td>[Pixel shader](/previous-versions//bb205146(v=vs.85)) per 9,1 e 9,2 (limiti simili a ps_2_0)
<ul>
<li>64 istruzioni di trama aritmetiche e 32</li>
<li>12 registri temporanei</li>
<li>4 livelli di letture dipendenti</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_4_0_level_9_3</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> per 9,3 (limiti simili a ps_2_x ² con funzionalità shader aggiuntive)
<ul>
<li>512 istruzioni</li>
<li>32 registri temporanei</li>
<li>Controllo di flusso statico (profondità massima di 4)</li>
<li>Controllo dinamico del flusso (profondità massima di 24)</li>
<li>D3DPS20CAPS_ARBITRARYSWIZZLE</li>
<li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li>
<li>D3DPS20CAPS_PREDICATION</li>
<li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li>
<li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li>
</ul></td>
</tr>
<tr class="odd">
<td>vs_4_0_level_9_1</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> per 9,1 e 9,2 (simile a VS_2_0)
<ul>
<li>256 istruzioni</li>
<li>12 registri temporanei</li>
<li>Controllo di flusso statico (profondità massima di 1)</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_4_0_level_9_3</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> per 9,3 (simile a vs_2_a ² con funzionalità e istanze shader aggiuntive)
<ul>
<li>256 istruzioni</li>
<li>32 registri temporanei</li>
<li>Controllo di flusso statico (profondità massima di 4)</li>
<li>D3DVS20CAPS_PREDICATION</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a>Modello di shader Direct3D 9 Legacy 3,0

Di seguito sono riportate le destinazioni shader per il modello di shader Direct3D 9 Legacy 3,0 ³.



| Destinazione    | Descrizione                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 3 \_ 0  | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 3,0               |
| PS \_ 3 \_ SW | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 3,0 (software)    |
| vs \_ 3 \_ 0  | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 3,0            |
| Visual Studio \_ 3 \_ SW | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 3,0 (software) |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>Modello di shader Direct3D 9 Legacy 2,0

Di seguito sono riportate le destinazioni shader per il modello di shader Direct3D 9 Legacy 2,0 ³.



| Destinazione    | Descrizione                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 2 \_ 0  | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 2,0             |
| PS \_ 2 \_ a  | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a              |
| PS \_ 2 \_ b  | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 2B              |
| PS \_ 2 \_ SW | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 2,0 software    |
| vs \_ 2 \_ 0  | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 2,0          |
| vs \_ 2 \_ a  | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a           |
| vs \_ 2 \_ SW | Software [vertex shader](/previous-versions//bb205146(v=vs.85)) 2,0 |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>Modello 1. x legacy Direct3D 9 shader

Di seguito sono riportate le destinazioni dello shader per la versione 1. x precedente di Direct3D 9 shader ⁴.



| Destinazione   | Descrizione                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TX \_ 1 \_ 0 | Profilo shader texture che usa le funzioni ⁵ di D3DX9 legacy [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) e [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) |
| vs \_ 1 \_ 1 | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 1,1                                                            |



 

## <a name="legacy-effects"></a>Effetti legacy

Ecco le destinazioni degli effetti degli effetti legacy.



| Destinazione   | Descrizione                               |
|----------|-------------------------------------------|
| FX \_ 2 \_ 0 | Effetti (FX) per Direct3D 9 in D3DX9 ⁵     |
| FX \_ 4 \_ 0 | Effetti (FX) per Direct3D 10,0 in D3DX10 ⁵ |
| FX \_ 4 \_ 1 | Effetti (FX) per Direct3D 10,1 in D3DX10 ⁵ |
| FX \_ 5 \_ 0 | Effetti (FX) per Direct3D 11 ⁵             |



 

## <a name="notes"></a>Note

Di seguito sono riportate alcune note a cui fanno riferimento le sezioni precedenti:

1.  i dispositivi con [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 e 10,1 possono facoltativamente supportare DirectCompute. Per verificare il supporto, utilizzare [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con le [**\_ \_ \_ \_ \_ Opzioni hardware della funzionalità d3d11 D3D10 X**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).
2.  il [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 richiede in modo efficace l'hardware che soddisfa i requisiti per il [3,0 modello di shader Direct3D 9 legacy](#legacy-direct3d-9-shader-model-30), ma questo livello di funzionalità non usa \_ destinazioni vs 3 \_ 0 o PS \_ 3 \_ 0.
3.  Usare i modelli di shader Direct3D 9 legacy con l'API Direct3D 9. Usare invece i profili 9. x con l'API Direct3D 10. x e 11. x.
4.  Le funzioni HLSL shader **D3DCompile \*** correnti non supportano gli shader Legacy 1. x pixel. L'ultima versione di HLSL per il supporto di queste destinazioni è stata D3DX9 nella versione ottobre 2006 di DirectX SDK.
5.  Tutte le versioni di D3DX e DirectX SDK sono deprecate. Per ulteriori informazioni, vedere [la pagina relativa alla posizione di DirectX SDK](/windows/desktop/directx-sdk--august-2009-).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 