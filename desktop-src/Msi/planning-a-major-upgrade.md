---
description: Se Windows Installer viene utilizzato per l'installazione e la configurazione di un'applicazione, è possibile gestire gli aggiornamenti successivi dell'applicazione installando un pacchetto di aggiornamento.
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: Pianificazione di un aggiornamento principale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ca6b82e53a38dde8131525eb885a5f17603ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313808"
---
# <a name="planning-a-major-upgrade"></a>Pianificazione di un aggiornamento principale

Se Windows Installer viene utilizzato per l'installazione e la configurazione di un'applicazione, è possibile gestire gli aggiornamenti successivi dell'applicazione installando un pacchetto di aggiornamento. Gli sviluppatori del programma di installazione possono scegliere di creare un pacchetto di aggiornamento modificando il pacchetto di installazione originale. Questo approccio è illustrato nell'esempio di aggiornamento seguente.

L'installazione del prodotto originale, MNP2000, seguito dall'installazione del pacchetto di aggiornamento fornisce all'utente i file seguenti richiesti dal prodotto MNP2001.



| File          | Descrizione                                                    | Percorso dell'origine                                    | Percorso della destinazione                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | File eseguibile dell'editor di testo. Non modificato rispetto ai prodotti precedenti. | C: \\ \\ blocco note di esempio \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red \_ Park \\Redpark.exe          |
| Readme.txt    | Un file di informazioni. Non modificato rispetto ai prodotti precedenti.         | C: \\ \\ blocco note di esempio \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red \_ Park \\Readme.txt           |
| Help.txt      | Manuale della guida. Non modificato rispetto ai prodotti precedenti.                 | C: \\ \\ blocco note di esempio \\Help.txt                     | Non installato. Eseguire sempre dall'origine.                  |
| Baseba01.txt  | Pianificazione della partita di baseball per l'anno 2001.                          | C: \\ \\ eventi del blocco note di esempio \\ \\Baseba01.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Baseball.txt |
| Footba01.txt  | La pianificazione del gioco Football per l'anno 2001.                          | C: \\ \\ eventi del blocco note di esempio \\ \\Footba01.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Football.txt |
| Basket01.txt  | Pianificazione del gioco basket per l'anno 2001.                        | C: \\ \\ eventi del blocco note di esempio \\ \\Basket01.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Basket01.txt |
| Dance01.txt   | Performance Dance per l'anno 2001.                              | C: \\ \\ eventi del blocco note di esempio \\ \\Dance01.txt          | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Dance.txt      |
| Concert01.txt | Prestazioni di musica per l'anno 2001.                              | C: \\ \\ eventi del blocco note di esempio \\ \\Concer01.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Concert.txt    |
| Opera01.txt   | Performance opera per l'anno 2001.                              | C: \\ \\ eventi del blocco note di esempio \\ \\Opera01.txt          | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Opera01.txt    |
| Januar01.txt  | Ricoveri nel gennaio dell'anno 2001.                            | C: controllo del \\ \\ blocco note di esempio \\ \\Januar01.txt           | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\January.txt    |
| NewYea01.txt  | Ricoveri il giorno dell'anno 2001 del nuovo anno.                      | C: \\ esempio di \\ blocco note \\ Gate \\ \\NewYea01.txt | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\NewYears.txt   |
| Memori01.txt  | Ricoveri sul giorno dell'anno Memorial 2001.                       | C: \\ esempio di \\ blocco note \\ Gate \\ \\Memori01.txt | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\Memori01.txt   |



 

Con l'installazione del pacchetto di aggiornamento vengono rimosse tutte le funzionalità installate con il prodotto originale che non vengono utilizzate dal prodotto aggiornato.

Ad esempio, quando si esegue l'aggiornamento da MNP2000, l'installazione dell'aggiornamento rimuove i file seguenti dal computer dell'utente:

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

L'installazione del pacchetto di aggiornamento scrive i valori seguenti nel registro di sistema dell'utente in:

**HKEY \_ \_** Esempio di \\  \\  \\ **blocco note** software del computer locale Microsoft



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



 

L'aggiornamento aggiorna i collegamenti obsoleti ai collegamenti seguenti. Uno di questi tasti di scelta rapida può essere selezionato durante l'installazione come collegamento annunciato, in modo che l'utente possa installare su richiesta la funzionalità di baseball.



| Nome        | Percorso collegamento                         | Destinazione collegamento                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| sNotepad    | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\Redpark.exe            |
| sReadme     | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\Readme.txt             |
| sHelp       | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[\] \\ \\Help.txt blocco note di esempio ProgramFilesFolder \\         |
| sBaseball   | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Baseba01.txt   |
| sFootball   | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Footba01.txt   |
| sBasketball | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sports \\Basketba01.txt |
| sDance      | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Dance01.txt      |
| sConcert    | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Concer01.txt     |
| sOpera      | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Opera01.txt      |
| sJanuary    | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\Januar01.txt     |
| sNewYears   | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\NewYea01.txt     |
| sMemorial   | \[Menu di ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Gate \\Memori01.txt     |



 

Quando un utente disinstalla il pacchetto di aggiornamento, Windows Installer rimuove completamente tutte le versioni del prodotto dal computer dell'utente. L'utente non viene lasciato con alcuna parte di MNP2000 o MNP2001.

[Continua](importing-original-installation-database.md)

 

 



