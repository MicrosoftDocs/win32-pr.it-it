---
description: Dopo aver creato un file INF, in genere si scriverà il codice sorgente per l'applicazione di installazione. È possibile chiamare le funzioni di installazione dell'applicazione di installazione per eseguire numerose operazioni di installazione.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Creazione di applicazioni di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314661"
---
# <a name="creating-setup-applications"></a><span data-ttu-id="7c204-104">Creazione di applicazioni di installazione</span><span class="sxs-lookup"><span data-stu-id="7c204-104">Creating Setup Applications</span></span>

<span data-ttu-id="7c204-105">Dopo aver creato un file INF, in genere si scriverà il codice sorgente per l'applicazione di installazione.</span><span class="sxs-lookup"><span data-stu-id="7c204-105">After you create an INF file, you will typically write the source code for your setup application.</span></span> <span data-ttu-id="7c204-106">È possibile chiamare le funzioni di installazione dell'applicazione di installazione per eseguire numerose operazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="7c204-106">You call the setup functions from your setup application to perform many installation operations.</span></span>

<span data-ttu-id="7c204-107">I passaggi seguenti illustrano come usare le funzioni di installazione per creare un'applicazione di installazione.</span><span class="sxs-lookup"><span data-stu-id="7c204-107">The following steps cover one way to use the setup functions to create a setup application.</span></span> <span data-ttu-id="7c204-108">È possibile usare questo esempio come punto di partenza o sviluppare un algoritmo di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7c204-108">You can use this example as a starting point, or develop your own installation algorithm.</span></span>

<span data-ttu-id="7c204-109">**Inizializzazione**</span><span class="sxs-lookup"><span data-stu-id="7c204-109">**Initialization**</span></span>

-   [<span data-ttu-id="7c204-110">Aprire il file INF e, se necessario, aggiungere altri file INF.</span><span class="sxs-lookup"><span data-stu-id="7c204-110">Open the INF and, if appropriate, append other INF files.</span></span>](opening-the-inf-file.md)
-   [<span data-ttu-id="7c204-111">Estrarre le informazioni sul file dal file INF.</span><span class="sxs-lookup"><span data-stu-id="7c204-111">Extract file information from the INF file.</span></span>](extracting-file-information-from-the-inf-file.md)
-   [<span data-ttu-id="7c204-112">Raccogliere le informazioni di installazione dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7c204-112">Gather setup information from the user.</span></span>](gathering-setup-information-from-the-user.md)
-   [<span data-ttu-id="7c204-113">Creare una coda.</span><span class="sxs-lookup"><span data-stu-id="7c204-113">Create a queue.</span></span>](creating-a-queue-and-queuing-file-operations.md)

<span data-ttu-id="7c204-114">**Installa file**</span><span class="sxs-lookup"><span data-stu-id="7c204-114">**Install files**</span></span>

-   [<span data-ttu-id="7c204-115">Eseguire il commit della coda, specificando una routine di callback.</span><span class="sxs-lookup"><span data-stu-id="7c204-115">Commit the queue, specifying a callback routine.</span></span>](committing-the-queue.md)
-   [<span data-ttu-id="7c204-116">Aggiornare le informazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7c204-116">Update registry information.</span></span>](updating-registry-information.md)

<span data-ttu-id="7c204-117">**Eseguire la pulizia**</span><span class="sxs-lookup"><span data-stu-id="7c204-117">**Clean up**</span></span>

-   [<span data-ttu-id="7c204-118">Chiudere la coda di file e il file INF.</span><span class="sxs-lookup"><span data-stu-id="7c204-118">Close the file queue and INF.</span></span>](closing-the-file-queue-and-inf-file.md)
-   [<span data-ttu-id="7c204-119">Rilasciare tutte le altre risorse di sistema e terminare il programma.</span><span class="sxs-lookup"><span data-stu-id="7c204-119">Release any other system resources and end the program.</span></span>](releasing-other-system-resources.md)

 

 



