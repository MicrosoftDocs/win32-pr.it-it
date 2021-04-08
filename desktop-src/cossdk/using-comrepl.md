---
description: Uso di COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Uso di COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748639"
---
# <a name="using-comrepl"></a><span data-ttu-id="7f78f-103">Uso di COMREPL</span><span class="sxs-lookup"><span data-stu-id="7f78f-103">Using COMREPL</span></span>

<span data-ttu-id="7f78f-104">Per avviare l'utilità da riga di comando COMREPL, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="7f78f-104">To launch the COMREPL command line utility, use the following steps:</span></span>

1.  <span data-ttu-id="7f78f-105">Aggiungere% windir% \\ system32 \\ com al percorso dell'ambiente predefinito digitando quanto segue nel prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="7f78f-105">Add %windir%\\system32\\Com to the default environment path by typing the following in the command prompt:</span></span>

    <span data-ttu-id="7f78f-106">**set PATH =% PATH%;% WINDIR% \\ system32 \\ com**</span><span class="sxs-lookup"><span data-stu-id="7f78f-106">**set path = %PATH%;%windir%\\system32\\Com**</span></span>

2.  <span data-ttu-id="7f78f-107">Immettere il comando COMREPL seguente:</span><span class="sxs-lookup"><span data-stu-id="7f78f-107">Enter the following COMREPL command:</span></span>

    <span data-ttu-id="7f78f-108">**Comrepl** *sourceComputer* *targetComputerList* **\[ \[ /n \] /v \]**</span><span class="sxs-lookup"><span data-stu-id="7f78f-108">**COMREPL** *sourceComputer* *targetComputerList* **\[/n \[/v\]\]**</span></span>

    <span data-ttu-id="7f78f-109">dove:</span><span class="sxs-lookup"><span data-stu-id="7f78f-109">where:</span></span>

    -   <span data-ttu-id="7f78f-110">*sourceComputer* è il nome del computer di origine</span><span class="sxs-lookup"><span data-stu-id="7f78f-110">*sourceComputer* is the computer name of the source</span></span>

    -   <span data-ttu-id="7f78f-111">*targetComputerList* è il nome computer delle destinazioni separate da spazi</span><span class="sxs-lookup"><span data-stu-id="7f78f-111">*targetComputerList* is the computer names of the targets separated by spaces</span></span>

    -   <span data-ttu-id="7f78f-112">**/n** disattiva la richiesta di conferma prima di avviare la replica</span><span class="sxs-lookup"><span data-stu-id="7f78f-112">**/n** suppresses confirmation prompt before starting replication</span></span>

    -   <span data-ttu-id="7f78f-113">**/v** restituisce l'output del file di log alla console</span><span class="sxs-lookup"><span data-stu-id="7f78f-113">**/v** echoes log file output to the console</span></span>

## <a name="notes"></a><span data-ttu-id="7f78f-114">Note</span><span class="sxs-lookup"><span data-stu-id="7f78f-114">Notes</span></span>

-   <span data-ttu-id="7f78f-115">Poiché COM+ non viene replicato (solo dati di configurazione e applicazioni), in tutti i computer di destinazione deve essere già installato COM+.</span><span class="sxs-lookup"><span data-stu-id="7f78f-115">Because COM+ is not replicated (only configuration data and applications), all target computers must already have COM+ installed.</span></span>
-   <span data-ttu-id="7f78f-116">L'utente deve passare i controlli dei ruoli per l'applicazione di sistema nei computer di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7f78f-116">The user must pass role checks for the system application on both the source and the target computers.</span></span>
-   <span data-ttu-id="7f78f-117">Non sono stati replicati account computer locali che possono essere utilizzati dai ruoli.</span><span class="sxs-lookup"><span data-stu-id="7f78f-117">No local machine accounts that may be used by roles are replicated.</span></span>
-   <span data-ttu-id="7f78f-118">I computer di destinazione devono essere online.</span><span class="sxs-lookup"><span data-stu-id="7f78f-118">The target computer(s) must be online.</span></span>
-   <span data-ttu-id="7f78f-119">L'utente è responsabile della replica di tutti i dati non COM (ad esempio, tabelle di database, file di dati e così via) nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7f78f-119">The user is responsible for replicating all non-COM+ data (for example, database tables, data files, and so forth) to the target computer(s).</span></span>
-   <span data-ttu-id="7f78f-120">I cluster possono partecipare alla replica, ma si noti che COMREPL viene replicato solo in computer denominati.</span><span class="sxs-lookup"><span data-stu-id="7f78f-120">Clusters can participate in replication, but note that COMREPL replicates only to named computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f78f-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f78f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f78f-122">Gestione dei file</span><span class="sxs-lookup"><span data-stu-id="7f78f-122">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="7f78f-123">Registrazione e segnalazione errori</span><span class="sxs-lookup"><span data-stu-id="7f78f-123">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="7f78f-124">Fasi di replica</span><span class="sxs-lookup"><span data-stu-id="7f78f-124">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="7f78f-125">Cosa viene replicato</span><span class="sxs-lookup"><span data-stu-id="7f78f-125">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



