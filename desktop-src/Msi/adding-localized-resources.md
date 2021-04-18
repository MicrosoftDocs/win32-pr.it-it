---
description: A seconda dell'applicazione, la localizzazione potrebbe richiedere la modifica o l'aggiunta di risorse, ad esempio file o chiavi del registro di sistema.
ms.assetid: f5af0ecd-cb57-4858-88b4-4608893004f6
title: Aggiunta di risorse localizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7646499e4bb48e3df9fc1527bff1273e6b6784bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311080"
---
# <a name="adding-localized-resources"></a>Aggiunta di risorse localizzate

A seconda dell'applicazione, la localizzazione potrebbe richiedere la modifica o l'aggiunta di risorse, ad esempio file o chiavi del registro di sistema. Per la localizzazione dell'applicazione di esempio MNP2000 è necessario aggiungere un file aggiuntivo al pacchetto, Fre.txt e le versioni in francese di due file esistenti: Help.txt e Readme.txt.

In questo caso, la procedura consigliata consiste nel localizzare il pacchetto in modo che le versioni in inglese e in francese possano coesistere nel computer. Ciò include mai l'installazione di due file diversi con nomi di file identici nella stessa directory. Poiché Help.txt e Readme.txt hanno nomi di file identici nelle versioni in due lingue, il pacchetto francese dovrebbe installare questi file in una directory diversa da quella inglese.

Il pacchetto francese installa Help.txt in una nuova sottodirectory della cartella RedPark, francese. Poiché l'aggiunta di Fre.txt aggiunge una risorsa al componente della guida originale, il codice componente per il componente della guida deve essere diverso nei pacchetti francese e inglese. Vedere le regole per i codici componente nella [modifica del codice componente](changing-the-component-code.md).

Il pacchetto francese installa Readme.txt nella directory francese, in modo che il nome file non possa entrare in conflitto con la versione in lingua inglese. Il file Readme.txt viene installato con il componente blocco note, ma le regole dei componenti non richiedono la modifica del codice componente. In questo esempio, il codice componente del blocco note non deve essere modificato perché RedPark.exe, i valori del registro di sistema specificati nella [tabella del registro di sistema](registry-table.md), sono condivisi da entrambe le versioni del linguaggio. Vedere [aggiunta delle informazioni del registro di sistema](adding-registry-information.md).

Rimuovere le versioni in lingua inglese di Help.txt e Readme.txt dai file di origine e aggiungere le nuove versioni in francese di Help.txt, Readme.txt e Fre.txt. Il pacchetto localizzato deve eseguire il mapping dell'installazione dei file dall'origine alla destinazione, come indicato di seguito.



| File        | Descrizione                  | Percorso dell'origine                   | Percorso della destinazione                                         |
|-------------|------------------------------|----------------------------------|--------------------------------------------------------|
| Redpark.exe | File eseguibile dell'editor di testo. | C: \\ \\ blocco note di esempio \\Redpark.exe | \[ProgramFilesFolder \] \\ Red \_ Park \\ francese \\Redpark.exe |
| Readme.txt  | Un file informativo.       | C: \\ \\ blocco note di esempio \\Readme.txt  | \[ProgramFilesFolder \] \\ Red \_ Park \\ francese \\Readme.txt  |
| Help.txt    | Manuale della Guida                  | C: \\ \\ blocco note di esempio \\Help.txt    | \[ProgramFilesFolder \] \\ Red \_ Park \\ francese \\Help.txt    |
| Fre.txt     | Elenco telefonico                   | C: \\ \\ blocco note di esempio \\Fre.txt     | \[ProgramFilesFolder \] \\ Red \_ Park \\ francese \\Fre.txt     |



 

Utilizzare l'editor di database Orca fornito con l'SDK o un altro editor per aprire la tabella di directory e aggiungere un record per l'installazione della nuova directory, francese.

[Tabella directory](directory-table.md)



| Directory                                        | \_Padre directory                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | Arts: eventi       |
| HOLDIR                                           | MONDIno                                           | .: Festività        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIno                                           | NOTEPADDIR                                       | Cancello              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | Red \_ Park: blocco note |
| SPORTDIR                                         | NOTEPADDIR                                       | Sport: eventi     |
| FRENCHDIR                                        | NOTEPADDIR                                       | Francese:.          |



 

Utilizzare l'editor di tabelle per modificare il ComponentId del componente della Guida in MNPFren.msi in un nuovo GUID.

[Tabella componenti](component-table.md)



| Componente | ComponentId                            | Directory\_ | Attributi | Condizione | KeyPath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Baseball  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concerto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Concert.txt  |
| Danza     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Dance.txt    |
| Calcio  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Help      | {9ED21229-FE3C-4FE9-B01D-57E00224FD0B} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIno      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Blocco note   | {19BED232-30AB-11D3-91D3-00C04FD70856} | FRENCHDIR   | 2          |           | Redpark.exe  |



 

Utilizzare l'Editor tabelle per aggiungere Fre.txt alla [tabella file](file-table.md) di MNPFren.msi. Immettere LANGID per French nel campo Language per i file localizzati. Tutti gli altri elementi sono uguali, se il file da installare ha una lingua diversa da quella del file nel computer, il programma di installazione predilige il file con la lingua corrispondente al prodotto da installare. I file indipendenti dalla lingua vengono considerati come un altro linguaggio, in modo che il prodotto da installare venga nuovamente favorito. Per altre informazioni, vedere [regole di controllo delle versioni dei file](file-versioning-rules.md).

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



 

Questa operazione completa la localizzazione degli esempi.

 

 



