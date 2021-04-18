---
description: Un'applicazione server fornisce servizi ai client.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Controllo di accesso client/server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308654"
---
# <a name="clientserver-access-control"></a><span data-ttu-id="d840a-103">Controllo di accesso client/server</span><span class="sxs-lookup"><span data-stu-id="d840a-103">Client/Server Access Control</span></span>

<span data-ttu-id="d840a-104">Un'applicazione server fornisce servizi ai client.</span><span class="sxs-lookup"><span data-stu-id="d840a-104">A server application provides services to clients.</span></span> <span data-ttu-id="d840a-105">Ad esempio, un server può eseguire i servizi seguenti per conto di un client:</span><span class="sxs-lookup"><span data-stu-id="d840a-105">For example, a server could perform the following services on behalf of a client:</span></span>

-   <span data-ttu-id="d840a-106">Salvare e recuperare informazioni da un database privato</span><span class="sxs-lookup"><span data-stu-id="d840a-106">Save and retrieve information from a private database</span></span>
-   <span data-ttu-id="d840a-107">Accedere alle risorse di rete</span><span class="sxs-lookup"><span data-stu-id="d840a-107">Access network resources</span></span>
-   <span data-ttu-id="d840a-108">Avviare i [*processi*](/windows/desktop/SecGloss/p-gly) nel contesto di [*sicurezza*](/windows/desktop/SecGloss/s-gly) del client nel computer del server</span><span class="sxs-lookup"><span data-stu-id="d840a-108">Start [*processes*](/windows/desktop/SecGloss/p-gly) in the client's [*security context*](/windows/desktop/SecGloss/s-gly) on the server's computer</span></span>

<span data-ttu-id="d840a-109">Un server protetto controlla l'accesso ai servizi.</span><span class="sxs-lookup"><span data-stu-id="d840a-109">A protected server controls access to its services.</span></span> <span data-ttu-id="d840a-110">Windows fornisce supporto per la sicurezza che consente a un server di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d840a-110">Windows provides security support that enables a server to do the following:</span></span>

-   <span data-ttu-id="d840a-111">Rappresenta il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly)di un client, che fa in modo che il sistema esegua la maggior parte dei controlli di accesso e dei [*privilegi*](/windows/desktop/SecGloss/p-gly) rispetto al [*token di accesso*](/windows/desktop/SecGloss/a-gly) del client anziché al server</span><span class="sxs-lookup"><span data-stu-id="d840a-111">Impersonate a client's [*security context*](/windows/desktop/SecGloss/s-gly), which causes the system to perform most access and [*privilege*](/windows/desktop/SecGloss/p-gly) checks against the client's [*access token*](/windows/desktop/SecGloss/a-gly) rather than the server's</span></span>
-   <span data-ttu-id="d840a-112">Registrare un client nel computer del server</span><span class="sxs-lookup"><span data-stu-id="d840a-112">Log a client on to the server's computer</span></span>
-   <span data-ttu-id="d840a-113">Connettersi alle risorse di rete usando il contesto di sicurezza del client</span><span class="sxs-lookup"><span data-stu-id="d840a-113">Connect to network resources using the client's security context</span></span>
-   <span data-ttu-id="d840a-114">Creare [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly) per proteggere gli oggetti privati</span><span class="sxs-lookup"><span data-stu-id="d840a-114">Create [*security descriptors*](/windows/desktop/SecGloss/s-gly) to protect private objects</span></span>
-   <span data-ttu-id="d840a-115">Determinare se un descrittore di sicurezza consente l'accesso a un client</span><span class="sxs-lookup"><span data-stu-id="d840a-115">Determine whether a security descriptor allows access to a client</span></span>
-   <span data-ttu-id="d840a-116">Determinare se un set di privilegi è abilitato nel token di un client</span><span class="sxs-lookup"><span data-stu-id="d840a-116">Determine whether a set of privileges are enabled in a client's token</span></span>
-   <span data-ttu-id="d840a-117">Generare messaggi di controllo nel registro eventi di sicurezza per registrare i tentativi da parte di un client di accedere agli oggetti o utilizzare i privilegi</span><span class="sxs-lookup"><span data-stu-id="d840a-117">Generate audit messages in the security event log to record attempts by a client to access objects or use privileges</span></span>

 

 
