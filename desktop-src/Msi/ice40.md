---
description: ICE40 esegue la convalida varie.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077c44154413d9aa9e75b1c13fe2f2f80ccb52fee6459888c7bc9678ea0e935f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528431"
---
# <a name="ice40"></a>ICE40

ICE40 esegue la convalida varie.

## <a name="result"></a>Risultato

ICE40 invia avvisi sugli elementi seguenti:

-   La [**proprietà REINSTALLMODE**](reinstallmode.md) è stata sottoposta a override.
-   La [tabella RemoveIniFile](removeinifile-table.md) include una voce Delete Tag senza valore.
-   Nel .msi manca la tabella [Error](error-table.md) e [**la proprietà Page Count Summary**](page-count-summary.md) è minore o uguale a 100. Questo avviso ICE è obsoleto perché Windows programma di installazione non richiede che il pacchetto abbia una tabella Di errore. I messaggi di errore possono essere recuperati usando Msimsg.dll.

## <a name="example"></a>Esempio

[Tabella delle proprietà](property-table.md)



| Proprietà                               | Valore |
|----------------------------------------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | A     |



 

[Tabella RemoveIniFile](removeinifile-table.md)



| RemoveIniFile                          | Azione | Valore |
|----------------------------------------|--------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | 4      |       |



 

## <a name="results"></a>Risultati

ICE40 segnala gli errori seguenti.



| Errore ICE40                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REINSTALLMODE**](reinstallmode.md) è definito nella tabella Property. Ciò può causare difficoltà. | La definizione della [**proprietà REINSTALLMODE**](reinstallmode.md) nel file .msi può causare un comportamento imprevisto. Per correggere l'errore, non definire questa proprietà.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| La voce RemoveIniFile Remove1 deve avere un valore perché Action è "Delete Tag" (4).                | È presente un'azione Elimina tag nella colonna RemoveIniFile della tabella [RemoveIniFile](removeinifile-table.md) senza specificare un tag da eliminare nella colonna Valore.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Tabella degli errori mancante. Verranno generati solo messaggi di errore numerici.                              | Questo avviso ICE è obsoleto perché Windows programma di installazione non richiede che il pacchetto abbia una [tabella Di errore](error-table.md). I messaggi di errore possono essere recuperati usando Msimsg.dll.<br/> Questo avviso indica che nel file .msi manca la tabella [Error](error-table.md) e [**che la proprietà Page Count Summary**](page-count-summary.md) è minore o uguale a 100. <br/> Per correggere l'errore, usare una versione corrente del programma di installazione di Windows oppure aggiungere una tabella Errore al pacchetto di installazione e creare modelli di formattazione nella colonna Messaggio per i messaggi di errore.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




