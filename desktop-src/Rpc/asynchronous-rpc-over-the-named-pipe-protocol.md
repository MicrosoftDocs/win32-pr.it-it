---
title: RPC asincrona sul protocollo Named-Pipe
description: Se si usa Named Pipes (ncacn \_ NP) come protocollo di trasporto, è consigliabile evitare di consentire un numero elevato di chiamate in sospeso sul server.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963381"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a><span data-ttu-id="ec826-103">RPC asincrona sul protocollo Named-Pipe</span><span class="sxs-lookup"><span data-stu-id="ec826-103">Asynchronous RPC over the Named-Pipe Protocol</span></span>

<span data-ttu-id="ec826-104">Se si usa Named Pipes ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) come protocollo di trasporto, è consigliabile evitare di consentire un numero elevato di chiamate in sospeso sul server.</span><span class="sxs-lookup"><span data-stu-id="ec826-104">If you use named pipes ([**ncacn\_np**](/windows/desktop/Midl/ncacn-np)) as your transport protocol, you should avoid allowing a large number of idle pending calls on the server.</span></span> <span data-ttu-id="ec826-105">Con Named Pipes, ogni client in attesa di una risposta avrà una lettura named pipe in sospeso sul server, ognuna delle quali richiede una certa quantità di memoria del kernel.</span><span class="sxs-lookup"><span data-stu-id="ec826-105">With named pipes, each client waiting for a reply will have a pending named pipe read on the server, each of which requires a certain amount of kernel memory.</span></span>

<span data-ttu-id="ec826-106">Ad esempio, non si desidera utilizzare una chiamata di notifica per un nuovo messaggio di posta elettronica con il trasporto named pipe, perché tale chiamata rimarrà in sospeso anche quando i client sono inattivi e la memoria kernel potrebbe essere esaurita.</span><span class="sxs-lookup"><span data-stu-id="ec826-106">For example, you would not want to use a notification call for new e-mail with the named-pipe transport, because such a call would remain pending even when clients are idle, and kernel memory could be depleted.</span></span> <span data-ttu-id="ec826-107">Si noti che questo non è un problema con gli altri protocolli orientati alla connessione, ad esempio [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).</span><span class="sxs-lookup"><span data-stu-id="ec826-107">Note that this is not a problem with the other connection-oriented protocols, such as [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp).</span></span>

<span data-ttu-id="ec826-108">Poiché le named pipe sono un protocollo di trasporto, l'applicazione può usarle specificando [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) come protocollo in un'associazione di stringa.</span><span class="sxs-lookup"><span data-stu-id="ec826-108">Since named pipes are a transport protocol, your application can use them by specifying [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) as the protocol in a string binding.</span></span> <span data-ttu-id="ec826-109">Per ulteriori informazioni sulle named pipe, vedere [Named Pipes](/windows/desktop/ipc/named-pipes).</span><span class="sxs-lookup"><span data-stu-id="ec826-109">For more information on named pipes, see [Named Pipes](/windows/desktop/ipc/named-pipes).</span></span> <span data-ttu-id="ec826-110">Per informazioni dettagliate sulla creazione di associazioni di stringa, vedere [uso di associazioni di stringa](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="ec826-110">For details on creating string bindings, see [Using String Bindings](finding-server-host-systems.md).</span></span>

 

 