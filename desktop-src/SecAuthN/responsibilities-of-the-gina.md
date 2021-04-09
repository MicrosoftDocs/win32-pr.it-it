---
description: Elenca e spiega le responsabilità di GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilità di GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049976"
---
# <a name="responsibilities-of-the-gina"></a><span data-ttu-id="c3c66-103">Responsabilità di GINA</span><span class="sxs-lookup"><span data-stu-id="c3c66-103">Responsibilities of the GINA</span></span>

> [!Note]  
> <span data-ttu-id="c3c66-104">Le DLL GINA vengono ignorate in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3c66-104">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="c3c66-105">Una dll [*Gina*](../secgloss/g-gly.md) ha le responsabilità seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3c66-105">A [*GINA*](../secgloss/g-gly.md) DLL has the following responsibilities:</span></span>

-   <span data-ttu-id="c3c66-106">Monitoraggio SAS</span><span class="sxs-lookup"><span data-stu-id="c3c66-106">SAS monitoring</span></span>

    <span data-ttu-id="c3c66-107">GINA è responsabile del riconoscimento di una [*Secure Attention Sequence*](../secgloss/s-gly.md) (SAS), del monitoraggio degli eventi SAS e della notifica di Winlogon quando si verifica una firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="c3c66-107">The GINA is responsible for recognizing a [*secure attention sequence*](../secgloss/s-gly.md) (SAS), monitoring for SAS events, and notifying Winlogon when a SAS has occurred.</span></span> <span data-ttu-id="c3c66-108">Si noti che è possibile definire più di una firma di accesso condiviso e il set di SASs definito può variare nel tempo.</span><span class="sxs-lookup"><span data-stu-id="c3c66-108">Note that there can be more than one SAS defined, and the set of defined SASs can change over time.</span></span> <span data-ttu-id="c3c66-109">Ad esempio, può essere presente un set di SASs quando [*Winlogon*](../secgloss/w-gly.md) si trova nello stato disconnesso e un altro set quando si trova nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="c3c66-109">For example, there can be one set of SASs when [*Winlogon*](../secgloss/w-gly.md) is in the logged-off state and another set when it is in the logged-on state.</span></span>

    <span data-ttu-id="c3c66-110">Winlogon fornisce servizi per consentire a GINA di usare la firma di accesso condiviso CTRL + ALT + CANC.</span><span class="sxs-lookup"><span data-stu-id="c3c66-110">Winlogon provides services to assist the GINA in using the CTRL+ALT+DEL SAS.</span></span>

-   <span data-ttu-id="c3c66-111">Elaborazione SAS</span><span class="sxs-lookup"><span data-stu-id="c3c66-111">SAS processing</span></span>

    <span data-ttu-id="c3c66-112">Uno dei motivi per cui GINA può essere sostituita è fornire meccanismi di identificazione e autenticazione alternativi.</span><span class="sxs-lookup"><span data-stu-id="c3c66-112">One reason for making the GINA replaceable is to provide alternative identification and authentication mechanisms.</span></span> <span data-ttu-id="c3c66-113">A tale scopo, è necessario che GINA presenti tutte le interfacce utente derivanti dal riconoscimento di una firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="c3c66-113">To do this, the GINA must present all user interfaces resulting from the recognition of a SAS.</span></span> <span data-ttu-id="c3c66-114">Quando nessun utente è connesso, GINA è responsabile della presentazione delle opzioni di identificazione e autenticazione, nonché di eventuali altre opzioni consentite che non vengono autenticate.</span><span class="sxs-lookup"><span data-stu-id="c3c66-114">When no user is logged on, the GINA is responsible for presenting identification and authentication options as well as any other permissible options that are not authenticated.</span></span> <span data-ttu-id="c3c66-115">Quando un utente è connesso, GINA è responsabile della presentazione delle opzioni rilevanti per l'utente, nonché dell'esecuzione di qualsiasi azione ritenuta appropriata.</span><span class="sxs-lookup"><span data-stu-id="c3c66-115">When a user is logged on, the GINA is responsible for presenting the relevant options to the user as well as taking whatever actions are deemed appropriate.</span></span> <span data-ttu-id="c3c66-116">Ad esempio, in un sistema che include una [*Smart Card*](../secgloss/s-gly.md), potrebbe essere opportuno bloccare automaticamente la workstation se l'utente rimuove la smart card.</span><span class="sxs-lookup"><span data-stu-id="c3c66-116">For example, in a system that includes a [*smart card*](../secgloss/s-gly.md), it may be appropriate to automatically lock the workstation if the user removes the smart card.</span></span>

-   <span data-ttu-id="c3c66-117">Attivazione della shell</span><span class="sxs-lookup"><span data-stu-id="c3c66-117">Shell activation</span></span>

    <span data-ttu-id="c3c66-118">Quando un utente esegue l'accesso, GINA è responsabile della creazione di uno o più processi iniziali per tale utente.</span><span class="sxs-lookup"><span data-stu-id="c3c66-118">When a user logs on, the GINA is responsible for creating one or more initial processes for that user.</span></span> <span data-ttu-id="c3c66-119">In questa documentazione si presuppone che questi processi iniziali presentino un'interfaccia per l'utente.</span><span class="sxs-lookup"><span data-stu-id="c3c66-119">(In this documentation, it is assumed that these initial processes present an interface to the user.</span></span> <span data-ttu-id="c3c66-120">Tuttavia, i processi possono essere effettivamente processi e non devono necessariamente interagire con l'utente. Questi processi sono detti *Shell utente* o solo la *Shell*.</span><span class="sxs-lookup"><span data-stu-id="c3c66-120">However, the processes can actually be any processes and do not necessarily have to interact with the user.) These processes are referred to as the *user shell* or just the *shell*.</span></span> <span data-ttu-id="c3c66-121">Come parte dell'attivazione della shell, GINA deve assegnare il token dell'utente appena connesso ai processi.</span><span class="sxs-lookup"><span data-stu-id="c3c66-121">As part of shell activation, the GINA must assign the newly logged-on user's token to the processes.</span></span> <span data-ttu-id="c3c66-122">Winlogon fornisce un servizio per aiutare la GINA ad assegnare il token.</span><span class="sxs-lookup"><span data-stu-id="c3c66-122">Winlogon provides a service to assist the GINA in assigning the token.</span></span>

 

 
