---
title: Handle con binding completo e parziale
description: Quando si usano gli endpoint dinamici, le librerie di runtime ottengono le informazioni sull'endpoint in modo necessario.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471323"
---
# <a name="fully-and-partially-bound-handles"></a><span data-ttu-id="5c0c4-103">Handle con binding completo e parziale</span><span class="sxs-lookup"><span data-stu-id="5c0c4-103">Fully and Partially Bound Handles</span></span>

<span data-ttu-id="5c0c4-104">Quando si usano gli endpoint dinamici, le librerie di runtime ottengono le informazioni sull'endpoint in modo necessario.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-104">When you use dynamic endpoints, the run-time libraries obtain endpoint information as they need it.</span></span> <span data-ttu-id="5c0c4-105">Le librerie di runtime fanno distinzione tra un *handle completamente associato* (uno che include informazioni sull'endpoint) e un *handle parzialmente associato* (uno che non include informazioni sull'endpoint).</span><span class="sxs-lookup"><span data-stu-id="5c0c4-105">The run-time libraries make the distinction between a *fully bound handle* (one that includes endpoint information) and a *partially bound handle* (one that does not include endpoint information).</span></span>

<span data-ttu-id="5c0c4-106">La libreria di runtime del client deve convertire l'handle parzialmente associato in un handle completamente associato prima che il client possa essere associato al server.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-106">The client run-time library must convert the partially bound handle to a fully bound handle before the client can bind to the server.</span></span> <span data-ttu-id="5c0c4-107">La libreria di runtime del client tenta di convertire l'handle parzialmente associato per l'applicazione client ottenendo le informazioni sull'endpoint come illustrato:</span><span class="sxs-lookup"><span data-stu-id="5c0c4-107">The client run-time library tries to convert the partially bound handle for the client application by obtaining the endpoint information as shown:</span></span>

-   <span data-ttu-id="5c0c4-108">Dalla specifica di interfaccia del client</span><span class="sxs-lookup"><span data-stu-id="5c0c4-108">From the client's interface specification</span></span>
-   <span data-ttu-id="5c0c4-109">Da un servizio di mapping degli endpoint in esecuzione nel server</span><span class="sxs-lookup"><span data-stu-id="5c0c4-109">From an endpoint-mapping service running on the server</span></span>

<span data-ttu-id="5c0c4-110">Se il client tenta di utilizzare un handle parzialmente associato quando le informazioni sull'endpoint non sono disponibili nella specifica dell'interfaccia e l'endpoint mapper del server non dispone di informazioni sull'endpoint server, il client non dispone di informazioni sufficienti per eseguire la chiamata di procedura remota e la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-110">If the client tries to use a partially bound handle when the endpoint information is not available in the interface specification and the server's endpoint-mapper does not have information about the server endpoint, the client will not have enough information to make its remote procedure call and that call will fail.</span></span> <span data-ttu-id="5c0c4-111">Per evitare questo problema, è necessario registrare l'endpoint nel mapper di endpoint quando l'applicazione distribuita utilizza handle parzialmente associati.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-111">To prevent this, you must register the endpoint in the endpoint mapper when your distributed application uses partially bound handles.</span></span> <span data-ttu-id="5c0c4-112">Per ulteriori informazioni sul mapper di endpoint, vedere [specifica di endpoint dinamici](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="5c0c4-112">For more information about the endpoint mapper, see [Specifying Dynamic Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="5c0c4-113">Quando una chiamata di procedura remota ha esito negativo, l'applicazione client può chiamare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) per rimuovere informazioni sull'endpoint non aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-113">When a remote procedure call fails, the client application can call [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) to remove out-of-date endpoint information.</span></span> <span data-ttu-id="5c0c4-114">Quando il client tenta di chiamare la procedura remota, la libreria di runtime del client tenta nuovamente di convertire l'handle completamente associato in un handle parzialmente associato.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-114">When the client tries to call the remote procedure, the client run-time library again tries to convert the fully bound handle to a partially bound handle.</span></span> <span data-ttu-id="5c0c4-115">Questa operazione è utile quando il server è stato arrestato e riavviato utilizzando un endpoint dinamico diverso.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-115">This is useful when the server has been stopped and restarted using a different dynamic endpoint.</span></span>

 

 




