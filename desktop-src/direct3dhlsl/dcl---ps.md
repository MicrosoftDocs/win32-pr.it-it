---
title: dcl - (sm2, sm3 - ps asm)
description: Dichiarare un registro pixel shader di input.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dab377a36cb1323daf450b9566e419b60edc1fb80dde54591a932b2e0f28223a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793467"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>dcl - (sm2, sm3 - ps asm)

Dichiarare un registro pixel shader di input.

## <a name="syntax"></a>Sintassi

dcl \[ \_ pp \] dest \[ .mask\]



 

Dove:

-   \[\_pp \] è una precisione parziale facoltativa. Vedere [Precisione parziale.](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)
-   dest è un registro di destinazione. Deve essere un registro colori [di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn) o un registro delle coordinate di [trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).
-   \[.mask è una maschera di scrittura facoltativa che controlla i componenti del registro di \] destinazione in cui è possibile scrivere. Vedere [Maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Dcl                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Tutte le istruzioni dcl devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




