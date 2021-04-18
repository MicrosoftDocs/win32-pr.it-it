---
description: Un'azione personalizzata può chiamare funzioni scritte in VBScript o JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312315"
---
# <a name="scripts"></a>Script

Un'azione personalizzata può chiamare funzioni scritte in VBScript o JScript. Windows Installer non fornisce il modulo di gestione di script. Gli autori che desiderano utilizzare un linguaggio di scripting durante l'installazione devono pertanto garantire che sia disponibile il motore di scripting appropriato.

Il programma di installazione non supporta la versione JScript 1,0.

Un'azione personalizzata a 64 bit basata sugli script deve essere contrassegnata in modo esplicito come azione personalizzata a 64 bit aggiungendo il bit **msidbCustomActionType64BitScript** al tipo numerico azioni personalizzate nella colonna Type della tabella [CustomAction](customaction-table.md) . Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).

I tipi di azione personalizzati di base seguenti chiamano funzioni scritte nello script.



| Tipo di azione personalizzata                                 | Descrizione                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Tipo di azione personalizzata 5](custom-action-type-5.md)   | File JScript archiviato in un flusso di tabella binario.                                                  |
| [Tipo di azione personalizzata 21](custom-action-type-21.md) | File JScript installato con un prodotto.                                                 |
| [Tipo di azione personalizzata 53](custom-action-type-53.md) | Testo JScript specificato da un valore della proprietà.                                                    |
| [Tipo di azione personalizzata 37](custom-action-type-37.md) | Testo JScript archiviato nella colonna di destinazione della tabella [CustomAction](customaction-table.md) .  |
| [Tipo di azione personalizzata 6](custom-action-type-6.md)   | File VBScript archiviato in un flusso di tabella [binario](binary-table.md) .                             |
| [Tipo di azione personalizzata 22](custom-action-type-22.md) | File VBScript installato con un prodotto.                                                |
| [Tipo di azione personalizzata 54](custom-action-type-54.md) | Testo VBScript specificato da un valore della proprietà.                                                   |
| [Tipo di azione personalizzata 38](custom-action-type-38.md) | Testo VBScript archiviato nella colonna di destinazione della tabella [CustomAction](customaction-table.md) . |



 

> [!Note]  
> Il programma di installazione esegue azioni personalizzate script direttamente e non usa Windows script host. Impossibile utilizzare l'oggetto **WScript** all'interno di un'azione personalizzata script perché questo oggetto viene fornito da Windows script host. Gli oggetti nel modello a oggetti di Windows script host possono essere utilizzati solo in azioni personalizzate se Windows script host è installato nel computer creando nuove istanze dell'oggetto, con una chiamata a CreateObject e specificando il ProgId dell'oggetto, ad esempio "WScript. Shell". A seconda del tipo di azione personalizzata script, l'accesso ad alcuni oggetti e metodi del modello a oggetti di Windows script host può essere negato per motivi di sicurezza.

 

Per ulteriori informazioni, vedere l' [elenco riepilogativo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md) per un riepilogo di tutti i tipi di azioni personalizzate e la relativa modalità di codifica nella tabella [CustomAction](customaction-table.md) .

 

 



