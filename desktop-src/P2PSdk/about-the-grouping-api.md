---
description: L'API di raggruppamento peer combina la tecnologia dell'API del provider di spazio dei nomi PNRP e l'API Graphing.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Informazioni sull'API di raggruppamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312305"
---
# <a name="about-the-grouping-api"></a><span data-ttu-id="7516d-103">Informazioni sull'API di raggruppamento</span><span class="sxs-lookup"><span data-stu-id="7516d-103">About the Grouping API</span></span>

<span data-ttu-id="7516d-104">L'API di raggruppamento peer combina la tecnologia dell' [API del provider di spazio dei nomi PNRP](pnrp-namespace-provider-api.md) e l' [API Graphing](graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="7516d-104">The Peer Grouping API combines the technology of the [PNRP Name Space Provider API](pnrp-namespace-provider-api.md) and the [Graphing API](graphing-api.md).</span></span> <span data-ttu-id="7516d-105">Il raggruppamento aggiunge le due seguenti tecnologie:</span><span class="sxs-lookup"><span data-stu-id="7516d-105">Grouping adds the following two pieces of technology:</span></span>

-   <span data-ttu-id="7516d-106">Livello di multiplexing che consente a più applicazioni di utilizzare un grafo, una porta e un database di record.</span><span class="sxs-lookup"><span data-stu-id="7516d-106">A multiplexing layer that allows multiple applications to use one graph, one port, and one record database.</span></span>
-   <span data-ttu-id="7516d-107">Sicurezza che garantisce che solo i peer invitati a un gruppo possano entrare e connettersi per tutta la durata di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="7516d-107">Security that ensures only peers invited to a group can join and connect throughout the lifetime of a group.</span></span>

<span data-ttu-id="7516d-108">Il raggruppamento offre un approccio semplice e accessibile alla rete peer a causa del semplice flusso di chiamate e della messaggistica sicura.</span><span class="sxs-lookup"><span data-stu-id="7516d-108">Grouping provides an accessible and easy approach to peer networking because of the straightforward call flow and secure messaging.</span></span> <span data-ttu-id="7516d-109">Questa API USA PNRP per l'individuazione del gruppo e un provider di sicurezza standard basato su PKI anziché richiedere a uno sviluppatore di implementarne uno.</span><span class="sxs-lookup"><span data-stu-id="7516d-109">This API utilizes PNRP for group discovery and a standard PKI-based security provider instead of requiring a developer to implement one.</span></span> <span data-ttu-id="7516d-110">Tuttavia, se l'applicazione richiede una maggiore flessibilità in termini di opzioni di sicurezza, provare a usare l' [API Graphing](about-the-graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="7516d-110">However, if your application demands greater flexibility in terms of security options, consider using the [Graphing API](about-the-graphing-api.md).</span></span>

<span data-ttu-id="7516d-111">La tabella seguente identifica gli argomenti in questa sezione relativa all'API di raggruppamento:</span><span class="sxs-lookup"><span data-stu-id="7516d-111">The following table identifies the topics in this Grouping API section:</span></span>

| <span data-ttu-id="7516d-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="7516d-112">Topic</span></span>                                                                | <span data-ttu-id="7516d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7516d-113">Description</span></span>                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7516d-114">Come lavorare con i gruppi</span><span class="sxs-lookup"><span data-stu-id="7516d-114">How to Work With Groups</span></span>](how-to-work-with-groups.md)               | <span data-ttu-id="7516d-115">Descrive il flusso di chiamate in un'applicazione di raggruppamento peer dall'avvio all'arresto.</span><span class="sxs-lookup"><span data-stu-id="7516d-115">Describes the call flow in a Peer Grouping application from startup to shutdown.</span></span>         |
| [<span data-ttu-id="7516d-116">Funzionamento della sicurezza del gruppo</span><span class="sxs-lookup"><span data-stu-id="7516d-116">How Group Security Works</span></span>](how-group-security-works.md)             | <span data-ttu-id="7516d-117">Viene descritto come proteggere l'appartenenza al gruppo peer e gli scambi di dati.</span><span class="sxs-lookup"><span data-stu-id="7516d-117">Describes how peer group membership and data exchanges are secured.</span></span>                      |
| [<span data-ttu-id="7516d-118">Invito di un peer a un gruppo</span><span class="sxs-lookup"><span data-stu-id="7516d-118">Inviting a Peer to a Group</span></span>](inviting-a-peer-to-a-group.md)         | <span data-ttu-id="7516d-119">Descrive il processo mediante il quale i peer vengono invitati e aggiunti a un gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="7516d-119">Describes the process by which peers are invited and added to a peer group.</span></span>              |
| [<span data-ttu-id="7516d-120">Come connettersi a un gruppo peer</span><span class="sxs-lookup"><span data-stu-id="7516d-120">How to Connect to a Peer Group</span></span>](how-to-connect-to-a-peer-group.md) | <span data-ttu-id="7516d-121">Viene descritto il modo in cui un peer si connette e interagisce con un gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="7516d-121">Describes how a peer connects to and interacts with a peer group.</span></span>                        |
| [<span data-ttu-id="7516d-122">Gestione dei record di gruppo</span><span class="sxs-lookup"><span data-stu-id="7516d-122">Managing Group Records</span></span>](managing-group-records.md)                 | <span data-ttu-id="7516d-123">Vengono descritti i record del gruppo peer e viene illustrato come gestirli come membri e come amministratori.</span><span class="sxs-lookup"><span data-stu-id="7516d-123">Describes peer group records and how to manage them as a member and as an administrator.</span></span> |



 

> [!Note]  
> <span data-ttu-id="7516d-124">Le applicazioni che usano l'API di raggruppamento in un ambiente con un firewall richiedono gruppi di eccezioni che coprono la porta specifica per l'applicazione, nonché la porta "3587-TCP" per l'API di raggruppamento e la porta "3540-UDP" per PNRP.</span><span class="sxs-lookup"><span data-stu-id="7516d-124">Applications using the Grouping API in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3587-TCP' for the Grouping API and port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="7516d-125">Questi gruppi di eccezioni devono essere abilitati ogni volta che l'applicazione è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7516d-125">These exception groups should be enabled whenever the application is running.</span></span>

 

 

 



