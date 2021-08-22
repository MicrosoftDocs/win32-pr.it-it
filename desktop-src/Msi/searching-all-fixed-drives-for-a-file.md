---
description: Durante un Windows installazione del programma di installazione, il programma di installazione può cercare un file in tutte le unità fisse.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Ricerca di un file in tutte le unità fisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d460cd55fe54a98c6a02e23e49af9ea9838c7651262fa03f868bdb76acc2d506
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041251"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>Ricerca di un file in tutte le unità fisse

**Per cercare un file in tutte le unità fisse**

1.  Immettere la firma e il nome del file nella [tabella delle firme.](signature-table.md) I campi rimanenti in questo record possono essere Null per cercare qualsiasi versione di MyApp.exe.

    [Tabella delle firme](signature-table.md) (parziale)

    

    | Firma          | File Name            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Immettere la proprietà che il programma di installazione deve impostare se MyApp.exe installato.

    [Tabella AppSearch](appsearch-table.md)

    

    | Proprietà         | Firma          |
    |------------------|--------------------|
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Usare la [tabella DrLocator](drlocator-table.md). Lasciare vuoti i campi Padre e Percorso per cercare tutte le unità fisse del sistema utente. Specificare nella colonna Profondità il numero di livelli di sottodirectory in cui eseguire la ricerca. Ad esempio, l'impostazione di Depth su 0 rileva c:MyApp.exe, ma non rileva il file a una profondità \\ di 2, ad esempio: c: \\ Programmi \\ MyApps \\MyApp.exe.

    [Tabella DrLocator](drlocator-table.md)

    

    | Firma          | Padre | Percorso | Profondità        |
    |--------------------|--------|------|--------------|
    | AppFile<br/> |        |      | 3<br/> |

    

     

4.  Includere l'azione AppSearch nella sequenza di azioni. Se MyApp.exe installato, il programma di installazione imposta la proprietà MYAPP sul percorso del file. Se il file è installato, MYAPP restituisce True in un'espressione condizionale.

 

 




