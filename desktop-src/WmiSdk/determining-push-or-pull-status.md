---
description: È possibile modellare un provider di classi come provider push o pull, che specifica come un provider prevede di interagire con WMI.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Determinazione dello stato di push o pull
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310372"
---
# <a name="determining-push-or-pull-status"></a><span data-ttu-id="609c4-103">Determinazione dello stato di push o pull</span><span class="sxs-lookup"><span data-stu-id="609c4-103">Determining Push or Pull Status</span></span>

<span data-ttu-id="609c4-104">È possibile modellare un provider di classi come provider push o pull, che specifica come un provider prevede di interagire con WMI.</span><span class="sxs-lookup"><span data-stu-id="609c4-104">You can model a class provider as a push or pull provider, which specifies how a provider expects to interact with WMI.</span></span> <span data-ttu-id="609c4-105">I provider pull ricevono una richiesta da WMI e soddisfano la richiesta generando i dati in modo dinamico o recuperando i dati da una cache locale.</span><span class="sxs-lookup"><span data-stu-id="609c4-105">Pull providers receive a request from WMI and satisfy the request either by generating the data dynamically or retrieving it from a local cache.</span></span> <span data-ttu-id="609c4-106">I provider pull devono inoltre implementare un numero elevato di interfacce.</span><span class="sxs-lookup"><span data-stu-id="609c4-106">Pull providers also must implement a large number of interfaces.</span></span>

<span data-ttu-id="609c4-107">Un provider di pull genera in modo dinamico le definizioni delle classi.</span><span class="sxs-lookup"><span data-stu-id="609c4-107">A pull provider generates class definitions dynamically.</span></span> <span data-ttu-id="609c4-108">In genere, i dati gestiti da un provider di pull cambiano di frequente, richiedendo al provider di generare la classe in modo dinamico o recuperare la classe da una cache locale ogni volta che un'applicazione invia una richiesta.</span><span class="sxs-lookup"><span data-stu-id="609c4-108">Typically, the data managed by a pull provider changes frequently, requiring the provider to either generate the class dynamically or retrieve the class from a local cache whenever an application issues a request.</span></span> <span data-ttu-id="609c4-109">Un provider di pull deve implementare i propri meccanismi di recupero dati, cache e notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="609c4-109">A pull provider must implement its own data retrieval, cache, and event notification mechanisms.</span></span> <span data-ttu-id="609c4-110">Poiché la maggior parte dei provider è provider di pull, la documentazione in questo file presuppone che si stia compilando un provider di pull se non diversamente specificato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="609c4-110">Because most providers are pull providers, the documentation in this file assumes you are building a pull provider unless explicitly stated otherwise.</span></span>

<span data-ttu-id="609c4-111">WMI utilizza invece i dati nel repository WMI per gestire tutte le richieste di applicazioni per i provider di push.</span><span class="sxs-lookup"><span data-stu-id="609c4-111">In contrast, WMI uses data in the WMI repository to handle all application requests for push providers.</span></span> <span data-ttu-id="609c4-112">I provider di push utilizzano anche un minor numero di metodi di interfaccia e pertanto sono più facili da implementare.</span><span class="sxs-lookup"><span data-stu-id="609c4-112">Push providers also use fewer interface methods, and thus are easier to implement.</span></span> <span data-ttu-id="609c4-113">Un provider di push utilizza il repository WMI come area di archiviazione per ottenere informazioni sull'oggetto gestito e aggiorna tali informazioni solo durante l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="609c4-113">A push provider uses the WMI repository as a storage area for information on the managed object, and updates that information only during initialization.</span></span> <span data-ttu-id="609c4-114">Il provider di classi WDM incluso nella sezione WMI di Microsoft Windows Software Development Kit (SDK), ad esempio, è modellato come provider di push.</span><span class="sxs-lookup"><span data-stu-id="609c4-114">For example, the WDM class provider included in the WMI section of the Microsoft Windows Software Development Kit (SDK) is modeled as a push provider.</span></span>

<span data-ttu-id="609c4-115">Utilizzando il repository WMI come area di archiviazione, un provider di push ottiene i vantaggi seguenti rispetto a un provider di pull:</span><span class="sxs-lookup"><span data-stu-id="609c4-115">By using the WMI repository as a storage area, a push provider gains the following benefits over a pull provider:</span></span>

-   <span data-ttu-id="609c4-116">Non è necessario che il provider implementi una cache locale per archiviare i dati.</span><span class="sxs-lookup"><span data-stu-id="609c4-116">The provider does not need to implement a local cache to store data.</span></span>
-   <span data-ttu-id="609c4-117">Non è necessario che il provider supporti il recupero dei dati; il provider può invece avvalersi di WMI per fornire supporto per il recupero.</span><span class="sxs-lookup"><span data-stu-id="609c4-117">The provider does not need to support data retrieval; instead, the provider can rely on WMI to provide retrieval support.</span></span>
-   <span data-ttu-id="609c4-118">Quando un'applicazione richiede i dati forniti dal provider, WMI soddisfa la richiesta.</span><span class="sxs-lookup"><span data-stu-id="609c4-118">When an application requests data supplied by the provider, WMI fulfills that request.</span></span>
-   <span data-ttu-id="609c4-119">Il provider può inoltre basarsi su WMI per supportare la notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="609c4-119">The provider can also rely on WMI to support event notification.</span></span>

<span data-ttu-id="609c4-120">Tuttavia, poiché un provider di push viene aggiornato solo durante l'inizializzazione, le eventuali modifiche apportate a una classe potrebbero non essere riflesse nel repository WMI per un certo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="609c4-120">However, because a push provider updates only during initialization, any changes to a class may not be reflected in the WMI repository for some time.</span></span> <span data-ttu-id="609c4-121">Pertanto, il modello del provider di Push funziona meglio con le classi che cambiano poco o altrimenti sono completamente statiche.</span><span class="sxs-lookup"><span data-stu-id="609c4-121">Therefore, the push provider model works best with classes that change little or else are completely static.</span></span>

 

 



