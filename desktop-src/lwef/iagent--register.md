---
title: Registro IAgent
description: Registro IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856241"
---
# <a name="iagentregister"></a><span data-ttu-id="b034a-103">IAgent:: Register</span><span class="sxs-lookup"><span data-stu-id="b034a-103">IAgent::Register</span></span>

<span data-ttu-id="b034a-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b034a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

<span data-ttu-id="b034a-105">Registra un sink di notifica per l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="b034a-105">Registers a notification sink for the client application.</span></span>

-   <span data-ttu-id="b034a-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b034a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b034a-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="b034a-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="b034a-108">Indirizzo di [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) per l'interfaccia del sink di notifica.</span><span class="sxs-lookup"><span data-stu-id="b034a-108">Address of [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) for your notification sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="b034a-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span><span class="sxs-lookup"><span data-stu-id="b034a-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="b034a-110">Indirizzo dell'ID sink di notifica (utilizzato per annullare la registrazione del sink di notifica).</span><span class="sxs-lookup"><span data-stu-id="b034a-110">Address of notification sink ID (used to unregister the notification sink).</span></span>

</dd> </dl>

<span data-ttu-id="b034a-111">Per ricevere gli eventi dal server Microsoft Agent, è necessario registrare il sink di notifica (noto anche come sink di notifica o sink di evento).</span><span class="sxs-lookup"><span data-stu-id="b034a-111">You need to register your notification sink (also known as a notify sink or event sink) to receive events from the Microsoft Agent server.</span></span>

## <a name="see-also"></a><span data-ttu-id="b034a-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b034a-112">See Also</span></span>

[<span data-ttu-id="b034a-113">**IAgent:: Annulla registrazione**</span><span class="sxs-lookup"><span data-stu-id="b034a-113">**IAgent::Unregister**</span></span>](iagent--unregister.md)


 

 




