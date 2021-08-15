---
description: Se Windows programma di installazione viene usato per l'installazione e l'installazione di un'applicazione, gli aggiornamenti successivi di tale applicazione possono essere gestiti installando un pacchetto di aggiornamento.
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: Pianificazione di un aggiornamento principale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07ece8acf0dbc37ecdfddaa3505e5e54a283a8e8efd7b4eb0dc1a0a365a461e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377372"
---
# <a name="planning-a-major-upgrade"></a>Pianificazione di un aggiornamento principale

Se Windows programma di installazione viene usato per l'installazione e l'installazione di un'applicazione, gli aggiornamenti successivi di tale applicazione possono essere gestiti installando un pacchetto di aggiornamento. Gli sviluppatori del programma di installazione possono scegliere di creare un pacchetto di aggiornamento modificando il pacchetto di installazione originale. Questo approccio è illustrato nell'esempio di aggiornamento seguente.

L'installazione del prodotto originale, MNP2000, seguita dall'installazione del pacchetto di aggiornamento fornisce all'utente i file seguenti richiesti dal prodotto MNP2001.



| File          | Descrizione                                                    | Percorso dell'origine                                    | Percorso della destinazione                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | File eseguibile dell'editor di testo. Invariato rispetto ai prodotti precedenti. | C: \\ Esempi \\ Blocco note \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| Readme.txt    | File di informazioni. Invariato rispetto ai prodotti precedenti.         | C: \\ Esempi \\ Blocco note \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| Help.txt      | Manuale della Guida. Invariato rispetto ai prodotti precedenti.                 | C: \\ Esempi \\ Blocco note \\Help.txt                     | Non installato. Eseguire sempre dall'origine.                  |
| Baseba01.txt  | Pianificazione della partita di baseball per l'anno 2001.                          | C: \\ Esempio di Blocco note eventi \\ \\ \\Baseba01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| Footba01.txt  | Pianificazione della partita di football per l'anno 2001.                          | C: \\ Esempio di Blocco note eventi \\ \\ \\Footba01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| Basket01.txt  | Pianificazione dei giochi di basket per l'anno 2001.                        | C: \\ Esempio di Blocco note eventi \\ \\ \\Basket01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Basket01.txt |
| Dance01.txt   | Performance di musica classica per l'anno 2001.                              | C: \\ Esempio di Blocco note eventi \\ \\ \\Dance01.txt          | \[ProgramFilesFolder \] \\ Red Park \_ \\Dance.txt \\      |
| Concert01.txt | Musica prestazioni per l'anno 2001.                              | C: \\ Esempio di Blocco note eventi \\ \\ \\Concer01.txt         | \[ProgramFilesFolder \] \\ Red Park \_ \\Concert.txt \\    |
| Opera01.txt   | Prestazioni dell'opera per l'anno 2001.                              | C: \\ Esempio di Blocco note eventi \\ \\ \\Opera01.txt          | \[ProgramFilesFolder \] \\ Red Park \_ \\Opera01.txt \\    |
| Januar01.txt  | Ammissioni nel gennaio 2001.                            | C: \\ Esempio di Blocco note gate \\ \\ \\Januar01.txt           | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| NewYea01.txt  | Ammissioni il giorno di New Years Day of year 2001.                      | C: \\ Esempio di Blocco note \\ \\ \\ \\ gate-NewYea01.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |
| Memori01.txt  | Ammissioni il giorno dell'anno 2001.                       | C: \\ Esempio di Blocco note \\ \\ \\ \\ gate-Memori01.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Memori01.txt   |



 

L'installazione del pacchetto di aggiornamento rimuove tutte le funzionalità installate con il prodotto originale che non vengono utilizzate dal prodotto aggiornato.

Ad esempio, quando si esegue l'aggiornamento da MNP2000, l'installazione dell'aggiornamento rimuove i file seguenti dal computer dell'utente:

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

L'installazione del pacchetto di aggiornamento scrive i valori seguenti nel Registro di sistema dell'utente in :

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Blocco note Sample**



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



 

L'aggiornamento aggiorna i collegamenti precedenti ai collegamenti seguenti. Uno di questi tasti di scelta rapida può essere selezionato durante l'installazione come collegamento annunciato in modo che l'utente possa installare su richiesta la funzionalità Baseball.



| Nome        | Percorso collegamento                         | Destinazione collegamento                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| sNotepad    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe            |
| sReadme     | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt             |
| sHelp       | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[Esempio di ProgramFilesFolder \] \\ \\ Blocco note \\Help.txt         |
| sBaseball   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseba01.txt   |
| sBall   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Footba01.txt   |
| sBasketball | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Basketba01.txt |
| sDance      | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Dance01.txt \\      |
| sConcert    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Concer01.txt \\     |
| sOpera      | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Opera01.txt \\      |
| sJanuary    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Januar01.txt     |
| sNewYears   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYea01.txt     |
| sMemorial   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Memori01.txt     |



 

Quando un utente disinstalla il pacchetto di aggiornamento, Windows installer rimuove completamente tutte le versioni del prodotto dal computer dell'utente. All'utente non viene lasciata alcuna parte di MNP2000 o MNP2001.

[Continua](importing-original-installation-database.md)

 

 



