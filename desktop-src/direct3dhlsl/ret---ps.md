---
title: RET-PS
description: Accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione. Nel caso della funzione Main, questa istruzione arresta l'esecuzione dello shader.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976346"
---
# <a name="ret---ps"></a>RET-PS

Accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione. Nel caso della funzione Main, questa istruzione arresta l'esecuzione dello shader.

## <a name="syntax"></a>Sintassi



| RET |
|-----|



 

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| RET                   |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione. Nel caso della funzione Main, questa istruzione arresta l'esecuzione dello shader.

L'istruzione RET usa uno slot di istruzioni vertex shader.

Se uno shader non contiene subroutine, l'utilizzo di RET alla fine del programma principale è facoltativo.

Non sono consentite più istruzioni return nel programma principale o in una subroutine, la prima istruzione return viene considerata come la fine del programma principale o della subroutine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




