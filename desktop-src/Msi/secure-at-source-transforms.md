---
description: Le trasformazioni secure-at-source devono avere un'origine che si trova nella radice dell'origine per il pacchetto.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Trasformazioni secure-at-source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f591e6f30c11ec9fa7edf2f943ef1f660a0a3b12ff87c3c1de0984328652565b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041001"
---
# <a name="secure-at-source-transforms"></a>Trasformazioni secure-at-source

Le trasformazioni secure-at-source devono avere un'origine che si trova nella radice dell'origine per il pacchetto. Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni in una cache in cui, in un file system sicuro, l'utente non ha accesso in scrittura. Se la copia locale della trasformazione non è più disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è identico alla ricerca di un file .msi di origine nell'elenco di origine. Per altre informazioni, vedere [Resilienza dell'origine.](source-resiliency.md) La rimozione di un prodotto da parte di qualsiasi utente rimuove tutte le trasformazioni sicure per tale prodotto dal computer dell'utente.

Per applicare trasformazioni secure-at-source all'installazione di un pacchetto, impostare il criterio [TransformsSecure](transformssecure-policy.md) o la [**proprietà TRANSFORMSSECURE**](transformssecure.md) oppure impostare @ come primo carattere passato nell'elenco delle trasformazioni. Ogni trasformazione deve essere indicata da un nome file e deve trovarsi nella radice dell'origine per il pacchetto. Se una delle trasformazioni non si trova nella radice dell'origine del pacchetto, l'installazione non riesce. Per altre informazioni, vedere [Applicazione di trasformazioni](applying-transforms.md).

 

 



