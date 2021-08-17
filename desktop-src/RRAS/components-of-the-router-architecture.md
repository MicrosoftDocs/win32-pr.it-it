---
title: Componenti dell'architettura del router
description: La documentazione relativa all'amministrazione del router fa spesso riferimento ai componenti seguenti del router.
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- router RRAS , componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f39f104e001db99076dcd29d9d5b603d5cf9f3c526d54cd16e1ed0e4d10c575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791595"
---
# <a name="components-of-the-router-architecture"></a>Componenti dell'architettura del router

La documentazione relativa all'amministrazione del router fa spesso riferimento ai componenti seguenti del router.

Dynamic Interface Manager (DIM)

Tutte le funzioni di amministrazione del router passano attraverso DIM. A seconda della natura della funzione, DIM può passare la chiamata a uno dei gestori di router. Le funzioni che gestiscono solo le interfacce vengono gestite da DIM. Se la funzione influisce sui protocolli di routing, DIM chiamerà il gestore router per il trasporto corrispondente a tale protocollo. Ad esempio, se la funzione influisce sul protocollo OSPF (Open Shortest Path First), DIM chiamerà in Gestione router IP, poiché OSPF è un protocollo di routing IP.

Gestori router

Ogni trasporto instradabile che rientra nell'architettura del router ha un proprio gestore router. Attualmente esistono gestori di router per i trasporti IP e IPX. I gestori router gestiscono i protocolli router e altri tipi di client di routing eseguiti nelle interfacce del computer locale.

Protocolli di routing e altri client

I client sono provider di servizi che funzionano all'interno del framework dell'architettura del router. I protocolli di routing sono un tipo di client supportato dal router.

I client sono specifici di un trasporto instradabile specifico: IP o IPX. I protocolli di routing per il trasporto IP includono Open Shortest Path First (OSPF) e Routing Information Protocol (RIP). Esempi di protocolli di routing IPX sono Service Advertising Protocol (SAP) e RIP per IPX. Un esempio di client che non è un protocollo di routing è Network Address Translation (NAT) per IP.

L'interfaccia tra la gestione router e un client è descritta nella sezione [Interfaccia del protocollo di routing](about-routing-protocol-interface.md). Tutti i client sono conformi a questa interfaccia. Usando questa interfaccia, i fornitori possono implementare i propri client compatibili con il router.

[Interfacce](interfaces.md)

Un'interfaccia è una connessione a una rete esterna. Ogni interfaccia è identificata da un indice di interfaccia *univoco*. Le interfacce sono entità logiche. I client router come NAT o OSPF si occupano di tutti i tipi di interfacce in modo analogo. In termini di implementazione, tuttavia, un'interfaccia può rappresentare una connessione dedicata (ad esempio a una rete locale (LAN) o una connessione remota non dedicata (ad esempio una connessione PPP a una rete WAN).

Nel caso di un'interfaccia LAN, l'interfaccia corrisponde a un dispositivo fisico effettivo nel computer, una scheda LAN. Nel caso di un'interfaccia WAN, viene eseguito il mapping dell'interfaccia a una porta al momento della connessione. La porta può essere una porta COM, una porta parallela o una porta virtuale (per tunnel come PPTP e L2TP).

Le interfacce WAN hanno la qualità aggiuntiva che in genere ricevono un indirizzo di rete solo al momento in cui viene stabilita una connessione. Ad esempio, un'interfaccia WAN che usa PPP riceve l'indirizzo del livello di rete dal peer remoto durante il processo di connessione. La ricezione di un indirizzo di rete come parte del processo di connessione viene talvolta definita *associazione tardiva.*

 

 




