---
title: sample_l (SM4-ASM)
description: Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | sample_l (SM4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353361"
---
# <a name="sample_l-sm4---asm"></a>\_l di esempio (SM4-ASM)

Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.



| esempio \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcLOD. Select \_ Component |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo dei risultati dell'operazione.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] un set di coordinate di trama. Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] un registro di trama. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] un registro del campionatore. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                 |
| <span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*<br/>                     | \[in \] LOD.<br/>                                                                                                 |



 

## <a name="remarks"></a>Commenti

Questa istruzione è identica a [Sample](sample--sm4---asm-.md), ad eccezione del fatto che il valore di LOD viene fornito direttamente dall'applicazione come valore scalare, che non rappresenta alcuna anisotropia. Questa istruzione è disponibile in tutte le fasi dello shader progammable.

**esempio \_ l** esegue il campionamento della trama usando *srcLOD* come LOD. Se il valore LOD è <= 0, viene scelto zero'th (maggiore mappa) con il filtro di ingrandimento applicato (se applicabile in base alla modalità di filtro). Dal momento che *srcLOD* è un valore a virgola mobile, il valore frazionario viene usato per interpolare tra due livelli MIP, se il filtro minimizzare è lineare o con filtro anisotropico.

l' **esempio \_ l** ignora i derivati degli indirizzi, quindi il comportamento del filtro è esclusivamente del filtro dei tipi. Poiché i derivati vengono ignorati, il filtro anisotropico si comporta come filtro di applicazione del filtro.

Gli Stati del campionatore MIPLODBIAS e MAX/MINMIPLEVEL vengono rispettati.

Se usato nel pixel shader, l' **esempio \_ l** implica che la scelta di LOD è per pixel, senza alcun effetto dai pixel adiacenti, ad esempio nello stesso timbro 2x2.

Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





