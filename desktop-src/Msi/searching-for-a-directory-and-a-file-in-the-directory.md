---
description: Durante un Windows installazione del programma di installazione, il programma di installazione può cercare una directory e un file in tale directory.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Ricerca di una directory e di un file nella directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e857460dc58fa5fded802cb53b9ae6a558e5a27426baef87be9f561fa35fe6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041181"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a>Ricerca di una directory e di un file nella directory

**Per cercare una directory e quindi un file in tale directory**

1.  Cercare prima di tutto la directory.

    AppDir deve essere definito come firma valida della directory. Se AppDir non è definito come firma valida, AppSearch non ha una posizione in cui trovare il file, ad esempio, se la ricerca è per c: MyDirMyApp.exe, AppDir deve essere definito come \\ \\ c: \\ MyDir. AppDir può essere definito includendo un record nella [tabella DrLocator](drlocator-table.md)o con un altro metodo. Nella tabella delle firme non è incluso [alcun](signature-table.md) record per la ricerca nella directory. Per la ricerca di file, elencare la firma e il nome del file nella tabella delle firme. I campi rimanenti in questo record possono essere Null per cercare qualsiasi versione di MyApp.exe.

    [Tabella delle firme](signature-table.md) (parziale)

    

    | Firma          | File Name            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Usare la [tabella AppSearch](appsearch-table.md).

    Immettere la proprietà che il programma di installazione deve impostare se è installata la directory con la firma AppDir. Se il programma di installazione rileva che questa directory è installata, imposta MYDIR sul percorso della directory. Immettere la proprietà che il programma di installazione deve impostare se MyApp.exe installato.

    [Tabella AppSearch](appsearch-table.md) (parziale)

    

    | Proprietà         | Firma          |
    |------------------|--------------------|
    | MYDIR<br/> | Appdir<br/>  |
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Usare la [tabella DrLocator](drlocator-table.md).

    Immettere nella colonna Padre la firma AppDir, definita come percorso della directory. Specificare nella colonna Profondità il numero di livelli di sottodirectory in cui eseguire la ricerca in questa directory. AppDir deve essere definito come firma della directory. AppDir può essere definito includendo un record come illustrato qui o con un altro metodo.

    [Tabella DrLocator](drlocator-table.md)

    

    | Firma | Padre | Percorso      | Profondità |
    |-----------|--------|-----------|-------|
    | Appdir    |        | C: \\ MyDir | 0     |
    | AppFile   | Appdir |           | 0     |

    

     

4.  Includere l'azione AppSearch nella sequenza di azioni.

    Se MyApp.exe viene trovato installato in AppDir, il programma di installazione imposta la proprietà MYAPP sul percorso del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca di applicazioni, file, voci del Registro di sistema o .ini file esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




