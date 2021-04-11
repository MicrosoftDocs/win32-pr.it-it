---
description: Il provider dello spazio dei nomi PNRP (Peer Name Resolution Protocol) (NSP) è una tecnologia di risoluzione dei nomi senza server che consente ai nodi di individuarsi reciprocamente.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Informazioni su PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131702"
---
# <a name="about-pnrp"></a>Informazioni su PNRP

Il provider dello spazio dei nomi PNRP (Peer Name Resolution Protocol) (NSP) è una tecnologia di risoluzione dei nomi senza server che consente ai nodi di individuarsi reciprocamente. PNRP usa l'API del provider dello spazio dei nomi Winsock 2.

Il supporto IPv6 è richiesto da PNRP ed è l'unico protocollo Internet nativo per l'API. Tuttavia, PNRP può risolvere gli indirizzi IPv4 tramite le tecnologie di transizione 6to4 o [Teredo](/windows/desktop/Teredo/portal) . Windows XP con Service Pack 1 (SP1) gli utenti devono scaricare [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) per abilitare il supporto IPv6 richiesto da PNRP.

> [!Note]  
> Le applicazioni che usano PNRP in un ambiente con un firewall richiedono gruppi di eccezioni che coprono la porta specifica per l'applicazione, nonché la porta "3540-UDP" per PNRP. Questi gruppi di eccezioni devono essere abilitati ogni volta che l'applicazione è in esecuzione.

 

Sebbene PNRP 2,0 sia nativo per le piattaforme Windows Vista e Windows Server 2008, gli utenti di Windows XP devono scaricare Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) per eseguire l'aggiornamento a PNRP 2,0.

 

 
