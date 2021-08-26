---
title: sample_c (sm4 - asm)
description: Esegue un filtro di confronto.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2656f70a95487ce98aadc30a028fccaed00cb1c8d6324d64bb22c9672543d5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067731"
---
# <a name="sample_c-sm4---asm"></a>esempio \_ c (sm4 - asm)

Esegue un filtro di confronto.



| sample \_ c \[ \_ aoffimmi(u,v,w) \] dest \[ \] .mask, srcAddress \[ .swizzle, \] srcResource.r, // deve essere .r swizzle srcSampler, srcReferenceValue // componente singolo selezionato |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[in \] Indirizzo dei risultati dell'operazione.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] Un set di coordinate della trama. Per altre informazioni, vedere [l'istruzione di](sample--sm4---asm-.md) esempio.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] Un registro trame. Per altre informazioni, vedere **l'istruzione di** esempio.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] Un registro sampler. Per altre informazioni, vedere **l'istruzione di** esempio.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] Un registro con un singolo componente selezionato, usato nel confronto.<br/>                            |



 

## <a name="remarks"></a>Commenti

Lo scopo principale di questa istruzione è fornire un blocco predefinito per il filtro Percentage-Closer profondità. "c" **nell'esempio \_ c** è l'acronimo di Comparison.

Gli operandi dell'esempio **\_ c** [](sample--sm4---asm-.md) sono identici all'istruzione di esempio, ad eccezione del fatto che è presente un operando di origine float32 aggiuntivo, *srcReferenceValue*, che deve essere un registro con un singolo componente selezionato o un valore letterale scalare.

Il *parametro srcResource* deve avere uno swizzle .r (rosso). **\_ L'esempio c** opera esclusivamente sul componente rosso e restituisce un singolo valore. Lo swizzle .r in *srcResource* indica che il risultato scalare viene replicato in tutti i componenti.

Quando un buffer di profondità è impostato come trama di input, il valore di profondità viene visualizzato nel componente rosso.

Se questa istruzione viene usata con una risorsa che non è una Texture1D/2DArray/Cube/CubeArray, produce risultati non definiti.

Quando questa istruzione viene eseguita, l'hardware di campionamento usa comparisonFunction del sampler corrente per confrontare *srcReferenceValue* con il valore del componente Red per la risorsa di origine in ogni posizione di "tocco" del filtro (texel) che il filtro di trama attualmente configurato copre, in base alle coordinate fornite in *srcAddress*.

Il confronto si verifica dopo che *srcReferenceValue* è stato quantificato alla precisione del formato della trama, esattamente come z viene quantificato in precisione del buffer di profondità prima del confronto di profondità nel test di visibilità output merger. Include un blocco per l'intervallo di formato (ad \[ esempio, 0..1 \] per un formato UNORM).

Il componente Red del texel di origine viene confrontato con *srcReferenceValue quantizzato.* Per i texel che rientrano nella risorsa, il valore del componente Red viene determinato applicando le modalità indirizzo (e BorderColorR se in modalità Bordo) dal sampler. Il confronto rispetta tutte le regole di confronto a virgola mobile D3D11, nel caso in cui il formato della trama sia a virgola mobile.

Ogni confronto che passa restituisce 1,0f come valore del componente Red per il texel e ogni confronto che ha esito negativo restituisce 0,0f come valore Red per la trama. Il filtro viene quindi applicato esattamente come specificato dagli stati sampler, operando solo nel componente Red e restituisce un singolo risultato di filtro scalare allo shader, replicato in tutti i componenti *dest mascherati.*

L'uso **dell'esempio \_ c** è ortogonale per tutti gli altri controlli di filtro per utilizzo generico. **\_ L'esempio c** funziona perfettamente con le altre modalità di filtro per utilizzo generico. **\_ L'esempio c** modifica il comportamento dei filtri per utilizzo generico in modo che i valori filtrati diventino tutti 1.0f o 0.0f a causa dei risultati del confronto.

Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

Per altre informazioni, vedere [l'istruzione di](sample--sm4---asm-.md) esempio.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





