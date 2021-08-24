---
description: Il provider Peer Name Resolution Protocol (PNRP) è una tecnologia di risoluzione dei nomi serverless che consente ai nodi di individuarsi a vicenda.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Informazioni su PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50023fe48d0cd0dc28fae91174942e03dc9df513732378888df0f53242d09f14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119338171"
---
# <a name="about-pnrp"></a>Informazioni su PNRP

Il provider Peer Name Resolution Protocol (PNRP) è una tecnologia di risoluzione dei nomi serverless che consente ai nodi di individuarsi a vicenda. PNRP usa l'API del provider dello spazio dei nomi Winsock 2.

Il supporto IPv6 è richiesto da PNRP ed è l'unico protocollo Internet nativo per l'API. Tuttavia, PNRP può risolvere gli indirizzi IPv4 tramite le tecnologie 6to4 [o Teredo](/windows/desktop/Teredo/portal) transizione. Windows Gli utenti di XP con Service Pack 1 (SP1) devono scaricare [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) per abilitare il supporto IPv6 richiesto da PNRP.

> [!Note]  
> Le applicazioni che usano PNRP in un ambiente con un firewall richiedono gruppi di eccezioni che coprono la porta specifica dell'applicazione, nonché la porta "3540-UDP" per PNRP. Questi gruppi di eccezioni devono essere abilitati ogni volta che l'applicazione è in esecuzione.

 

Mentre PNRP 2.0 è nativo per le piattaforme Windows Vista e Windows Server 2008, gli utenti di Windows XP devono scaricare l'aggiornamento [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) di Windows Xp per eseguire l'aggiornamento a PNRP 2.0.

 

 
