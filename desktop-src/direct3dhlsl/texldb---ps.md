---
title: texldb-PS
description: Istruzione di caricamento trama distorta. Questa istruzione usa il quarto elemento (. a o. w) per inclinare il livello di dettaglio del campionamento della trama appena prima del campionamento.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117894"
---
# <a name="texldb---ps"></a>texldb-PS

Istruzione di caricamento trama distorta. Questa istruzione usa il quarto elemento (. a o. w) per inclinare il livello di dettaglio del campionamento della trama appena prima del campionamento.

## <a name="syntax"></a>Sintassi



| texldb DST, src0, src1 |
|------------------------|



 

Dove:

-   DST è il registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama. Vedere [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifica il [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , dove specifica il \# numero di campionamento di trama da campionare. Il campionatore è associato a una trama e a uno stato del campionatore definito da [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Per le restrizioni relative all'uso di texldb, vedere le istruzioni [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md) .

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 e PS \_ 2 \_ x

l'ora legale deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) ed è consentita solo la maschera xyzw (maschera predefinita).

src0 deve essere un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), senza modificatore o Swizzle.

src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatore o Swizzle.

Se il \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT CAP non è impostato (in D3DPSHADERCAPS2 \_ 0), è possibile che una determinata istruzione di trama (texld, texldp, texldb, texldd) dipenda al massimo dal terzo ordine. Un'istruzione di trama dipendente dal primo ordine è un'istruzione di trama in cui:

-   src0 è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   l'ora legale è stata scritta in precedenza.

Un'istruzione di trama dipendente di secondo ordine è definita come un'istruzione di trama che legge o scrive in un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) il cui contenuto, prima di eseguire l'istruzione di trama, dipende (forse indirettamente) dal risultato di un'istruzione di trama dipendente dal primo ordine. Un'<sup>istruzione di trama</sup>dipendente dall'ordine (n) deriva da un'istruzione di trama dell'ordine (n-<sup>1).</sup>

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatori. Swizzle è consentito in src1 e, se applicato, i risultati della ricerca di trama sono pre-swizzled prima della scrittura nell'ora legale.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldb                |      |      |      |      | x    | x    | x     | x    | x     |



 

texldb polarizza il livello di dettaglio mipmap, calcolato normalmente come parte del processo di esempio mediante il valore (con segno) in src0. w. I valori di bias positivi comporteranno la selezione di mipmap più piccoli e viceversa. Per PS \_ 2 \_ 0 e PS \_ 2 \_ x, i valori di distorsione possono essere compresi nell'intervallo compreso tra \[ -3,0 e + 3,0 \] . Per PS \_ 3 \_ 0, i valori di distorsione possono essere compresi nell'intervallo compreso tra \[ -16,0 e + 15,0 \] . I valori di distorsione al di fuori di questi intervalli producono risultati non definiti. Lo stato del campionatore D3DSAMP \_ MIPMAPLODBIAS viene comunque rispettato e la distorsione texldb viene aggiunta a questa, ma in base ai singoli pixel. Dopo il calcolo del livello di dettaglio distorta, D3DSAMP \_ MAXMIPLEVEL viene comunque rispettato e si verifica l'esempio di trama. Dopo texldb, il contenuto di src0 non è interessato (a meno che DST non sia lo stesso registro).

Il numero di coordinate necessarie per l'esecuzione dell'esempio di trama da parte di src0 dipende dalla modalità con cui è stato dichiarato src1, più dal componente. w. I tipi di campionatore sono dichiarati con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md). Se src1 viene dichiarato come campionatore 2D, src0 deve contenere le coordinate. XYW; Se src1 viene dichiarato come Sampler del cubo o campionatore del volume, src0 deve contenere le coordinate. xyzw. Campionamento di una trama 2D con coordinate xyzw consentite (la coordinata. z viene ignorata).

Se la trama di origine contiene meno di quattro componenti, i valori predefiniti vengono inseriti nei componenti mancanti. Le impostazioni predefinite dipendono dal formato di trama, come illustrato nella tabella seguente:



| Formato trama                                                                                          | Valori predefiniti       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT L8 \_ , D3DFMT L16 \_ , \_ \_ \_ D3DFMT R3G3B2, D3DFMT CxV8U8, D3DFMT L6V5U5 | A = 1,0              |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT G16R16 \_ , D3DFMT G16R16F \_ , D3DFMT \_ G32R32F                          | B = A = 1,0          |
| D3DFMT \_ a8                                                                                              | R = G = B = 0,0      |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0      |
| Tutti i formati di profondità/stencil                                                                               | R = B = 0,0, A = 1,0 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 