---
description: Durante un'installazione di Windows Installer, il programma di installazione può cercare una directory e un file in tale directory.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Ricerca di una directory e di un file nella directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313790"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a>Ricerca di una directory e di un file nella directory

**Per cercare una directory e quindi un file nella directory**

1.  Eseguire prima la ricerca della directory.

    AppDir deve essere definito come la firma valida della directory. Se AppDir non è definito come una firma valida, AppSearch non dispone di una posizione per trovare il file, ad esempio, se la ricerca è per c: \\ MyDir \\MyApp.exe, appdir deve essere definito come c: \\ mydir. AppDir può essere definito includendo un record nella [tabella DrLocator](drlocator-table.md)o con un altro metodo. Nessun record è incluso nella [tabella delle firme](signature-table.md) per la ricerca nella directory. Per la ricerca di file, elencare la firma e il nome del file nella tabella della firma. I campi rimanenti di questo record possono essere null per cercare qualsiasi versione di MyApp.exe.

    [Tabella delle firme](signature-table.md) (parziale)

    

    | Firma          | File Name            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Usare la [tabella AppSearch](appsearch-table.md).

    Immettere la proprietà che verrà impostata dal programma di installazione se è installata la directory con la firma AppDir. Se il programma di installazione rileva che questa directory è installata, imposta MYDIR sul percorso della directory. Immettere la proprietà che verrà impostata dal programma di installazione se MyApp.exe è installato.

    [Tabella AppSearch](appsearch-table.md) (parziale)

    

    | Proprietà         | Firma          |
    |------------------|--------------------|
    | MYDIR<br/> | AppDir<br/>  |
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Usare la [tabella DrLocator](drlocator-table.md).

    Immettere nella colonna padre la firma, AppDir, definita come percorso della directory. Specificare nella colonna profondità il numero di livelli di sottodirectory in cui eseguire la ricerca in questa directory. AppDir deve essere definito come firma di directory. AppDir può essere definito includendo un record, come illustrato qui o da un altro metodo.

    [Tabella DrLocator](drlocator-table.md)

    

    | Firma | Padre | Percorso      | Profondità |
    |-----------|--------|-----------|-------|
    | AppDir    |        | C: \\ mydir | 0     |
    | AppFile   | AppDir |           | 0     |

    

     

4.  Includere l'azione AppSearch nella sequenza di azione.

    Se viene trovato MyApp.exe da installare in AppDir, il programma di installazione imposta la proprietà MYAPP sul percorso del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




