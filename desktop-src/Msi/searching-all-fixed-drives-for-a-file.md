---
description: Durante un'installazione di Windows Installer, il programma di installazione può eseguire ricerche in tutte le unità fisse per un file.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Ricerca in tutte le unità fisse per un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313793"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>Ricerca in tutte le unità fisse per un file

**Per eseguire la ricerca in tutte le unità fisse di un file**

1.  Immettere la firma e il nome del file nella [tabella della firma](signature-table.md). I campi rimanenti di questo record possono essere null per cercare qualsiasi versione di MyApp.exe.

    [Tabella delle firme](signature-table.md) (parziale)

    

    | Firma          | File Name            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Immettere la proprietà che verrà impostata dal programma di installazione se MyApp.exe è installato.

    [Tabella AppSearch](appsearch-table.md)

    

    | Proprietà         | Firma          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Usare la [tabella DrLocator](drlocator-table.md). Lasciare vuoti i campi padre e percorso per eseguire la ricerca in tutte le unità fisse del sistema utente. Specificare nella colonna profondità il numero di livelli di sottodirectory in cui eseguire la ricerca. Se ad esempio si imposta depth su 0, viene rilevato c: \\MyApp.exe, ma il file non viene rilevato con una profondità di 2, ad esempio: c: \\ Program Files \\ app \\MyApp.exe.

    [Tabella DrLocator](drlocator-table.md)

    

    | Firma          | Padre | Percorso | Profondità        |
    |--------------------|--------|------|--------------|
    | AppFile<br/> |        |      | 3<br/> |

    

     

4.  Includere l'azione AppSearch nella sequenza di azione. Se MyApp.exe è installato, il programma di installazione imposta la proprietà MYAPP sul percorso del file. Se il file è installato, MYAPP restituisce true in un'espressione condizionale.

 

 




