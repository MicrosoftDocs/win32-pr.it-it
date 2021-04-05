---
title: Concessione dell'accesso come servizio direttamente nel computer host
description: Quando si installa un servizio per l'esecuzione con un account utente di dominio, l'account deve avere il diritto di accedere come servizio nel computer locale.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707612"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a><span data-ttu-id="45003-103">Concessione dell'accesso come servizio direttamente nel computer host</span><span class="sxs-lookup"><span data-stu-id="45003-103">Granting Logon as Service Right on the Host Computer</span></span>

<span data-ttu-id="45003-104">Quando si installa un servizio per l'esecuzione con un account utente di dominio, l'account deve avere il diritto di accedere come servizio nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="45003-104">When installing a service to run under a domain user account, the account must have the right to logon as a service on the local computer.</span></span> <span data-ttu-id="45003-105">Tenere presente che questo diritto di accesso si applica solo al computer locale e deve essere concesso nei criteri LSA locali di ogni computer host.</span><span class="sxs-lookup"><span data-stu-id="45003-105">Be aware that this logon right applies only to the local computer and must be granted in the local LSA policy of each host computer.</span></span> <span data-ttu-id="45003-106">Questo passaggio non è necessario se il servizio viene eseguito come LocalSystem, a cui, per impostazione predefinita, viene concesso questo diritto.</span><span class="sxs-lookup"><span data-stu-id="45003-106">This step is not required if your service runs as LocalSystem, which, by default, is granted this right.</span></span>

<span data-ttu-id="45003-107">Per ulteriori informazioni su come concedere il diritto di accesso come servizio a livello di codice, vedere il [codice di esempio LSAPrivs](https://www.google.com/#q=LSAPrivs).</span><span class="sxs-lookup"><span data-stu-id="45003-107">For more information on how to programmatically grant logon as a service right, see the [LSAPrivs sample code](https://www.google.com/#q=LSAPrivs).</span></span>

 

 




