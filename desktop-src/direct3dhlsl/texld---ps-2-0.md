---
title: texld-ps_2_0 e su
description: Campionare una trama in un particolare campionatore, usando le coordinate di trama fornite. Questa istruzione è diversa dall'istruzione texld-PS \_ 1 \_ 4 usata in pixel shader versione 1 \_ 4.
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47f47a937123ce252189aac57e922b10c2a015fc
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "106334306"
---
# <a name="texld---ps_2_0-and-up"></a>texld-PS \_ 2 \_ 0 e su

Campionare una trama in un particolare campionatore, usando le coordinate di trama fornite. Questa istruzione è diversa dall'istruzione [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) usata in pixel shader versione 1 \_ 4.

## <a name="syntax"></a>Sintassi



| texld DST, src0, src1 |
|-----------------------|



 

Dove:

-   DST è un registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama.
-   src1 identifica il [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , dove specifica il \# numero di campionamento di trama da campionare. Il campionatore è associato a una trama e a uno stato del campionatore definito da [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 e PS \_ 2 \_ x

l'ora legale deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) ed è consentita solo la maschera xyzw (maschera predefinita).

src0 deve essere un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), senza modificatore o Swizzle.

src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatore o Swizzle.

Se il \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT non è impostato (in D3DPSHADERCAPS2 \_ 0), è possibile che una determinata istruzione di trama ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) dipenda al massimo dal terzo ordine. Un'istruzione di trama dipendente dal primo ordine è un'istruzione di trama in cui:

-   src0 è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   l'ora legale è stata scritta in precedenza.

Un'istruzione di trama dipendente di secondo ordine è definita come un'istruzione di trama che legge o scrive in un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) il cui contenuto, prima di eseguire l'istruzione di trama, dipende (forse indirettamente) dal risultato di un'istruzione di trama dipendente dal primo ordine. Un'<sup>istruzione di trama</sup>dipendente dall'ordine (n) deriva da un'istruzione di trama dell'ordine (n-<sup>1).</sup>

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatori. Swizzle è consentito in src0 o src1. Swizzle viene applicato alle coordinate di trama prima della ricerca della trama.

## <a name="remarks"></a>Commenti

Questa istruzione è supportata nelle versioni seguenti:



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      |      | x    | x    | x     | x    | x     |



 

Il numero di coordinate necessarie per l'esecuzione dell'esempio di trama da parte di src0 dipende dalla modalità con cui è stato dichiarato src1, più dal componente. w. I tipi di campionatore sono dichiarati con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md). Se src1 viene dichiarato come campionatore 2D, src0 deve contenere le coordinate. XY; Se src1 viene dichiarato come Sampler del cubo o campionatore del volume, src0 deve contenere le coordinate. xyz. Il campionamento di una trama con meno dimensioni rispetto a quelli presenti nella coordinata di trama è consentito perché i componenti delle coordinate di trama aggiuntivi vengono ignorati.

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

 

 
