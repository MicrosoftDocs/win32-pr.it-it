---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307144"
---
# <a name="s-volume-shadow-copy-service"></a><span data-ttu-id="1dbed-103">S (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="1dbed-103">S (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="1dbed-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="1dbed-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="1dbed-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selezione per il backup**</span><span class="sxs-lookup"><span data-stu-id="1dbed-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selectability for backup**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-106">Un componente viene definito selezionabile per il backup se l'inclusione esplicita in un'operazione di backup è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="1dbed-106">A component is said to be selectable for backup if its explicit inclusion in a backup operation is optional.</span></span> <span data-ttu-id="1dbed-107">La selezione per il backup è abilitata se il valore del membro **bSelectable** della [**struttura \_ COMPONENTINFO VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) è **true**.</span><span class="sxs-lookup"><span data-stu-id="1dbed-107">Selectability for backup is enabled if the value of the **bSelectable** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="1dbed-108">Non esiste alcun valore predefinito per la selezione di un componente per il backup; un writer deve sempre impostare questo valore in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1dbed-108">There is no default value for a component's selectability for backup; a writer must always set this value explicitly.</span></span>

<span data-ttu-id="1dbed-109">I writer utilizzano inoltre la selezione per il ripristino per organizzare la partecipazione del componente alle operazioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1dbed-109">Writers also use selectability for restore to organize their component's participation in restore operations.</span></span>

