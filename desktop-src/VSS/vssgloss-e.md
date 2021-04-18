---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307149"
---
# <a name="e-volume-shadow-copy-service"></a><span data-ttu-id="d6469-103">E (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="d6469-103">E (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="d6469-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="d6469-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d6469-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusione componente esplicito**</span><span class="sxs-lookup"><span data-stu-id="d6469-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**explicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="d6469-106">Aggiunta delle informazioni di un componente al documento dei componenti di backup di un richiedente quando partecipa a un'operazione di backup o ripristino.</span><span class="sxs-lookup"><span data-stu-id="d6469-106">Adding of a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span> <span data-ttu-id="d6469-107">I richiedenti usano [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per includere in modo esplicito un componente in un'operazione di backup e [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) o [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) per includere in modo esplicito un componente in un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d6469-107">Requesters use [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to explicitly include a component in a backup operation, and [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) or [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) to explicitly include a component in a restore operation.</span></span>

<span data-ttu-id="d6469-108">Se viene eseguito il backup o il ripristino di un componente di un writer, tutti i componenti non selezionabili senza alcun predecessore selezionabile devono essere inclusi in modo esplicito in un'operazione di backup o ripristino.</span><span class="sxs-lookup"><span data-stu-id="d6469-108">If any component of a writer is backed up or restored, all nonselectable components without any selectable ancestors must be explicitly included in a backup or restore operation.</span></span>

<span data-ttu-id="d6469-109">I componenti selezionabili senza predecessori selezionabili scelti da un richiedente per la partecipazione a un backup o un ripristino devono essere inclusi in modo esplicito nell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d6469-109">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore must be explicitly included in the operation.</span></span>

<span data-ttu-id="d6469-110">I componenti non selezionabili con un predecessore selezionabile non sono mai inclusi in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="d6469-110">Nonselectable components with a selectable ancestor are never explicitly included.</span></span>

<span data-ttu-id="d6469-111">I componenti selezionabili con un predecessore selezionabile possono essere inclusi in modo esplicito oppure possono essere inclusi in modo implicito se il predecessore è incluso in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="d6469-111">Selectable components with a selectable ancestor may be included explicitly, or may be included implicitly if the ancestor is included explicitly.</span></span>

</dd> <dt>

<span data-ttu-id="d6469-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**copia shadow esposta**</span><span class="sxs-lookup"><span data-stu-id="d6469-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**exposed shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="d6469-113">Copia shadow del volume montata in un sistema e disponibile per processi diversi da quello che la gestisce.</span><span class="sxs-lookup"><span data-stu-id="d6469-113">A volume shadow copy that is mounted on a system and available to processes other than the one that manages it.</span></span> <span data-ttu-id="d6469-114">Un volume di copia Shadow montato sotto una lettera di unità o un percorso di directory viene definito "esposto localmente".</span><span class="sxs-lookup"><span data-stu-id="d6469-114">A shadow copy volume mounted under a drive letter or a directory location is referred to as "locally exposed."</span></span> <span data-ttu-id="d6469-115">Un volume di copia shadow accessibile tramite una condivisione (ad eccezione delle copie shadow accessibili dal client) viene definito "esposto in modalità remota".</span><span class="sxs-lookup"><span data-stu-id="d6469-115">A shadow copy volume accessible through a share (except for client-accessible shadow copies) is referred to as "remotely exposed."</span></span> <span data-ttu-id="d6469-116">Tutte le copie shadow esposte sono anche copie shadow di superficie.</span><span class="sxs-lookup"><span data-stu-id="d6469-116">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="d6469-117">Vedere anche [*Copia Shadow accessibile dal client*](vssgloss-c.md), [*Copia Shadow*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="d6469-117">See also [*client accessible shadow copy*](vssgloss-c.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



