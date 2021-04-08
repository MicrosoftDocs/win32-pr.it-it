---
description: Durante un'installazione di Windows Installer, il programma di installazione può cercare una voce del registro di sistema e creare una proprietà contenente il valore del registro di sistema.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Ricerca di una voce del registro di sistema e creazione di una proprietà contenente il valore del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878682"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a>Ricerca di una voce del registro di sistema e creazione di una proprietà contenente il valore del registro di sistema

**Per cercare una voce del registro di sistema e creare una proprietà contenente il valore di tale file**

1.  Non aggiungere la firma alla tabella della [firma](signature-table.md) o alla [tabella CompLocator](complocator-table.md). Se la firma di un file è elencata nella [tabella AppSearch](appsearch-table.md) e non è elencata nelle tabelle Signature o CompLocator, il programma di installazione cerca nella [tabella RegLocator](reglocator-table.md).

2.  Consente di specificare la voce del registro di sistema da cercare nella [tabella RegLocator](reglocator-table.md). Se la firma è assente dalla [tabella di firma](signature-table.md) e il valore della colonna del tipo è **msidbLocatorTypeRawValue**, si presuppone che la ricerca sia per il nome della chiave del registro di sistema a cui punta la tabella RegLocator.

    [Tabella RegLocator](reglocator-table.md) (parziale)

    

    | Firma\_         | Radice         | Codice                                                           | Nome                  | Tipo                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | AppValue<br/> | 2<br/> | **Software** \\ di **Microsoft** \\ **MyApp**<br/> <br/> | **Myname**<br/> | **msidbLocatorTypeRawValue**<br/> |

    

     

3.  Infine, popolare la [tabella AppSearch](appsearch-table.md) in modo che l' [azione AppSearch](appsearch-action.md) restituisce il valore di AppValue. Dopo che il programma di installazione ha eseguito l'azione AppSearch, il valore di MYREGVAL corrisponde al valore di AppValue.

    [Tabella AppSearch](appsearch-table.md) (parziale)

    

    | Proprietà            | Firma           |
    |---------------------|---------------------|
    | MYREGVAL<br/> | AppValue<br/> |

    

     

 

 




