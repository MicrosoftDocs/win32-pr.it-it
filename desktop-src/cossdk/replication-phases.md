---
description: COMREPL funziona in tre fasi.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Fasi di replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305210"
---
# <a name="replication-phases"></a><span data-ttu-id="7c35f-103">Fasi di replica</span><span class="sxs-lookup"><span data-stu-id="7c35f-103">Replication Phases</span></span>

<span data-ttu-id="7c35f-104">COMREPL funziona in tre fasi.</span><span class="sxs-lookup"><span data-stu-id="7c35f-104">COMREPL does its work in three phases.</span></span> <span data-ttu-id="7c35f-105">Il processo di replica è suddiviso in fasi distinte per i due motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c35f-105">The replication process is divided into distinct phases for the following two reasons:</span></span>

-   <span data-ttu-id="7c35f-106">Per separare il lavoro svolto per preparare l'origine dal lavoro eseguito in ogni destinazione</span><span class="sxs-lookup"><span data-stu-id="7c35f-106">To separate work done to prepare the source from work that is done on each target</span></span>
-   <span data-ttu-id="7c35f-107">Per ritardare la modifica della destinazione fino a quando tutti i dati non sono stati acquisiti dall'origine</span><span class="sxs-lookup"><span data-stu-id="7c35f-107">To delay modification of the target until all data has been acquired from the source</span></span>

<span data-ttu-id="7c35f-108">Di seguito sono riportate le fasi di replica.</span><span class="sxs-lookup"><span data-stu-id="7c35f-108">The replication phases are as follows.</span></span>



| <span data-ttu-id="7c35f-109">Fase</span><span class="sxs-lookup"><span data-stu-id="7c35f-109">Phase</span></span>         | <span data-ttu-id="7c35f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c35f-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c35f-111">Fase preparatoria</span><span class="sxs-lookup"><span data-stu-id="7c35f-111">Prepare phase</span></span> | <span data-ttu-id="7c35f-112">Esporta tutte le applicazioni installate localmente nel computer di origine.</span><span class="sxs-lookup"><span data-stu-id="7c35f-112">Exports all the installed applications locally on the source computer.</span></span> <span data-ttu-id="7c35f-113">Questa fase non tocca la configurazione di alcuna destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c35f-113">This phase does not touch the configuration of any targets.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7c35f-114">Fase di copia</span><span class="sxs-lookup"><span data-stu-id="7c35f-114">Copy phase</span></span>    | <span data-ttu-id="7c35f-115">Copia i dati in un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c35f-115">Copies data to a target computer.</span></span> <span data-ttu-id="7c35f-116">Tutte le applicazioni esportate nell'origine vengono copiate nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c35f-116">All applications exported on the source are copied to the target.</span></span> <span data-ttu-id="7c35f-117">Si tratta di un'operazione di copia file.</span><span class="sxs-lookup"><span data-stu-id="7c35f-117">This is a file copy operation.</span></span> <span data-ttu-id="7c35f-118">Vedere [Gestione file](file-management.md). Questo passaggio acquisisce anche alcuni dati dal computer di origine che non è incapsulato all'interno dei file dell'applicazione esportati, ad esempio le identità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c35f-118">(See [File Management](file-management.md).) This step also acquires some data from the source computer that is not encapsulated within exported application files (for example, application identities).</span></span> <span data-ttu-id="7c35f-119">Questi dati vengono conservati in memoria all'interno di COMREPL.</span><span class="sxs-lookup"><span data-stu-id="7c35f-119">This data is held in memory within COMREPL.</span></span> <span data-ttu-id="7c35f-120">Questa fase non tocca la configurazione dei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c35f-120">This phase does not touch the configuration of any target computers.</span></span>                                                                               |
| <span data-ttu-id="7c35f-121">Fase di installazione</span><span class="sxs-lookup"><span data-stu-id="7c35f-121">Install phase</span></span> | <span data-ttu-id="7c35f-122">Installa il catalogo di origine in un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c35f-122">Installs source catalog on a target computer.</span></span> <span data-ttu-id="7c35f-123">Quando questo passaggio viene avviato, tutti i dati necessari per riconfigurare la destinazione si trovano all'interno dei file dell'applicazione nella file system della destinazione o vengono mantenuti come dati di istanza all'interno di COMREPL.</span><span class="sxs-lookup"><span data-stu-id="7c35f-123">When this step is initiated, all data required to reconfigure the target is within application files in the target's file system or is held as instance data within COMREPL.</span></span> <span data-ttu-id="7c35f-124">Questa fase eliminerà tutte le applicazioni installate nella destinazione (ad eccezione delle applicazioni descritte in [ciò che viene replicato](what-gets-replicated.md)) prima di installare le applicazioni copiate dall'origine.</span><span class="sxs-lookup"><span data-stu-id="7c35f-124">This phase will delete all the installed applications on the target (except the applications described in [What Gets Replicated](what-gets-replicated.md)) prior to installing the applications copied from the source.</span></span> <span data-ttu-id="7c35f-125">COMREPL viene installato su più destinazioni contemporaneamente usando un thread di installazione per destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c35f-125">COMREPL installs on multiple targets concurrently by using an install thread per target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7c35f-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c35f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c35f-127">Gestione dei file</span><span class="sxs-lookup"><span data-stu-id="7c35f-127">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="7c35f-128">Registrazione e segnalazione errori</span><span class="sxs-lookup"><span data-stu-id="7c35f-128">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="7c35f-129">Uso di COMREPL</span><span class="sxs-lookup"><span data-stu-id="7c35f-129">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="7c35f-130">Cosa viene replicato</span><span class="sxs-lookup"><span data-stu-id="7c35f-130">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



