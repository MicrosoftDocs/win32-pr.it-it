---
description: I richiedenti controllano le funzionalità di una copia shadow impostando il relativo contesto. Questo contesto indica se la copia shadow sopravviverà all'operazione corrente e il livello di coordinamento del writer o del provider.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Configurazioni del contesto per copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528698"
---
# <a name="shadow-copy-context-configurations"></a><span data-ttu-id="1ebb3-104">Configurazioni del contesto per copie shadow</span><span class="sxs-lookup"><span data-stu-id="1ebb3-104">Shadow Copy Context Configurations</span></span>

<span data-ttu-id="1ebb3-105">I richiedenti controllano le funzionalità di una copia shadow impostando il relativo contesto.</span><span class="sxs-lookup"><span data-stu-id="1ebb3-105">Requesters control a shadow copy's features by setting its context.</span></span> <span data-ttu-id="1ebb3-106">Questo contesto indica se la copia shadow sopravviverà all'operazione corrente e il livello di coordinamento del writer o del provider.</span><span class="sxs-lookup"><span data-stu-id="1ebb3-106">This context indicates whether the shadow copy will survive the current operation, and the degree of writer/provider coordination.</span></span>

## <a name="persistence-and-shadow-copy-context"></a><span data-ttu-id="1ebb3-107">Persistenza e contesto della copia shadow</span><span class="sxs-lookup"><span data-stu-id="1ebb3-107">Persistence and Shadow Copy Context</span></span>

<span data-ttu-id="1ebb3-108">Una copia shadow può essere [*permanente*](vssgloss-p.md), ovvero la copia shadow non viene eliminata in seguito alla chiusura di un'operazione di backup o al rilascio di un oggetto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .</span><span class="sxs-lookup"><span data-stu-id="1ebb3-108">A shadow copy may be [*persistent*](vssgloss-p.md)—that is, the shadow copy is not deleted following the termination of a backup operation or the release of an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object.</span></span>

<span data-ttu-id="1ebb3-109">Le copie shadow permanenti richiedono contesti del [**\_ \_ \_ contesto dello snapshot VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) di **VSS \_ ctx \_ client \_ accessibili**, **\_ rollback dell' \_ app \_ VSS CTX** o **rollback del \_ \_ server \_ VSS CTX**.</span><span class="sxs-lookup"><span data-stu-id="1ebb3-109">Persistent shadow copies require [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) contexts of **VSS\_CTX\_CLIENT\_ACCESSIBLE**, **VSS\_CTX\_APP\_ROLLBACK**, or **VSS\_CTX\_NAS\_ROLLBACK**.</span></span> <span data-ttu-id="1ebb3-110">Le copie shadow permanenti possono essere eseguite solo per i volumi NTFS.</span><span class="sxs-lookup"><span data-stu-id="1ebb3-110">Persistent shadow copies can be made only for NTFS volumes.</span></span>

<span data-ttu-id="1ebb3-111">Le copie shadow non permanenti vengono create con i contesti del backup **VSS \_ ctx \_** o del **\_ \_ \_ \_ backup della condivisione file VSS CTX**.</span><span class="sxs-lookup"><span data-stu-id="1ebb3-111">Nonpersistent shadow copies are created with contexts of **VSS\_CTX\_BACKUP** or **VSS\_CTX\_FILE\_SHARE\_BACKUP**.</span></span> <span data-ttu-id="1ebb3-112">È possibile effettuare copie shadow non permanenti per i volumi NTFS e non NTFS.</span><span class="sxs-lookup"><span data-stu-id="1ebb3-112">Nonpersistent shadow copies can be made for NTFS and non-NTFS volumes.</span></span>

## <a name="writer-participation-and-shadow-copies"></a><span data-ttu-id="1ebb3-113">Partecipazione e copie shadow del writer</span><span class="sxs-lookup"><span data-stu-id="1ebb3-113">Writer Participation and Shadow Copies</span></span>

<span data-ttu-id="1ebb3-114">Un contesto di copia shadow può essere classificato come coinvolgimento di writer o senza coinvolgere i writer.</span><span class="sxs-lookup"><span data-stu-id="1ebb3-114">A shadow copy context can be classified as either involving writers or not involving writers.</span></span>

<span data-ttu-id="1ebb3-115">I contesti di copia shadow che coinvolgono i writer nella loro creazione includono:</span><span class="sxs-lookup"><span data-stu-id="1ebb3-115">Shadow copy contexts that involve writers in their creation include:</span></span>

