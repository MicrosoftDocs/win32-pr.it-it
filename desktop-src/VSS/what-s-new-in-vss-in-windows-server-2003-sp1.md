---
description: "Nell'elenco seguente vengono indicate le aggiunte e le modifiche apportate all'interfaccia Servizio Copia Shadow del volume in Windows Server 2003 con Service Pack 1 (SP1):"
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Novità di VSS in Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485020"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a><span data-ttu-id="bff76-103">Novità di VSS in Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="bff76-103">What's New in VSS in Windows Server 2003 SP1</span></span>

<span data-ttu-id="bff76-104">Nell'elenco seguente vengono indicate le aggiunte e le modifiche apportate all'interfaccia Servizio Copia Shadow del volume in Windows Server 2003 con Service Pack 1 (SP1):</span><span class="sxs-lookup"><span data-stu-id="bff76-104">The following list indicates additions and changes to the Volume Shadow Copy Service interface in Windows Server 2003 with Service Pack 1 (SP1):</span></span>

## <a name="auto-recovery"></a><span data-ttu-id="bff76-105">Ripristino automatico</span><span class="sxs-lookup"><span data-stu-id="bff76-105">Auto-recovery</span></span>

<span data-ttu-id="bff76-106">Il [*Ripristino automatico*](vssgloss-a.md) consente ai writer di aggiornare i componenti in una copia shadow prima che la copia shadow venga modificata in modo permanente in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bff76-106">[*Auto-recovery*](vssgloss-a.md) allows writers a time to update components in a shadow copy before the shadow copy is permanently changed to read-only.</span></span> <span data-ttu-id="bff76-107">Ad esempio, è possibile che un database debba eseguire il rollback di tutte le transazioni incomplete per tutte le copie shadow. il writer del database potrebbe impostare il flag di **\_ ripristino del \_ backup \_ di VSS CF** per i componenti del database.</span><span class="sxs-lookup"><span data-stu-id="bff76-107">For example, a database may need to rollback any incomplete transactions for all shadow copies (the database writer would set the **VSS\_CF\_BACKUP\_RECOVERY** flag for the database components).</span></span> <span data-ttu-id="bff76-108">Il recupero automatico avviato dal richiedente consente il ripristino con granularità fine, ad esempio il ripristino di una tabella in un database o in una cartella in un server di posta, oppure il rollback per supportare data mining per eseguire analisi che potrebbero essere troppo lente per un server di produzione (il richiedente aggiungerà il **rollback di VSS \_ VolSnap \_ attr \_ \_** al contesto della copia shadow). Il ripristino automatico non è compatibile con le copie shadow trasportabili, ma la stessa funzionalità è supportata tramite il [ripristino rapido tramite volumi di copia shadow trasportabili](fast-recovery-using-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="bff76-108">Auto-recovery initiated by the requester allows both fine-grained restore (for example restoring one table in a database or one folder on a mail server), or the rollback to support data mining to perform analysis that would be too slow for a production server (the requester would add **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** to the shadow copy context.) Auto-recovery is not compatible with transportable shadow copies, but the same functionality is supported by using [Fast Recovery Using Transportable Shadow Copied Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md).</span></span>

<span data-ttu-id="bff76-109">Gli elementi di programmazione seguenti presentano modifiche per supportare il ripristino automatico:</span><span class="sxs-lookup"><span data-stu-id="bff76-109">The following programming elements have changes to support auto-recovery:</span></span>

<span data-ttu-id="bff76-110">Metodi della classe</span><span class="sxs-lookup"><span data-stu-id="bff76-110">Class methods</span></span>

-   [<span data-ttu-id="bff76-111">**CVssWriter:: GetSnapshotDeviceName**</span><span class="sxs-lookup"><span data-stu-id="bff76-111">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [<span data-ttu-id="bff76-112">**CVssWriter:: OnPostSnapshot**</span><span class="sxs-lookup"><span data-stu-id="bff76-112">**CVssWriter::OnPostSnapshot**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

<span data-ttu-id="bff76-113">Enumerazioni</span><span class="sxs-lookup"><span data-stu-id="bff76-113">Enumerations</span></span>

-   [<span data-ttu-id="bff76-114">**\_flag componente \_ VSS**</span><span class="sxs-lookup"><span data-stu-id="bff76-114">**VSS\_COMPONENT\_FLAGS**</span></span>](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [<span data-ttu-id="bff76-115">**\_\_ \_ attributi snapshot del volume VSS \_**</span><span class="sxs-lookup"><span data-stu-id="bff76-115">**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

<span data-ttu-id="bff76-116">Metodi di interfaccia</span><span class="sxs-lookup"><span data-stu-id="bff76-116">Interface methods</span></span>

-   [<span data-ttu-id="bff76-117">**IVssProviderCreateSnapshotSet::P reFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="bff76-117">**IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [<span data-ttu-id="bff76-118">**IVssProviderCreateSnapshotSet::P ostFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="bff76-118">**IVssProviderCreateSnapshotSet::PostFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a><span data-ttu-id="bff76-119">Supporto completo per le copie shadow trasportabili</span><span class="sxs-lookup"><span data-stu-id="bff76-119">Full Support for Transportable Shadow Copies</span></span>

<span data-ttu-id="bff76-120">Le copie shadow trasportabili sono supportate in tutte le edizioni di Windows Server 2003 con SP1.</span><span class="sxs-lookup"><span data-stu-id="bff76-120">Transportable shadow copies are supported in all editions of Windows Server 2003 with SP1.</span></span> <span data-ttu-id="bff76-121">Per ulteriori informazioni, vedere [importazione di volumi di copie shadow trasportabili](importing-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="bff76-121">For more information, see [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).</span></span>

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="bff76-122">Ripristino rapido tramite volumi di copie shadow trasportabili</span><span class="sxs-lookup"><span data-stu-id="bff76-122">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

[<span data-ttu-id="bff76-123">Ripristino rapido tramite volumi di copie shadow trasportabili</span><span class="sxs-lookup"><span data-stu-id="bff76-123">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a><span data-ttu-id="bff76-124">Gestione area di archiviazione copia shadow</span><span class="sxs-lookup"><span data-stu-id="bff76-124">Shadow copy storage area management</span></span>

[<span data-ttu-id="bff76-125">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="bff76-125">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



