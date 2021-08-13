---
description: La tabella Collegamento e le tabelle correlate del database di installazione contengono le informazioni necessarie per installare i collegamenti. Vedere Gruppo tabelle informazioni programma e Modifica dei tasti di scelta rapida del programma di installazione.
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: Specifica dei tasti di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67b43a104ee05b3711ac98395098acf9393faab8e046296e58d93df4d6b9218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624685"
---
# <a name="specifying-shortcuts"></a>Specifica dei tasti di scelta rapida

La [tabella Collegamento e](shortcut-table.md) le tabelle correlate del database di installazione contengono le informazioni necessarie per installare i collegamenti. Vedere Gruppo [tabelle informazioni programma e](program-information-tables-group.md) Modifica dei tasti di scelta rapida del programma di [installazione](editing-installer-shortcuts.md).

In questa sezione si aggiungono informazioni che specificano i collegamenti annunciati e non annunciati per l'Blocco note esempio.

Usare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella Collegamento.

[Tabella dei collegamenti](shortcut-table.md)



| Tasto di scelta rapida  | Directory\_ | Nome         | Componente\_ | Destinazione             | Argomenti | Descrizione | Tasto di scelta rapida | Icona\_         | IconIndex | ShowCmd | WkDir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sBaseball | MENUDIR     | Baseball.txt | Baseball    | Baseball           |           |             |        | orca \_icon.exe |           |         |       |
| sConcert  | MENUDIR     | Concert.txt  | Concerto     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sDance    | MENUDIR     | Dance.txt    | Danza       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sFootball | MENUDIR     | Football.txt | Calcio    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| sHelp     | MENUDIR     | Help.txt     | Help        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sJanuary  | MENUDIR     | January.txt  | January     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| sNewYears | MENUDIR     | NewYears.txt | NewYears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| sNotepad  | MENUDIR     | Redpark.exe  | Blocco note     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sReadme   | MENUDIR     | Readme.txt   | Blocco note     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

L'installazione di esempio deve abilitare l'installazione di un collegamento annunciato per la funzionalità Baseball. A questo scopo, è necessario specificare una chiave per la tabella Icona nella colonna \_ Icona della tabella Collegamento. Ai fini di questo esempio, è possibile copiare l'icona per l'editor di database Orca fornito con Windows Installer SDK. Esportare la [tabella Icon](icon-table.md) Orca.msi e quindi unire la tabella nel database MNP2000.msi usando Orca o un altro strumento di merge. Orca crea anche una directory denominata Icon nella directory contenente MNP2000.msi e aggiunge il file di dati binario dell'icona orca \_icon.exe.ibd. Vedere la colonna Dati nella tabella Icona. La tabella Icona completata dovrebbe essere simile alla seguente quando viene visualizzata in Orca.

[Tabella icona](icon-table.md)



| Nome           | Dati            |
|----------------|-----------------|
| orca \_icon.exe | \[Binary Data\] |



 

[Continua](specifying-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifica dei tasti di scelta rapida del programma di installazione](editing-installer-shortcuts.md)
</dt> </dl>

 

 



