---
title: dcl_samplerType (sm3 - vs asm)
description: Dichiarare un campionatore vertex shader.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 048246f8a48430dca26a763e9266f00edd61215e769f4ff5385036054aebc34b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726571"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>dcl \_ samplerType (sm3 - vs asm)

Dichiarare un campionatore vertex shader.

## <a name="syntax"></a>Sintassi

dcl \_ samplerType s\#



 

dove:

-   \_samplerType definisce il tipo di dati sampler. Questo determina il numero di coordinate richieste da ogni coordinata di trama durante il campionamento. Vengono definite le dimensioni delle coordinate di trama seguenti.
    -   \_2d
    -   \_Cubo
    -   \_Volume
-   s \# identifica un campionatore dove s è l'abbreviazione del campionatore e \# è il numero del campionatore. [I sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)sono pseudoregistri perché non è possibile leggerli o scrivervi direttamente.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ samplerType       |      |      |      |       | x    | x     |



 

Tutte le istruzioni dcl \_ samplerType devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




