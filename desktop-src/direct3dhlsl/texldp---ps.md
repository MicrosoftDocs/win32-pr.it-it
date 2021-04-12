---
title: texldp-PS
description: Istruzione di caricamento trama proiettata. Questa istruzione divide la coordinata di trama di input in base al quarto elemento (. a o. w) appena prima del campionamento.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 045caf6ec922183893df252488946546602d2459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339151"
---
# <a name="texldp---ps"></a>texldp-PS

Istruzione di caricamento trama proiettata. Questa istruzione divide la coordinata di trama di input in base al quarto elemento (. a o. w) appena prima del campionamento.

## <a name="syntax"></a>Sintassi



| texldp DST, src0, src1 |
|------------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama. Vedere [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifica il [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , dove specifica il \# numero di campionamento di trama da campionare. Il campionatore è associato a una trama e a uno stato del campionatore definito da [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Per il set di restrizioni quando si usa texldp, vedere [texld](texld---ps-2-0.md).

## <a name="remarks"></a>Commenti

texldp esegue la proiezione sulle coordinate lette da src0 prima di eseguire l'esempio. Ogni coordinata di trama è divisa per src0. w, quindi la trama viene campionata. Al termine dell'esecuzione di texldp, il contenuto di src0 non è interessato (a meno che DST non sia lo stesso registro). Un'alternativa all'uso di texldp consiste nell'eseguire manualmente la divisione della proiezione nello shader. Tuttavia, l'esecuzione della divisione nel codice dello shader è in genere più lenta rispetto a quando viene eseguita dall'istruzione texldp, evitando così una matematica aggiuntiva, quando possibile.

Il numero di coordinate necessarie per l'esecuzione dell'esempio di trama da parte di src0 dipende dalla modalità con cui è stato dichiarato src1, più dal componente. w. I tipi di campionatore sono dichiarati con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md). Se src1 viene dichiarato come campionatore 2D, src0 deve contenere le coordinate. XYW; Se src1 viene dichiarato come Sampler del cubo o campionatore del volume, src0 deve contenere le coordinate. xyzw. Campionamento di una trama 2D con coordinate xyzw consentite (la coordinata. z viene ignorata).

Se la trama di origine contiene meno di quattro componenti, i valori predefiniti vengono inseriti nei componenti mancanti. Le impostazioni predefinite dipendono dal formato di trama, come illustrato nella tabella seguente.



| Formato trama                                                                                          | Valori predefiniti per i componenti mancanti |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT L8 \_ , D3DFMT L16 \_ , \_ \_ \_ D3DFMT R3G3B2, D3DFMT CxV8U8, D3DFMT L6V5U5 | A = 1,0                               |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT G16R16 \_ , D3DFMT G16R16F \_ , D3DFMT \_ G32R32F                          | B = A = 1,0                           |
| D3DFMT \_ a8                                                                                              | R = G = B = 0,0                       |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0                       |
| Tutti i formati di profondità/stencil                                                                               | R = B = 0,0, A = 1,0                  |



 

Questa istruzione è supportata nelle versioni seguenti:



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldp                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 e PS \_ 2 \_ x

l'ora legale deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) ed è consentita solo la maschera xyzw (maschera predefinita).

src0 deve essere un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), senza modificatore o Swizzle.

src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatore o Swizzle.

Se il \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT non è impostato (in D3DPSHADERCAPS2 \_ 0), è possibile che una determinata istruzione di trama ([texld](texld---ps-1-4.md), texldp, [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) dipenda al massimo dal terzo ordine. Un'istruzione di trama dipendente dal primo ordine è un'istruzione di trama in cui:

-   src0 è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )
-   l'ora legale è stata scritta in precedenza.

Un'istruzione di trama dipendente di secondo ordine è definita come un'istruzione di trama che legge o scrive in un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) il cui contenuto, prima di eseguire l'istruzione di trama, dipende (forse indirettamente) dal risultato di un'istruzione di trama dipendente dal primo ordine. Un'<sup>istruzione di trama</sup>dipendente dall'ordine (n) deriva da un'istruzione di trama dell'ordine (n-<sup>1).</sup>

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Per PS \_ 3 \_ 0, src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatori. Swizzle è consentito in src1 e, se applicato, i risultati della ricerca di trama sono pre-swizzled prima della scrittura nell'ora legale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 