---
description: ICE40 esegue la convalida varie.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131871"
---
# <a name="ice40"></a>ICE40

ICE40 esegue la convalida varie.

## <a name="result"></a>Risultato

ICE40 invia avvisi sugli elementi seguenti:

-   La proprietà [**REINSTALLMODE**](reinstallmode.md) è stata sottoposta a override.
-   La [tabella RemoveIniFile](removeinifile-table.md) include una voce Delete tag senza valore.
-   Nel file con estensione msi manca la [tabella degli errori](error-table.md) e la proprietà di [**Riepilogo dei conteggi delle pagine**](page-count-summary.md) è minore o uguale a 100. Questo avviso di ghiaccio è obsoleto perché per Windows Installer non è necessario che il pacchetto includa una tabella degli errori. È possibile recuperare i messaggi di errore utilizzando Msimsg.dll.

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

ICE40 segnala i seguenti errori.



| Errore ICE40                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REINSTALLMODE**](reinstallmode.md) è definito nella tabella delle proprietà. Questo può causare problemi. | La definizione della proprietà [**REINSTALLMODE**](reinstallmode.md) nel file con estensione msi può causare un comportamento imprevisto. Per correggere l'errore, non definire questa proprietà.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| La voce RemoveIniFile Remove1 deve avere un valore, perché l'azione è "Delete tag" (4).                | È presente un'azione Elimina tag nella colonna RemoveIniFile della [tabella RemoveIniFile](removeinifile-table.md) senza specificare un tag da eliminare nella colonna valore.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Tabella degli errori mancante. Verranno generati solo i messaggi di errore numerici.                              | Questo avviso di ghiaccio è obsoleto perché per Windows Installer non è necessario che il pacchetto includa una [tabella degli errori](error-table.md). È possibile recuperare i messaggi di errore utilizzando Msimsg.dll.<br/> Questo avviso indica che nel file con estensione msi manca la [tabella degli errori](error-table.md) e che la proprietà di [**Riepilogo dei conteggi delle pagine**](page-count-summary.md) è minore o uguale a 100. <br/> Per correggere l'errore, utilizzare una versione corrente del Windows Installer oppure aggiungere una tabella degli errori al pacchetto di installazione e creare modelli di formattazione nella colonna messaggio per i messaggi di errore.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




