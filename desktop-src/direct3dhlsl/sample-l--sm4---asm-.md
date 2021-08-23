---
title: sample_l (sm4 - asm)
description: Campionare i dati dall'elemento/trama specificato usando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | sample_l (sm4 - asm)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbd65be095476cdac16ee95009994041af0b1812101b1d0d0b9a33a315ed58d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671811"
---
# <a name="sample_l-sm4---asm"></a>sample \_ l (sm4 - asm)

Campionare i dati dall'elemento/trama specificato usando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.



| sample \_ l \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler, srcLOD.select \_ component |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo dei risultati dell'operazione.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Un set di coordinate di trama. Per altre informazioni, vedere [l'istruzione di](sample--sm4---asm-.md) esempio.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Un registro di trama. Per altre informazioni, vedere **l'istruzione di** esempio.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] Un registro del campionatore. Per altre informazioni, vedere **l'istruzione di** esempio.<br/>                                 |
| <span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*<br/>                     | \[nel \] loD.<br/>                                                                                                 |



 

## <a name="remarks"></a>Commenti

Questa istruzione è [](sample--sm4---asm-.md)identica all'esempio , ad eccezione del fatto che il lod viene fornito direttamente dall'applicazione come valore scalare, che non rappresenta alcuna anisotropia. Questa istruzione è disponibile in tutte le fasi progammable Shader.

**sample \_ l campiona** la trama *usando srcLOD* come LOD. Se il valore LOD è <= 0, viene scelto l'zero (mappa principale) con il filtro di ingrandimento applicato (se applicabile in base alla modalità di filtro). Poiché *srcLOD* è un valore a virgola mobile, il valore frazionario viene usato per eseguire l'interpolazione tra due livelli mip, se il filtro minify è LINEAR o con il filtro anisotropo.

**\_ L'esempio ignora** i derivati degli indirizzi, quindi il comportamento di filtro è puramente isotropo. Poiché i derivati vengono ignorati, il filtro anisotropo si comporta come filtro isotropo.

Vengono rispettati gli stati del campionatore MIPLODBIAS e MAX/MINMIPLEVEL.

Se usato nel pixel shader, l'esempio **\_ l** implica che la scelta di LOD è per pixel, senza alcun effetto dai pixel adiacenti, ad esempio nello stesso stamp 2x2.

Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





