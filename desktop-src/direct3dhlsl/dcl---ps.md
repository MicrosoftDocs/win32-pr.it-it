---
title: DCL-(SM2, SM3-PS ASM)
description: Dichiarare un registro pixel shader input.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad61ea8d733ed01fcd2e57ba06c38e0b3efac682
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398270"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>DCL-(SM2, SM3-PS ASM)

Dichiarare un registro pixel shader input.

## <a name="syntax"></a>Sintassi



|                           |
|---------------------------|
| \[ \_ \] dest \[ . mask di DCL PP\] |



 

Dove:

-   \[\_PP \] è una precisione parziale facoltativa. Vedere [precisione parziale](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).
-   dest è un registro di destinazione. Deve essere un registro del [colore di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN) o un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN).
-   \[. mask \] è una maschera di scrittura facoltativa che controlla i componenti del registro di destinazione in cui è possibile scrivere. Vedere la [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DCL                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Tutte le istruzioni di DCL devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




