---
title: Architettura dei servizi routing e accesso remoto
description: Nella figura seguente è illustrata una visualizzazione architetturale generale del router Windows 2000.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- Servizio Routing e accesso remoto RRAS, routing e accesso remoto architettura RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471515"
---
# <a name="routing-and-remote-access-services-architecture"></a>Architettura dei servizi routing e accesso remoto

Nella figura seguente è illustrata una visualizzazione architetturale generale del router Windows 2000.

I componenti specifici della famiglia di protocolli IP vengono visualizzati in grigio chiaro. I componenti specifici della famiglia di protocolli IPX sono visualizzati in grigio scuro. I componenti generali per tutte le famiglie di protocolli non sono ombreggiati.

Il servizio Routing e accesso remoto fornisce le API per l'amministrazione e la configurazione del servizio. Queste API includono gli agenti SNMP per IP e IPX.

RRAS include protocolli di routing sia per IP che per IPX. Per l'indirizzo IP, RRAS fornisce i protocolli di routing Routing Information Protocol (RIP) e Open Short Path First (OSPF). Per IPX, RRAS fornisce RIP e Service Advertising Protocol IPX (SAP).

RRAS usa una gestione tabelle di routing (RTM) per IP e IPX. Ogni famiglia di protocolli dispone tuttavia di una propria gestione router. RRAS dispone inoltre di un componente separato per la gestione dei gruppi multicast.

Interfacce Dynamic Interface Manager (DIM) con servizi PPP e TAPI per gestire le interfacce PPP utilizzate da alcune route.

![visualizzazione architettura generale del router Windows 2000](images/rtarch.png)

 

 




