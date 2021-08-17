---
title: texldl - ps
description: Campionare una trama con un determinato campionatore. Il particolare livello di dettaglio mipmap campionato deve essere specificato come quarto componente della coordinata della trama. | texldl - ps
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f66bc54f00e5eb560589429f1cb116183e165a36d90f5d560d8895678a2d5bad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723178"
---
# <a name="texldl---ps"></a>texldl - ps

Campionare una trama con un determinato campionatore. Il particolare livello di dettaglio mipmap campionato deve essere specificato come quarto componente della coordinata della trama.

## <a name="syntax"></a>Sintassi



| texldl dst, src0, src1 |
|------------------------|



 

Dove:

-   dst è un registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate di trama per il campione di trama. Vedere [Registro delle coordinate della trama.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifica il registro del campionatore di origine (s ), dove specifica il numero del \# \# campionatore di trama da campionare. Al campionatore è associata una trama e uno stato del controllo definiti dall'enumerazione [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) ,ad esempio D3DSAMP \_ MINFILTER.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldl                |      |      |      |      |      |      |       | x    | x     |



 

texldl cerca il set di trame nella fase del campionatore a cui fa riferimento src1. Il livello di dettaglio viene selezionato da src0.w. Questo valore può essere negativo, nel qual caso il livello di dettaglio selezionato è l'zero(mappa principale) con MAGFILTER. Poiché src0.w è un valore a virgola mobile, il valore frazionario viene usato per eseguire l'interpolazione (se MIPFILTER è LINEARE) tra due livelli mip. Vengono rispettati gli stati del campionatore MIPMAPLODBIAS e MAXMIPLEVEL. Per altre informazioni sugli stati del campionatore, vedere [**D3DSAMPLERSTATETYPE.**](/windows/desktop/direct3d9/d3dsamplerstatetype)

Se un programma shader esegue il campionamento da un campionatore per cui non è impostata una trama, viene ottenuto 0001 nel registro di destinazione.

Di seguito è riportato un algoritmo approssimativo seguito dal dispositivo di riferimento:


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



Restrizioni:

-   Le coordinate della trama non devono essere ridimensionate in base alle dimensioni della trama.
-   dst deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   dst può accettare una maschera di scrittura. Vedere [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).
-   I valori predefiniti per i componenti mancanti sono 0 o 1 e dipendono dal formato della trama.
-   src1 deve essere un [campionatore (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ). src1 non può usare un modificatore di negazione (vedere [Destination Register Write Mask).](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) src1 può usare swizzle (vedere Source [Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), che viene applicato dopo il campionamento, ma prima che venga rispettata la maschera di scrittura (vedere Destination Register Write Mask). Il campionatore deve essere stato dichiarato [(usando dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)) all'inizio dello shader.
-   Il numero di coordinate necessarie per eseguire il campione di trama dipende da come è stato dichiarato il campionatore. Se è stato dichiarato come cubo, è necessaria una coordinata di trama a tre componenti (RGB). La convalida impone che le coordinate fornite a tex \_ ldl Siano sufficienti per la dimensione della trama dichiarata per il campionatore. Tuttavia, non è garantito che l'applicazione imposta effettivamente una trama (tramite l'API) con dimensioni uguali alla dimensione dichiarata per il campionatore. In tal caso, il runtime tenterà di rilevare le mancate corrispondenze (possibilmente solo in fase di debug). Il campionamento di una trama con meno dimensioni di quelle presenti nella coordinata della trama sarà consentito e si presuppone che ignori i componenti aggiuntivi delle coordinate della trama. Al contrario, il campionamento di una trama con più dimensioni di quelle presenti nella coordinata della trama non è valido.
-   Se src0 (coordinata trama) è [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md), i componenti necessari per la ricerca (descritti in precedenza) devono essere stati scritti in precedenza.
-   Il campionamento di trame RGB senza segno avrà come risultato valori float compresi tra 0,0 e 1,0.
-   Il campionamento delle trame con segno comporta valori float compresi tra -1,0 e 1,0.
-   Quando si esegue il campionamento di trame a virgola mobile, Float16 indica che i dati saranno intervalli all'interno di MAX \_ FLOAT16. Float32 indica che verrà usato l'intervallo massimo della pipeline. Il campionamento al di fuori di entrambi gli intervalli non è definito.
-   Non esiste alcun limite di lettura dipendente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
