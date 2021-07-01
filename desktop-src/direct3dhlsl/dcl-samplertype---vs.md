---
title: dcl_samplerType (sm3 - vs asm)
description: Dichiarare un campionatore di vertex shader.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129869"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>dcl \_ samplerType (sm3 - vs asm)

Dichiarare un campionatore di vertex shader.

## <a name="syntax"></a>Sintassi

dcl \_ samplerType s\#



 

dove:

-   \_samplerType definisce il tipo di dati sampler. In questo modo viene determinato il numero di coordinate richieste da ogni coordinata di trama durante il campionamento. Vengono definite le dimensioni delle coordinate di trama seguenti.
    -   \_2d
    -   \_Cubo
    -   \_Volume
-   s \# identifica un campionatore, dove s è un'abbreviazione del campionatore e \# è il numero del campionatore. [I sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)sono pseudoregistri perché non è possibile leggerli o scriverli direttamente.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ samplerType       |      |      |      |       | x    | x     |



 

Tutte le istruzioni dcl \_ samplerType devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




