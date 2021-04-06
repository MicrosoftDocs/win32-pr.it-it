---
title: Associazione di attributi ACF
description: Specificare il modo in cui il client si connette al server per le chiamate di procedure remote con gli attributi elencati nella tabella seguente.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- MIDL, attributi, associazione di ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045112"
---
# <a name="binding-acf-attributes"></a><span data-ttu-id="69a9f-104">Associazione di attributi ACF</span><span class="sxs-lookup"><span data-stu-id="69a9f-104">Binding ACF Attributes</span></span>

<span data-ttu-id="69a9f-105">Specificare il modo in cui il client si connette al server per le chiamate di procedure remote con gli attributi elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="69a9f-105">Specify how the client connects to the server for remote procedure calls with the attributes listed in the following table.</span></span>



| <span data-ttu-id="69a9f-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="69a9f-106">Attribute</span></span>                                                          | <span data-ttu-id="69a9f-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="69a9f-107">Usage</span></span>                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69a9f-108">**async**</span><span class="sxs-lookup"><span data-stu-id="69a9f-108">**async**</span></span>](async.md)                                             | <span data-ttu-id="69a9f-109">Definisce un handle che consente al chiamante di eseguire una chiamata asincrona e di restituire immediatamente un valore senza attendere i risultati, quindi di eseguire nuovamente la sincronizzazione con la funzione chiamata per ricevere i dati al termine della chiamata.</span><span class="sxs-lookup"><span data-stu-id="69a9f-109">Defines a handle that allows the caller to make an asynchronous call and return immediately without waiting for results, and then resynchronize with the called function to receive data after the call completes.</span></span> |
| [<span data-ttu-id="69a9f-110">**\_handle automatico**</span><span class="sxs-lookup"><span data-stu-id="69a9f-110">**auto\_handle**</span></span>](auto-handle.md)                                | <span data-ttu-id="69a9f-111">Indica a MIDL di consentire al codice dello stub di controllare automaticamente l'associazione.</span><span class="sxs-lookup"><span data-stu-id="69a9f-111">Tells MIDL to let the stub code control the binding automatically.</span></span> <span data-ttu-id="69a9f-112">Si tratta dell'impostazione predefinita se non si specifica alcun handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="69a9f-112">This is the default if you don't specify any binding handle.</span></span>                                                                                    |
| [<span data-ttu-id="69a9f-113">**gestore del contesto \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="69a9f-113">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md) | <span data-ttu-id="69a9f-114">Garantisce che un handle di contesto non verrà mai serializzato, indipendentemente dal comportamento predefinito dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69a9f-114">Guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>                                                                                                       |
| [<span data-ttu-id="69a9f-115">**\_serializzazione handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="69a9f-115">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)     | <span data-ttu-id="69a9f-116">Garantisce che un handle di contesto venga sempre serializzato, indipendentemente dal comportamento predefinito dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="69a9f-116">Guarantees that a context handle will always be serialized, regardless of the application's default behavior</span></span>                                                                                                       |
| [<span data-ttu-id="69a9f-117">**handle esplicito \_**</span><span class="sxs-lookup"><span data-stu-id="69a9f-117">**explicit\_handle**</span></span>](explicit-handle.md)                        | <span data-ttu-id="69a9f-118">Consente all'applicazione client di controllare l'associazione con un parametro esplicito in ogni routine.</span><span class="sxs-lookup"><span data-stu-id="69a9f-118">Lets the client application control the binding with an explicit parameter in each procedure.</span></span>                                                                                                                      |
| [<span data-ttu-id="69a9f-119">**handle implicito \_**</span><span class="sxs-lookup"><span data-stu-id="69a9f-119">**implicit\_handle**</span></span>](implicit-handle.md)                        | <span data-ttu-id="69a9f-120">Specifica un handle per le routine che non dispongono di un parametro di handle esplicito.</span><span class="sxs-lookup"><span data-stu-id="69a9f-120">Specifies a handle for procedures that do not have an explicit handle parameter.</span></span> <span data-ttu-id="69a9f-121">L'applicazione client controlla ancora l'associazione.</span><span class="sxs-lookup"><span data-stu-id="69a9f-121">The client application still controls the binding.</span></span>                                                                                |
| [<span data-ttu-id="69a9f-122">**\_handle di contesto Strict \_**</span><span class="sxs-lookup"><span data-stu-id="69a9f-122">**strict\_context\_handle**</span></span>](strict-context-handle.md)           | <span data-ttu-id="69a9f-123">Garantisce che i metodi dell'interfaccia accettino solo handle di contesto creati da un metodo di tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="69a9f-123">Guarantees that the methods in the interface will only accept context handles that were created by a method of that interface.</span></span>                                                                                     |



 

 

 




