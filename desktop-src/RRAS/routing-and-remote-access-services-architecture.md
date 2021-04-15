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
# <a name="routing-and-remote-access-services-architecture"></a><span data-ttu-id="47cae-104">Architettura dei servizi routing e accesso remoto</span><span class="sxs-lookup"><span data-stu-id="47cae-104">Routing and Remote Access Services Architecture</span></span>

<span data-ttu-id="47cae-105">Nella figura seguente è illustrata una visualizzazione architetturale generale del router Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="47cae-105">The following illustration presents a general architectural view of the Windows 2000 router.</span></span>

<span data-ttu-id="47cae-106">I componenti specifici della famiglia di protocolli IP vengono visualizzati in grigio chiaro.</span><span class="sxs-lookup"><span data-stu-id="47cae-106">Components that are specific to the IP protocol family are shown in light gray.</span></span> <span data-ttu-id="47cae-107">I componenti specifici della famiglia di protocolli IPX sono visualizzati in grigio scuro.</span><span class="sxs-lookup"><span data-stu-id="47cae-107">Components that are specific to the IPX protocol family are shown in dark gray.</span></span> <span data-ttu-id="47cae-108">I componenti generali per tutte le famiglie di protocolli non sono ombreggiati.</span><span class="sxs-lookup"><span data-stu-id="47cae-108">Components that are general to all protocol families are unshaded.</span></span>

<span data-ttu-id="47cae-109">Il servizio Routing e accesso remoto fornisce le API per l'amministrazione e la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="47cae-109">The Routing and Remote Access Service provides APIs for administering and configuring the service.</span></span> <span data-ttu-id="47cae-110">Queste API includono gli agenti SNMP per IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="47cae-110">These APIs include SNMP agents for both IP and IPX.</span></span>

<span data-ttu-id="47cae-111">RRAS include protocolli di routing sia per IP che per IPX.</span><span class="sxs-lookup"><span data-stu-id="47cae-111">RRAS includes routing protocols for both IP and IPX.</span></span> <span data-ttu-id="47cae-112">Per l'indirizzo IP, RRAS fornisce i protocolli di routing Routing Information Protocol (RIP) e Open Short Path First (OSPF).</span><span class="sxs-lookup"><span data-stu-id="47cae-112">For IP, RRAS provides the Routing Information Protocol (RIP) and Open Shortest Path First (OSPF) routing protocols.</span></span> <span data-ttu-id="47cae-113">Per IPX, RRAS fornisce RIP e Service Advertising Protocol IPX (SAP).</span><span class="sxs-lookup"><span data-stu-id="47cae-113">For IPX, RRAS provides IPX RIP and Service Advertising Protocol (SAP).</span></span>

<span data-ttu-id="47cae-114">RRAS usa una gestione tabelle di routing (RTM) per IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="47cae-114">RRAS uses one Routing Table Manager (RTM) for both IP and IPX.</span></span> <span data-ttu-id="47cae-115">Ogni famiglia di protocolli dispone tuttavia di una propria gestione router.</span><span class="sxs-lookup"><span data-stu-id="47cae-115">However, each protocol family has its own Router Manager.</span></span> <span data-ttu-id="47cae-116">RRAS dispone inoltre di un componente separato per la gestione dei gruppi multicast.</span><span class="sxs-lookup"><span data-stu-id="47cae-116">RRAS also has separate component for managing Multicast Groups.</span></span>

<span data-ttu-id="47cae-117">Interfacce Dynamic Interface Manager (DIM) con servizi PPP e TAPI per gestire le interfacce PPP utilizzate da alcune route.</span><span class="sxs-lookup"><span data-stu-id="47cae-117">The Dynamic Interface Manager (DIM) interfaces with PPP and TAPI services in order to manage PPP interfaces used by some routes.</span></span>

![visualizzazione architettura generale del router Windows 2000](images/rtarch.png)

 

 




