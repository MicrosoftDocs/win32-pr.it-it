---
description: Durante un Windows installazione del programma di installazione, il programma di installazione può cercare un file e creare una proprietà contenente il percorso del file.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Ricerca di un file e creazione di una proprietà contenente il percorso del file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d1315616c6d2ea24052ddad85c005d53716f8b130f4aa2d23d69754c946416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041141"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a>Ricerca di un file e creazione di una proprietà contenente il percorso del file

**Per cercare un file e creare una proprietà contenente il percorso del file**

1.  Per prima cosa, cercare il file elencando la firma e il nome del file nella [tabella delle firme](signature-table.md).

    I campi rimanenti di questo record possono essere lasciati vuoti per specificare una ricerca di qualsiasi versione MyApp.exe.

    [Tabella delle firme](signature-table.md) (parziale)

    

    | Firma          | Nome file            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Specificare quindi il percorso del file da cercare nella [tabella DrLocator](drlocator-table.md).

    Poiché AppFolder non è elencato nella [tabella delle](signature-table.md)firme, il programma di installazione determina che AppFolder è una cartella anziché un file.

    [Tabella DrLocator](drlocator-table.md)

    

    | Firma            | Padre             | Percorso | Profondità |
    |----------------------|--------------------|------|-------|
    | AppFile<br/>   |                    |      |       |
    | AppFolder<br/> | AppFile<br/> |      |       |

    

     

3.  Infine, popolare la tabella [AppSearch in](appsearch-table.md) modo che l'azione [AppSearch](appsearch-action.md) restituisca il percorso di AppFolder.

    Dopo che il programma di installazione ha eseguito l'azione AppSearch, il valore di MYFOLDER è il percorso completo di AppFolder.

    [Tabella AppSearch](appsearch-table.md) (parziale)

    

    | Proprietà            | Firma            |
    |---------------------|----------------------|
    | CARTELLA<br/> | AppFolder<br/> |

    

     

 

 




