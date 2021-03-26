---
title: def-PS
description: Definisce pixel shader costanti a virgola mobile.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047302"
---
# <a name="def---ps"></a>def-PS

Definisce pixel shader costanti a virgola mobile.

## <a name="syntax"></a>Sintassi



| def DST, fVvalue1, fValue2, fValue3, fValue4 |
|----------------------------------------------|



 

Dove:

-   DST è il registro di destinazione.
-   fValue1 a fValue4 sono valori a virgola mobile.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| def                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Esistono due modi per impostare una costante a virgola mobile in una pixel shader.

1.  Usare def per definire la costante direttamente all'interno di uno shader.
2.  Usare l'API per impostare una costante con [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

def definisce una costante dello shader il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo. Sono denominate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API.

-   Deve comparire prima della prima istruzione aritmetica o di indirizzamento nello shader.
-   È possibile combinare le istruzioni [DCL-(SM2, SM3-PS ASM),](dcl---ps.md) ovvero l'altro tipo di istruzione che risiede all'inizio di uno shader.
-   il registro DST deve essere un [registro costante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).
-   La maschera di scrittura deve essere piena (impostazione predefinita).
-   Se un [registro costante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) viene definito più volte in uno shader, l'ultimo viene reso permanente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 