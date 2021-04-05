---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751543"
---
# <a name="f-volume-shadow-copy-service"></a><span data-ttu-id="c8b9e-103">F (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="c8b9e-103">F (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="c8b9e-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="c8b9e-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c8b9e-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**componente del gruppo di file**</span><span class="sxs-lookup"><span data-stu-id="c8b9e-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**file group component**</span></span>
</dt> <dd>

<span data-ttu-id="c8b9e-106">Gruppo di file diversi da quelli usati come database e definiti da un writer per la necessità di essere gestiti come unità durante le operazioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-106">A group of files other than those used as a database and defined by a writer as needing to be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="c8b9e-107">Vedere anche [*componente*](vssgloss-c.md), [*componente di database*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="c8b9e-107">See also [*component*](vssgloss-c.md), [*database component*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b9e-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**set di file**</span><span class="sxs-lookup"><span data-stu-id="c8b9e-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**file set**</span></span>
</dt> <dd>

<span data-ttu-id="c8b9e-109">Combinazione di un percorso, una specifica del file e un flag ricorsivo che descrive uno di un file o un gruppo di file.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-109">The combination of a path, file specification, and recursive flag describing one of a file or group of files.</span></span> <span data-ttu-id="c8b9e-110">Ad esempio, i file vengono aggiunti ai componenti nei set di file.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-110">For example, files are added to components in file sets.</span></span>

<span data-ttu-id="c8b9e-111">Se non diversamente specificato, i percorsi di un set di file sono percorsi standard di Windows e possono contenere variabili di ambiente (ad esempio,% SystemRoot%) ma non può contenere caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-111">Unless otherwise indicated, a file set's paths are standard Windows paths and can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.</span></span> <span data-ttu-id="c8b9e-112">Non è necessario che il percorso termini con una barra rovesciata (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="c8b9e-112">There is no requirement that the path end with a backslash ("\\").</span></span> <span data-ttu-id="c8b9e-113">Sono le applicazioni che recuperano queste informazioni per verificarle.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-113">It is up to applications that retrieve this information to check it.</span></span>

<span data-ttu-id="c8b9e-114">La specifica del file contenuta in un set di file indica il nome del file o dei file inclusi.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-114">The file specification contained in a file set indicates the name of the file or files it includes.</span></span> <span data-ttu-id="c8b9e-115">Questa specifica del file non può contenere specifiche di directory (ad esempio, nessuna barra rovesciata), ma può contenere?</span><span class="sxs-lookup"><span data-stu-id="c8b9e-115">This file specification cannot contain directory specifications (for example, no backslashes) but can contain the ?</span></span> <span data-ttu-id="c8b9e-116">e \* caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-116">and \* wildcard characters.</span></span>

<span data-ttu-id="c8b9e-117">Il tag ricorsivo è un valore booleano che specifica se il percorso del set di file deve essere trattato come una sola directory o se indica una gerarchia di directory da attraversare in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-117">The recursive tag is a Boolean specifying whether the file set's path should be treated as a only a single directory or if it indicates a hierarchy of directories to be traversed recursively.</span></span> <span data-ttu-id="c8b9e-118">Il valore booleano è **true** se il percorso viene considerato come una gerarchia di directory da attraversare in modo ricorsivo; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="c8b9e-118">The Boolean is **true** if the path is treated as a hierarchy of directories to be traversed recursively, or **false** if not.</span></span>

<span data-ttu-id="c8b9e-119">Le informazioni su un set di file vengono restituite tramite istanze dell'interfaccia **IVssWMFiledesc** e possono contenere informazioni aggiuntive, tra cui percorsi alternativi, mapping dei percorsi alternativi e impostazioni di supporto dello schema a livello di file.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-119">Information about a file set is returned through instances of the **IVssWMFiledesc** interface, and can contain additional information includes alternate paths, alternate location mappings, and file-level schema support settings.</span></span>

<span data-ttu-id="c8b9e-120">Vedere anche [*percorso alternativo*](vssgloss-a.md), [*mapping del percorso alternativo*](vssgloss-a.md), [*componente*](vssgloss-c.md), *specifica del file*.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-120">See also [*alternate path*](vssgloss-a.md), [*alternate location mapping*](vssgloss-a.md), [*component*](vssgloss-c.md), *file specification*.</span></span>

</dd> <dt>

<span data-ttu-id="c8b9e-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**Specifica file**</span><span class="sxs-lookup"><span data-stu-id="c8b9e-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**file specification**</span></span>
</dt> <dd>

<span data-ttu-id="c8b9e-122">Utilizzato per la corrispondenza dei file all'interno di una directory e per la definizione di un set di file.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-122">Used to match files within a directory and to define a file set.</span></span> <span data-ttu-id="c8b9e-123">Non può contenere specifiche di directory (ad esempio, nessuna barra rovesciata), ma può contenere?</span><span class="sxs-lookup"><span data-stu-id="c8b9e-123">It cannot contain directory specifications (for example, no backslashes) but it can contain the ?</span></span> <span data-ttu-id="c8b9e-124">e \* caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-124">and \* wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="c8b9e-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Servizio Replica file**</span><span class="sxs-lookup"><span data-stu-id="c8b9e-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**File Replication Service**</span></span>
</dt> <dd>

<span data-ttu-id="c8b9e-126">Utilizzato per replicare i file di sistema in una directory di volume di sistema ridondante (SysVol) per supportare file system la sopravvivenza, in particolare per i file system distribuiti.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-126">Used to replicate system files in a redundant system volume (SysVol) directory to support file system survivability, particularly for distributed file systems.</span></span>

</dd> <dt>

<span data-ttu-id="c8b9e-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**congelare**</span><span class="sxs-lookup"><span data-stu-id="c8b9e-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**freeze**</span></span>
</dt> <dd>

<span data-ttu-id="c8b9e-128">Periodo di tempo durante il processo di creazione della copia shadow quando tutti i writer hanno scaricato le scritture nei volumi e non stanno avviando scritture aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-128">A period of time during the shadow copy creation process when all writers have flushed their writes to the volumes and are not initiating additional writes.</span></span>

</dd> <dt>

<span data-ttu-id="c8b9e-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Blocca evento**</span><span class="sxs-lookup"><span data-stu-id="c8b9e-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Freeze event**</span></span>
</dt> <dd>

<span data-ttu-id="c8b9e-130">Evento VSS che indica che è in corso un blocco della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-130">A VSS event indicating that a shadow copy freeze is in progress.</span></span> <span data-ttu-id="c8b9e-131">Vedere anche *Freeze*, [*Copia Shadow*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="c8b9e-131">See also *freeze*, [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b9e-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**applicazioni di livello front-end**</span><span class="sxs-lookup"><span data-stu-id="c8b9e-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**front-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="c8b9e-133">Indica il punto al quale un writer riceve una notifica di blocco da parte del servizio Copia Shadow del volume.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-133">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="c8b9e-134">I writer inizializzati come applicazioni di livello front-end ricevono una notifica prima che i writer siano inizializzati come applicazioni di livello back-end o come applicazioni a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c8b9e-134">Writers that were initialized as front-end level applications are notified prior to writers initialized either as back-end level applications or as system-level applications.</span></span> <span data-ttu-id="c8b9e-135">Vedere anche il [*livello applicazione*](vssgloss-a.md), [*le applicazioni a livello di back-end*](vssgloss-b.md), [*le applicazioni a livello di sistema*](vssgloss-s.md)e il [*writer*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="c8b9e-135">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> </dl>

 

 



