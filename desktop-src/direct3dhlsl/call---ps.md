---
title: chiamata a PS
description: Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita. | chiamata a PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995493"
---
# <a name="call---ps"></a>chiamata a PS

Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita.

## <a name="syntax"></a>Sintassi



| chiama l\# |
|----------|



 

Dove:

-   l \# è un' [etichetta-PS](label---ps.md) che contrassegna l'inizio della subroutine da chiamare.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| chiamare                  |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione esegue le operazioni seguenti:

1.  Indirizzo push dell'istruzione successiva allo stack di indirizzi restituito.
2.  Continua l'esecuzione dall'istruzione contrassegnata dall'etichetta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




