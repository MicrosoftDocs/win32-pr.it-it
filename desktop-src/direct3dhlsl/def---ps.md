---
title: def - ps
description: Definisce pixel shader costanti a virgola mobile.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce5f842f44e915d3f3240618261b501f2240c3636227f930538e1bbcbe0d9367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726561"
---
# <a name="def---ps"></a>def - ps

Definisce pixel shader costanti a virgola mobile.

## <a name="syntax"></a>Sintassi



| def dst, fVvalue1, fValue2, fValue3, fValue4 |
|----------------------------------------------|



 

Dove:

-   dst è il registro di destinazione.
-   Da fValue1 a fValue4 sono valori a virgola mobile.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| def                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Esistono due modi per impostare una costante a virgola mobile in un pixel shader.

1.  Usare def per definire la costante direttamente all'interno di uno shader.
2.  Usare l'API per impostare una costante [**con SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

def definisce una costante shader il cui valore viene caricato ogni volta che uno shader viene impostato su un dispositivo. Queste sono chiamate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API.

-   Deve essere visualizzato prima della prima istruzione aritmetica o di indirizzamento nello shader.
-   Può essere intermixed con istruzioni [dcl - (sm2, sm3 - ps asm),](dcl---ps.md) che sono l'altro tipo di istruzione che si trova all'inizio di uno shader.
-   dst register deve essere un [registro costante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).
-   La maschera di scrittura deve essere piena (impostazione predefinita).
-   Se un [registro costante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) viene definito più volte in uno shader, l'ultimo viene mantenuto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 