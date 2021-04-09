---
title: Concetti di base sulla sicurezza RPC
description: Per completare qualsiasi chiamata di procedura remota, tutte le applicazioni distribuite devono creare un'associazione tra il client e il server.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856766"
---
# <a name="rpc-security-essentials"></a><span data-ttu-id="e57c2-103">Concetti di base sulla sicurezza RPC</span><span class="sxs-lookup"><span data-stu-id="e57c2-103">RPC Security Essentials</span></span>

<span data-ttu-id="e57c2-104">Per completare qualsiasi chiamata di procedura remota, tutte le applicazioni distribuite devono creare un'associazione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="e57c2-104">To complete any remote procedure call, all distributed applications must create a binding between the client and the server.</span></span> <span data-ttu-id="e57c2-105">Per ulteriori informazioni sulle associazioni, vedere [Binding e handle](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="e57c2-105">For more information on bindings, see [Binding and Handles](binding-and-handles.md).</span></span> <span data-ttu-id="e57c2-106">Per completare una chiamata di procedura remota sicura, sono necessari passaggi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="e57c2-106">To complete a secure remote procedure call, additional steps are necessary.</span></span> <span data-ttu-id="e57c2-107">In primo luogo, il server deve scegliere un provider di sicurezza (servizio di autenticazione nella terminologia DCE).</span><span class="sxs-lookup"><span data-stu-id="e57c2-107">First, the server must choose a security provider (authentication service in DCE terminology).</span></span> <span data-ttu-id="e57c2-108">Quindi deve decidere il meccanismo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e57c2-108">Then it must decide on its authentication mechanism.</span></span> <span data-ttu-id="e57c2-109">Successivamente, il client ottiene un'associazione al server e richiede una chiamata di procedura remota sicura dal runtime RPC e specifica varie opzioni di sicurezza, ad esempio il provider di sicurezza, le opzioni QOS di sicurezza e così via.</span><span class="sxs-lookup"><span data-stu-id="e57c2-109">After that, the client obtains a binding to the server, and requests a secure remote procedure call from the RPC run time, and specifies various security options, such as security provider, security QOS options, and so on.</span></span>

<span data-ttu-id="e57c2-110">In questa sezione vengono illustrati i concetti e le informazioni essenziali necessari per utilizzare le funzioni RPC per creare un client e un server per un'applicazione distribuita autenticata.</span><span class="sxs-lookup"><span data-stu-id="e57c2-110">This section explains the essential concepts and information required to use the RPC functions to create a client and server for an authenticated distributed application.</span></span> <span data-ttu-id="e57c2-111">Sono organizzati negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="e57c2-111">It is organized into the following topics:</span></span>

-   [<span data-ttu-id="e57c2-112">Nomi principali</span><span class="sxs-lookup"><span data-stu-id="e57c2-112">Principal Names</span></span>](principal-names.md)
-   [<span data-ttu-id="e57c2-113">Livelli di autenticazione</span><span class="sxs-lookup"><span data-stu-id="e57c2-113">Authentication Levels</span></span>](authentication-levels.md)
-   [<span data-ttu-id="e57c2-114">Servizi di autenticazione</span><span class="sxs-lookup"><span data-stu-id="e57c2-114">Authentication Services</span></span>](authentication-services.md)
-   [<span data-ttu-id="e57c2-115">Credenziali di autenticazione client</span><span class="sxs-lookup"><span data-stu-id="e57c2-115">Client Authentication Credentials</span></span>](client-authentication-credentials.md)
-   [<span data-ttu-id="e57c2-116">Servizi di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="e57c2-116">Authorization Services</span></span>](authorization-services.md)
-   [<span data-ttu-id="e57c2-117">QoS (Quality of Service)</span><span class="sxs-lookup"><span data-stu-id="e57c2-117">Quality of Service</span></span>](quality-of-service.md)
-   [<span data-ttu-id="e57c2-118">Funzioni di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="e57c2-118">Authorization Functions</span></span>](authorization-functions.md)
-   [<span data-ttu-id="e57c2-119">Funzioni di acquisizione chiave</span><span class="sxs-lookup"><span data-stu-id="e57c2-119">Key Acquisition Functions</span></span>](key-acquisition-functions.md)
-   [<span data-ttu-id="e57c2-120">Rappresentazione client</span><span class="sxs-lookup"><span data-stu-id="e57c2-120">Client Impersonation</span></span>](client-impersonation.md)

 

 




