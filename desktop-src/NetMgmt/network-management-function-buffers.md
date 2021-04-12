---
title: Buffer della funzione di gestione di rete
description: La libreria di runtime RPC gestisce i buffer richiesti dalle funzioni di gestione della rete per il recupero dei dati a 32 bit, come indicato di seguito.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221572"
---
# <a name="network-management-function-buffers"></a>Buffer della funzione di gestione di rete

La libreria di runtime RPC gestisce i buffer richiesti dalle funzioni di gestione della rete per il recupero dei dati a 32 bit, come indicato di seguito:

-   **Invio di dati al server** (dati specificati da \[ nei \] parametri in).

    Il chiamante deve allocare e deallocare il buffer per la struttura delle informazioni (o le strutture) pertinente e passare una variabile puntatore alla funzione. Non è necessario che il chiamante specifichi la lunghezza del buffer.

    Esempio: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)

-   **Recupero dei dati dal server** (dati specificati da \[ parametri out \] ).

    Il sistema alloca il buffer per le informazioni restituite. Il chiamante deve passare una variabile puntatore alla funzione nell'input. In esito positivo, il puntatore riceve l'indirizzo del buffer allocato dal sistema che contiene le informazioni restituite. In questo modo il codice chiamante viene semplificato, perché il chiamante non deve stimare la dimensione del buffer o ridimensionare il buffer e riemettere la funzione.

    Al termine dell'elaborazione delle informazioni restituite, il chiamante deve liberare la memoria allocata dal sistema chiamando la funzione [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) . Per ulteriori informazioni su come specificare le dimensioni del buffer, vedere [lunghezze del buffer della funzione di gestione di rete](network-management-function-buffer-lengths.md).

    Esempio: [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)

 

 




