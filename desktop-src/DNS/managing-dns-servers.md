---
title: Gestione dei server DNS
description: Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712427"
---
# <a name="managing-dns-servers"></a>Gestione dei server DNS

Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS. I server DNS contengono file, denominati *file di zona*, che consentono di risolvere i nomi in indirizzi IP (o viceversa). Quando viene eseguita una query, un server DNS risponde in uno dei tre modi seguenti:

-   Il server restituisce le informazioni richieste per la risoluzione dei nomi o la risoluzione IP.
-   Il server restituisce un puntatore a un altro server DNS che può servire la richiesta.
-   Il server indica che non sono disponibili le informazioni richieste.

I server DNS potrebbero, durante la preparazione della restituzione delle informazioni di risoluzione richieste, eseguire una query su altri server DNS. Tuttavia, oltre a questo, i server DNS non eseguono alcuna operazione diversa da quella indicata nell'elenco precedente.

Sono disponibili tre tipi principali di server DNS: server primari, server secondari e server di memorizzazione nella cache. Per ulteriori informazioni su questi server DNS, vedere [server DNS](dns-servers.md) .

## <a name="administration-steps"></a>Procedura di amministrazione

Il provider WMI DNS consente l'amministrazione dei server DNS dal server stesso o da host remoti. I passaggi generali necessari per amministrare un server DNS tramite il provider WMI DNS sono:

-   Connessione al provider WMI DNS
-   Recupero di un'istanza del server
-   Elenco o modifica di una proprietà del server o utilizzo di un metodo

Per illustrare come implementare tali passaggi di amministrazione, vengono forniti alcuni esempi. Le attività seguenti sono collegate agli esempi di script associati.

-   [Arresto di un server DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Avvio di un server DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Riavvio di un server DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Aggiunta di un indirizzo IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Rimozione di un indirizzo IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Elenco delle proprietà del server DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Visualizzazione di tipi di proprietà del server DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Modifica delle proprietà del server DNS](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




