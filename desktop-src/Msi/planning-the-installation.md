---
description: Quando l'installazione di un'applicazione esistente viene spostata in Windows Installer da un'altra tecnologia di installazione, lo sviluppatore del programma di installazione può iniziare a creare un pacchetto di Windows Installer utilizzando le immagini dei file di origine e di destinazione dell'installazione esistente.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Pianificazione dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb98368c5c5c8e13a8f9b03a44805a8cff6e517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882729"
---
# <a name="planning-the-installation"></a>Pianificazione dell'installazione

Quando l'installazione di un'applicazione esistente viene spostata in Windows Installer da un'altra tecnologia di installazione, lo sviluppatore del programma di installazione può iniziare a creare un pacchetto di Windows Installer utilizzando le immagini dei file di origine e di destinazione dell'installazione esistente. Un piano dettagliato del modo in cui i file e altre risorse sono organizzati nell'origine e nella destinazione è anche un valido punto di partenza per lo sviluppo di un pacchetto per una nuova applicazione.

Il pacchetto di installazione di esempio utilizza i file seguenti archiviati nel percorso di origine dell'applicazione e li installa nella destinazione nel computer dell'utente.



| File         | Descrizione                               | Percorso dell'origine                                    | Percorso della destinazione                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | File eseguibile dell'editor di testo.              | C: \\ \\ blocco note di esempio \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red \_ Park \\Redpark.exe          |
| Readme.txt   | Un file informativo.                    | C: \\ \\ blocco note di esempio \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red \_ Park \\Readme.txt           |
| Help.txt     | Manuale della Guida                               | C: \\ \\ blocco note di esempio \\Help.txt                     | Non installato. Eseguire sempre dall'origine.                  |
| Baseball.txt | Pianificazione della partita di baseball per l'anno 2000.     | C: \\ \\ eventi del blocco note di esempio \\ \\Baseball.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Baseball.txt |
| Football.txt | La pianificazione del gioco Football per l'anno 2000.     | C: \\ \\ eventi del blocco note di esempio \\ \\Football.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Football.txt |
| Dance.txt    | Performance Dance per l'anno 2000.         | C: \\ \\ eventi del blocco note di esempio \\ \\Dance.txt            | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Dance.txt      |
| Concert.txt  | Prestazioni di musica per l'anno 2000.         | C: \\ \\ eventi del blocco note di esempio \\ \\Concert.txt          | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Concert.txt    |
| January.txt  | Ricoveri nel gennaio dell'anno 2000.       | C: controllo del \\ \\ blocco note di esempio \\ \\January.txt            | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\January.txt    |
| NewYears.txt | Ricoveri il giorno dell'anno 2000 del nuovo anno. | C: \\ esempio di \\ blocco note \\ Gate \\ \\NewYears.txt | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\NewYears.txt   |



 

Nell'esempio vengono scritti i valori seguenti nel registro di sistema dell'utente in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ notepad Sample**.



| Nome             | Valore    |
|------------------|----------|
| lfCharSet        | 0        |
| lfClipPrecision  | 2        |
| lfFaceName       | FixedSys |
| lfItalic         | 0        |
| lfOrientation    | 0        |
| lfOutPrecision   | 1        |
| fSavePageSetting | 0        |
| lfPitchAndFamily | 49       |
| iPointSize       | 120      |
| lfQuality        | 2        |
| lfStrikeOut      | 0        |
| lfWeight         | 400      |
| fWrap            | 0        |



 

Nell'esempio vengono installati i collegamenti seguenti. Uno di questi tasti di scelta rapida può essere selezionato durante l'installazione come collegamento annunciato, in modo che l'utente possa installare su richiesta la funzionalità di baseball.



| Nome      | Percorso collegamento                         | Destinazione collegamento                                         |
|-----------|-------------------------------------------|---------------------------------------------------------|
| sNotepad  | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\Redpark.exe          |
| sReadme   | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\Readme.txt           |
| sHelp     | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[\] \\ \\Help.txt blocco note di esempio ProgramFilesFolder \\       |
| sBaseball | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Baseball.txt |
| sFootball | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Football.txt |
| sDance    | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Dance.txt      |
| sConcert  | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Concert.txt    |
| sJanuary  | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\January.txt    |
| sNewYears | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\NewYears.txt   |



 

Per riprodurre l'esempio, iniziare creando la struttura della directory di origine specificata nella prima tabella. È possibile creare una copia del file di Notepad.exe del sistema e rinominare questa copia Redpark.exe. Utilizzare l'editor del blocco note per creare i file di testo rimanenti. La struttura di directory della destinazione, i valori del registro di sistema e i collegamenti vengono aggiunti mediante la creazione del database di installazione.

[Continua](importing-a-blank-database.md)

 

 



