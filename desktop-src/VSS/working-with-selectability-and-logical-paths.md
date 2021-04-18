---
description: La partecipazione di un writer a un'operazione di backup o ripristino e i relativi dati vengono salvati, a seconda di quali componenti sono inclusi in modo esplicito come parte del documento dei componenti di backup del richiedente e della relazione tra tali componenti e il percorso logico di altri componenti all'interno del documento di metadati del writer.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Uso della selezione e dei percorsi logici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307123"
---
# <a name="working-with-selectability-and-logical-paths"></a><span data-ttu-id="79a28-103">Uso della selezione e dei percorsi logici</span><span class="sxs-lookup"><span data-stu-id="79a28-103">Working with Selectability and Logical Paths</span></span>

<span data-ttu-id="79a28-104">La partecipazione di un writer a un'operazione di backup o ripristino e i relativi dati vengono salvati, a seconda di quali componenti sono inclusi in [*modo esplicito*](vssgloss-e.md) come parte del documento dei componenti di backup del richiedente e della relazione tra tali componenti e il percorso logico di altri componenti all'interno del documento di metadati del writer.</span><span class="sxs-lookup"><span data-stu-id="79a28-104">A writer's participation in a backup or restore operation, and which of its data are saved, depends on which of its components are [*explicitly included*](vssgloss-e.md) as part of a requester's Backup Components Document and the relationship between those components and the logical path of other components within the Writer Metadata Document.</span></span>

<span data-ttu-id="79a28-105">I writer senza componenti aggiunti al documento del componente di backup di un richiedente prima della generazione di un evento [*PrepareForBackup*](vssgloss-p.md) (nel caso di operazioni di backup) o di un evento di [**preripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (in caso di operazioni di ripristino) non ricevono eventi dopo questo punto e non parteciperanno all'operazione di backup o ripristino.</span><span class="sxs-lookup"><span data-stu-id="79a28-105">Writers with no components added to a requester's Backup Component Document prior to the generation of a [*PrepareForBackup*](vssgloss-p.md) event (in the case of backup operations) or of a [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) event (in the case of restore operations) receive no events after this point and will not participate in the backup or restore operation.</span></span>

<span data-ttu-id="79a28-106">Tuttavia, la libertà di un richiedente di includere o escludere un determinato componente in un backup o un ripristino è regolata dai seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="79a28-106">However, a requester's freedom to include or exclude any given component in a backup or restore is governed by the following:</span></span>

-   <span data-ttu-id="79a28-107">Qualsiasi gerarchia esistente tra i componenti gestiti da un writer ed espressi da [ *percorsi logici*](vssgloss-l.md)</span><span class="sxs-lookup"><span data-stu-id="79a28-107">Any hierarchy that exists between the components managed by a writer and expressed by [*logical paths*](vssgloss-l.md)</span></span>
-   <span data-ttu-id="79a28-108">Indica se il componente è designato come [ *selezionabile per il backup*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="79a28-108">Whether the component is designated as being [*selectable for backup*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="79a28-109">Indica se è designato come [ *selezionabile per il ripristino*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="79a28-109">Whether it is designated as being [*selectable for restore*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="79a28-110">Indica se esiste una dipendenza esplicita tra un determinato componente in un determinato writer e altri componenti di altri writer</span><span class="sxs-lookup"><span data-stu-id="79a28-110">Whether an explicit dependency exists between a given component in a given writer and other components in other writers</span></span>

<span data-ttu-id="79a28-111">Per ulteriori informazioni su questi problemi, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="79a28-111">More information on these issues is in the following topics:</span></span>

-   [<span data-ttu-id="79a28-112">Percorso logico dei componenti</span><span class="sxs-lookup"><span data-stu-id="79a28-112">Logical Pathing of Components</span></span>](logical-pathing-of-components.md)
-   [<span data-ttu-id="79a28-113">Utilizzo della selezione per il backup</span><span class="sxs-lookup"><span data-stu-id="79a28-113">Working with Selectability for Backup</span></span>](working-with-selectability-for-backup.md)
-   [<span data-ttu-id="79a28-114">Utilizzo della selezione per il ripristino e i sottocomponenti</span><span class="sxs-lookup"><span data-stu-id="79a28-114">Working with Selectability For Restore and Subcomponents</span></span>](working-with-selectability-for-restore-and-subcomponents.md)
-   [<span data-ttu-id="79a28-115">Selezione e utilizzo delle proprietà dei componenti</span><span class="sxs-lookup"><span data-stu-id="79a28-115">Selectability and Working with Component Properties</span></span>](selectability-and-working-with-component-properties.md)
-   [<span data-ttu-id="79a28-116">Dipendenze tra componenti gestiti da Writer diversi</span><span class="sxs-lookup"><span data-stu-id="79a28-116">Dependencies between Components Managed by Different Writers</span></span>](dependencies-between-components-managed-by-different-writers.md)

 

 



