---
description: Illustra le interazioni tra i provider di rete e Winlogon.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interazione con i provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884501"
---
# <a name="interaction-with-network-providers"></a><span data-ttu-id="ab6db-103">Interazione con i provider di rete</span><span class="sxs-lookup"><span data-stu-id="ab6db-103">Interaction with Network Providers</span></span>

<span data-ttu-id="ab6db-104">È possibile configurare un sistema per supportare zero o più provider di rete.</span><span class="sxs-lookup"><span data-stu-id="ab6db-104">You can configure a system to support zero or more network providers.</span></span> <span data-ttu-id="ab6db-105">Ognuno di questi provider di rete può specificare di richiedere l'elaborazione interattiva speciale.</span><span class="sxs-lookup"><span data-stu-id="ab6db-105">Each of these network providers can specify that it requires special interactive authentication processing.</span></span> <span data-ttu-id="ab6db-106">Questa funzionalità consente alle reti installate di raccogliere informazioni di identificazione e autenticazione specifiche per ogni rete, ma consente loro di raccoglierle durante il normale accesso e sotto l'ombrello sicuro del [*contesto*](../secgloss/c-gly.md) e del desktop di [*Winlogon*](../secgloss/w-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ab6db-106">This capability allows installed networks to collect identification and authentication information specific to each network, yet allows them to collect it during normal logon and under the secure umbrella of [*Winlogon's*](../secgloss/w-gly.md) [*context*](../secgloss/c-gly.md) and desktop.</span></span>

<span data-ttu-id="ab6db-107">Winlogon chiama i provider di rete in diverse circostanze.</span><span class="sxs-lookup"><span data-stu-id="ab6db-107">Winlogon calls network providers under a number of circumstances.</span></span> <span data-ttu-id="ab6db-108">Dopo un accesso riuscito, Winlogon chiama i provider di rete in modo che possano raccogliere le [*credenziali*](../secgloss/c-gly.md) e autenticare l'utente per la rete.</span><span class="sxs-lookup"><span data-stu-id="ab6db-108">Following a successful logon, Winlogon calls network providers so they can collect [*credentials*](../secgloss/c-gly.md) and authenticate the user for their network.</span></span> <span data-ttu-id="ab6db-109">Winlogon chiama anche i provider di rete quando gli utenti cambiano le password.</span><span class="sxs-lookup"><span data-stu-id="ab6db-109">Winlogon also calls network providers when users change their passwords.</span></span> <span data-ttu-id="ab6db-110">Questo consente a ogni utente di mantenere una singola password per l'uso in tutte le reti.</span><span class="sxs-lookup"><span data-stu-id="ab6db-110">This lets each user maintain a single password for use on all networks.</span></span>

<span data-ttu-id="ab6db-111">La struttura delle [**\_ informazioni di \_ notifica \_ di WLX MPR**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) viene usata per fornire informazioni di identificazione e autenticazione nelle funzioni Gina pertinenti.</span><span class="sxs-lookup"><span data-stu-id="ab6db-111">The [**WLX\_MPR\_NOTIFY\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) structure is used to provide identification and authentication information in the relevant GINA functions.</span></span> <span data-ttu-id="ab6db-112">Questa struttura include i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ab6db-112">This structure includes the following members.</span></span>



| <span data-ttu-id="ab6db-113">Membro</span><span class="sxs-lookup"><span data-stu-id="ab6db-113">Member</span></span>             | <span data-ttu-id="ab6db-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab6db-114">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6db-115">**pszUserName**</span><span class="sxs-lookup"><span data-stu-id="ab6db-115">**pszUserName**</span></span>    | <span data-ttu-id="ab6db-116">Nome dell'account dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="ab6db-116">The account name of the logged-on user.</span></span>                                                                                                                                                      |
| <span data-ttu-id="ab6db-117">**pszDomain**</span><span class="sxs-lookup"><span data-stu-id="ab6db-117">**pszDomain**</span></span>      | <span data-ttu-id="ab6db-118">Nome di dominio dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="ab6db-118">The domain name of the logged-on user.</span></span> <span data-ttu-id="ab6db-119">Non tutti i modelli di autenticazione hanno un concetto di dominio (o l'equivalente), pertanto questo membro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ab6db-119">Not all authentication models have a domain concept (or its equivalent), so this member can be **NULL**.</span></span>                                              |
| <span data-ttu-id="ab6db-120">**pszPassword**</span><span class="sxs-lookup"><span data-stu-id="ab6db-120">**pszPassword**</span></span>    | <span data-ttu-id="ab6db-121">Quando l'utente ha assegnato una password in testo non crittografato durante l'autenticazione, la fornisce qui consente agli altri provider di rete di usare la stessa password (per ottenere l'accesso singolo) senza richiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="ab6db-121">When the user gave a plaintext password during authentication, providing it here lets other network providers use the same password (to achieve single logon) without prompting the user.</span></span>    |
| <span data-ttu-id="ab6db-122">**pszOldPassword**</span><span class="sxs-lookup"><span data-stu-id="ab6db-122">**pszOldPassword**</span></span> | <span data-ttu-id="ab6db-123">Dopo una modifica della password, fornendo qui la password originale e la nuova password nel membro **pszPassword** , consente ai provider di rete di aggiornare le password senza richiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="ab6db-123">After a password change, providing the original password here and the new password in the **pszPassword** member, lets network providers upgrade their passwords without prompting the user.</span></span> |



 

<span data-ttu-id="ab6db-124">Non è necessario che [*Gina*](../secgloss/g-gly.md) fornisca tali informazioni ai provider di rete.</span><span class="sxs-lookup"><span data-stu-id="ab6db-124">A [*GINA*](../secgloss/g-gly.md) does not have to provide this information to network providers.</span></span> <span data-ttu-id="ab6db-125">Se viene passato un puntatore **null** anziché un puntatore di struttura valido, i provider di rete richiederanno all'utente le informazioni.</span><span class="sxs-lookup"><span data-stu-id="ab6db-125">If a **NULL** pointer is passed instead of a valid structure pointer, the network providers will prompt the user for information.</span></span>

 

 
