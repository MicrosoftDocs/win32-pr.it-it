---
title: Risoluzione dei nomi per Teredo
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 'Altre informazioni su: Risoluzione dei nomi per Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d9c41685977ef5a4ae3e94996a8d1a59db5f9812e2ed8efe758878a9055c28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001689"
---
# <a name="name-resolution-for-teredo"></a>Risoluzione dei nomi per Teredo

L Teredo inter interface attualmente usa i protocolli seguenti per la risoluzione dei nomi:

## <a name="domain-name-system"></a>Domain Name System

Il Domain Name System (DNS) è attualmente la tecnologia di risoluzione dei nomi più importante su Internet. La maggior parte dei server Web registra gli indirizzi URL con i server DNS. Tuttavia, gli indirizzi di una rete domestica non sono registrati con i server DNS poiché la maggior parte degli utenti privati ottiene gli indirizzi IP tramite Dynamic Host Configuration Protocol (DHCP) dal provider di servizi Internet. I lease DHCP hanno una durata relativamente breve e possono richiedere da 48 a 72 ore per propagare un nome in tutto il cloud DNS. Di conseguenza, DNS si è dimostrato un metodo inefficace per ottenere l'indirizzo IP pubblico di un utente principale. Un Teredo include l'indirizzo IPv4 pubblico e quindi eredita almeno la stessa volatilità degli indirizzi IPv4. Di conseguenza, Teredo indirizzi non sono attualmente registrati in DNS.

## <a name="peer-name-resolution-protocol"></a>Protocollo PNRP (Peer Name Resolution Protocol)

Il Peer Name Resolution Protocol (PNRP) è una tecnologia DNS distribuita che archivia gli indirizzi IP in migliaia di computer utente che fanno parte di un cloud PNRP. Usando Windows Vista, qualsiasi utente domestico può scegliere di diventare un membro di un cloud PNRP e annunciare il proprio indirizzo IPv6 Teredo nella rete PNRP. A differenza degli indirizzi dati ai server DNS, la propagazione degli indirizzi nella rete PNRP richiede spesso meno di un minuto. Poiché gli indirizzi Teredo possono cambiare di frequente (l'indirizzo IPv4 esterno fornito dall'ISP può cambiare o la porta esterna usata dal dispositivo gateway Internet dell'utente può cambiare), PNRP si è dimostrato un meccanismo efficace per gli utenti privati. I nomi PNRP, gli indirizzi che terminano con ".pnrp.net" si basano su proprietà di sistema univoche che non cambiano. Di conseguenza, un nome PNRP è un modo affidabile per connettersi a un utente principale. [**L'API WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) può essere usata per ottenere l'indirizzo IP usando la tecnologia PNRP (nomi DNS che terminano con ".pnrp.net") e stabilire una connessione con altri host.

 

 
