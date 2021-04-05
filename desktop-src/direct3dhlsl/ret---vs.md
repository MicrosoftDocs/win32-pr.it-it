---
title: RET-vs
description: Restituisce da una subroutine o da una funzione Main.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335495"
---
# <a name="ret---vs"></a>RET-vs

Restituisce da una subroutine o da una funzione Main.

## <a name="syntax"></a>Sintassi



| RET |
|-----|



 

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| RET                    |      | x    | x    | x     | x    | x     |



 

Questa istruzione accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione. Nel caso della funzione Main, questa istruzione arresta l'esecuzione dello shader.

L'istruzione RET usa uno slot di istruzioni vertex shader.

Se uno shader non contiene subroutine, l'utilizzo di RET alla fine del programma principale è facoltativo.

Non sono consentite più istruzioni return nel programma principale o in una subroutine, la prima istruzione return viene considerata come la fine del programma principale o della subroutine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




