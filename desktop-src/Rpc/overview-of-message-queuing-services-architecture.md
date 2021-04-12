---
title: Panoramica dell'architettura dei servizi di Accodamento messaggi
description: I servizi di Accodamento messaggi (MSMQ) utilizzano un modello di sito/organizzazione. In genere, un sito è una posizione fisica, ad esempio un edificio. Un'azienda è costituita da uno o più siti e rappresenta un'organizzazione.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331367"
---
# <a name="overview-of-message-queuing-services-architecture"></a><span data-ttu-id="ce495-105">Panoramica dell'architettura dei servizi di Accodamento messaggi</span><span class="sxs-lookup"><span data-stu-id="ce495-105">Overview of Message Queuing Services Architecture</span></span>

<span data-ttu-id="ce495-106">I servizi di Accodamento messaggi (MSMQ) utilizzano un modello di sito/organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ce495-106">Message Queuing Services (MSMQ) uses a site/enterprise model.</span></span> <span data-ttu-id="ce495-107">In genere, un sito è una posizione fisica, ad esempio un edificio.</span><span class="sxs-lookup"><span data-stu-id="ce495-107">Typically, a site is a physical location, such as a building.</span></span> <span data-ttu-id="ce495-108">Un'azienda è costituita da uno o più siti e rappresenta un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ce495-108">An enterprise consists of one or more sites and represents an organization.</span></span>

<span data-ttu-id="ce495-109">Nel diagramma seguente viene illustrata l'architettura del servizio MSMQ.</span><span class="sxs-lookup"><span data-stu-id="ce495-109">The following diagram illustrates the architecture of the MSMQ Service.</span></span>

![architettura MSMQ](images/msmq.png)

<span data-ttu-id="ce495-111">Il nucleo di MSMQ è il database Message Queue Information Service (MQIS), che viene eseguito sopra SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ce495-111">At the heart of MSMQ is the Message Queue Information Service (MQIS) database, which runs on top of SQL Server.</span></span> <span data-ttu-id="ce495-112">Un'azienda ha un singolo MQIS Master, denominato controller Enterprise primario.</span><span class="sxs-lookup"><span data-stu-id="ce495-112">An enterprise has a single master MQIS, called the Primary Enterprise Controller.</span></span> <span data-ttu-id="ce495-113">Ogni sito dispone di un proprio MQIS, denominato *controller del sito primario* e zero o più *controller del sito di backup*.</span><span class="sxs-lookup"><span data-stu-id="ce495-113">Each site has its own MQIS, called a *primary site controller* and zero or more *backup site controllers*.</span></span> <span data-ttu-id="ce495-114">Infine, vi sono i singoli computer client, ognuno dei quali ha un proprio gestore code, implementato come servizio.</span><span class="sxs-lookup"><span data-stu-id="ce495-114">Finally, there are the individual client computers, each of which has its own queue manager, implemented as a service.</span></span> <span data-ttu-id="ce495-115">Il controller Enterprise primario può anche essere un controller del sito primario e qualsiasi controller può essere anche un client.</span><span class="sxs-lookup"><span data-stu-id="ce495-115">The Primary Enterprise Controller can also be a Primary Site Controller, and any controller can also be a client.</span></span>

<span data-ttu-id="ce495-116">Le code di messaggi possono essere pubbliche o private.</span><span class="sxs-lookup"><span data-stu-id="ce495-116">Message queues can be either public or private.</span></span> <span data-ttu-id="ce495-117">Le code pubbliche sono registrate in Active Directory e sono accessibili attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="ce495-117">Public queues are registered in Active Directory and are accessible across the network.</span></span> <span data-ttu-id="ce495-118">I messaggi in una coda pubblica vengono instradati in tutta l'organizzazione, sotto il controllo di MSMQ.</span><span class="sxs-lookup"><span data-stu-id="ce495-118">Messages in a public queue are routed throughout the enterprise, under the control of MSMQ.</span></span> <span data-ttu-id="ce495-119">I messaggi dell'applicazione client passano dal gestore delle code del client alla coda di destinazione, viaggiando tra i gestori delle code dei controller del sito.</span><span class="sxs-lookup"><span data-stu-id="ce495-119">Client application messages move from the client's queue manager to the destination queue by traveling between the queue managers of the site controllers.</span></span>

<span data-ttu-id="ce495-120">Le code private vengono gestite dal gestore delle code locali e non sono registrate in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ce495-120">Private queues are maintained by the local queue manager and are not registered in Active Directory.</span></span> <span data-ttu-id="ce495-121">L'ambito dei messaggi della coda privata è limitato al computer in cui si trovano.</span><span class="sxs-lookup"><span data-stu-id="ce495-121">The scope of private queue messages is limited to the computer on which they reside.</span></span>

 

 




