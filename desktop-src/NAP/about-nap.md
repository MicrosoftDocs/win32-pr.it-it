---
title: Informazioni su NAP
description: Informazioni su NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707825"
---
# <a name="about-nap"></a>Informazioni su NAP

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Protezione accesso alla rete (NAP) è progettato per consentire agli amministratori di mantenere l'integrità dei computer nella rete, che a sua volta consente di mantenere l'integrità complessiva della rete. Non è progettato per proteggere una rete da utenti malintenzionati. Se, ad esempio, un computer dispone di tutto il software e le configurazioni necessarie per i criteri di accesso alla rete, il computer viene considerato integro o conforme e viene concesso l'accesso appropriato alla rete. NAP non impedisce a un utente autorizzato con un computer conforme di caricare un programma dannoso in rete o di impegnarsi in un altro comportamento non appropriato.

Per proteggere l'accesso a una rete, un'infrastruttura di rete deve fornire le seguenti aree di funzionalità:

-   Convalida dell'integrità: determina se i computer sono conformi ai requisiti di integrità del sistema.
-   Restrizione di rete: limita l'accesso alla rete o alla comunicazione per i client che non sono conformi ai requisiti di integrità del sistema.
-   Monitoraggio e aggiornamento: fornisce gli aggiornamenti necessari per consentire al computer di correggere lo stato di integrità non conforme.
-   Conformità continua: consente l'accesso alla rete purché il computer dell'utente soddisfi i requisiti dei criteri di integrità.

Windows XP con Service Pack 3 (SP3), Windows Vista e Windows Server 2008 forniscono metodi di imposizione di protezione accesso alla rete per la configurazione dell'indirizzo Dynamic Host Configuration Protocol (DHCP), connessioni VPN (Virtual Private Network) basate sull'accesso remoto, connessioni cablate e wireless autenticate tramite IEEE 802.1 X e comunicazioni basate su Internet Protocol Security (IPsec). La piattaforma NAP supporta inoltre un'architettura in cui la convalida dell'integrità, la restrizione di rete, la correzione e la conformità continua sono supportate da componenti aggiuntivi che possono essere forniti da fornitori di software di terze parti o da Microsoft.

La piattaforma NAP include i componenti seguenti:

-   [Architettura client NAP](nap-client-architecture.md)
-   [Architettura lato server NAP](nap-server-side-architecture.md)
-   [Comunicazione tra client NAP e componenti lato server](nap-client-and-server-side-component-communication.md)

Il client di protezione accesso alla rete richiede Windows Vista, Windows XP con SP3 o Windows Server 2008. Il server criteri di integrità protezione accesso alla rete e i punti di imposizione di protezione accesso alla rete per DHCP, VPN e IPsec richiedono Windows Server 2008.

 

 




