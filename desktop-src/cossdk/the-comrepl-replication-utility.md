---
description: COMREPL è un'utilità che consente di replicare il catalogo COM+ da un computer di origine specifico a uno o più computer di destinazione.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: Utilità di replica COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966283"
---
# <a name="the-comrepl-replication-utility"></a><span data-ttu-id="6fcb8-103">Utilità di replica COMREPL</span><span class="sxs-lookup"><span data-stu-id="6fcb8-103">The COMREPL Replication Utility</span></span>

<span data-ttu-id="6fcb8-104">COMREPL è un'utilità che consente di replicare il catalogo COM+ da un computer di origine specifico a uno o più computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6fcb8-104">COMREPL is a utility that will replicate the COM+ catalog from a given source computer to one or more target computers.</span></span> <span data-ttu-id="6fcb8-105">Si pensi al computer di origine che rappresenta una "configurazione Master".</span><span class="sxs-lookup"><span data-stu-id="6fcb8-105">Think of the source computer representing a "master configuration."</span></span> <span data-ttu-id="6fcb8-106">COMREPL viene utilizzato per replicare questa configurazione Master per mantenere un set di computer configurati in modo identico.</span><span class="sxs-lookup"><span data-stu-id="6fcb8-106">COMREPL is used to replicate this master configuration to maintain a set of identically configured computers.</span></span>

<span data-ttu-id="6fcb8-107">L'unità di replica è l'intera configurazione COM+ nel computer master.</span><span class="sxs-lookup"><span data-stu-id="6fcb8-107">The unit of replication is the entire COM+ configuration on the master computer.</span></span> <span data-ttu-id="6fcb8-108">Tutte le applicazioni COM+ nel database master vengono replicate nei computer di destinazione. tutto o niente.</span><span class="sxs-lookup"><span data-stu-id="6fcb8-108">All COM+ applications on the master are replicated to the target computers; it's all or nothing.</span></span> <span data-ttu-id="6fcb8-109">Inoltre, tutte le applicazioni COM+ installate in precedenza nei computer di destinazione, ad eccezione delle applicazioni COM+ preinstallate, verranno eliminate come parte del processo di replica.</span><span class="sxs-lookup"><span data-stu-id="6fcb8-109">In addition, all COM+ applications previously installed on the target computers, with the exception of the COM+ preinstalled applications, will be deleted as part of the replication process.</span></span>

<span data-ttu-id="6fcb8-110">COMREPL replica solo i dati di configurazione COM+.</span><span class="sxs-lookup"><span data-stu-id="6fcb8-110">COMREPL replicates only COM+ configuration data.</span></span> <span data-ttu-id="6fcb8-111">Sono incluse le applicazioni COM+ e le impostazioni specifiche del computer COM+.</span><span class="sxs-lookup"><span data-stu-id="6fcb8-111">This includes COM+ applications and COM+ specific computer settings.</span></span> <span data-ttu-id="6fcb8-112">Microsoft Internet Information Services (IIS) ha un'utilità simile (IISSync) che usa COMREPL per replicare la configurazione di IIS e COM+.</span><span class="sxs-lookup"><span data-stu-id="6fcb8-112">Microsoft Internet Information Services (IIS) has a similar utility (IISSync), which makes use of COMREPL to replicate IIS and COM+ configuration.</span></span>

<span data-ttu-id="6fcb8-113">Per informazioni dettagliate sull'avvio e sull'uso di COMREPL, vedere gli argomenti seguenti in questa sezione:</span><span class="sxs-lookup"><span data-stu-id="6fcb8-113">For detailed information on launching and using COMREPL, see the following topics in this section:</span></span>

-   [<span data-ttu-id="6fcb8-114">Uso di COMREPL</span><span class="sxs-lookup"><span data-stu-id="6fcb8-114">Using COMREPL</span></span>](using-comrepl.md)
-   [<span data-ttu-id="6fcb8-115">Cosa viene replicato</span><span class="sxs-lookup"><span data-stu-id="6fcb8-115">What Gets Replicated</span></span>](what-gets-replicated.md)
-   [<span data-ttu-id="6fcb8-116">Fasi di replica</span><span class="sxs-lookup"><span data-stu-id="6fcb8-116">Replication Phases</span></span>](replication-phases.md)
-   [<span data-ttu-id="6fcb8-117">Gestione dei file</span><span class="sxs-lookup"><span data-stu-id="6fcb8-117">File Management</span></span>](file-management.md)
-   [<span data-ttu-id="6fcb8-118">Registrazione e segnalazione errori</span><span class="sxs-lookup"><span data-stu-id="6fcb8-118">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)

## <a name="related-topics"></a><span data-ttu-id="6fcb8-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fcb8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fcb8-120">Creazione di pacchetti di installazione per applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="6fcb8-120">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="6fcb8-121">Distribuzione di proxy di applicazione</span><span class="sxs-lookup"><span data-stu-id="6fcb8-121">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="6fcb8-122">Catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="6fcb8-122">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



