---
title: Componenti dell'architettura del router
description: La documentazione di amministrazione del router fa riferimento spesso ai componenti seguenti del router.
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- router RRAS, componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb0cc69de5402b03550873b3b052f6329b5238
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471267"
---
# <a name="components-of-the-router-architecture"></a>Componenti dell'architettura del router

La documentazione di amministrazione del router fa riferimento spesso ai componenti seguenti del router.

Gestione interfaccia dinamica (DIM)

Tutte le funzioni di amministrazione del router passano attraverso DIM. A seconda della natura della funzione, DIM può passare la chiamata a uno dei gestori di router. Le funzioni che gestiscono solo le interfacce sono gestite da DIM. Se la funzione influiscono sui protocolli di routing, DIM effettuerà una chiamata a gestione router per il trasporto corrispondente a tale protocollo. Se, ad esempio, la funzione influisca sul protocollo OSPF (Open shorter Path First), DIM effettuerà una chiamata a gestione router IP, poiché OSPF è un protocollo di routing IP.

Gestione router

Ogni trasporto instradabile che si inserisce nell'architettura del router dispone di un proprio gestore di router. Attualmente sono presenti gestori router per i trasporti IP e IPX. I gestori router gestiscono i protocolli router e altri tipi di client di routing eseguiti sulle interfacce del computer locale.

Protocolli di routing e altri client

I client sono provider di servizi che funzionano all'interno del Framework dell'architettura del router. I protocolli di routing sono un tipo di client supportato dal router.

I client sono specifici di un trasporto instradabile specifico, ovvero IP o IPX. I protocolli di routing per il trasporto IP includono il primo percorso (OSPF) e il Routing Information Protocol (RIP) aperti. Esempi di protocolli di routing IPX sono Service Advertising Protocol (SAP) e RIP per IPX. Un esempio di un client che non è un protocollo di routing è NAT (Network Address Translation) per IP.

L'interfaccia tra gestione router e un client è descritta nella sezione interfaccia del [protocollo di routing](about-routing-protocol-interface.md). Tutti i client sono conformi a questa interfaccia. Utilizzando questa interfaccia, i fornitori possono implementare i propri client compatibili con il router.

[Interfacce](interfaces.md)

Un'interfaccia è una connessione a una rete esterna. Ogni interfaccia è identificata da un *Indice* di interfaccia univoco. Le interfacce sono entità logiche. i client router, ad esempio NAT o OSPF, gestiscono tutti i tipi di interfacce in modo analogo. In termini di implementazione, tuttavia, un'interfaccia può rappresentare una connessione dedicata, ad esempio una rete locale (LAN), o una connessione remota non dedicata, ad esempio una connessione PPP a una rete WAN (Wide Area Network).

Nel caso di un'interfaccia LAN, l'interfaccia corrisponde a un dispositivo fisico reale nel computer, una scheda LAN. Nel caso di un'interfaccia WAN, viene eseguito il mapping dell'interfaccia a una porta nel momento in cui viene stabilita una connessione. La porta può essere una porta COM, una porta parallela o una porta virtuale (per i tunnel come PPTP e L2TP).

Le interfacce WAN hanno la qualità aggiuntiva che ricevono in genere un indirizzo di rete solo quando viene stabilita una connessione. Ad esempio, un'interfaccia WAN che utilizza PPP riceve l'indirizzo del livello di rete dal peer remoto durante il processo di connessione. La ricezione di un indirizzo di rete come parte del processo di connessione viene talvolta definita *associazione tardiva*.

 

 




