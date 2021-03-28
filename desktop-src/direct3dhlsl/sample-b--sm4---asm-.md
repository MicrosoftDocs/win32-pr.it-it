---
title: sample_b (SM4-ASM)
description: Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | sample_b (SM4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234827"
---
# <a name="sample_b-sm4---asm"></a>esempio \_ b (SM4-ASM)

Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.



| esempio \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcLODBias. Select \_ Component |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo del risultato dell'operazione.<br/>                                                              |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] un set di coordinate di trama. Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] un registro di trama. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] un registro del campionatore. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                 |
| <span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*<br/>     | \[\]per informazioni su questo parametro, vedere la sezione **osservazioni** .<br/>                                        |



 

## <a name="remarks"></a>Commenti

I dati di origine possono provenire da qualsiasi tipo di risorsa, ad eccezione dei buffer. Viene applicata un'ulteriore distorsione al livello di dettaglio calcolato come parte dell'esecuzione dell'istruzione.

Questa istruzione si comporta come l'istruzione di [esempio](sample--sm4---asm-.md) con l'aggiunta dell'applicazione del valore *srcLODBias* specificato al livello di dettaglio calcolato come parte dell'esecuzione dell'istruzione prima di selezionare le mappe MIP. Il valore *srcLODBias* viene aggiunto all'oggetto LOD calcolato per ogni pixel, insieme al valore MipLODBias del campionatore, prima del morsetto a MinLOD e MaxLOD.

### <a name="restrictions"></a>Restrizioni

-   l' **esempio \_ b** eredita le stesse restrizioni dell'istruzione di [esempio](sample--sm4---asm-.md) , oltre alle restrizioni aggiuntive per il parametro aggiuntivo.
-   L'intervallo di *srcLODBias* è (-16 f a 15.99 f); i valori al di fuori di questo intervallo produrranno risultati non definiti.
-   *srcLODBias* deve usare un selettore di componente singolo se non è un controllo immediato scalare.

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

 

 





