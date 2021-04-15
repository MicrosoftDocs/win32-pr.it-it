---
title: Associazione al punto di inizio della ricerca
description: Il punto iniziale di una ricerca è un contenitore che contiene direttamente o indirettamente gli oggetti cercati.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, associazione a un punto di inizio della ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470766"
---
# <a name="binding-to-the-search-start-point"></a>Associazione al punto di inizio della ricerca

Il punto iniziale di una ricerca è un contenitore che contiene direttamente o indirettamente gli oggetti cercati. La ricerca non verrà eseguita nei contenitori sopra il punto di inizio della ricerca. Ad esempio, adottare la seguente struttura di directory ipotetica:

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

Se viene eseguita una ricerca per tutti gli oggetti e il punto di inizio della ricerca è "container 2", verranno recuperati solo "Object 3" e "Object 4". Se è stata eseguita la stessa ricerca con il punto di inizio della ricerca in "container 1", verranno recuperati "Object 1" e "Object 2".

Per eseguire l'associazione al punto di inizio della ricerca, associare al ADsPath del contenitore che costituirà il punto di inizio della ricerca.

 

 




