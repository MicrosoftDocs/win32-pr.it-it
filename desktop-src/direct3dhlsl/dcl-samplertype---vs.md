---
title: dcl_samplerType (SM3-vs ASM)
description: Dichiarare un campionatore vertex shader.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993205"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>DCL \_ samplerType (SM3-vs ASM)

Dichiarare un campionatore vertex shader.

## <a name="syntax"></a>Sintassi



|                      |
|----------------------|
| samplerType di DCL \_\# |



 

dove:

-   \_samplerType definisce il tipo di dati del campionatore. Determina il numero di coordinate necessarie per ogni coordinata di trama durante il campionamento. Sono definite le dimensioni delle coordinate di trama seguenti.
    -   \_2D
    -   \_cubo
    -   \_volume
-   s \# identifica un campionatore dove s è un'abbreviazione del campionatore e \# è il numero di campionatore. [Sampler (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s sono pseudo-registri perché non è possibile leggere o scrivere direttamente.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \_samplerType DCL       |      |      |      |       | x    | x     |



 

Tutte le \_ istruzioni samplerType di DCL devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




