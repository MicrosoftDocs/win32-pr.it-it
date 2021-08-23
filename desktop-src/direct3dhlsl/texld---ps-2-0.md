---
title: texld - ps_2_0 e su
description: Campionare una trama in corrispondenza di un determinato campionatore, usando le coordinate di trama specificate. Questa istruzione è diversa dall'istruzione texld - ps \_ \_ 1 4 usata nella pixel shader versione 1 \_ 4.
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e718bccc05d871cf3d79ec23530c0c891f484f6980b460d497a878742e1b57c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505806"
---
# <a name="texld---ps_2_0-and-up"></a>texld - ps \_ 2 \_ 0 e up

Campionare una trama in corrispondenza di un determinato campionatore, usando le coordinate di trama specificate. Questa istruzione è diversa [dall'istruzione texld - ps \_ 1 \_ 4](texld---ps-1-4.md) usata pixel shader versione 1 \_ 4.

## <a name="syntax"></a>Sintassi



| texld dst, src0, src1 |
|-----------------------|



 

Dove:

-   dst è un registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate di trama per il campione di trama.
-   src1 identifica il [campionatore (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s ), dove specifica il numero del campionatore \# di trama da \# campionare. Al campionatore è associata una trama e uno stato del campionatore definiti da [**D3DSAMPLERSTATETYPE.**](/windows/desktop/direct3d9/d3dsamplerstatetype)

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 e ps \_ 2 \_ x

dst deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r ) ed è consentita solo la maschera \# .xyzw (maschera predefinita).

src0 deve essere un registro delle coordinate di [trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t ) o un registro \# temporaneo (r [](dx9-graphics-reference-asm-ps-registers-temporary.md) ), senza \# modificatore o swizzle.

src1 deve essere un [campionatore (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s ), senza \# modificatore o swizzle.

Se il bit limite NODEPENDENTREADLIMIT D3DD3DPSHADERCAPS2 0 non è impostato \_ \_ (in D3DPSHADERCAPS2 0), una determinata istruzione di trama \_ ( texld , [texldp](texldp---ps.md), [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) )[](texld---ps-1-4.md)può dipendere al massimo dal terzo ordine. Un'istruzione di trama dipendente dal primo ordine è un'istruzione di trama in cui:

-   src0 è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   dst è stato scritto in precedenza, ora viene scritto di nuovo.

Un'istruzione di trama dipendente dal secondo ordine è definita come istruzione di trama che legge o scrive in un registro temporaneo [(r](dx9-graphics-reference-asm-ps-registers-temporary.md) ) il cui contenuto, prima di eseguire l'istruzione di trama, dipende (forse indirettamente) dal risultato di un'istruzione di trama dipendente dal primo \# ordine. Un'istruzione<sup></sup>di trama dipendente dall'ordine (n) deriva da un'istruzione di trama (n - 1)<sup>th</sup>-order.

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

src1 deve essere un [campionatore (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), senza modificatore. Lo swizzle è consentito in src0 o src1. Lo swizzle viene applicato alle coordinate della trama prima della ricerca della trama.

## <a name="remarks"></a>Commenti

Questa istruzione è supportata nelle versioni seguenti:



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      |      | x    | x    | x     | x    | x     |



 

Il numero di coordinate necessarie a src0 per eseguire il campione di trama dipende dalla modalità di dichiarazione di src1, più il componente .w. I tipi di campionatore vengono [dichiarati con dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md). Se src1 viene dichiarato come campionatore 2D, src0 deve contenere coordinate XY; se src1 viene dichiarato come campionatore di cubo o campionatore di volume, src0 deve contenere coordinate XYZ. Il campionamento di una trama con meno dimensioni di quelle presenti nella coordinata della trama è consentito perché i componenti aggiuntivi delle coordinate della trama vengono ignorati.

Se la trama di origine contiene meno di quattro componenti, i valori predefiniti vengono inseriti nei componenti mancanti. I valori predefiniti dipendono dal formato della trama, come illustrato nella tabella seguente:



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

 

 
