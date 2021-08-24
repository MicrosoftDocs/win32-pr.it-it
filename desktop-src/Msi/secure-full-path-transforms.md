---
description: Le trasformazioni secure-full-path devono avere un'origine che si trova nel percorso completo specificato nella proprietà TRANSFORMS.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Trasformazioni secure-full-path
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f55e16f40d99deceb8b625297cf447ebf5ec7dfb14a25518554804cf35b572e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040901"
---
# <a name="secure-full-path-transforms"></a>Trasformazioni secure-full-path

Le trasformazioni secure-full-path devono avere un'origine che si trova nel percorso completo specificato nella [**proprietà TRANSFORMS.**](transforms.md) Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni in una cache in cui, in un file system sicuro, l'utente non ha accesso in scrittura. Se la copia locale della trasformazione non è più disponibile, può ripristinare la cache solo usando il percorso specificato. La rimozione di un prodotto da parte di qualsiasi utente rimuove tutte le trasformazioni sicure per tale prodotto dal computer dell'utente.

Per applicare trasformazioni secure-full-paths durante l'installazione di un pacchetto, impostare il criterio [TransformsSecure](transformssecure-policy.md) o la [**proprietà TRANSFORMSSECURE**](transformssecure.md) oppure impostare il primo carattere passato nell'elenco \| delle trasformazioni. I percorsi completi dell'origine di ogni trasformazione devono essere passati nella stringa delle trasformazioni. Se nell'elenco sono presenti percorsi relativi, l'installazione non riesce. Non è necessario che l'origine della trasformazione si trovi con l'origine del pacchetto.

 

 



