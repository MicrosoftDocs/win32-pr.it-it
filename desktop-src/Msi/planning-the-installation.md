---
description: Quando l'installazione di un'applicazione esistente viene spostata nel programma di installazione di Windows da un'altra tecnologia di installazione, lo sviluppatore del programma di installazione può iniziare a creare un pacchetto del programma di installazione di Windows usando le immagini di file di origine e di destinazione dell'installazione esistente.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Pianificazione dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d406ec97fd5edb34468586eb9f707eff32b289df3dc88b803b8c55d4aad10cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042361"
---
# <a name="planning-the-installation"></a>Pianificazione dell'installazione

Quando l'installazione di un'applicazione esistente viene spostata nel programma di installazione di Windows da un'altra tecnologia di installazione, lo sviluppatore del programma di installazione può iniziare a creare un pacchetto del programma di installazione di Windows usando le immagini di file di origine e di destinazione dell'installazione esistente. Un piano dettagliato dell'organizzazione dei file e di altre risorse nell'origine e nella destinazione è anche un buon punto di partenza per lo sviluppo di un pacchetto per una nuova applicazione.

Il pacchetto di installazione di esempio accetta i file seguenti archiviati nel percorso di origine dell'applicazione e li installa nella destinazione nel computer dell'utente.



| File         | Descrizione                               | Percorso dell'origine                                    | Percorso della destinazione                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | File eseguibile dell'editor di testo.              | C: \\ Esempi \\ Blocco note \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| Readme.txt   | File informativo.                    | C: \\ Esempi \\ Blocco note \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| Help.txt     | Manuale della Guida                               | C: \\ Esempi \\ Blocco note \\Help.txt                     | Non installato. Eseguire sempre dall'origine.                  |
| Baseball.txt | Pianificazione della partita di baseball per l'anno 2000.     | C: \\ Esempio di Blocco note eventi \\ \\ \\Baseball.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| Football.txt | Pianificazione della partita di football per l'anno 2000.     | C: \\ Esempio di Blocco note eventi \\ \\ \\Football.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| Dance.txt    | Performance di musica classica per l'anno 2000.         | C: \\ Esempio di Blocco note eventi \\ \\ \\Dance.txt            | \[ProgramFilesFolder \] \\ Red Park \_ \\Dance.txt \\      |
| Concert.txt  | Musica prestazioni per l'anno 2000.         | C: \\ Esempio di Blocco note eventi \\ \\ \\Concert.txt          | \[ProgramFilesFolder \] \\ Red Park \_ \\Concert.txt \\    |
| January.txt  | Ammissioni nel gennaio dell'anno 2000.       | C: \\ Esempio di Blocco note gate \\ \\ \\January.txt            | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| NewYears.txt | Ammissioni il giorno di New Years Day of year 2000. | C: \\ Esempio di Blocco note \\ \\ \\ \\ gate-NewYears.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |



 

L'esempio scrive i valori seguenti nel Registro di sistema dell'utente in **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Blocco note \_ \\ \\ \\ Sample**.



| Nome             | Valore    |
|------------------|----------|
| lfCharSet        | 0        |
| lfClipPrecision  | 2        |
| lfFaceName       | Fixedsys |
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



 

Nell'esempio vengono installati i collegamenti seguenti. Uno di questi tasti di scelta rapida può essere selezionato durante l'installazione come collegamento annunciato in modo che l'utente possa installare su richiesta la funzionalità Baseball.



| Nome      | Percorso collegamento                         | Destinazione collegamento                                         |
|-----------|-------------------------------------------|---------------------------------------------------------|
| sNotepad  | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| sReadme   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| sHelp     | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[Esempio di ProgramFilesFolder \] \\ \\ Blocco note \\Help.txt       |
| sBaseball | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| sBall | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| sDance    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Dance.txt \\      |
| sConcert  | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Concert.txt \\    |
| sJanuary  | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| sNewYears | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |



 

Per riprodurre l'esempio, iniziare creando la struttura di directory di origine specificata nella prima tabella. È possibile creare una copia del file di Notepad.exe sistema e quindi rinominare questa copia Redpark.exe. Usare l'editor Blocco note per creare i file di testo rimanenti. La struttura di directory della destinazione, i valori del Registro di sistema e i collegamenti vengono aggiunti mediante la creazione del database di installazione.

[Continua](importing-a-blank-database.md)

 

 



