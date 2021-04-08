---
title: Pubblicazione con il servizio nome RPC
description: I servizi RPC possono pubblicare i relativi identificatori in uno spazio dei nomi usando le API RpcNs (RPC Name Service).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Pubblicazione con il nome RPC servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046496"
---
# <a name="publishing-with-the-rpc-name-service"></a><span data-ttu-id="3e4e0-104">Pubblicazione con il servizio nome RPC</span><span class="sxs-lookup"><span data-stu-id="3e4e0-104">Publishing with the RPC Name Service</span></span>

<span data-ttu-id="3e4e0-105">I servizi RPC possono pubblicare i relativi identificatori in uno spazio dei nomi usando le API RpcNs (RPC Name Service).</span><span class="sxs-lookup"><span data-stu-id="3e4e0-105">RPC services can publish their identifiers in a namespace using the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="3e4e0-106">Le API RpcNs in Windows 2000 pubblicano le voci RPC in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-106">The RpcNs APIs in Windows 2000 publish the RPC entries in Active Directory Domain Services.</span></span> <span data-ttu-id="3e4e0-107">I servizi creano binding RPC e li pubblicano nello spazio dei nomi come voci del server RPC denominate con attributi che includono l'ID di interfaccia univoco, un GUID riconosciuto dai client.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-107">Services create RPC bindings and publish them in the namespace as named RPC Server entries with attributes including the unique interface ID, a GUID that is recognized by clients.</span></span> <span data-ttu-id="3e4e0-108">Un client può quindi cercare i server RPC che offrono l'interfaccia desiderata, importare l'associazione e connettersi al server.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-108">A client can then search for RPC Servers offering the desired interface, import the binding, and connect to the server.</span></span>

<span data-ttu-id="3e4e0-109">Per ulteriori informazioni sulla pubblicazione di un servizio RPC, vedere [Binding lato server](/windows/desktop/Rpc/server-side-binding).</span><span class="sxs-lookup"><span data-stu-id="3e4e0-109">For more information about publishing an RPC service, see [Server-side Binding](/windows/desktop/Rpc/server-side-binding).</span></span>

 

 