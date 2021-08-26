---
description: Durante un Windows installazione del programma di installazione, il programma di installazione può cercare un file in un percorso specifico nel sistema dell'utente.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Ricerca di un file in un percorso specifico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b131708e5f9ff37474864aa5d6ef13abcab8f0d162563ca810c7e31fe2c41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041151"
---
# <a name="searching-for-a-file-in-a-specific-location"></a>Ricerca di un file in un percorso specifico

**Per cercare un file in un percorso specifico in un sistema utente**

1.  Elencare la firma e il nome del file nella [tabella delle firme](signature-table.md). I campi rimanenti in questo record possono essere Null per cercare qualsiasi versione di MyApp.exe.

    [Tabella delle firme](signature-table.md)

    

    | Firma          | Nome file            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Immettere la proprietà che il programma di installazione deve impostare se MyApp.exe installato.

    [Tabella AppSearch](appsearch-table.md) (parziale)

    

    | Proprietà         | Firma          |
    |------------------|--------------------|
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Usare la [tabella DrLocator](drlocator-table.md). Immettere il percorso completo del file nel sistema utente nel campo Percorso. Immettere il valore 0 nella colonna Profondità per eseguire la ricerca nella cartella bin.

    [Tabella DrLocator](drlocator-table.md)

    

    | Firma          | Padre | Percorso                                                    | Profondità        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C: \\ Program Files \\ MyProducts \\ Projects \\ bin<br/> | 0<br/> |

    

     

4.  Includere l'azione AppSearch nella sequenza di azioni. Se MyApp.exe è installato nel bin C: Programmi MyProducts Projects, il programma di installazione imposta la proprietà \\ \\ \\ \\ MYAPP sul percorso del file.

 

 




