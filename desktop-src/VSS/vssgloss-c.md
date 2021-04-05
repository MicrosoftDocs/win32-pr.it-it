---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751554"
---
# <a name="c-volume-shadow-copy-service"></a><span data-ttu-id="ba285-103">C (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="ba285-103">C (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="ba285-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="ba285-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="ba285-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="ba285-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="ba285-106">Entità considerata attendibile per emettere certificati che dichiara che il destinatario, il computer o l'organizzazione che richiede il certificato soddisfa le condizioni di un criterio stabilito.</span><span class="sxs-lookup"><span data-stu-id="ba285-106">An entity entrusted to issue certificates asserting that the recipient individual, machine, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="ba285-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**copia shadow accessibile dal client**</span><span class="sxs-lookup"><span data-stu-id="ba285-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**client-accessible shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ba285-108">Copia shadow creata dal provider di sistema per supportare copie shadow per cartelle condivise e altri meccanismi di rollback, che consentono ai client di visualizzare le versioni precedenti dei file e di annullare gli errori senza richiedere un ripristino completo.</span><span class="sxs-lookup"><span data-stu-id="ba285-108">A shadow copy created by the system provider to support Shadow Copies for Shared Folders and other rollback mechanisms, which allow clients to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="ba285-109">Viene creata una copia shadow accessibile dal client usando il **valore \_ \_ \_ accessibile del client VSS CTX** dell'enumerazione del [**\_ \_ \_ contesto dello snapshot VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) .</span><span class="sxs-lookup"><span data-stu-id="ba285-109">A client-accessible shadow copy is created using the **VSS\_CTX\_CLIENT\_ACCESSIBLE** value of the [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) enumeration.</span></span> <span data-ttu-id="ba285-110">Inoltre, il \_ \_ valore accessibile del client VSS VolSnap attr \_ \_ dell'enumerazione degli [**\_ \_ attributi degli \_ snapshot \_ del volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) viene impostato automaticamente per le copie shadow accessibili dal client.</span><span class="sxs-lookup"><span data-stu-id="ba285-110">In addition, the VSS\_VOLSNAP\_ATTR\_CLIENT\_ACCESSIBLE value of the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration is set automatically for client-accessible shadow copies.</span></span> <span data-ttu-id="ba285-111">Vedere anche [*copie shadow per cartelle condivise*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="ba285-111">See also [*Shadow Copies for Shared Folders*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba285-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**componente**</span><span class="sxs-lookup"><span data-stu-id="ba285-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="ba285-113">Gruppo di file, definito da un writer, che deve essere gestito come un'unità durante le operazioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="ba285-113">A group of files, defined by a writer, that must be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="ba285-114">Vedere anche componente del [*database*](vssgloss-d.md), [*componente del gruppo di file*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="ba285-114">See also [*database component*](vssgloss-d.md), [*file group component*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba285-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dipendenza componente**</span><span class="sxs-lookup"><span data-stu-id="ba285-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**component dependency**</span></span>
</dt> <dd>

<span data-ttu-id="ba285-116">Una situazione in cui un componente (e il set di componenti che definisce) gestito da un writer non può essere eseguito il backup o il ripristino indipendentemente dai componenti gestiti da altri writer.</span><span class="sxs-lookup"><span data-stu-id="ba285-116">A situation in which a component (and the component set it defines) managed by one writer cannot be backed up or restore independently of components managed by others writers.</span></span> <span data-ttu-id="ba285-117">Una dipendenza non indica un ordine di preferenza tra il componente con le dipendenze documentate e i componenti da cui dipende: una dipendenza indica semplicemente che il componente e i componenti da cui dipende devono essere sempre sottoposti a backup o ripristino contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="ba285-117">A dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on: a dependency merely indicates that the component and the components it depends on must always be backed up or restored together.</span></span>

</dd> <dt>

<span data-ttu-id="ba285-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**modalità componente**</span><span class="sxs-lookup"><span data-stu-id="ba285-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**component mode**</span></span>
</dt> <dd>

<span data-ttu-id="ba285-119">Modalità in cui un'operazione di backup o ripristino usa le informazioni sul componente di un writer.</span><span class="sxs-lookup"><span data-stu-id="ba285-119">A mode in which a backup or restore operation makes use of a writer's component information.</span></span> <span data-ttu-id="ba285-120">Vedere anche [*componente selezionabile*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="ba285-120">See also [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba285-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**set di componenti**</span><span class="sxs-lookup"><span data-stu-id="ba285-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**component set**</span></span>
</dt> <dd>

<span data-ttu-id="ba285-122">Gruppo di componenti con almeno un componente selezionabile (per il backup o il ripristino) e un numero di componenti non selezionabili organizzati in una gerarchia in base ai relativi percorsi logici.</span><span class="sxs-lookup"><span data-stu-id="ba285-122">A group of components with at least one selectable (for either backup or restore) component and a number of nonselectable components organized in a hierarchy by their logical paths.</span></span> <span data-ttu-id="ba285-123">La partecipazione implicita a un'operazione di backup o ripristino dipende dall'inclusione esplicita del componente selezionabile di primo livello.</span><span class="sxs-lookup"><span data-stu-id="ba285-123">The implicit participation in a backup or restore operation depends on the explicit inclusion of the top-level selectable component.</span></span> <span data-ttu-id="ba285-124">Solo le informazioni sul componente di questo componente selezionabile sono incluse nel documento componenti di backup.</span><span class="sxs-lookup"><span data-stu-id="ba285-124">Only the component information of this selectable component is included in the Backup Components Document.</span></span> <span data-ttu-id="ba285-125">Un set di componenti può includere sottocomponenti selezionabili e non selezionabili.</span><span class="sxs-lookup"><span data-stu-id="ba285-125">A component set may include selectable and nonselectable subcomponents.</span></span> <span data-ttu-id="ba285-126">Vedere anche [*percorso logico*](vssgloss-l.md), [*componente selezionabile*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="ba285-126">See also [*logical path*](vssgloss-l.md), [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba285-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copia shadow copia su scrittura**</span><span class="sxs-lookup"><span data-stu-id="ba285-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copy-on-write shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ba285-128">Copia shadow creata salvando solo le differenze rispetto al volume originale.</span><span class="sxs-lookup"><span data-stu-id="ba285-128">A shadow copy created by saving only the differences from the original volume.</span></span>

</dd> <dt>

<span data-ttu-id="ba285-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**stato di arresto anomalo del sistema**</span><span class="sxs-lookup"><span data-stu-id="ba285-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**crash consistent state**</span></span>
</dt> <dd>

<span data-ttu-id="ba285-130">Stato dei dischi equivalente a quello che verrebbe rilevato in seguito a un errore irreversibile che arresta improvvisamente il sistema.</span><span class="sxs-lookup"><span data-stu-id="ba285-130">The state of disks equivalent to what would be found following a catastrophic failure that abruptly shuts down the system.</span></span> <span data-ttu-id="ba285-131">Un ripristino da un set di copie shadow di questo tipo sarebbe equivalente a un riavvio dopo un arresto improvviso.</span><span class="sxs-lookup"><span data-stu-id="ba285-131">A restore from such a shadow copy set would be equivalent to a reboot following an abrupt shutdown.</span></span> <span data-ttu-id="ba285-132">Si tratta dello stato predefinito dei dati che sono stati replicati senza il supporto dei writer.</span><span class="sxs-lookup"><span data-stu-id="ba285-132">This is the default state of data that has been shadow copied without the support of writers.</span></span>

</dd> </dl>

 

 



