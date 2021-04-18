---
description: Un richiedente crea un documento di componenti di backup all'inizio dell'esecuzione di un backup.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Utilizzo del documento componenti di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307121"
---
# <a name="working-with-the-backup-components-document"></a><span data-ttu-id="d9e99-103">Utilizzo del documento componenti di backup</span><span class="sxs-lookup"><span data-stu-id="d9e99-103">Working with the Backup Components Document</span></span>

<span data-ttu-id="d9e99-104">Un richiedente crea un documento di componenti di backup all'inizio dell'esecuzione di un backup.</span><span class="sxs-lookup"><span data-stu-id="d9e99-104">A requester creates a Backup Components Document at the start of performing a backup.</span></span> <span data-ttu-id="d9e99-105">Il documento contiene inizialmente solo una descrizione dello stato dell'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="d9e99-105">The document initially contains only a description of the state of the backup operation.</span></span> <span data-ttu-id="d9e99-106">Durante il ripristino, nel documento devono essere fornite istruzioni sul modo in cui un richiedente deve procedere alla copia dei file sul disco.</span><span class="sxs-lookup"><span data-stu-id="d9e99-106">During restore, the document should provide instructions on how a requester should proceed in copying files back to disk.</span></span> <span data-ttu-id="d9e99-107">Nel corso dell'operazione di ripristino, il documento componenti di backup viene modificato e contiene lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d9e99-107">In the course of the restore operation, the Backup Components Document is modified and contains the state of that operation.</span></span>

<span data-ttu-id="d9e99-108">Diversamente dal documento di metadati del writer, che è di sola lettura, è presente una finestra in cui il documento dei componenti di backup può essere modificato da richiedenti e writer.</span><span class="sxs-lookup"><span data-stu-id="d9e99-108">Unlike the Writer Metadata Document, which is read-only, there is a window in which the Backup Components Document can be modified by both requesters and writers.</span></span> <span data-ttu-id="d9e99-109">Il documento può essere aggiornato fino alla generazione di un evento [*BackupComplete*](vssgloss-b.md) o [*BackupShutdown*](vssgloss-b.md) durante le operazioni di backup e fino a quando non viene eseguito il ripristino di un evento [*PostRestore*](vssgloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e99-109">The document can be updated until the generation of a [*BackupComplete*](vssgloss-b.md) or [*BackupShutdown*](vssgloss-b.md) event during backup operations, and until a [*PostRestore*](vssgloss-p.md) event during restores.</span></span>

<span data-ttu-id="d9e99-110">Per utilizzare il documento dei componenti di backup di un richiedente è necessario conoscere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9e99-110">To use a requester's Backup Components Document requires an understanding of the following topics:</span></span>

-   [<span data-ttu-id="d9e99-111">Ciclo di vita del documento dei componenti di backup</span><span class="sxs-lookup"><span data-stu-id="d9e99-111">Backup Components Document Life Cycle</span></span>](backup-components-document-life-cycle.md)
-   [<span data-ttu-id="d9e99-112">Contenuto del documento dei componenti di backup</span><span class="sxs-lookup"><span data-stu-id="d9e99-112">Backup Components Document Contents</span></span>](backup-components-document-contents.md)

 

 