-   <span data-ttu-id="1ebb3-116">**\_rollback dell' \_ app VSS CTX \_**</span><span class="sxs-lookup"><span data-stu-id="1ebb3-116">**VSS\_CTX\_APP\_ROLLBACK**</span></span>
-   <span data-ttu-id="1ebb3-117">**BACKUP di VSS \_ ctx \_**</span><span class="sxs-lookup"><span data-stu-id="1ebb3-117">**VSS\_CTX\_BACKUP**</span></span>
-   <span data-ttu-id="1ebb3-118">**\_ \_ writer accessibili del client VSS CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ebb3-118">**VSS\_CTX\_CLIENT\_ACCESSIBLE\_WRITERS**</span></span>

<span data-ttu-id="1ebb3-119">Quelli che non coinvolgono i writer nella loro creazione includono:</span><span class="sxs-lookup"><span data-stu-id="1ebb3-119">Those that do not involve writers in their creation include:</span></span>

-   <span data-ttu-id="1ebb3-120">**\_client CTX \_ VSS \_ accessibile**</span><span class="sxs-lookup"><span data-stu-id="1ebb3-120">**VSS\_CTX\_CLIENT\_ACCESSIBLE**</span></span>
-   <span data-ttu-id="1ebb3-121">**\_backup della \_ \_ condivisione file VSS CTX \_**</span><span class="sxs-lookup"><span data-stu-id="1ebb3-121">**VSS\_CTX\_FILE\_SHARE\_BACKUP**</span></span>
-   <span data-ttu-id="1ebb3-122">**\_rollback del \_ Server VSS CTX \_**</span><span class="sxs-lookup"><span data-stu-id="1ebb3-122">**VSS\_CTX\_NAS\_ROLLBACK**</span></span>

<span data-ttu-id="1ebb3-123">Un contesto può essere utilizzato con entrambi i tipi di copie shadow, ma non può essere utilizzato per la creazione di una copia shadow:</span><span class="sxs-lookup"><span data-stu-id="1ebb3-123">One context can be used with both types of shadow copies, but cannot be used in creating a shadow copy:</span></span>

-   <span data-ttu-id="1ebb3-124">**\_totale VSS CTX \_**</span><span class="sxs-lookup"><span data-stu-id="1ebb3-124">**VSS\_CTX\_ALL**</span></span>

<span data-ttu-id="1ebb3-125">La creazione di una copia shadow con un contesto di **VSS \_ ctx \_ All** (using [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) e [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="1ebb3-125">Creating a shadow copy with a context of **VSS\_CTX\_ALL** (using [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) and [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) is not supported.</span></span>

<span data-ttu-id="1ebb3-126">Le operazioni che supportano un contesto di **VSS \_ CTX sono \_ tutte** le operazioni [**amministrative IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)e [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="1ebb3-126">Operations that support a context of **VSS\_CTX\_ALL** are the administrative operations [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::DeleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset), and [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span></span>

## <a name="obtaining-shadow-copy-information"></a><span data-ttu-id="1ebb3-127">Recupero delle informazioni sulla copia shadow</span><span class="sxs-lookup"><span data-stu-id="1ebb3-127">Obtaining Shadow Copy Information</span></span>

<span data-ttu-id="1ebb3-128">Se un richiedente conosce il GUID di identificazione di una copia shadow (il relativo **\_ ID VSS**), può ottenere informazioni sul contesto di una copia shadow specifica (identificata dal **relativo \_ ID VSS**) decomprimendo la struttura di [**\_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) restituita da una chiamata a [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span><span class="sxs-lookup"><span data-stu-id="1ebb3-128">If a requester knows the identifying GUID of a shadow copy (its **VSS\_ID**), it can obtain information about the context of a specific shadow copy (identified by its **VSS\_ID**) by unpacking the [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure returned by a call to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="1ebb3-129">Per ottenere informazioni di contesto su tutte le copie shadow di un sistema, un richiedente esamina il membro **\_ LSnapshotAttributes** di **obj. snap del membro obj. snap** della struttura [**\_ \_ prop dell'oggetto VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (ovvero una struttura di [**\_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) ottenuta usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) per scorrere l'elenco di oggetti restituiti da una chiamata a [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="1ebb3-129">To obtain context information about all shadow copies on a system, a requester examines the **m\_lSnapshotAttributes** member of the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) structure obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

 

 



