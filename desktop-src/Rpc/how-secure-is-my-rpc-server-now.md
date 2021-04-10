---
title: Sicurezza del server RPC
description: Seguendo le procedure di sicurezza descritte in questa sezione, fornite altrove in RPC SDK e generalmente accettate come procedure di sicurezza appropriate, comporterà un server molto sicuro. Tali server sono protetti da attacchi di penetrazione o violazioni della privacy.
ms.assetid: 528ff35c-f37c-43d8-8cc1-dbc36a9a826c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34279e4fb8899db6b7e980a0e868e91c6edb8166
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955521"
---
# <a name="how-secure-is-my-rpc-server-now"></a><span data-ttu-id="fd938-104">Quanto è sicuro il server RPC?</span><span class="sxs-lookup"><span data-stu-id="fd938-104">How Secure is My RPC Server Now?</span></span>

<span data-ttu-id="fd938-105">Seguendo le procedure di sicurezza descritte in questa sezione, fornite altrove in RPC SDK e generalmente accettate come procedure di sicurezza appropriate, comporterà un server molto sicuro.</span><span class="sxs-lookup"><span data-stu-id="fd938-105">Following the security outlined in this section, provided elsewhere in the RPC SDK, and generally accepted as proper security practices, will result in a server that is very secure.</span></span> <span data-ttu-id="fd938-106">Tali server sono protetti da attacchi di penetrazione o violazioni della privacy.</span><span class="sxs-lookup"><span data-stu-id="fd938-106">Such servers are protected from penetration attacks or privacy breaches.</span></span>

<span data-ttu-id="fd938-107">Se lo stato viene mantenuto tra le chiamate RPC, assicurarsi che un singolo client non provochi l'allocazione di risorse eccessive che potrebbero potenzialmente negare il servizio ad altri client.</span><span class="sxs-lookup"><span data-stu-id="fd938-107">If state is kept between RPC calls, make sure a single client does not cause the allocation of excessive resources, which could potentially deny service to other clients.</span></span>

 

 




