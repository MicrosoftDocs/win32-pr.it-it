---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f018a19c1d00ff3c6530e7c45fbca2350df8fec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526280"
---
# <a name="p-volume-shadow-copy-service"></a><span data-ttu-id="09352-103">P (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="09352-103">P (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="09352-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="09352-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="09352-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**supporto file parziale**</span><span class="sxs-lookup"><span data-stu-id="09352-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**partial file support**</span></span>
</dt> <dd>

<span data-ttu-id="09352-106">Capacità di implementare le operazioni di backup modificando le sottosezioni dei file interessati, anziché usare l'intero file.</span><span class="sxs-lookup"><span data-stu-id="09352-106">The capacity to implement backup operations by modifying subsections of the files involved, rather than working with the entire files.</span></span> <span data-ttu-id="09352-107">Vedere anche [*targeting diretto*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="09352-107">See also [*directed targeting*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="09352-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**copia shadow persistente**</span><span class="sxs-lookup"><span data-stu-id="09352-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**persistent shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="09352-109">Copia shadow che non viene eliminata automaticamente quando il richiedente rilascia un oggetto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) o quando il computer viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="09352-109">A shadow copy that is not deleted automatically when the requester releases an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object or when the computer is restarted.</span></span> <span data-ttu-id="09352-110">Vedere anche [*copia shadow di rilascio automatico*](vssgloss-a.md), [*Copia Shadow*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="09352-110">See also [*auto-release shadow copy*](vssgloss-a.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="09352-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plessi**</span><span class="sxs-lookup"><span data-stu-id="09352-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**</span></span>
</dt> <dd>

<span data-ttu-id="09352-112">Un tipo speciale di volume di copia shadow che rappresenta completamente e completamente un volume di copia shadow senza la necessità di un volume originale.</span><span class="sxs-lookup"><span data-stu-id="09352-112">A special type of shadow copy volume that fully and completely represents a shadow copy volume without the need for either original volume.</span></span> <span data-ttu-id="09352-113">Questo è anche noto come mirroring diviso, ma in questa documentazione viene usato il termine Plex.</span><span class="sxs-lookup"><span data-stu-id="09352-113">This is also commonly known as a split-mirror, but this documentation uses the term Plex.</span></span>

</dd> <dt>

<span data-ttu-id="09352-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Evento PostRestore**</span><span class="sxs-lookup"><span data-stu-id="09352-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**PostRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="09352-115">Evento VSS che indica il completamento di un ripristino VSS.</span><span class="sxs-lookup"><span data-stu-id="09352-115">A VSS event indicating that a VSS restore has completed.</span></span>

</dd> <dt>

<span data-ttu-id="09352-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Evento PostSnapshot**</span><span class="sxs-lookup"><span data-stu-id="09352-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="09352-117">Evento VSS che indica che è stata completata una copia shadow.</span><span class="sxs-lookup"><span data-stu-id="09352-117">A VSS event indicating that a shadow copy has been completed.</span></span> <span data-ttu-id="09352-118">Vedere anche [*Copia Shadow*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="09352-118">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="09352-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Evento PrepareForBackup**</span><span class="sxs-lookup"><span data-stu-id="09352-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup event**</span></span>
</dt> <dd>

<span data-ttu-id="09352-120">Evento VSS che indica che sta per essere eseguita un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="09352-120">A VSS event indicating that a backup operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="09352-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Evento PrepareForSnapshot**</span><span class="sxs-lookup"><span data-stu-id="09352-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**PrepareForSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="09352-122">Evento VSS che indica che i writer devono eseguire i passaggi necessari per preparare un'operazione di copia shadow imminente.</span><span class="sxs-lookup"><span data-stu-id="09352-122">A VSS event indicating that writers should take steps to prepare for an upcoming shadow copy operation.</span></span> <span data-ttu-id="09352-123">Vedere anche [*Copia Shadow*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="09352-123">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="09352-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Evento di preripristino**</span><span class="sxs-lookup"><span data-stu-id="09352-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="09352-125">Evento VSS che indica che sta per essere eseguita un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="09352-125">A VSS event indicating that a restore operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="09352-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**provider**</span><span class="sxs-lookup"><span data-stu-id="09352-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="09352-127">Oggetto sistema operativo che intercetta e gestisce le richieste di I/O per creare e rappresentare copie shadow del volume nel file system.</span><span class="sxs-lookup"><span data-stu-id="09352-127">An operating system object that intercepts and manages I/O requests to create and represent volume shadow copies to the file system.</span></span> <span data-ttu-id="09352-128">Vedere anche [*provider hardware*](vssgloss-h.md), [*provider di software*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="09352-128">See also [*hardware provider*](vssgloss-h.md), [*software provider*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



