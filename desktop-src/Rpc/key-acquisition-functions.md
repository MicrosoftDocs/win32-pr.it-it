---
title: Funzioni di acquisizione chiave
description: Per impostazione predefinita, il provider di servizi condivisi fornisce chiavi di crittografia ai programmi server che li richiedono. Ogni SSP implementa il proprio sistema di generazione delle chiavi. Il formato delle chiavi generate dal provider di servizi condivisi è specifico del provider di servizi condivisi.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856746"
---
# <a name="key-acquisition-functions"></a><span data-ttu-id="10456-105">Funzioni di acquisizione chiave</span><span class="sxs-lookup"><span data-stu-id="10456-105">Key Acquisition Functions</span></span>

<span data-ttu-id="10456-106">Per impostazione predefinita, il provider di servizi condivisi fornisce chiavi di crittografia ai programmi server che li richiedono.</span><span class="sxs-lookup"><span data-stu-id="10456-106">By default, the SSP supplies encryption keys to server programs that request them.</span></span> <span data-ttu-id="10456-107">Ogni SSP implementa il proprio sistema di generazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="10456-107">Each SSP implements its own system of generating keys.</span></span> <span data-ttu-id="10456-108">Il formato delle chiavi generate dal provider di servizi condivisi è specifico del provider di servizi condivisi.</span><span class="sxs-lookup"><span data-stu-id="10456-108">The format of the keys that the SSP generates are specific to the SSP.</span></span>

<span data-ttu-id="10456-109">RPC offre la possibilità di eseguire l'override del metodo predefinito di generazione delle chiavi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="10456-109">RPC provides you with the ability to override the default method of generating encryption keys.</span></span> <span data-ttu-id="10456-110">L'applicazione può chiamare la funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) e passargli un puntatore a una funzione di acquisizione della chiave.</span><span class="sxs-lookup"><span data-stu-id="10456-110">Your application can call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function and pass it a pointer to a key acquisition function.</span></span> <span data-ttu-id="10456-111">È possibile scrivere la funzione di acquisizione della chiave in modo che generi chiavi usando qualsiasi metodo scelto.</span><span class="sxs-lookup"><span data-stu-id="10456-111">You can write the key acquisition function so that it generates keys using any method you choose.</span></span> <span data-ttu-id="10456-112">Tuttavia, la chiave passata al programma server deve corrispondere al formato necessario per il provider di servizi condivisi.</span><span class="sxs-lookup"><span data-stu-id="10456-112">However, the key it passes to the server program must match the format that the SSP requires.</span></span>

> [!Note]  
> <span data-ttu-id="10456-113">Per la maggior parte delle applicazioni non è necessario usare funzioni di acquisizione chiavi e può semplicemente fornire **null** a tutti i parametri in cui è richiesta una funzione di acquisizione di chiavi.</span><span class="sxs-lookup"><span data-stu-id="10456-113">Most applications do not need to use key acquisition functions, and can simply supply **NULL** to all parameters where a key acquisition function is requested.</span></span>

 

 

 




