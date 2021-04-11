---
title: Delega di QueryInterface
description: Delega di QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118510"
---
# <a name="delegation-of-queryinterface"></a><span data-ttu-id="19c1d-103">Delega di QueryInterface</span><span class="sxs-lookup"><span data-stu-id="19c1d-103">Delegation of QueryInterface</span></span>

<span data-ttu-id="19c1d-104">I gestori che richiedono l'accesso ad alcune interfacce interne di gestione proxy devono passare attraverso l'interfaccia [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) .</span><span class="sxs-lookup"><span data-stu-id="19c1d-104">Handlers that require access to some of the internal interfaces on the proxy manager have to go through the [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) interface.</span></span> <span data-ttu-id="19c1d-105">Ciò impedisce ai gestori di delegare in modo cieco ed esporre le interfacce interne dell'aggregazione al di fuori dell'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="19c1d-105">This prevents handlers from blindly delegating and exposing the aggregatee's internal interfaces outside of the aggregate.</span></span> <span data-ttu-id="19c1d-106">Queste interfacce includono [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span><span class="sxs-lookup"><span data-stu-id="19c1d-106">These interfaces include [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) and [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span></span> <span data-ttu-id="19c1d-107">Se il gestore vuole esporre **IClientSecurity** o **IMultiQI**, deve implementarli.</span><span class="sxs-lookup"><span data-stu-id="19c1d-107">If the handler wants to expose **IClientSecurity** or **IMultiQI**, it should implement them itself.</span></span>

<span data-ttu-id="19c1d-108">Nel caso di [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), se il client tenta di impostare la sicurezza su un'interfaccia esposta dal gestore, il gestore deve impostare la sicurezza sul proxy dell'interfaccia di rete sottostante.</span><span class="sxs-lookup"><span data-stu-id="19c1d-108">In the case of [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), if the client tries to set the security on an interface that the handler has exposed, the handler should set the security on the underlying network interface proxy.</span></span>

<span data-ttu-id="19c1d-109">Nel caso di [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), il gestore deve compilare le interfacce che conosce e quindi inviare la chiamata a gestione proxy per ottenere il resto delle interfacce compilate.</span><span class="sxs-lookup"><span data-stu-id="19c1d-109">In the case of [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), the handler should fill in the interfaces it knows about and then forward the call to the proxy manager to get the rest of the interfaces filled in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19c1d-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19c1d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19c1d-111">Gestore di Client-Side Lightweight</span><span class="sxs-lookup"><span data-stu-id="19c1d-111">The Lightweight Client-Side Handler</span></span>](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 