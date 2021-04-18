---
description: La tabella dei collegamenti e le tabelle correlate del database di installazione contengono le informazioni necessarie per installare i collegamenti. Vedere il gruppo tabelle informazioni sul programma e modificare i collegamenti del programma di installazione.
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: Specifica dei collegamenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29edf10a51827880a67826320d7f8415e70ea52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310793"
---
# <a name="specifying-shortcuts"></a>Specifica dei collegamenti

La [tabella](shortcut-table.md) dei collegamenti e le tabelle correlate del database di installazione contengono le informazioni necessarie per installare i collegamenti. Vedere il [gruppo tabelle informazioni sul programma](program-information-tables-group.md) e [modificare i collegamenti](editing-installer-shortcuts.md)del programma di installazione.

In questa sezione vengono aggiunte informazioni che specificano i collegamenti annunciati e non annunciati per l'esempio del blocco note.

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella dei collegamenti.

[Tabella di collegamento](shortcut-table.md)



| Tasto di scelta rapida  | Directory\_ | Nome         | Componente\_ | Destinazione             | Argomenti | Descrizione | Tasto di scelta rapida | Icona\_         | IconIndex | ShowCmd | WkDir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sBaseball | MENUDIR     | Baseball.txt | Baseball    | Baseball           |           |             |        | \_icon.exe Orca |           |         |       |
| sConcert  | MENUDIR     | Concert.txt  | Concerto     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sDance    | MENUDIR     | Dance.txt    | Danza       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sFootball | MENUDIR     | Football.txt | Calcio    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| sHelp     | MENUDIR     | Help.txt     | Help        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sJanuary  | MENUDIR     | January.txt  | January     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| sNewYears | MENUDIR     | NewYears.txt | NewYears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| sNotepad  | MENUDIR     | Redpark.exe  | Blocco note     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sReadme   | MENUDIR     | Readme.txt   | Blocco note     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

L'installazione di esempio deve consentire l'installazione di un collegamento annunciato per la funzionalità di baseball. È necessario specificare una chiave per la tabella delle icone nella \_ colonna icona della tabella dei collegamenti. Ai fini di questo esempio, è possibile copiare l'icona per l'editor di database Orca fornito con Windows Installer SDK. Esportare la [tabella icone](icon-table.md) da Orca.msi, quindi unire la tabella nel database di MNP2000.msi usando Orca o un altro strumento di merge. Orca crea anche una directory denominata Icon nella directory che contiene MNP2000.msi e aggiunge il file di dati binari dell'icona Orca \_icon.exe. IBD. Vedere la colonna di dati nella tabella delle icone. La tabella dell'icona completata dovrebbe essere simile alla seguente quando viene visualizzata in Orca.

[Icona tabella](icon-table.md)



| Nome           | Data            |
|----------------|-----------------|
| \_icon.exe Orca | \[Binary Data\] |



 

[Continua](specifying-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifica dei collegamenti del programma di installazione](editing-installer-shortcuts.md)
</dt> </dl>

 

 