<span data-ttu-id="1dbed-110">Vedere anche *componente selezionabile*, *selezione per ripristino*, [*inclusione componente esplicita*](vssgloss-e.md), [*inclusione componente implicito*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="1dbed-110">See also *selectable component*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selezione per il ripristino**</span><span class="sxs-lookup"><span data-stu-id="1dbed-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selectability for restore**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-112">Un componente viene definito selezionabile per il ripristino se è possibile eseguirne il backup in modo implicito come parte di un set di componenti e successivamente ripristinato singolarmente senza il resto del set di componenti.</span><span class="sxs-lookup"><span data-stu-id="1dbed-112">A component is said to be selectable for restore if it can be implicitly backed up as part of a component set, and then later individually restored without the rest of the component set.</span></span> <span data-ttu-id="1dbed-113">La selezione per il ripristino è abilitata se il valore del membro **bSelectableForRestore** della [**struttura \_ COMPONENTINFO VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) è **true**.</span><span class="sxs-lookup"><span data-stu-id="1dbed-113">Selectability for restore is enabled if the value of the **bSelectableForRestore** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="1dbed-114">Per impostazione predefinita, la selezione di un componente per il ripristino è **false**.</span><span class="sxs-lookup"><span data-stu-id="1dbed-114">By default, a component's selectability for restore is **false**.</span></span> <span data-ttu-id="1dbed-115">La selezione per il ripristino ha un significato solo quando un componente non è stato aggiunto al documento di backup.</span><span class="sxs-lookup"><span data-stu-id="1dbed-115">Selectability for restore has meaning only when a component has not been added to the backup document.</span></span>

<span data-ttu-id="1dbed-116">Vedere anche *componente selezionabile*, *selezione per backup*, [*inclusione componente esplicita*](vssgloss-e.md), [*inclusione componente implicito*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="1dbed-116">See also *selectable component*, *selectability for backup*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**componente selezionabile**</span><span class="sxs-lookup"><span data-stu-id="1dbed-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**selectable component**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-118">Un componente viene definito selezionabile se la relativa inclusione esplicita in un'operazione di backup o ripristino è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="1dbed-118">A component is said to be selectable if its explicit inclusion in a backup or restore operation is optional.</span></span>

<span data-ttu-id="1dbed-119">La selezione per il backup e la selezione per il ripristino sono indipendenti tra loro: è possibile selezionare un componente per entrambe le operazioni, per il ripristino e non per il backup o per il backup e non per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="1dbed-119">Selectability for backup and selectability for restore are independent of each other—a component may be selectable for both operations, for restore and not backup, or for backup and not restore.</span></span>

<span data-ttu-id="1dbed-120">I writer utilizzano anche la selezione per organizzare i componenti in gruppi:</span><span class="sxs-lookup"><span data-stu-id="1dbed-120">Writers also use selectability to organize their components into groups:</span></span>

-   <span data-ttu-id="1dbed-121">I componenti non selezionabili senza predecessori selezionabili nei percorsi logici devono essere sempre inclusi in modo esplicito se è necessario eseguire il backup o il ripristino di un writer.</span><span class="sxs-lookup"><span data-stu-id="1dbed-121">Nonselectable components with no selectable ancestors in their logical paths must always be explicitly included if a writer is to be backed up or restored.</span></span>
-   <span data-ttu-id="1dbed-122">I componenti non selezionabili con i predecessori selezionabili verranno inclusi solo in un backup o un ripristino se è incluso almeno un predecessore selezionabile.</span><span class="sxs-lookup"><span data-stu-id="1dbed-122">Nonselectable components with selectable ancestors will only be included in a backup or restore if at least one selectable ancestor is included.</span></span>
-   <span data-ttu-id="1dbed-123">I componenti selezionabili senza predecessori selezionabili possono essere inclusi solo in un'operazione di backup o ripristino in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1dbed-123">Selectable components without selectable ancestors can only be included in a backup or restore operation explicitly.</span></span>
-   <span data-ttu-id="1dbed-124">I componenti selezionabili con i predecessori selezionabili possono essere inclusi in modo esplicito in un'operazione di backup o ripristino oppure possono essere inclusi implicitamente se uno dei relativi predecessori selezionabili è incluso.</span><span class="sxs-lookup"><span data-stu-id="1dbed-124">Selectable components with selectable ancestors can be explicitly included in a backup or restore operation, or can be implicitly included if one of their selectable ancestors is included.</span></span>

<span data-ttu-id="1dbed-125">Vedere anche [*componenti*](vssgloss-c.md), *selezione per il backup*, *selezione per il ripristino*, [*inclusione di componenti espliciti*](vssgloss-e.md), [*inclusione di componenti impliciti*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="1dbed-125">See also [*components*](vssgloss-c.md), *selectability for backup*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**copia shadow**</span><span class="sxs-lookup"><span data-stu-id="1dbed-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-127">Replica temporizzata di sola lettura del contenuto di un volume originale.</span><span class="sxs-lookup"><span data-stu-id="1dbed-127">A read-only point-in-time replica of an original volume's contents.</span></span> <span data-ttu-id="1dbed-128">Ogni copia shadow è codificata da un GUID permanente.</span><span class="sxs-lookup"><span data-stu-id="1dbed-128">Each shadow copy is keyed by a persistent GUID.</span></span> <span data-ttu-id="1dbed-129">Detto anche copia shadow del volume.</span><span class="sxs-lookup"><span data-stu-id="1dbed-129">Also called a volume shadow copy.</span></span> <span data-ttu-id="1dbed-130">Vedere anche *set di copie shadow*.</span><span class="sxs-lookup"><span data-stu-id="1dbed-130">See also *shadow copy set*.</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**copie shadow per cartelle condivise**</span><span class="sxs-lookup"><span data-stu-id="1dbed-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Shadow Copies for Shared Folders**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-132">Funzionalità di Windows che consente di creare copie di backup leggere in linea dei volumi con VSS.</span><span class="sxs-lookup"><span data-stu-id="1dbed-132">A feature of Windows that creates lightweight, online backup copies of volumes using VSS.</span></span> <span data-ttu-id="1dbed-133">I client possono accedere a questi backup tramite la shell di Windows per visualizzare le versioni precedenti dei file e annullare gli errori senza richiedere un ripristino completo.</span><span class="sxs-lookup"><span data-stu-id="1dbed-133">Clients can access these backups through the Windows shell to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="1dbed-134">Vedere anche [*Copia Shadow accessibile dal client*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="1dbed-134">See also [*client accessible shadow copy*](vssgloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**set di copie shadow**</span><span class="sxs-lookup"><span data-stu-id="1dbed-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**shadow copy set**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-136">Raccolta di copie shadow del volume create contemporaneamente e identificate da un valore di ID del set di copie shadow comune (un GUID permanente).</span><span class="sxs-lookup"><span data-stu-id="1dbed-136">A collection of volume shadow copies created at the same time and identified by a common shadow copy set ID (a persistent GUID) value.</span></span> <span data-ttu-id="1dbed-137">Si tratta del meccanismo utilizzato per consentire la gestione di un'operazione di copia shadow tra i volumi.</span><span class="sxs-lookup"><span data-stu-id="1dbed-137">This is the mechanism used to allow a shadow copy operation to be managed across volumes.</span></span> <span data-ttu-id="1dbed-138">Vedere anche *Copia Shadow*.</span><span class="sxs-lookup"><span data-stu-id="1dbed-138">See also *shadow copy*.</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**provider software**</span><span class="sxs-lookup"><span data-stu-id="1dbed-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-140">Provider che intercetta le richieste di I/O a livello di software tra il file system e il gestore dei volumi.</span><span class="sxs-lookup"><span data-stu-id="1dbed-140">A provider that intercepts I/O requests at the software level between the file system and the volume manager.</span></span> <span data-ttu-id="1dbed-141">Vedere anche [*provider hardware*](vssgloss-h.md), [*provider*](vssgloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="1dbed-141">See also [*hardware provider*](vssgloss-h.md), [*provider*](vssgloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**sottocomponente**</span><span class="sxs-lookup"><span data-stu-id="1dbed-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponent**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-143">Qualsiasi componente con un percorso logico contenente un componente padre selezionabile (per il backup o il ripristino).</span><span class="sxs-lookup"><span data-stu-id="1dbed-143">Any component that has a logical path containing a selectable (for either backup or restore) parent component.</span></span> <span data-ttu-id="1dbed-144">I sottocomponenti devono avere un percorso logico nel formato { \_ nome componente} \\ {nome sottocomponente \_ }.</span><span class="sxs-lookup"><span data-stu-id="1dbed-144">Subcomponents must have a logical path of the form {component\_name}\\{subcomponent\_name}.</span></span> <span data-ttu-id="1dbed-145">Se il predecessore selezionabile di un sottocomponente (per backup o ripristino) viene incluso in modo esplicito in un backup o un ripristino, il sottocomponente viene incluso in modo implicito nell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1dbed-145">If a subcomponent's selectable (for either backup or restore) ancestor is explicitly included in a backup or restore, then the subcomponent is implicitly included in the operation.</span></span> <span data-ttu-id="1dbed-146">I sottocomponenti inclusi in modo implicito non dispongono di dati inclusi nel documento componenti di backup, indipendentemente dal fatto che siano selezionabili (per il ripristino o il backup).</span><span class="sxs-lookup"><span data-stu-id="1dbed-146">Implicitly included subcomponents do not have their data included in the Backup Components Document—regardless of whether they are selectable (for either restore or backup) or not.</span></span> <span data-ttu-id="1dbed-147">Vedere anche [*componente*](vssgloss-c.md), [*percorso logico*](vssgloss-l.md).</span><span class="sxs-lookup"><span data-stu-id="1dbed-147">See also [*component*](vssgloss-c.md), [*logical path*](vssgloss-l.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**copia shadow di superficie**</span><span class="sxs-lookup"><span data-stu-id="1dbed-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**surfaced shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-149">Volume replicato nascosto visibile allo spazio dei nomi del gestore di montaggio di un sistema, ovvero **FindFirstVolume** e **FindNextVolume** possono trovarlo e vengono generate le notifiche di arrivo e di partenza del volume.</span><span class="sxs-lookup"><span data-stu-id="1dbed-149">A shadow copied volume visible to a system's Mount Manager namespace—meaning **FindFirstVolume** and **FindNextVolume** can find it and that volume arrival and departure notifications are generated.</span></span> <span data-ttu-id="1dbed-150">Tutte le copie shadow esposte sono anche copie shadow di superficie.</span><span class="sxs-lookup"><span data-stu-id="1dbed-150">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="1dbed-151">Tuttavia, non è necessario esporre una copia shadow di superficie.</span><span class="sxs-lookup"><span data-stu-id="1dbed-151">However, a surfaced shadow copy need not be exposed.</span></span> <span data-ttu-id="1dbed-152">Se una copia shadow è trasportabile, non può essere rilevata.</span><span class="sxs-lookup"><span data-stu-id="1dbed-152">If a shadow copy is transportable, it cannot be surfaced.</span></span> <span data-ttu-id="1dbed-153">Vedere anche [*Copia Shadow esposta*](vssgloss-e.md), [*copia shadow trasportabile*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="1dbed-153">See also [*exposed shadow copy*](vssgloss-e.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Protezione file di sistema**</span><span class="sxs-lookup"><span data-stu-id="1dbed-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**System File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-155">Vedere [*protezione file di Windows*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="1dbed-155">See [*Windows File Protection*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**applicazioni a livello di sistema**</span><span class="sxs-lookup"><span data-stu-id="1dbed-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**system-level applications**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-157">Indica il punto in cui VSS invia una notifica al writer di un blocco.</span><span class="sxs-lookup"><span data-stu-id="1dbed-157">Indicates the point at which VSS notifies a writer of a freeze.</span></span> <span data-ttu-id="1dbed-158">I writer inizializzati come applicazioni a livello di sistema ricevono una notifica dopo che i writer sono stati inizializzati come applicazioni di livello front-end o come applicazioni di livello back-end.</span><span class="sxs-lookup"><span data-stu-id="1dbed-158">Writers that are initialized as system-level applications are notified after writers initialized either as front-end level applications or as back-end level applications.</span></span> <span data-ttu-id="1dbed-159">Vedere anche il [*livello applicazione*](vssgloss-a.md), [*le applicazioni di livello back-end*](vssgloss-b.md), [*le applicazioni di livello front-end*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="1dbed-159">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*front-end level applications*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**provider di sistema**</span><span class="sxs-lookup"><span data-stu-id="1dbed-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**system provider**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-161">Provider preinstallato predefinito fornito come parte di Windows.</span><span class="sxs-lookup"><span data-stu-id="1dbed-161">The default preinstalled provider provided as part of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1dbed-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Cartella volume di sistema**</span><span class="sxs-lookup"><span data-stu-id="1dbed-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**System Volume Folder**</span></span>
</dt> <dd>

<span data-ttu-id="1dbed-163">Una directory condivisa in cui sono archiviate le copie condivise dei file pubblici di un dominio, ovvero i file replicati tra tutti i controller di dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="1dbed-163">A shared directory that stores the shared copies of a domain's public files—that is, those files that are replicated among all domain controllers in the domain.</span></span>

</dd> </dl>

 

 



