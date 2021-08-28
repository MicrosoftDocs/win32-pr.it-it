---
title: Specifica delle destinazioni del compilatore
description: Di seguito sono elencate le destinazioni per i vari profili supportati dalla funzione D3DCompile\ e dal compilatore HLSL.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d020edaabf4c618b1fa911a91bc4cc0e8b37e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481837"
---
# <a name="specifying-compiler-targets"></a>Specifica delle destinazioni del compilatore

È necessario specificare la destinazione dello shader, ovvero il set di funzionalità dello shader, da compilare quando si chiama la funzione [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)o [**D3DCompileFromFile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) Di seguito sono elencate le destinazioni per i vari profili supportati dalla **funzione D3DCompile \*** e dal compilatore HLSL.

-   [Livelli di funzionalità Direct3D 11.0 e 11.1](#direct3d-110-and-111-feature-levels)
-   [Livello di funzionalità Direct3D 10.1](#direct3d-101-feature-level)
-   [Livello di funzionalità Direct3D 10.0](#direct3d-100-feature-level)
-   [Livelli di funzionalità Direct3D 9.1, 9.2 e 9.3](#direct3d-91-92-and-93-feature-levels)
-   [Modello di shader Direct3D 9 legacy 3.0](#legacy-direct3d-9-shader-model-30)
-   [Modello di shader Direct3D 9 legacy 2.0](#legacy-direct3d-9-shader-model-20)
-   [Modello di shader Direct3D 9 legacy 1.x](#legacy-direct3d-9-shader-model-1x)
-   [Effetti legacy](#legacy-effects)
-   [Note](#notes)
-   [Argomenti correlati](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Livelli di funzionalità Direct3D 11.0 e 11.1

Ecco le destinazioni shader supportate dal livello di funzionalità Direct3D [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 e 11.1.



| Destinazione   | Descrizione                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 5 \_ 0 | DirectCompute 5.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))                              |
| ds \_ 5 \_ 0 | [Shader di dominio](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| gs \_ 5 \_ 0 | [Shader geometry](/previous-versions//bb205146(v=vs.85)) |
| hs \_ 5 \_ 0 | [Hull shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| ps \_ 5 \_ 0 | [Pixel shader](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 5 \_ 0 | [Vertex shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Livello di funzionalità Direct3D 10.1

Ecco le destinazioni shader supportate dal livello di [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) funzionalità Direct3D 10.1.



| Destinazione   | Descrizione                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 1 | DirectCompute 4.1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹                             |
| gs \_ 4 \_ 1 | [Shader geometry](/previous-versions//bb205146(v=vs.85)) |
| ps \_ 4 \_ 1 | [Pixel shader](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 1 | [Vertex shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Livello di funzionalità Direct3D 10.0

Ecco le destinazioni shader supportate dal livello di [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) funzionalità Direct3D 10.0.



| Destinazione   | Descrizione                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 0 | DirectCompute 4.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹                             |
| gs \_ 4 \_ 0 | [Shader geometry](/previous-versions//bb205146(v=vs.85)) |
| ps \_ 4 \_ 0 | [Pixel shader](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 0 | [Vertex shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Livelli di funzionalità Direct3D 9.1, 9.2 e 9.3

Ecco le destinazioni shader supportate dal livello di funzionalità Direct3D 9.1, 9.2 e 9.3. [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)

> [!Note]  
> Quando si usano \* i profili shader 4 0 livello 9 x HLSL, si usano in modo implicito i profili Shader Model 2.x per supportare l'hardware compatibile \_ \_ con \_ \_ \_ Direct3D 9. [](dx-graphics-hlsl-sm2.md) I profili modello shader 2.x supportano un comportamento di controllo del flusso più limitato rispetto ai profili [modello shader 4.x](dx-graphics-hlsl-sm4.md) e versioni successive.

 




| Destinazione | Descrizione | 
|--------|-------------|
| ps_4_0_level_9_1 | [Pixel shader](/previous-versions//bb205146(v=vs.85)) per 9.1 e 9.2 (limiti simili ps_2_0)<ul><li>64 istruzioni aritmetiche e 32 trame</li><li>12 registri temporanei</li><li>4 livelli di operazioni di lettura dipendenti</li></ul> | 
| ps_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> per 9.3 (limiti simili a ps_2_x² con funzionalità shader aggiuntive)<ul><li>512 istruzioni</li><li>32 registri temporanei</li><li>Controllo di flusso statico (profondità massima di 4)</li><li>Controllo dinamico del flusso (profondità massima di 24)</li><li>D3DPS20CAPS_ARBITRARYSWIZZLE</li><li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li><li>D3DPS20CAPS_PREDICATION</li><li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li><li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li></ul> | 
| vs_4_0_level_9_1 | <a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> per 9.1 e 9.2 (simile a vs_2_0)<ul><li>256 istruzioni</li><li>12 registri temporanei</li><li>Controllo di flusso statico (profondità massima di 1)</li></ul> | 
| vs_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> per la versione 9.3 (simile a vs_2_a² con funzionalità e istanze dello shader aggiuntive)<ul><li>256 istruzioni</li><li>32 registri temporanei</li><li>Controllo di flusso statico (profondità massima di 4)</li><li>D3DVS20CAPS_PREDICATION</li></ul> | 




 

## <a name="legacy-direct3d-9-shader-model-30"></a>Modello di shader Direct3D 9 legacy 3.0

Ecco le destinazioni shader per il modello di shader Direct3D 9 legacy 3.0 SHADER.



| Destinazione    | Descrizione                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| ps \_ 3 \_ 0  | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0               |
| ps \_ 3 \_ sw | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)    |
| vs \_ 3 \_ 0  | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0            |
| vs \_ 3 \_ sw | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software) |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>Modello di shader Direct3D 9 legacy 2.0

Ecco le destinazioni dello shader per il modello di shader Direct3D 9 legacy 2.0 SHADER.



| Destinazione    | Descrizione                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| ps \_ 2 \_ 0  | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0             |
| ps \_ 2 \_ a  | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a              |
| ps \_ 2 \_ b  | [Pixel shader](/previous-versions//bb205146(v=vs.85)) 2b              |
| ps \_ 2 \_ sw | [Software Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0    |
| vs \_ 2 \_ 0  | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0          |
| vs \_ 2 \_ a  | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a           |
| vs \_ 2 \_ sw | [Software Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0 |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>Modello di shader Direct3D 9 legacy 1.x

Ecco le destinazioni dello shader per il modello di shader Direct3D 9 legacy 1.x⁴.



| Destinazione   | Descrizione                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| tx \_ 1 \_ 0 | Profilo dello shader con trama utilizzato da D3DX9⁵ funzioni [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) e [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) |
| vs \_ 1 \_ 1 | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 1.1                                                            |



 

## <a name="legacy-effects"></a>Effetti legacy

Ecco le destinazioni degli effetti per gli effetti legacy.



| Destinazione   | Descrizione                               |
|----------|-------------------------------------------|
| fx \_ 2 \_ 0 | Effetti (FX) per Direct3D 9 in D3DX9⁵     |
| fx \_ 4 \_ 0 | Effetti (FX) per Direct3D 10.0 in D3DX10⁵ |
| fx \_ 4 \_ 1 | Effetti (FX) per Direct3D 10.1 in D3DX10⁵ |
| fx \_ 5 \_ 0 | Effetti (FX) per Direct3D 11⁵             |



 

## <a name="notes"></a>Note

Di seguito sono riportate alcune note a cui fanno riferimento le sezioni precedenti:

1.  [I dispositivi](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) con livello di funzionalità 10.0 e 10.1 possono facoltativamente supportare DirectCompute. Per verificare il supporto, usare [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**D3D11 \_ FEATURE \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).
2.  [Il](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) livello di funzionalità 9.3 richiede in modo efficace hardware conforme ai requisiti per il modello [di shader Direct3D 9 legacy 3.0,](#legacy-direct3d-9-shader-model-30)ma questo livello di funzionalità non usa le destinazioni \_ 3 0 o ps \_ \_ 3 \_ 0.
3.  Usare solo modelli shader Direct3D 9 legacy con l'API Direct3D 9. Usare invece i profili 9.x con l'API Direct3D 10.x e 11.x.
4.  Le funzioni **D3DCompile \*** dello shader HLSL corrente non supportano pixel shader legacy 1.x. L'ultima versione di HLSL per supportare queste destinazioni è stata D3DX9 nella versione di ottobre 2006 di DirectX SDK.
5.  Tutte le versioni di D3DX e DirectX SDK sono deprecate. Per altre informazioni, vedere [Dove si trova DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
