---
title: Funzionamento dell'indicizzazione delle tuple
description: Gli indici di tupla vengono usati per ottimizzare le ricerche con 0 o più stringhe di ricerca mediale e 0 o 1 stringa di ricerca finale. Possono anche essere usati per ottimizzare le ricerche di una stringa di ricerca iniziale se non è disponibile alcun indice comune su tale attributo.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indicizzazione di tuple
- Ricerca in Active Directory Active Directory , ottimizzazione
- Active Directory, ottimizzazione della ricerca Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9d15bad8de15e4f559123d2d3cb3b6b9ec6446328e6ed4c4c52cf18355d634
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188034"
---
# <a name="how-tuple-indexing-works"></a>Funzionamento dell'indicizzazione delle tuple

Gli indici di tupla vengono usati per ottimizzare le ricerche con 0 o più stringhe di ricerca [mediale](search-string-types.md) e 0 o 1 stringa di ricerca finale. Possono anche essere usati per ottimizzare le ricerche di una stringa di ricerca iniziale se non è disponibile alcun indice comune su tale attributo.

È possibile attivare l'indicizzazione delle tuple per un attributo impostando il bit 5, che corrisponde al valore 32, [**nell'attributo searchFlags.**](/windows/desktop/ADSchema/a-searchflags) Questo attributo viene impostato nell'oggetto schema che rappresenta l'attributo che richiede l'indice di tupla. L'impatto sulle prestazioni dell'attivazione dell'indicizzazione della tupla è che qualsiasi valore stringa impostato per tale attributo verrà espanso in un numero elevato di frammenti nell'indice di tupla. Quando un attributo si espande, utilizza una quantità maggiore di spazio su disco nel file albero delle informazioni sulla directory e viene aggiornato più lentamente.

Gli indici di tupla sono progettati per accelerare le ricerche nel formato `*string*` . L'accelerazione può essere notevole perché questa forma di ricerca non può essere ottimizzata in altro modo e, nella sua forma non ottimizzata, forza il server Active Directory a eseguire la query in ogni oggetto nell'ambito della ricerca. Di conseguenza, una ricerca di base cerca solo un oggetto, che usa meno risorse, una ricerca figlio immediata cerca solo gli elementi figlio di un oggetto (che potrebbe usare un numero minore di risorse o più risorse a seconda delle dimensioni del contenitore) e una ricerca sottoalbero peserà l'intero sottoalbero sotto l'oggetto di base, che in genere richiederebbe molte risorse e sarebbe molto lenta a causa delle dimensioni del sottoalbero.

Gli indici di tupla funzionano suddividendo una stringa in *tuple*. Ad esempio, la stringa "Active Directory" verrebbe suddivisa nelle tuple seguenti:

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
> La directory si arresta a 32767 caratteri quando si espande una stringa per l'indicizzazione di tuple.

 

Un indice di tupla conterrà una voce per ognuna di queste tuple. Pertanto, se un utente cerca , il server Active Directory cerca tutte le corrispondenze per "cto" nell'indice e, in questo caso, trova un puntatore al record con un attributo (tupla indicizzata) con il valore `*cto*` "Directory".

Se la stringa di ricerca mediale ( nell'esempio precedente) è sufficientemente specifica, la ricerca sarà abbastanza efficiente perché riduce notevolmente il numero di oggetti che il server Active Directory deve controllare per eseguire la `*cto*` query.

 

 