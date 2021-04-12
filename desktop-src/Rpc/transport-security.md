---
title: Protezione del trasporto
description: Sebbene questo non sia il metodo preferito, è possibile utilizzare le impostazioni di sicurezza offerte dal trasporto named pipe per aggiungere funzionalità di sicurezza all'applicazione distribuita.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d129b5a373ed7304c142c66dd0e8b2d4e9035416
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331476"
---
# <a name="transport-security"></a><span data-ttu-id="94b96-103">Protezione del trasporto</span><span class="sxs-lookup"><span data-stu-id="94b96-103">Transport Security</span></span>

<span data-ttu-id="94b96-104">Sebbene questo non sia il metodo preferito, è possibile utilizzare le impostazioni di sicurezza offerte dal trasporto named pipe per aggiungere funzionalità di sicurezza all'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="94b96-104">Although this is not the preferred method, you can use the security settings that the named-pipe transport offers to add security features to your distributed application.</span></span> <span data-ttu-id="94b96-105">Queste impostazioni di sicurezza vengono usate con le funzioni RPC di Microsoft che iniziano con i prefissi [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)e le funzioni [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span><span class="sxs-lookup"><span data-stu-id="94b96-105">These security settings are used with the Microsoft RPC functions that start with the prefixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) and [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), and the functions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span></span>

> [!Note]  
> <span data-ttu-id="94b96-106">Se si esegue un'applicazione che è un servizio e si usa NTLM per la sicurezza, è necessario aggiungere una dipendenza esplicita del servizio per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="94b96-106">If you are running an application that is a service and you are using NTLM for security, you must add an explicit service dependency for your application.</span></span> <span data-ttu-id="94b96-107">Il Secur32.dll chiamerà Gestione controllo servizi (SCM) per avviare il servizio del pacchetto di sicurezza NTLM.</span><span class="sxs-lookup"><span data-stu-id="94b96-107">The Secur32.dll will call the Service Control Manager (SCM) to begin the NTLM security package service.</span></span> <span data-ttu-id="94b96-108">Tuttavia, un'applicazione RPC che è un servizio e viene eseguita come sistema, deve anche contattare il SC a meno che non si connetta a un altro servizio nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="94b96-108">However, an RPC application that is a service and is running as a system, must also contact the SC unless it is connecting to another service on the same computer.</span></span>

 

 

 




