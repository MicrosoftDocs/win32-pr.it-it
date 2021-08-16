---
title: texldb - ps
description: Istruzione di caricamento trame distorte. Questa istruzione usa il quarto elemento (.a o .w) per eseguire la distorsione del livello di dettaglio di campionamento della trama subito prima del campionamento.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddf340840e377ee03641ae33c0731f27e90ce4760cad4ddb6c636c1831fa80ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505794"
---
# <a name="texldb---ps"></a>texldb - ps

Istruzione di caricamento trame distorte. Questa istruzione usa il quarto elemento (.a o .w) per eseguire la distorsione del livello di dettaglio di campionamento della trama subito prima del campionamento.

## <a name="syntax"></a>Sintassi



| texldb dst, src0, src1 |
|------------------------|



 

Dove:

-   dst è il registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate della trama per l'esempio di trama. Vedere [Registro coordinate trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifica il [sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s), dove specifica il numero del \# \# campionatore di trama da campionare. Il campionatore ha associato una trama e uno stato del campionatore definito da [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Per le restrizioni quando si usa texldb, vedere l'istruzione [texld - ps \_ 2 \_ 0 e up.](texld---ps-2-0.md)

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 e ps \_ 2 \_ x

dst deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r ) ed è consentita solo la maschera \# .xyzw (maschera predefinita).

src0 deve essere un registro delle [coordinate](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) di trama (t ) o un registro temporaneo \# (r ), senza [](dx9-graphics-reference-asm-ps-registers-temporary.md) \# modificatore o scorrimento.

src1 deve essere un [sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# (s), senza modificatore o swizzle.

Se il bit limite D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT non è impostato \_ \_ (in D3DPSHADERCAPS2 0), una determinata istruzione di trama \_ (texld, texldp, texldb, texldd) può dipendere al massimo dal terzo ordine. Un'istruzione di trama dipendente dal primo ordine è un'istruzione di trama in cui:

-   src0 è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   dst è stato scritto in precedenza e ora viene scritto di nuovo.

Un'istruzione di trama dipendente dal secondo ordine è definita come un'istruzione di trama che legge o scrive in un registro temporaneo [(r](dx9-graphics-reference-asm-ps-registers-temporary.md) ) il cui contenuto, prima di eseguire l'istruzione di trama, dipende (forse indirettamente) dal risultato di un'istruzione di trama dipendente dal primo \# ordine. Un'istruzione<sup></sup>di trama dipendente dall'ordine (n) deriva da un'istruzione di trama (n - 1)<sup>th</sup>-order.

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

src1 deve essere un [sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# (s), senza modificatore. Lo swizzle è consentito in src1 e, se applicati, i risultati della ricerca trame vengono pre-swizzle prima di essere scritti in dst.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldb                |      |      |      |      | x    | x    | x     | x    | x     |



 

texldb biases the mipmap level-of-detail, computed normally as part of the sample process by the (signed) value in src0.w. I valori di distorsione positiva comportano la selezione di mipmap più piccoli e viceversa. Per ps 2 0 e ps 2 x, i valori di distorsione possono essere nell'intervallo \_ \_ \_ \_ \[ -3.0, +3.0 \] . Per ps 3 0, i valori di distorsione possono essere \_ \_ nell'intervallo \[ -16.0, +15.0 \] . I valori di distorsione al di fuori di questi intervalli producono risultati non definiti. Lo stato del campionatore D3DSAMP MIPMAPLODBIAS è ancora rispettato e la distorsione texldb viene aggiunta a questo, ma per \_ pixel. Dopo aver calcolato il livello di dettaglio distorto, D3DSAMP MAXMIPLEVEL viene comunque rispettato e si verifica \_ l'esempio di trama. Dopo texldb, il contenuto di src0 non è interessato (a meno che dst non sia lo stesso registro).

Il numero di coordinate necessarie per eseguire l'esempio di trama da parte di src0 dipende dalla modalità di dichiarazione di src1, oltre al componente con estensione w. I tipi sampler vengono dichiarati con [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md). Se src1 viene dichiarato come campionatore 2D, src0 deve contenere coordinate xyw. se src1 è dichiarato come campionatore di cubi o campionatore di volumi, src0 deve contenere coordinate xyzw. Il campionamento di una trama 2D con coordinate xyzw è consentito (la coordinata .z viene ignorata).

Se la trama di origine contiene meno di quattro componenti, i valori predefiniti vengono inseriti nei componenti mancanti. Le impostazioni predefinite dipendono dal formato della trama, come illustrato nella tabella seguente:



| Formato trama                                                                                          | Valori predefiniti       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5 | A = 1.0              |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F                          | B = A = 1,0          |
| D3DFMT \_ A8                                                                                              | R = G = B = 0,0      |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0      |
| Tutti i formati di profondità/stencil                                                                               | R = B = 0,0, A = 1,0 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 