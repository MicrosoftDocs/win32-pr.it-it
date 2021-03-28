---
title: texldl-vs
description: Campionare una trama con un campionatore specifico. Il livello di dettaglio mipmap specifico da campionare deve essere specificato come quarto componente della coordinata di trama. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058520"
---
# <a name="texldl---vs"></a>texldl-vs

Campionare una trama con un campionatore specifico. Il livello di dettaglio mipmap specifico da campionare deve essere specificato come quarto componente della coordinata di trama.

## <a name="syntax"></a>Sintassi



| texldl DST, src0, src1 |
|------------------------|



 

Dove:

-   DST è un registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama.
-   src1 identifica i registri del campionatore \# di origine, dove \# specifica il numero del campionatore di trama da campionare. Il campionatore è associato a una trama e a uno stato di controllo definiti dall'enumerazione [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (ad esempio, D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| texldl                 |      |      |      |       | x    | x     |



 

texldl Cerca il set di trame nella fase del campionatore a cui fa riferimento src1. Il livello di dettaglio è selezionato da src0. w. Questo valore può essere negativo, nel qual caso il livello di dettaglio selezionato è "Zero One" (mapping più grande) con il MAGFILTER. Poiché src0. w è un valore a virgola mobile, il valore frazionario viene usato per interpolare (se MIPFILTER è lineare) tra due livelli MIP. Gli Stati del campionatore MIPMAPLODBIAS e MAXMIPLEVEL vengono rispettati. Per ulteriori informazioni sugli Stati del campionatore, vedere [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Se uno shader esegue un campionamento di un campionatore che non dispone di un set di trame, 0001 viene ottenuto nel registro di destinazione.

Si tratta di un'approssimazione all'algoritmo del dispositivo di riferimento.


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
   LOD = MAX( MAXMIPLEVEL, LOD);
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



Restrizioni:

-   Le coordinate di trama non devono essere ridimensionate in base alle dimensioni della trama.
-   DST deve essere un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).
-   DST può accettare una maschera di scrittura. Vedere [mascheramento del registro di destinazione](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).
-   Le impostazioni predefinite per i componenti mancanti sono 0 o 1 e dipendono dal formato di trama.
-   src1 deve essere un [campionatore (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# ). src1 non può usare un modificatore negazioni. src1 può usare Swizzle, che viene applicato dopo il campionamento prima che venga rispettata la maschera di scrittura. Il campionatore deve essere stato dichiarato (usando [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)) all'inizio dello shader.
-   Il numero di coordinate necessarie per eseguire l'esempio di trama dipende dalla modalità di dichiarazione del campionatore. Se è stata dichiarata come cubo, è richiesta una coordinata di trama a tre componenti (. RGB). La convalida impone che le coordinate fornite a texldl siano sufficienti per la dimensione di trama dichiarata per il campionatore. Tuttavia, non è garantito che l'applicazione imposti effettivamente una trama (tramite l'API) con dimensioni uguali alla dimensione dichiarata per il campionatore. In tal caso, il runtime tenterà di rilevare le mancate corrispondenze (probabilmente solo in fase di debug). Il campionamento di una trama con meno dimensioni rispetto a quelli presenti nella coordinata di trama sarà consentito e si presuppone che ignori i componenti aggiuntivi delle coordinate di trama. Viceversa, il campionamento di una trama con più dimensioni rispetto a quelle presenti nella coordinata di trama non è consentito.
-   Se il src0 (coordinata di trama) è un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ), i componenti necessari per la ricerca (descritta in precedenza) devono essere stati scritti in precedenza.
-   Il campionamento di trame RGB senza segno comporterà valori float compresi tra 0,0 e 1,0.
-   Il campionamento delle trame con segno comporterà valori float compresi tra-1,0 e 1,0.
-   Quando si campionano trame a virgola mobile, il valore di Float16 indica che i dati variano entro il numero massimo di \_ Float16. Float32 indica che verrà utilizzato l'intervallo massimo della pipeline. Il campionamento esterno a uno dei due intervalli non è definito.
-   Nessun limite di lettura dipendente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
