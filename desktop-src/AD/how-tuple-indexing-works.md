---
title: Funzionamento dell'indicizzazione delle tuple
description: Gli indici di tupla vengono usati per ottimizzare le ricerche con 0 o più stringhe di ricerca mediale e 0 o 1 stringhe di ricerca finale. Possono essere usati anche per ottimizzare le ricerche di una stringa di ricerca iniziale se non è disponibile alcun indice comune per tale attributo.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indicizzazione tupla
- Ricerca di Active Directory Active Directory, ottimizzazione
- Active Directory, ottimizzazione della ricerca Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724487"
---
# <a name="how-tuple-indexing-works"></a>Funzionamento dell'indicizzazione delle tuple

Gli indici di tupla vengono usati per ottimizzare le ricerche con 0 o più [stringhe di ricerca mediale](search-string-types.md) e 0 o 1 stringhe di ricerca finale. Possono essere usati anche per ottimizzare le ricerche di una stringa di ricerca iniziale se non è disponibile alcun indice comune per tale attributo.

È possibile attivare l'indicizzazione tupla per un attributo impostando il bit 5, che corrisponde al valore 32, nell'attributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) . Questo attributo viene impostato nell'oggetto dello schema che rappresenta l'attributo che richiede l'indice della tupla. L'effetto sulle prestazioni di attivazione dell'indicizzazione delle tuple consiste nel fatto che qualsiasi valore stringa impostato per tale attributo verrà espanso in un numero elevato di frammenti nell'indice della tupla. Quando un attributo si espande, viene utilizzata una quantità maggiore di spazio su disco nel file di albero delle informazioni della directory e viene anche aggiornata più lentamente.

Gli indici di tupla sono progettati per accelerare le ricerche del modulo `*string*` . L'accelerazione può essere considerevole perché questa forma di ricerca non può essere ottimizzata in altro modo e, nella forma non ottimizzata, impone al server Active Directory di esaminare ogni oggetto nell'ambito della ricerca per eseguire la query. Pertanto, una ricerca di base Cerca solo un oggetto, che usa un minor numero di risorse, una ricerca di elementi figlio immediata Cerca solo gli elementi figlio di un oggetto (che potrebbero usare un minor numero di risorse o più risorse a seconda delle dimensioni del contenitore) e la ricerca di un sottoalbero produrrà l'intero sottoalbero sotto l'oggetto di base, che in genere richiederebbe una grande quantità di

Gli indici di tupla funzionano suddividendo una stringa in *Tuple*. Ad esempio, la stringa "Active Directory" verrebbe suddivisa nelle tuple seguenti:

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> La directory si arresterà a 32767 caratteri quando si espande una stringa per l'indicizzazione delle tuple.

 

Un indice tupla conterrebbe una voce per ogni tupla. Quindi, se un utente cerca `*cto*` , il server di Active Directory cercherà tutte le corrispondenze per "CTO" nell'indice e, in questo caso, rileverà un puntatore al record con un attributo (tupla indicizzata) con un valore "directory".

Se la stringa di ricerca mediale ( `*cto*` nell'esempio precedente) è sufficientemente specifica, la ricerca sarà abbastanza efficiente perché riduce notevolmente il numero di oggetti che il server di Active Directory deve esaminare per eseguire la query.

 

 