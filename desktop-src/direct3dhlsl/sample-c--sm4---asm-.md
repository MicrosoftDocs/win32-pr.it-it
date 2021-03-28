---
title: sample_c (SM4-ASM)
description: Esegue un filtro di confronto.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993024"
---
# <a name="sample_c-sm4---asm"></a>esempio \_ c (SM4-ASM)

Esegue un filtro di confronto.



| esempio \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource. r,//deve essere. r swizzle srcSampler, srcReferenceValue//componente singolo selezionato |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[nell' \] indirizzo dei risultati dell'operazione.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] un set di coordinate di trama. Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] un registro di trama. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] un registro del campionatore. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] un registro con un singolo componente selezionato, che viene utilizzato nel confronto.<br/>                            |



 

## <a name="remarks"></a>Commenti

Lo scopo principale di questa istruzione è fornire un blocco predefinito per Percentage-Closer filtro di profondità. "C" nell' **esempio \_ c** sta per essere confrontato.

Gli operandi dell' **esempio \_ c** sono identici a quelli dell'istruzione di [esempio](sample--sm4---asm-.md) , ad eccezione del fatto che esiste un operando di origine float32 aggiuntivo, *srcReferenceValue*, che deve essere un registro con un solo componente selezionato o un valore letterale scalare.

Il parametro *srcResource* deve avere un Swizzle. r (rosso). l' **esempio \_ c** opera esclusivamente sul componente rosso e restituisce un singolo valore. Il. r swizzle su *srcResource* indica che il risultato scalare viene replicato in tutti i componenti.

Quando un buffer di profondità viene impostato come trama di input, il valore di profondità viene visualizzato nel componente rosso.

Se questa istruzione viene usata con una risorsa che non è Texture1D/2D/2DArray/Cube/CubeArray, genera risultati non definiti.

Quando questa istruzione viene eseguita, l'hardware di campionamento usa il ComparisonFunction del campionatore corrente per confrontare *srcReferenceValue* con il valore del componente rosso per la risorsa di origine in ogni filtro "Tap" location (Texel) che il filtro di trama attualmente configurato copre, in base alle coordinate specificate in *srcAddress*.

Il confronto si verifica dopo che *srcReferenceValue* è stato quantizzato alla precisione del formato di trama, nello stesso modo in cui z è quantizzato alla precisione del buffer di profondità prima del confronto di profondità nel test di visibilità della fusione di output. Questo include un morsetto nell'intervallo di formato (ad esempio, \[ 0.. 1 \] per un formato UNORM).

Il componente rosso di Texel di origine viene confrontato con il *srcReferenceValue* quantizzato. Per i Texel che esulano dalla risorsa, il valore del componente rosso viene determinato applicando le modalità di indirizzo (e BorderColorR se in modalità bordo) dal campionatore. Il confronto rispetta tutte le regole di confronto a virgola mobile D3D11, nel caso in cui il formato di trama sia a virgola mobile.

Ogni confronto che passa restituisce 1,0 f come valore del componente rosso per il Texel e ogni confronto che ha esito negativo restituisce 0,0 f come valore rosso per la trama. Il filtro viene quindi eseguito esattamente come specificato dagli Stati del campionatore, operativo solo nel componente rosso e restituendo un singolo filtro scalare allo shader, replicato in tutti i componenti *dest* mascherati.

L'uso dell' **esempio \_ c** è ortogonale per tutti gli altri controlli di filtro per utilizzo generico. l' **esempio \_ c** funziona senza interruzioni con le altre modalità di filtro per utilizzo generico. nell' **esempio \_ c** il comportamento dei filtri per utilizzo generico viene modificato in modo che i valori filtrati diventino tutti 1,0 f o 0,0 f a causa di risultati di confronto.

Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





