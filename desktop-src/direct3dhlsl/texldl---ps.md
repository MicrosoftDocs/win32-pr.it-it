---
title: texldl-PS
description: Campionare una trama con un campionatore specifico. Il livello di dettaglio mipmap specifico da campionare deve essere specificato come quarto componente della coordinata di trama. | texldl-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981138"
---
# <a name="texldl---ps"></a>texldl-PS

Campionare una trama con un campionatore specifico. Il livello di dettaglio mipmap specifico da campionare deve essere specificato come quarto componente della coordinata di trama.

## <a name="syntax"></a>Sintassi



| texldl DST, src0, src1 |
|------------------------|



 

Dove:

-   DST è un registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama. Vedere [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifica i registri del campionatore \# di origine, dove \# specifica il numero del campionatore di trama da campionare. Il campionatore è associato a una trama e a uno stato di controllo definiti dall'enumerazione [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (ad esempio, D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldl                |      |      |      |      |      |      |       | x    | x     |



 

texldl Cerca il set di trame nella fase del campionatore a cui fa riferimento src1. Il livello di dettaglio è selezionato da src0. w. Questo valore può essere negativo, nel qual caso il livello di dettaglio selezionato è zero One (mapping più grande) con il MAGFILTER. Poiché src0. w è un valore a virgola mobile, il valore frazionario viene usato per interpolare (se MIPFILTER è lineare) tra due livelli MIP. Gli Stati del campionatore MIPMAPLODBIAS e MAXMIPLEVEL vengono rispettati. Per ulteriori informazioni sugli Stati del campionatore, vedere [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Se uno shader esegue un campionamento di un campionatore che non dispone di un set di trame, viene ottenuto il valore 0001 nel registro di destinazione.

Di seguito è riportato un algoritmo approssimativo che il dispositivo di riferimento segue:


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

-   Le coordinate di trama non devono essere ridimensionate in base alle dimensioni della trama.
-   DST deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   DST può accettare un writemask. Vedere la [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).
-   Le impostazioni predefinite per i componenti mancanti sono 0 o 1 e dipendono dal formato di trama.
-   src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# . src1 non può usare un modificatore negazioni (vedere la [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)). src1 può usare swizzle (vedere il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), che viene applicato dopo il campionamento, ma prima che venga rispettata la maschera di scrittura (vedere la maschera di scrittura del registro di destinazione). Il campionatore deve essere stato dichiarato (usando [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) all'inizio dello shader.
-   Il numero di coordinate necessarie per eseguire l'esempio di trama dipende dalla modalità di dichiarazione del campionatore. Se è stata dichiarata come cubo, è richiesta una coordinata di trama a tre componenti (. RGB). La convalida impone che le coordinate fornite a Tex \_ LDL siano sufficienti per la dimensione di trama dichiarata per il campionatore. Tuttavia, non è garantito che l'applicazione imposti effettivamente una trama (tramite l'API) con dimensioni uguali alla dimensione dichiarata per il campionatore. In tal caso, il runtime tenterà di rilevare le mancate corrispondenze (probabilmente solo in fase di debug). Il campionamento di una trama con un minor numero di dimensioni rispetto a quelli presenti nella coordinata di trama sarà consentito e dovrebbe ignorare i componenti della coordinata trama aggiuntiva. Viceversa, il campionamento di una trama con più dimensioni rispetto a quelle presenti nella coordinata di trama non è valido.
-   Se il src0 (coordinata di trama) è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md), è necessario che i componenti necessari per la ricerca (descritti in precedenza) siano stati precedentemente scritti.
-   Il campionamento di trame RGB senza segno comporterà valori float compresi tra 0,0 e 1,0.
-   Il campionamento delle trame con segno comporterà valori float compresi tra-1,0 e 1,0.
-   Quando si campionano trame a virgola mobile, Float16 significa che i dati variano entro il numero massimo di \_ Float16. Float32 indica che verrà utilizzato l'intervallo massimo della pipeline. Il campionamento esterno a uno dei due intervalli non è definito.
-   Nessun limite di lettura dipendente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
