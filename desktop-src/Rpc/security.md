---
title: Sicurezza (RPC)
description: Con l'aumento dell'utilizzo delle applicazioni distribuite, la necessità di proteggere le comunicazioni tra le parti client e server delle applicazioni è fondamentale.
ms.assetid: 0eceefed-644c-4e4b-a873-8005137c00ef
keywords:
- RPC (Remote Procedure Call), descrizione, sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a257b67fad90fe568615eb5731fc60dc9706d5ae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118782"
---
# <a name="security-rpc"></a><span data-ttu-id="f18f2-104">Sicurezza (RPC)</span><span class="sxs-lookup"><span data-stu-id="f18f2-104">Security (RPC)</span></span>

<span data-ttu-id="f18f2-105">Con l'aumento dell'utilizzo delle applicazioni distribuite, la necessità di proteggere le comunicazioni tra le parti client e server delle applicazioni è fondamentale.</span><span class="sxs-lookup"><span data-stu-id="f18f2-105">With the increased use of distributed applications, the need for secure communications between the client and server portions of applications is paramount.</span></span> <span data-ttu-id="f18f2-106">La libreria di runtime RPC (Remote Procedure Call) fornisce un'interfaccia standardizzata ai servizi di autenticazione per client e server.</span><span class="sxs-lookup"><span data-stu-id="f18f2-106">The Remote Procedure Call (RPC) run-time library provides a standardized interface to authentication services for both clients and servers.</span></span> <span data-ttu-id="f18f2-107">I servizi di autenticazione nel sistema host del server forniscono l'autenticazione RPC.</span><span class="sxs-lookup"><span data-stu-id="f18f2-107">The authentication services on the server host system provide RPC authentication.</span></span> <span data-ttu-id="f18f2-108">Le applicazioni utilizzano chiamate a procedure remote autenticate per garantire che tutte le chiamate provengano da client autorizzati.</span><span class="sxs-lookup"><span data-stu-id="f18f2-108">Applications use authenticated remote procedure calls to ensure that all calls come from authorized clients.</span></span> <span data-ttu-id="f18f2-109">Consentono inoltre di garantire che tutte le risposte del server provengano da server autenticati.</span><span class="sxs-lookup"><span data-stu-id="f18f2-109">They can also help ensure that all server replies come from authenticated servers.</span></span>

<span data-ttu-id="f18f2-110">In questa sezione viene presentata una panoramica di RPC autenticate nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f18f2-110">This section presents an overview of authenticated RPC in the following sections:</span></span>

-   [<span data-ttu-id="f18f2-111">Concetti di base sulla sicurezza RPC</span><span class="sxs-lookup"><span data-stu-id="f18f2-111">RPC Security Essentials</span></span>](rpc-security-essentials.md)
-   [<span data-ttu-id="f18f2-112">Metodi di sicurezza</span><span class="sxs-lookup"><span data-stu-id="f18f2-112">Security Methods</span></span>](security-methods.md)

 

 




