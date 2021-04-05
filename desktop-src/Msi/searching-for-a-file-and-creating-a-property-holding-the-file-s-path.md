---
description: Durante un'installazione di Windows Installer, il programma di installazione può cercare un file e creare una proprietà contenente il percorso del file.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Ricerca di un file e creazione di una proprietà che contiene il percorso del file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882709"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a>Ricerca di un file e creazione di una proprietà che contiene il percorso del file

**Per cercare un file e creare una proprietà contenente il percorso del file**

1.  Eseguire innanzitutto una ricerca del file elencando la firma e il nome del file nella [tabella della firma](signature-table.md).

    I campi rimanenti di questo record possono essere lasciati vuoti per specificare la ricerca di qualsiasi versione di MyApp.exe.

    [Tabella delle firme](signature-table.md) (parziale)

    

    | Firma          | Nome file            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Specificare quindi il percorso del file in cui viene eseguita la ricerca nella [tabella DrLocator](drlocator-table.md).

    Poiché AppFolder non è elencato nella [tabella Signature](signature-table.md), il programma di installazione determina che appfolder è una cartella anziché un file.

    [Tabella DrLocator](drlocator-table.md)

    

    | Firma            | Padre             | Percorso | Profondità |
    |----------------------|--------------------|------|-------|
    | AppFile<br/>   |                    |      |       |
    | AppFolder<br/> | AppFile<br/> |      |       |

    

     

3.  Infine, popolare la [tabella AppSearch](appsearch-table.md) in modo che l' [azione AppSearch](appsearch-action.md) restituisca il percorso di AppFolder.

    Dopo che il programma di installazione ha eseguito l'azione AppSearch, il valore di fileFolder è il percorso completo di AppFolder.

    [Tabella AppSearch](appsearch-table.md) (parziale)

    

    | Proprietà            | Firma            |
    |---------------------|----------------------|
    | MYFOLDER<br/> | AppFolder<br/> |

    

     

 

 




