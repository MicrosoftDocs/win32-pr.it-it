---
description: A seconda dell'applicazione, la localizzazione può richiedere la modifica o l'aggiunta di risorse come file o chiavi del Registro di sistema.
ms.assetid: f5af0ecd-cb57-4858-88b4-4608893004f6
title: Aggiunta di risorse localizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de37bfd3c216018f6c4a6f6866206020576153e55383a9d6b36e67533bbb3b6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829241"
---
# <a name="adding-localized-resources"></a>Aggiunta di risorse localizzate

A seconda dell'applicazione, la localizzazione può richiedere la modifica o l'aggiunta di risorse come file o chiavi del Registro di sistema. La localizzazione dell'applicazione di esempio MNP2000 richiede l'aggiunta di un file aggiuntivo al pacchetto Fre.txt e alle versioni in francese di due file esistenti: Help.txt e Readme.txt.

La procedura consigliata in questo caso consiste nel localizzare il pacchetto in modo che le versioni inglese e francese possano coesistere in modo sicuro nel computer. Ciò include l'installazione di due file diversi con nomi di file identici nella stessa directory. Poiché Help.txt e Readme.txt hanno nomi di file identici nelle due versioni linguistiche, il pacchetto francese deve installare questi file in una directory diversa da quella inglese.

Il pacchetto in francese Help.txt in una nuova sottodirectory della cartella RedPark, in francese. Poiché l'aggiunta di Fre.txt una risorsa al componente della Guida originale, il codice del componente della Guida deve essere diverso nei pacchetti francese e inglese. Vedere le regole per i codici dei componenti in [Modifica del codice componente](changing-the-component-code.md).

Il pacchetto francese installa Readme.txt nella directory francese in modo che questo nome file non possa entrare in conflitto con la versione inglese. Il file Readme.txt installato con il componente Blocco note, ma le regole del componente non richiedono la modifica del codice del componente. In questo esempio, il codice del componente di Blocco note non deve essere modificato perché RedPark.exe, i valori del Registro di sistema specificati nella tabella Del Registro di sistema [sono](registry-table.md)condivisi da entrambe le versioni del linguaggio. Vedere [Aggiunta di informazioni del Registro di sistema](adding-registry-information.md).

Rimuovere le versioni in lingua inglese di Help.txt e Readme.txt dai file di origine e aggiungere le nuove versioni in francese di Help.txt, Readme.txt e Fre.txt. Il pacchetto localizzato deve eseguire il mapping dell'installazione dei file dall'origine alla destinazione come indicato di seguito.



| File        | Descrizione                  | Percorso dell'origine                   | Percorso di destinazione                                         |
|-------------|------------------------------|----------------------------------|--------------------------------------------------------|
| Redpark.exe | File eseguibile dell'editor di testo. | C: \\ Esempio \\ Blocco note \\Redpark.exe | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Redpark.exe |
| Readme.txt  | Un file informativo.       | C: \\ Esempio \\ Blocco note \\Readme.txt  | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Readme.txt  |
| Help.txt    | Manuale della Guida                  | C: \\ Esempio \\ Blocco note \\Help.txt    | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Help.txt    |
| Fre.txt     | Telefono elenco                   | C: \\ Esempio \\ Blocco note \\Fre.txt     | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Fre.txt     |



 

Usare l'editor di database Orca fornito con l'SDK o un altro editor per aprire la tabella Directory e aggiungere un record per l'installazione della nuova directory, il francese.

[Tabella directory](directory-table.md)



| Directory                                        | Padre \_ della directory                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**Targetdir**](targetdir.md)                   |                                                  | SourceDir         |
| [**Cartella ProgramFilesFolder**](programfilesfolder.md) | [**Targetdir**](targetdir.md)                   | .                 |
| ARTODIR                                          | NOTEPADDIR                                       | Arti:Eventi       |
| HOLDIR                                           | MONDIR                                           | .:Holidays        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIR                                           | NOTEPADDIR                                       | Cancello              |
| NOTEPADDIR                                       | [**Cartella ProgramFilesFolder**](programfilesfolder.md) | Red \_ Park:Blocco note |
| SPORTDIR                                         | NOTEPADDIR                                       | Sport:Eventi     |
| FRENCHDIR                                        | NOTEPADDIR                                       | Francese:.          |



 

Usare l'editor di tabelle per modificare ComponentId del componente Guida in MNPFren.msi in un nuovo GUID.

[Tabella dei componenti](component-table.md)



| Componente | Componentid                            | Directory\_ | Attributi | Condition | Percorso chiave      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Baseball  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concerto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTODIR     | 2          |           | Concert.txt  |
| Danza     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTODIR     | 2          |           | Dance.txt    |
| Calcio  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Help      | {9ED21229-FE3C-4FE9-B01D-57E00224FD0B} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Blocco note   | {19BED232-30AB-11D3-91D3-00C04FD70856} | FRENCHDIR   | 2          |           | Redpark.exe  |



 

Usare l'editor di tabelle per Fre.txt alla tabella [File](file-table.md) di MNPFren.msi. Immettere LANGID per il francese nel campo Lingua per i file localizzati. Tutti gli altri elementi sono uguali, se il file da installare ha una lingua diversa rispetto al file nel computer, il programma di installazione preferisce il file con la lingua corrispondente al prodotto installato. I file indipendenti dalla lingua vengono considerati solo come un'altra lingua, quindi il prodotto da installare è di nuovo preferito. Per altre informazioni, vedere [Regole di controllo delle versioni dei file.](file-versioning-rules.md)

[Tabella file](file-table.md)



| File         | Componente\_ | FileName     | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Baseball    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Concerto     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Danza       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Calcio    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Help        | Help.txt     | 1000     |         | 1036     | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Blocco note     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Blocco note     | Readme.txt   | 1000     |         | 1036     | 0          | 1        |
| Fre.txt      | Help        | Fre.txt      | 1000     |         | 1036     | 0          | 1        |



 

Questa operazione completa la localizzazione di esempio.

 

 



