---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751538"
---
# <a name="i-volume-shadow-copy-service"></a><span data-ttu-id="a38f7-103">I (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="a38f7-103">I (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="a38f7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) i J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="a38f7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a38f7-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identifica evento**</span><span class="sxs-lookup"><span data-stu-id="a38f7-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identify event**</span></span>
</dt> <dd>

<span data-ttu-id="a38f7-106">Evento VSS che indica che un writer o un richiedente deve eseguire una query sul writer corrente.</span><span class="sxs-lookup"><span data-stu-id="a38f7-106">A VSS event indicating that a writer or a requester needs to query the current writer.</span></span> <span data-ttu-id="a38f7-107">Viene utilizzato per creare le informazioni sui metadati del writer corrente.</span><span class="sxs-lookup"><span data-stu-id="a38f7-107">It is used to construct the current writer's metadata information.</span></span> <span data-ttu-id="a38f7-108">Vedere anche [*richiedente*](vssgloss-r.md), [*writer*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="a38f7-108">See also [*requester*](vssgloss-r.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="a38f7-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusione di componenti impliciti**</span><span class="sxs-lookup"><span data-stu-id="a38f7-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**implicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="a38f7-110">Non aggiungere le informazioni di un componente al documento dei componenti di backup di un richiedente quando partecipa a un'operazione di backup o ripristino.</span><span class="sxs-lookup"><span data-stu-id="a38f7-110">Not adding a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span>

<span data-ttu-id="a38f7-111">I componenti non selezionabili con un predecessore selezionabile sono inclusi implicitamente solo se il relativo predecessore è incluso.</span><span class="sxs-lookup"><span data-stu-id="a38f7-111">Nonselectable components with a selectable ancestor are only implicitly included if their ancestor is included.</span></span>

<span data-ttu-id="a38f7-112">I componenti selezionabili con un predecessore selezionabile possono essere inclusi implicitamente, se il predecessore è incluso, oppure possono essere inclusi in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="a38f7-112">Selectable components with a selectable ancestor may be included implicitly, if the ancestor is included, or may be included explicitly.</span></span>

<span data-ttu-id="a38f7-113">I componenti non selezionabili senza predecessori selezionabili non sono mai inclusi in modo implicito in un'operazione di backup o ripristino. tutti questi componenti devono essere aggiunti in modo esplicito al documento componenti di backup se uno dei componenti del writer partecipa.</span><span class="sxs-lookup"><span data-stu-id="a38f7-113">Nonselectable components without any selectable ancestors are never implicitly included in a backup or restore operation—all such components must be explicitly added to the Backup Components Document if any of the writer's components participate.</span></span>

<span data-ttu-id="a38f7-114">I componenti selezionabili senza predecessori selezionabili scelti da un richiedente per la partecipazione a un backup o un ripristino non possono essere inclusi in modo implicito nell'operazione, ma devono essere aggiunti esplicitamente al documento componenti di backup.</span><span class="sxs-lookup"><span data-stu-id="a38f7-114">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore cannot be implicitly included in the operation, but must be explicitly added to the Backup Components Document.</span></span>

</dd> <dt>

<span data-ttu-id="a38f7-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**operazioni di backup incrementali**</span><span class="sxs-lookup"><span data-stu-id="a38f7-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**incremental backup operations**</span></span>
</dt> <dd>

<span data-ttu-id="a38f7-116">Un'operazione di backup o ripristino viene eseguita solo su file creati o modificati dopo il salvataggio dell'ultimo backup completo, incrementale o differenziale.</span><span class="sxs-lookup"><span data-stu-id="a38f7-116">A backup or restore operation is performed only on files created or changed since the last full, incremental, or differential backup was saved.</span></span> <span data-ttu-id="a38f7-117">Vedere anche [*operazioni di backup differenziali*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="a38f7-117">See also [*differential backup operations*](vssgloss-d.md).</span></span>

</dd> </dl>

 

 



