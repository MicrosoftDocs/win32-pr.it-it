---
title: Risoluzione dei nomi per Teredo
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 'Altre informazioni su: risoluzione dei nomi per Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700b5d40fda0546c29bd7c47ee773977c374784c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317626"
---
# <a name="name-resolution-for-teredo"></a>Risoluzione dei nomi per Teredo

L'interfaccia Teredo utilizza attualmente i protocolli seguenti per la risoluzione dei nomi:

## <a name="domain-name-system"></a>Domain Name System

Il Domain Name System (DNS) è attualmente la tecnologia di risoluzione dei nomi più importante su Internet. La maggior parte dei server Web registra gli indirizzi URL con i server DNS. Tuttavia, gli indirizzi di una rete domestica non sono registrati con i server DNS, perché la maggior parte degli utenti di casa riceve gli indirizzi IP tramite Dynamic Host Configuration Protocol (DHCP) dal provider di servizi Internet. I lease DHCP hanno una durata relativamente breve e possono richiedere da 48 a 72 ore per propagare un nome in tutto il Cloud DNS. Di conseguenza, DNS si è rivelato un metodo inefficace per ottenere l'indirizzo IP pubblico di un utente di casa. Un indirizzo Teredo include l'indirizzo IPv4 pubblico e pertanto eredita almeno la stessa volatilità degli indirizzi IPv4. Di conseguenza, gli indirizzi Teredo non sono attualmente registrati in DNS.

## <a name="peer-name-resolution-protocol"></a>Protocollo PNRP (Peer Name Resolution Protocol)

Il protocollo PNRP (Peer Name Resolution Protocol) è una tecnologia DNS distribuita che archivia gli indirizzi IP in migliaia di computer utente che fanno parte di un Cloud PNRP. Con Windows Vista, qualsiasi utente di casa può scegliere di diventare membro di un Cloud PNRP e annunciare il proprio indirizzo IPv6 Teredo sulla rete PNRP. A differenza degli indirizzi assegnati ai server DNS, la propagazione degli indirizzi sulla rete PNRP spesso importano meno di un minuto. Poiché gli indirizzi Teredo possono cambiare spesso (l'indirizzo IPv4 esterno fornito dall'ISP può cambiare o la porta esterna usata dal dispositivo gateway Internet dell'utente può cambiare), PNRP si è rivelato un meccanismo efficace per gli utenti privati. I nomi PNRP, gli indirizzi che terminano con ". pnrp.net" sono basati su proprietà di sistema univoche che non cambiano. Di conseguenza, un nome PNRP è un modo affidabile per connettersi a un utente di casa. L'API [**con WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) può essere usata per ottenere l'indirizzo IP usando la tecnologia PNRP (nomi DNS che terminano con ". PNRP.NET") e stabilire una connessione con altri host.

 

 
