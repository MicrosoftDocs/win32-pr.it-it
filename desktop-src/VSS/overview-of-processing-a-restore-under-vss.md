---
description: Durante l'elaborazione di un backup in VSS, i richiedenti e i writer collaborano per produrre un'immagine di sistema stabile dalla quale eseguire il backup dei dati, il che richiede il coordinamento e la creazione di una copia shadow del sistema corrente.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Panoramica dell'elaborazione di un ripristino in VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310684"
---
# <a name="overview-of-processing-a-restore-under-vss"></a><span data-ttu-id="ce2d6-103">Panoramica dell'elaborazione di un ripristino in VSS</span><span class="sxs-lookup"><span data-stu-id="ce2d6-103">Overview of Processing a Restore Under VSS</span></span>

<span data-ttu-id="ce2d6-104">Durante l'elaborazione di un backup in VSS, i richiedenti e i writer collaborano per produrre un'immagine di sistema stabile dalla quale eseguire il backup dei dati, il che richiede il coordinamento e la creazione di una copia shadow del sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="ce2d6-104">In processing a backup under VSS, requesters and writers worked together to produce a stable system image from which to back up data, which required coordination and the creation of a shadow copy of the current system.</span></span>

<span data-ttu-id="ce2d6-105">A differenza di un backup VSS, in cui lo scopo del richiedente e il coordinamento dei writer è quello di produrre un'immagine di sistema stabile da cui copiare i dati, l'obiettivo di un ripristino basato su VSS consiste nel restituire i file su disco in modo più utile per le applicazioni (writer) attualmente in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ce2d6-105">In contrast to a VSS backup, where the purpose of requester and writers coordination is to produce a stable system image from which to copy data, the objective of a VSS-based restore is to return files to disk in a manner most useful to applications (writers) currently running on the system.</span></span> <span data-ttu-id="ce2d6-106">Questa operazione non richiede un'immagine di sistema stabile, quindi non è necessaria alcuna copia shadow.</span><span class="sxs-lookup"><span data-stu-id="ce2d6-106">This does not require a stable system image, so no shadow copy is necessary.</span></span>

<span data-ttu-id="ce2d6-107">Al contrario, l'attenzione è incentrata sulla prevenzione dell'attività del writer, sulla prevenzione della creazione di set di dati incoerenti sul disco e sulla possibilità per gli autori di valutare e unire i dati quando necessario.</span><span class="sxs-lookup"><span data-stu-id="ce2d6-107">Instead, attention is focused on avoiding disruption of writer activity, preventing the creation of inconsistent data sets on disk, and allowing writers the necessary scope to evaluate and merge data when necessary.</span></span>

<span data-ttu-id="ce2d6-108">Analogamente a un'operazione di backup, un ripristino VSS richiede l'accesso sia a un documento dei componenti di backup che ai documenti di metadati del writer.</span><span class="sxs-lookup"><span data-stu-id="ce2d6-108">Like a backup operation, a VSS restore requires access to both a Backup Components Document and to Writer Metadata Documents.</span></span> <span data-ttu-id="ce2d6-109">Questi documenti non vengono in genere ottenuti eseguendo una query sulle applicazioni in esecuzione, ma vengono recuperate da versioni archiviate come documenti XML nei supporti di backup.</span><span class="sxs-lookup"><span data-stu-id="ce2d6-109">These documents are not generally obtained by querying running applications, but instead are retrieved from versions stored as XML documents on backup media.</span></span>

<span data-ttu-id="ce2d6-110">Come nel caso delle operazioni di backup, i documenti dei metadati del writer rimangono oggetti di sola lettura e, una volta recuperati, il documento componenti di backup può comunque essere modificato.</span><span class="sxs-lookup"><span data-stu-id="ce2d6-110">As is the case during backup operations, the Writer Metadata Documents remain read-only objects, and (once retrieved) the Backup Components Document can still be modified.</span></span> <span data-ttu-id="ce2d6-111">Le modifiche del documento componenti di backup consentono a writer e richiedente di comunicare nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce2d6-111">Modifications of the Backup Components Document allow writers and requester to communicate about the following:</span></span>

-   <span data-ttu-id="ce2d6-112">Override dei [*metodi di ripristino*](vssgloss-r.md) con [*destinazioni Restore*](vssgloss-r.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d6-112">Overriding [*restore methods*](vssgloss-r.md) with [*restore targets*](vssgloss-r.md)</span></span>
-   <span data-ttu-id="ce2d6-113">Uso di [ *mapping di percorsi alternativi*](vssgloss-a.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d6-113">Using [*alternate location mappings*](vssgloss-a.md)</span></span>
-   <span data-ttu-id="ce2d6-114">Ripristino dei file nei nuovi percorsi sul disco</span><span class="sxs-lookup"><span data-stu-id="ce2d6-114">Restoring files to new locations on disk</span></span>
-   <span data-ttu-id="ce2d6-115">Uso di regole di selezione diverse da quelle usate durante il backup</span><span class="sxs-lookup"><span data-stu-id="ce2d6-115">Using different selection rules from those used during backup</span></span>

<span data-ttu-id="ce2d6-116">Per comprendere appieno le attività di base dell'esecuzione di un ripristino, è utile suddividere questa panoramica negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce2d6-116">To more fully understand the basic tasks involved in performing a restore, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="ce2d6-117">Panoramica dell'inizializzazione del ripristino</span><span class="sxs-lookup"><span data-stu-id="ce2d6-117">Overview of Restore Initialization</span></span>](overview-of-restore-initialization.md)
-   [<span data-ttu-id="ce2d6-118">Panoramica della preparazione per il ripristino</span><span class="sxs-lookup"><span data-stu-id="ce2d6-118">Overview of Preparing for Restore</span></span>](overview-of-preparing-for-restore.md)
-   [<span data-ttu-id="ce2d6-119">Panoramica del ripristino dei file effettivi</span><span class="sxs-lookup"><span data-stu-id="ce2d6-119">Overview of Actual File Restoration</span></span>](overview-of-actual-file-restoration.md)
-   [<span data-ttu-id="ce2d6-120">Panoramica della pulizia e della chiusura del ripristino</span><span class="sxs-lookup"><span data-stu-id="ce2d6-120">Overview of Restore Clean up and Termination</span></span>](overview-of-restore-clean-up-and-termination.md)

 

 



