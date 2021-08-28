---
title: ret - ps
description: Accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione da esso. Nel caso della funzione main, questa istruzione arresta l'esecuzione dello shader.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77d2bb63655a83716d74621a5ece097259b0a90461f902801c375a079f118f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853781"
---
# <a name="ret---ps"></a>ret - ps

Accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione da esso. Nel caso della funzione main, questa istruzione arresta l'esecuzione dello shader.

## <a name="syntax"></a>Sintassi



| Ret |
|-----|



 

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Ret                   |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione da esso. Nel caso della funzione main, questa istruzione arresta l'esecuzione dello shader.

L'istruzione ret usa uno slot di istruzioni vertex shader.

Se uno shader non contiene subroutine, l'uso di ret alla fine del programma principale è facoltativo.

Non sono consentite più istruzioni return nel programma principale o in qualsiasi subroutine. La prima istruzione return viene considerata la fine del programma principale o della subroutine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




