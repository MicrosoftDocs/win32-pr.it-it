---
description: Non è necessario un provider per supportare le operazioni di istanza parziale. Tuttavia, un provider deve supportare tutta la semantica di un'operazione di istanza parziale, elaborare un'istanza completa o restituire il parametro WBEM \_ E non \_ supportato \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Supporto di Partial-Instance operazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309874"
---
# <a name="supporting-partial-instance-operations"></a><span data-ttu-id="9db11-104">Supporto di Partial-Instance operazioni</span><span class="sxs-lookup"><span data-stu-id="9db11-104">Supporting Partial-Instance Operations</span></span>

<span data-ttu-id="9db11-105">Non è necessario un provider per supportare le operazioni di istanza parziale.</span><span class="sxs-lookup"><span data-stu-id="9db11-105">A provider is not required to support any partial-instance operations.</span></span> <span data-ttu-id="9db11-106">Tuttavia, un provider deve supportare tutta la semantica di un'operazione di istanza parziale, elaborare un'istanza completa o restituire il **parametro WBEM \_ E non \_ supportato \_**.</span><span class="sxs-lookup"><span data-stu-id="9db11-106">However, a provider must either support all the semantics of a partial-instance operation, process a complete instance, or return **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="9db11-107">Quando si crea un provider che supporta operazioni di istanza parziale, è necessario rispettare le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="9db11-107">When creating a provider that supports partial-instance operations, you must observe the following rules:</span></span>

-   <span data-ttu-id="9db11-108">Riutilizzare lo stesso oggetto di contesto inviato da WMI al provider.</span><span class="sxs-lookup"><span data-stu-id="9db11-108">Reuse the same context object that WMI sends to the provider.</span></span> <span data-ttu-id="9db11-109">WMI utilizza il \_ \_ \_ valore denominato "Get ext \_ client \_ Request" per evitare deadlock e rimuove il client prima di inviare l'oggetto di contesto a un provider.</span><span class="sxs-lookup"><span data-stu-id="9db11-109">WMI uses the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value to prevent deadlocks and removes this client before forwarding the context object to a provider.</span></span>
-   <span data-ttu-id="9db11-110">Per le chiamate rientranti in WMI che non richiedono un'operazione di istanza parziale, assicurarsi di passare di nuovo lo stesso oggetto di contesto senza alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="9db11-110">For reentrant calls back into WMI that do not require a partial-instance operation, ensure to pass back the same context object without any modifications.</span></span> <span data-ttu-id="9db11-111">WMI riceve l'oggetto di contesto senza il \_ \_ \_ valore denominato "Get ext \_ client \_ Request" impostato ed Elimina tutti i valori denominati associati a operazioni di istanze parziali dall'oggetto context prima di passarli ad altri provider.</span><span class="sxs-lookup"><span data-stu-id="9db11-111">WMI receives the context object without the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value set and deletes all named values associated with partial-instance operations from the context object before passing it to other providers.</span></span> <span data-ttu-id="9db11-112">La mancata modifica dell'oggetto context impedisce ad altri provider di ricevere operazioni di recupero di istanze parziali destinate a un oggetto diverso e non correlato.</span><span class="sxs-lookup"><span data-stu-id="9db11-112">Not changing the context object blocks other providers from receiving partial-instance retrieval operations intended for a different, unrelated object.</span></span>
-   <span data-ttu-id="9db11-113">Per eseguire un'operazione di istanza parziale rientrante durante l'esecuzione di una richiesta, impostare il \_ \_ \_ valore denominato "Get ext \_ client \_ Request" e la proprietà Clear.</span><span class="sxs-lookup"><span data-stu-id="9db11-113">To perform a reentrant partial-instance operation while carrying out a request, set the missing "\_\_GET\_EXT\_CLIENT\_REQUEST" named value and property clear.</span></span> <span data-ttu-id="9db11-114">Facoltativamente, è possibile modificare le proprietà nel \_ \_ \_ valore denominato "Get ext \_ Properties" prima di inviare di nuovo l'oggetto context a WMI con la chiamata rientrante.</span><span class="sxs-lookup"><span data-stu-id="9db11-114">Optionally, you can modify the properties in the "\_\_GET\_EXT\_PROPERTIES" named value before sending the context object back into WMI with the reentrant call.</span></span>
-   <span data-ttu-id="9db11-115">Non accedere all'oggetto di contesto dopo che è stato restituito a WMI durante una chiamata rientrante. è possibile che altri provider modifichino gli elenchi di proprietà o altri valori durante la rientranza.</span><span class="sxs-lookup"><span data-stu-id="9db11-115">Do not access the context object after you return it to WMI during a reentrant call; other providers may modify the property lists or other values during reentrancy.</span></span> <span data-ttu-id="9db11-116">È possibile esaminare o modificare l'oggetto contesto solo per la durata della chiamata [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) implementata.</span><span class="sxs-lookup"><span data-stu-id="9db11-116">You can examine or modify the context object only for the duration of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call that you implement.</span></span>

 

 



