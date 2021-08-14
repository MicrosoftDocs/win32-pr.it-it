---
title: Attributi indicizzati (Ad DS)
description: Gli attributi possono essere indicizzati. L'indicizzazione di un attributo può migliorare le prestazioni delle query per tale attributo.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Attributi indicizzati AD
- Attributi AD , indicizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabd205fea66b198096a9a9427822eb4ba0ccb609fb3e6fef0854fa91848371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187585"
---
# <a name="indexed-attributes-ad-ds"></a>Attributi indicizzati (Ad DS)

Gli attributi possono essere indicizzati. L'indicizzazione di un attributo può migliorare le prestazioni delle query per tale attributo.

Un attributo viene indicizzato quando l'attributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) nella definizione dello schema dell'attributo ha il bit meno significativo impostato su 1. Se si imposta il bit meno significativo della definizione dello schema **dell'attributo searchFlags** su 1, verrà compilato dinamicamente un indice. Se si imposta il bit meno significativo della definizione dello schema dell'attributo **searchFlags** su 0, l'indice dell'attributo verrà rimosso. L'indice verrà compilato automaticamente da un thread in background nel controller di dominio.

Idealmente, gli attributi indicizzati devono essere a valore singolo con valori altamente univoci distribuiti uniformemente nel set di istanze. Minore è l'univocità dei valori di un attributo, minore sarà l'efficacia dell'indice.

Anche gli attributi multivalore possono essere indicizzati, ma il costo della compilazione dell'indice per un attributo multivalore è maggiore in termini di archiviazione, aggiornamento e tempo di ricerca. Il requisito di univocità per una proprietà multivalore è uguale a quello per una proprietà a valore singolo, più univoci sono i valori, più efficace è l'indice.

Maggiore è il numero di attributi indicizzati di una classe, maggiore è il tempo necessario per creare nuove istanze della classe.

Gli indici si applicano agli attributi, non alle classi. Quando un attributo viene contrassegnato come indicizzato, tutte le istanze dell'attributo vengono aggiunte all'indice, non solo le istanze che sono membri di una determinata classe.

Per verificare che un server utilizzi un indice per elaborare una query, impostare il valore del Registro di sistema seguente in un controller di dominio su 4. Eseguire quindi una query su tale controller di dominio e cercare nel registro eventi della directory i dati sugli eventuali indici usati per elaborare la query.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

Per altre informazioni su altri bit nella [**proprietà searchFlags,**](/windows/desktop/ADSchema/a-searchflags) vedere [Caratteristiche degli attributi.](characteristics-of-attributes.md)

 

 