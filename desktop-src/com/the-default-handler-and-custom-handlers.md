---
title: Gestore predefinito e gestori personalizzati
description: Gestore predefinito e gestori personalizzati
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955293"
---
# <a name="the-default-handler-and-custom-handlers"></a><span data-ttu-id="e2416-103">Gestore predefinito e gestori personalizzati</span><span class="sxs-lookup"><span data-stu-id="e2416-103">The Default Handler and Custom Handlers</span></span>

<span data-ttu-id="e2416-104">Il gestore predefinito, un'implementazione fornita da OLE, viene usato dalla maggior parte delle applicazioni come gestore.</span><span class="sxs-lookup"><span data-stu-id="e2416-104">The default handler, an implementation provided by OLE, is used by most applications as the handler.</span></span> <span data-ttu-id="e2416-105">Un'applicazione implementa un gestore personalizzato quando le funzionalità del gestore predefinite non sono sufficienti.</span><span class="sxs-lookup"><span data-stu-id="e2416-105">An application implements a custom handler when the default handler's capabilities are insufficient.</span></span> <span data-ttu-id="e2416-106">Un gestore personalizzato può sostituire completamente il gestore predefinito o usare parti della funzionalità che fornisce laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="e2416-106">A custom handler can either completely replace the default handler or use parts of the functionality it provides where appropriate.</span></span> <span data-ttu-id="e2416-107">Nel secondo caso, il gestore dell'applicazione viene implementato come un oggetto aggregato costituito da un nuovo oggetto controllo e dal gestore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e2416-107">In the latter case, the application handler is implemented as an aggregate object composed of a new control object and the default handler.</span></span> <span data-ttu-id="e2416-108">I gestori di applicazione/predefiniti combinati sono noti anche come *gestori in-process*.</span><span class="sxs-lookup"><span data-stu-id="e2416-108">Combination application/default handlers are also known as *in-process handlers*.</span></span> <span data-ttu-id="e2416-109">Il *gestore di comunicazione remota* viene usato per gli oggetti a cui non è assegnato un CLSID nel registro di sistema o che non hanno alcun gestore specificato.</span><span class="sxs-lookup"><span data-stu-id="e2416-109">The *remoting handler* is used for objects that are not assigned a CLSID in the system registry or that have no specified handler.</span></span> <span data-ttu-id="e2416-110">Tutto ciò che è necessario da un gestore per questi tipi di oggetti è che passano informazioni attraverso il limite del processo.</span><span class="sxs-lookup"><span data-stu-id="e2416-110">All that is required from a handler for these types of objects is that they pass information across the process boundary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2416-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2416-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2416-112">Gestori di oggetti</span><span class="sxs-lookup"><span data-stu-id="e2416-112">Object Handlers</span></span>](object-handlers.md)
</dt> </dl>

 

 




