---
title: sample_b (sm4 - asm)
description: Campionare i dati dall'elemento/trama specificato usando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | sample_b (sm4 - asm)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9193930aadf8874c759fde3beac7d7da4c9d01b709f6e0b1840b36fe0675ef8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790789"
---
# <a name="sample_b-sm4---asm"></a>sample \_ b (sm4 - asm)

Campionare i dati dall'elemento/trama specificato usando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.



| sample \_ b \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler, srcLODBias.select \_ component |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo del risultato dell'operazione.<br/>                                                              |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Un set di coordinate di trama. Per altre informazioni, vedere [l'istruzione di](sample--sm4---asm-.md) esempio.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Un registro di trama. Per altre informazioni, vedere **l'istruzione di** esempio.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] Un registro del campionatore. Per altre informazioni, vedere **l'istruzione di** esempio.<br/>                                 |
| <span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*<br/>     | \[Per \] informazioni su questo **parametro,** vedere la sezione Osservazioni.<br/>                                        |



 

## <a name="remarks"></a>Commenti

I dati di origine possono derivare da qualsiasi tipo di risorsa, diverso da Buffer. Viene applicata una distorsione aggiuntiva al livello di dettaglio calcolato come parte dell'esecuzione dell'istruzione.

Questa istruzione si [](sample--sm4---asm-.md) comporta come l'istruzione di esempio con l'aggiunta dell'applicazione del valore *srcLODBias* specificato al livello di valore di dettaglio calcolato come parte dell'esecuzione dell'istruzione prima di selezionare le mappe mip. Il *valore srcLODBias* viene aggiunto al LOD calcolato in base al pixel, insieme al valore MipLODBias del campionatore, prima della chiusura a MinLOD e MaxLOD.

### <a name="restrictions"></a>Restrizioni

-   **\_ L'esempio b** eredita le stesse restrizioni dell'istruzione [di](sample--sm4---asm-.md) esempio, oltre ad altre restrizioni per il parametro aggiuntivo.
-   L'intervallo *di srcLODBias* è (da -16,0f a 15,99f); I valori esterni a questo intervallo produrranno risultati indefiniti.
-   *srcLODBias* deve usare un selettore di componente singolo se non è un selettore scalare immediato.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





