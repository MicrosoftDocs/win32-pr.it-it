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
# <a name="about-pnrp"></a><span data-ttu-id="0537e-103">Informazioni su PNRP</span><span class="sxs-lookup"><span data-stu-id="0537e-103">About PNRP</span></span>

<span data-ttu-id="0537e-104">Il provider dello spazio dei nomi PNRP (Peer Name Resolution Protocol) (NSP) è una tecnologia di risoluzione dei nomi senza server che consente ai nodi di individuarsi reciprocamente.</span><span class="sxs-lookup"><span data-stu-id="0537e-104">The Peer Name Resolution Protocol (PNRP) Namespace Provider (NSP) is a serverless name resolution technology that allows nodes to discover each other.</span></span> <span data-ttu-id="0537e-105">PNRP usa l'API del provider dello spazio dei nomi Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="0537e-105">PNRP uses the Winsock 2 Namespace Provider API.</span></span>

<span data-ttu-id="0537e-106">Il supporto IPv6 è richiesto da PNRP ed è l'unico protocollo Internet nativo per l'API.</span><span class="sxs-lookup"><span data-stu-id="0537e-106">IPv6 support is required by PNRP and is the only Internet Protocol native to the API.</span></span> <span data-ttu-id="0537e-107">Tuttavia, PNRP può risolvere gli indirizzi IPv4 tramite le tecnologie di transizione 6to4 o [Teredo](/windows/desktop/Teredo/portal) .</span><span class="sxs-lookup"><span data-stu-id="0537e-107">However, PNRP can resolve IPv4 addresses via the 6to4 or [Teredo](/windows/desktop/Teredo/portal) transition technologies.</span></span> <span data-ttu-id="0537e-108">Windows XP con Service Pack 1 (SP1) gli utenti devono scaricare [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) per abilitare il supporto IPv6 richiesto da PNRP.</span><span class="sxs-lookup"><span data-stu-id="0537e-108">Windows XP with Service Pack 1 (SP1) users must download the [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) to enable the IPv6 support required by PNRP.</span></span>

> [!Note]  
> <span data-ttu-id="0537e-109">Le applicazioni che usano PNRP in un ambiente con un firewall richiedono gruppi di eccezioni che coprono la porta specifica per l'applicazione, nonché la porta "3540-UDP" per PNRP.</span><span class="sxs-lookup"><span data-stu-id="0537e-109">Applications using PNRP in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="0537e-110">Questi gruppi di eccezioni devono essere abilitati ogni volta che l'applicazione è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0537e-110">These exception groups should be enabled whenever the application is running.</span></span>

 

<span data-ttu-id="0537e-111">Sebbene PNRP 2,0 sia nativo per le piattaforme Windows Vista e Windows Server 2008, gli utenti di Windows XP devono scaricare Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) per eseguire l'aggiornamento a PNRP 2,0.</span><span class="sxs-lookup"><span data-stu-id="0537e-111">While PNRP 2.0 is native to the Windows Vista and Windows Server 2008 platforms, Windows XP users must download Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) to upgrade to PNRP 2.0.</span></span>

 

 
