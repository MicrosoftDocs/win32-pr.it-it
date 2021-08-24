---
description: Un'azione personalizzata può chiamare funzioni scritte in VBScript o JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af49e1863d43956e8ec799e467d8391873458d1879f78455abda9ee06fb739aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041371"
---
# <a name="scripts"></a>Script

Un'azione personalizzata può chiamare funzioni scritte in VBScript o JScript. Windows Il programma di installazione non fornisce il motore di script. Gli autori che desiderano usare un linguaggio di scripting durante l'installazione devono pertanto assicurarsi che sia disponibile il motore di scripting appropriato.

Il programma di installazione non supporta JScript versione 1.0.

Un'azione personalizzata a 64 bit basata su script deve essere contrassegnata in modo esplicito come azione personalizzata a 64 bit aggiungendo il bit **msidbCustomActionType64BitScript** al tipo numerico delle azioni personalizzate nella colonna Type della [tabella CustomAction.](customaction-table.md) Per informazioni, vedere [Azioni personalizzate a 64 bit.](64-bit-custom-actions.md)

I seguenti tipi di azione personalizzata di base chiamano funzioni scritte nello script.



| Tipo di azione personalizzata                                 | Descrizione                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Tipo di azione personalizzata 5](custom-action-type-5.md)   | JScript file archiviato in un flusso di tabella binaria.                                                  |
| [Tipo di azione personalizzata 21](custom-action-type-21.md) | JScript file installato con un prodotto.                                                 |
| [Tipo di azione personalizzata 53](custom-action-type-53.md) | JScript testo specificato da un valore della proprietà.                                                    |
| [Tipo di azione personalizzata 37](custom-action-type-37.md) | JScript testo archiviato nella colonna Target della [tabella CustomAction.](customaction-table.md)  |
| [Tipo di azione personalizzata 6](custom-action-type-6.md)   | File VBScript archiviato in un flusso di tabella [binaria.](binary-table.md)                             |
| [Tipo di azione personalizzata 22](custom-action-type-22.md) | File VBScript installato con un prodotto.                                                |
| [Tipo di azione personalizzata 54](custom-action-type-54.md) | Testo VBScript specificato da un valore della proprietà.                                                   |
| [Tipo di azione personalizzata 38](custom-action-type-38.md) | Testo VBScript archiviato nella colonna Target della [tabella CustomAction.](customaction-table.md) |



 

> [!Note]  
> Il programma di installazione esegue direttamente le azioni personalizzate dello script e non usa l'host Windows script. **L'oggetto WScript** non può essere usato all'interno di un'azione personalizzata dello script perché questo oggetto viene fornito dall'host Windows script. Gli oggetti nel modello a oggetti dell'host di script Windows possono essere usati nelle azioni personalizzate solo se Windows Script Host è installato nel computer creando nuove istanze dell'oggetto, con una chiamata a CreateObject e specificando il ProgId dell'oggetto ,ad esempio "WScript.Shell". A seconda del tipo di azione personalizzata script, l'accesso ad alcuni oggetti e metodi del modello a oggetti Windows Script Host può essere negato per motivi di sicurezza.

 

Per altre informazioni, vedere [Elenco](summary-list-of-all-custom-action-types.md) di riepilogo di tutti i tipi di azione personalizzati per un riepilogo di tutti i tipi di azioni personalizzate e di come vengono codificate nella [tabella CustomAction.](customaction-table.md)

 

 



