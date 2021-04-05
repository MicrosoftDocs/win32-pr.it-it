---
description: Le funzioni di installazione includono la funzionalità di Accodamento file.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Code di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967863"
---
# <a name="file-queues"></a><span data-ttu-id="e6232-103">Code di file</span><span class="sxs-lookup"><span data-stu-id="e6232-103">File Queues</span></span>

<span data-ttu-id="e6232-104">Le funzioni di installazione includono la funzionalità di Accodamento file.</span><span class="sxs-lookup"><span data-stu-id="e6232-104">The setup functions include file queue functionality.</span></span> <span data-ttu-id="e6232-105">Una coda di file è un elenco di operazioni di copia, ridenominazione ed eliminazione di file.</span><span class="sxs-lookup"><span data-stu-id="e6232-105">A file queue is a list of file copying, renaming, and deletion operations.</span></span> <span data-ttu-id="e6232-106">Queste operazioni possono essere inviate alla coda in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="e6232-106">These operations can be sent to the queue in any order.</span></span> <span data-ttu-id="e6232-107">Quando viene eseguito il commit della coda, le operazioni vengono elaborate come batch, in ordine di tipo di operazione.</span><span class="sxs-lookup"><span data-stu-id="e6232-107">When the queue is committed, these operations are processed as a batch, in order of the operation type.</span></span>

<span data-ttu-id="e6232-108">Nelle sezioni seguenti viene illustrata una coda e viene illustrato come utilizzarla quando si crea un'applicazione di installazione.</span><span class="sxs-lookup"><span data-stu-id="e6232-108">The following sections explain what a queue is and how to use it when creating a setup application.</span></span> <span data-ttu-id="e6232-109">Viene inoltre illustrato l'ordine in cui le operazioni di file accodate vengono elaborate durante il commit della coda e le notifiche inviate dalla coda a una routine di callback in ogni fase.</span><span class="sxs-lookup"><span data-stu-id="e6232-109">Also discussed is the order in which the enqueued file operations are processed as the queue commits and what notifications the queue sends to a callback routine at each stage.</span></span>

-   [<span data-ttu-id="e6232-110">Informazioni sulle code di file</span><span class="sxs-lookup"><span data-stu-id="e6232-110">About File Queues</span></span>](about-file-queues.md)
-   [<span data-ttu-id="e6232-111">Uso di code di file</span><span class="sxs-lookup"><span data-stu-id="e6232-111">Using File Queues</span></span>](using-file-queues.md)
-   [<span data-ttu-id="e6232-112">Riferimento alla coda di file</span><span class="sxs-lookup"><span data-stu-id="e6232-112">File Queue Reference</span></span>](file-queue-reference.md)

 

 



