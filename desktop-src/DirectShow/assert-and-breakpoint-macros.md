---
description: Macro di asserzione e punti di interruzione
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Macro di asserzione e punti di interruzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125349"
---
# <a name="assert-and-breakpoint-macros"></a>Macro di asserzione e punti di interruzione

Le [classi base di DirectShow](directshow-base-classes.md) forniscono diverse macro che eseguono asserzioni o generano punti di interruzione.



| Macro                                        | Descrizione                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**ASSERT**](assert.md)                     | Valuta un'espressione e visualizza un messaggio di diagnostica se l'espressione è **false**.                                         |
| [**DbgAssertAligned**](dbgassertaligned.md) | Verifica se un puntatore è allineato a un limite specificato.                                                                        |
| [**DbgBreak**](dbgbreak.md)                 | Visualizza una finestra di messaggio con la stringa specificata, il nome del file di origine e il numero di riga.                                |
| [**Esegui \_ asserzione**](execute-assert.md)    | Valuta un'espressione nelle compilazioni di debug e di vendita al dettaglio. Nelle build di debug, Visualizza un messaggio di diagnostica se l'espressione è **false**. |
| [**KASSERT**](kassert.md)                   | Valuta un'espressione e genera un'eccezione del punto di interruzione se l'espressione è **false**.                                         |
| [**KDbgBreak**](kdbgbreak.md)               | Causa un'eccezione del punto di interruzione e registra la stringa specificata.                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di debug](debugging-utilities.md)
</dt> </dl>

 

 



