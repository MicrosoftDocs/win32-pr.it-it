---
title: Attributi indicizzati (AD DS)
description: Gli attributi possono essere indicizzati. L'indicizzazione di un attributo può migliorare le prestazioni delle query per tale attributo.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Attributi indicizzati AD
- Attributi AD, indicizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299568"
---
# <a name="indexed-attributes-ad-ds"></a>Attributi indicizzati (AD DS)

Gli attributi possono essere indicizzati. L'indicizzazione di un attributo può migliorare le prestazioni delle query per tale attributo.

Gli attributi vengono indicizzati quando l'attributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) nella definizione dello schema dell'attributo presenta il bit meno significativo impostato su 1. Impostando il bit meno significativo della definizione dello schema dell'attributo **searchFlags** su 1, viene compilato dinamicamente un indice. Impostando il bit meno significativo della definizione dello schema dell'attributo **searchFlags** su 0, l'indice per l'attributo verrà rimosso. L'indice verrà compilato automaticamente da un thread in background sul controller di dominio.

Idealmente, gli attributi indicizzati devono essere a valore singolo con valori univoci distribuiti uniformemente nel set di istanze. Meno univoci i valori di un attributo sono, minore sarà l'efficacia dell'indice.

Gli attributi multivalore possono anche essere indicizzati, ma il costo per compilare l'indice per un attributo multivalore è maggiore in termini di archiviazione, aggiornamento e tempo di ricerca. Il requisito di univocità per una proprietà multivalore è identico a quello di una proprietà a valore singolo, più univoco è l'indice più efficiente.

Maggiore è l'attributo indicizzato di una classe, maggiore è il tempo necessario per creare nuove istanze della classe.

Gli indici si applicano agli attributi, non alle classi. Ovvero, quando un attributo viene contrassegnato come indicizzato, tutte le istanze dell'attributo vengono aggiunte all'indice e non solo alle istanze che sono membri di una classe specifica.

Per verificare che un server utilizzi un indice per elaborare una query, impostare il seguente valore del registro di sistema su un controller di dominio su 4. Eseguire quindi una query sul controller di dominio e cercare nel registro eventi della directory i dati sugli eventuali indici usati per elaborare la query.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

Per ulteriori informazioni sugli altri bit della proprietà [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) , vedere [caratteristiche degli attributi](characteristics-of-attributes.md).

 

 