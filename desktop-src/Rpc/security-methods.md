---
title: Metodi di sicurezza
description: Microsoft RPC supporta due metodi diversi per aggiungere sicurezza all'applicazione distribuita.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045167"
---
# <a name="security-methods"></a><span data-ttu-id="fb9c3-103">Metodi di sicurezza</span><span class="sxs-lookup"><span data-stu-id="fb9c3-103">Security Methods</span></span>

<span data-ttu-id="fb9c3-104">Microsoft RPC supporta due metodi diversi per aggiungere sicurezza all'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="fb9c3-104">Microsoft RPC supports two different methods for adding security to your distributed application.</span></span> <span data-ttu-id="fb9c3-105">Il primo metodo consiste nell'utilizzare l'interfaccia SSPI (Security Support Provider Interface), a cui è possibile accedere utilizzando le funzioni RPC.</span><span class="sxs-lookup"><span data-stu-id="fb9c3-105">The first method is to use the Security Support Provider Interface (SSPI), which can be accessed using the RPC functions.</span></span> <span data-ttu-id="fb9c3-106">In generale, è preferibile usare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fb9c3-106">In general, it is best to use this method.</span></span> <span data-ttu-id="fb9c3-107">SSPI fornisce le funzionalità di autenticazione più flessibili e indipendenti dalla rete.</span><span class="sxs-lookup"><span data-stu-id="fb9c3-107">The SSPI provides the most flexible and network-independent authentication features.</span></span>

<span data-ttu-id="fb9c3-108">Il secondo metodo consiste nell'utilizzare le funzionalità di sicurezza incorporate nei protocolli di trasporto di sistema.</span><span class="sxs-lookup"><span data-stu-id="fb9c3-108">The second method is to use the security features built into the system transport protocols.</span></span> <span data-ttu-id="fb9c3-109">Il metodo di sicurezza a livello di trasporto non è il metodo preferito.</span><span class="sxs-lookup"><span data-stu-id="fb9c3-109">The transport-level security method is not the preferred method.</span></span> <span data-ttu-id="fb9c3-110">L'uso di SSPI è consigliato perché funziona su tutti i trasporti, su più piattaforme e fornisce livelli elevati di sicurezza, inclusa la privacy.</span><span class="sxs-lookup"><span data-stu-id="fb9c3-110">Using the SSPI is recommended because it works on all transports, across platforms, and provides high levels of security, including privacy.</span></span>

<span data-ttu-id="fb9c3-111">In questa sezione vengono fornite panoramiche su SSPI e sulla sicurezza a livello di trasporto negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb9c3-111">This section provides overviews of both SSPI and transport-level security in the following topics:</span></span>

-   [<span data-ttu-id="fb9c3-112">Security Support Provider Interface (SSPI)</span><span class="sxs-lookup"><span data-stu-id="fb9c3-112">Security Support Provider Interface (SSPI)</span></span>](security-support-provider-interface-sspi-.md)
-   [<span data-ttu-id="fb9c3-113">Sicurezza del trasporto</span><span class="sxs-lookup"><span data-stu-id="fb9c3-113">Transport Security</span></span>](transport-security.md)

 

 




