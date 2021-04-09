---
description: Il ripristino di file in un sistema in esecuzione può risultare problematico. È importante che l'esecuzione di applicazioni (writer) indichi cosa fare quando si verificano problemi durante i ripristini, ad esempio se il file da ripristinare è attualmente in uso.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configurazioni del ripristino VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129294"
---
# <a name="vss-restore-configurations"></a><span data-ttu-id="565fa-104">Configurazioni del ripristino VSS</span><span class="sxs-lookup"><span data-stu-id="565fa-104">VSS Restore Configurations</span></span>

<span data-ttu-id="565fa-105">Il ripristino di file in un sistema in esecuzione può risultare problematico.</span><span class="sxs-lookup"><span data-stu-id="565fa-105">File restoration on a running system can be problematic.</span></span> <span data-ttu-id="565fa-106">È importante che l'esecuzione di applicazioni (writer) indichi cosa fare quando si verificano problemi durante i ripristini, ad esempio se il file da ripristinare è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="565fa-106">It is important that running applications (writers) indicate what to do when difficulties arise during restores, for instance, if the file being restored is currently in use.</span></span>

<span data-ttu-id="565fa-107">In VSS, i writer hanno due modalità complementari per la gestione dei ripristini, ovvero [*metodi di ripristino*](vssgloss-r.md) e [*destinazioni di ripristino*](vssgloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="565fa-107">Under VSS, writers have two complementary ways of managing restores—[*restore methods*](vssgloss-r.md) and [*restore targets*](vssgloss-r.md).</span></span>

<span data-ttu-id="565fa-108">Inoltre, i richiedenti possono scegliere di ripristinare i file in posizioni non specificate in precedenza e inviare notifiche ai writer (vedere [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span><span class="sxs-lookup"><span data-stu-id="565fa-108">In addition, requesters can choose to restore files to previously unspecified locations and notify writers (see [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span></span>

<span data-ttu-id="565fa-109">Il metodo Restore (chiama anche la destinazione di ripristino originale) viene specificato da un writer al momento del backup e imposta una definizione a livello di writer del metodo da utilizzare per ripristinare tutti i relativi componenti in futuro.</span><span class="sxs-lookup"><span data-stu-id="565fa-109">The restore method (also call the original restore target) is specified by a writer at a backup time, and sets a writer-wide definition of the method to be used to restore all its components in the future.</span></span> <span data-ttu-id="565fa-110">Tutti i file e i componenti gestiti da un writer condividono lo stesso metodo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="565fa-110">All files and components managed by a writer share the same restore method.</span></span>

<span data-ttu-id="565fa-111">Le destinazioni di ripristino consentono ai writer di modificare il modo in cui devono essere ripristinati i componenti specifici in fase di ripristino.</span><span class="sxs-lookup"><span data-stu-id="565fa-111">Restore targets allow writers to change how specific components are to be restored at restore time.</span></span> <span data-ttu-id="565fa-112">A differenza dei metodi di ripristino, le destinazioni di ripristino sono definite per un set di componenti.</span><span class="sxs-lookup"><span data-stu-id="565fa-112">Unlike restore methods, restore targets are defined for a component set.</span></span>

<span data-ttu-id="565fa-113">Una descrizione dettagliata dell'utilizzo dei metodi di ripristino e delle destinazioni di ripristino è disponibile negli argomenti elencati di seguito:</span><span class="sxs-lookup"><span data-stu-id="565fa-113">A detailed discussion of the usage of restore methods and restore targets is found in the topics listed below:</span></span>

-   [<span data-ttu-id="565fa-114">Stato ripristino VSS</span><span class="sxs-lookup"><span data-stu-id="565fa-114">VSS Restore State</span></span>](vss-restore-state.md)
-   [<span data-ttu-id="565fa-115">Impostazione di metodi di ripristino VSS</span><span class="sxs-lookup"><span data-stu-id="565fa-115">Setting VSS Restore Methods</span></span>](setting-vss-restore-methods.md)
-   [<span data-ttu-id="565fa-116">Impostazione delle destinazioni di ripristino VSS</span><span class="sxs-lookup"><span data-stu-id="565fa-116">Setting VSS Restore Targets</span></span>](setting-vss-restore-targets.md)
-   [<span data-ttu-id="565fa-117">Impostazione delle opzioni di ripristino VSS</span><span class="sxs-lookup"><span data-stu-id="565fa-117">Setting VSS Restore Options</span></span>](setting-vss-restore-options.md)

<span data-ttu-id="565fa-118">Per informazioni sui ripristini che non utilizzano questi meccanismi, vedere [ripristini senza partecipazione del writer](restores-without-writer-participation.md).</span><span class="sxs-lookup"><span data-stu-id="565fa-118">(For information on restores that do not use these mechanisms, see [Restores without Writer Participation](restores-without-writer-participation.md).)</span></span>

 

 



