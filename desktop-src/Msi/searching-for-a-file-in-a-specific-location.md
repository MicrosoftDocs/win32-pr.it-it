---
description: Durante un'installazione di Windows Installer, il programma di installazione può cercare un file in un percorso specifico nel sistema dell'utente.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Ricerca di un file in un percorso specifico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529497"
---
# <a name="searching-for-a-file-in-a-specific-location"></a>Ricerca di un file in un percorso specifico

**Per cercare un file in un percorso specifico in un sistema utente**

1.  Elencare la firma e il nome del file nella [tabella della firma](signature-table.md). I campi rimanenti di questo record possono essere null per cercare qualsiasi versione di MyApp.exe.

    [Tabella di firma](signature-table.md)

    

    | Firma          | Nome file            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Immettere la proprietà che verrà impostata dal programma di installazione se MyApp.exe è installato.

    [Tabella AppSearch](appsearch-table.md) (parziale)

    

    | Proprietà         | Firma          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Usare la [tabella DrLocator](drlocator-table.md). Immettere il percorso completo del file nel sistema utente nel campo percorso. Immettere il valore 0 nella colonna profondità per eseguire la ricerca nella cartella bin.

    [Tabella DrLocator](drlocator-table.md)

    

    | Firma          | Padre | Percorso                                                    | Profondità        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C: \\ programmi programmi per \\ prodotti \\ software \\ bin<br/> | 0<br/> |

    

     

4.  Includere l'azione AppSearch nella sequenza di azione. Se MyApp.exe è installato in C: \\ Program Files \\ prodotti prodotti \\ \\ bin, il programma di installazione imposta la proprietà MyApp sul percorso del file.

 

 




