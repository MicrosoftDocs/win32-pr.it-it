---
title: call - ps
description: Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta specificata. | call - ps
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ae1b8a19178b0a6633a98472814e225e9ac2f7de9e3e2f016720f2f5b1a9b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794085"
---
# <a name="call---ps"></a>call - ps

Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta specificata.

## <a name="syntax"></a>Sintassi



| chiamare l\# |
|----------|



 

Dove:

-   l \# è [un'etichetta: ps](label---ps.md) che contrassegna l'inizio della subroutine da chiamare.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| chiamare                  |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione esegue le operazioni seguenti:

1.  Eseguire il push dell'indirizzo dell'istruzione successiva nello stack di indirizzi mittente.
2.  Continuare l'esecuzione dall'istruzione contrassegnata dall'etichetta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




