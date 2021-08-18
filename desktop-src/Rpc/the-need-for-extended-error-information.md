---
title: Necessità di informazioni estese sugli errori
description: Una difficoltà principale associata alla risoluzione dei problemi RPC è il mapping di un codice di errore RPC al problema sottostante.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce13e2cb30c7cd9f2db4d7f518eb0a747cd15b2ba1ff7962cf5f41fbc9cf552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016801"
---
# <a name="the-need-for-extended-error-information"></a>Necessità di informazioni estese sugli errori

Una difficoltà principale associata alla risoluzione dei problemi RPC è il mapping di un codice di errore RPC al problema sottostante. Un errore di configurazione o un problema di rete può causare la ricezione di errori RPC S in una o più workstation, ma tale workstation può solo visualizzare l'errore, \_ \_ parafrasarlo o salvarlo in un file di \* log. Indipendentemente dall'approccio usato, la persona che ha risolto il problema è priva di informazioni essenziali:

-   Posizione in cui si è verificato l'errore. È possibile che si sia verificato nel computer locale, in un computer remoto chiamato dal computer locale o in un computer remoto chiamato da un altro computer remoto.
-   Codice di errore originale che ha causato il problema. Per conformità allo standard OSF, MS RPC esegue il mapping dei codici di errore ai codici \_ RPC \_ \* S. I \_ codici RPC S sono tuttavia troppo generici e offrono poche informazioni utili per la risoluzione dei \_ \* problemi.
-   Qualsiasi informazione di contesto correlata all'occorrenza del problema. Con gli errori non RPC, i debugger possono arrestare il processo ed esaminare il contesto in cui si è verificato l'errore. Gli errori RPC vengono spesso generati da un processo o un computer remoto, che continua l'elaborazione dopo la restituzione dell'errore e sovrascrive qualsiasi contesto relativo all'errore.

 

 




