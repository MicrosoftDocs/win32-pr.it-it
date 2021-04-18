---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307152"
---
# <a name="a-volume-shadow-copy-service"></a><span data-ttu-id="c8723-103">A (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="c8723-103">A (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="c8723-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="c8723-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c8723-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Evento Abort**</span><span class="sxs-lookup"><span data-stu-id="c8723-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abort event**</span></span>
</dt> <dd>

<span data-ttu-id="c8723-106">Evento VSS emesso dal Servizio Copia Shadow del volume che indica che un'operazione di backup o ripristino conforme è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="c8723-106">A VSS event issued by the Volume Shadow Copy Service indicating that a compliant backup or restore operation has been aborted.</span></span> <span data-ttu-id="c8723-107">Il gestore eventi è **CVssWriter:: OnAbort**.</span><span class="sxs-lookup"><span data-stu-id="c8723-107">The event handler is **CVssWriter::OnAbort**.</span></span>

</dd> <dt>

<span data-ttu-id="c8723-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="c8723-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span></span>
</dt> <dd>

<span data-ttu-id="c8723-109">Il servizio Active Directory (ADSI) è un servizio basato su COM che fornisce un meccanismo per l'individuazione, l'identificazione e l'accesso agli utenti e alle risorse disponibili in un sistema di ambiente di elaborazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="c8723-109">Active Directory Service (ADSI) is a COM-based service providing a mechanism for locating, identifying, and accessing the users and resources available in a distributed computing environment system.</span></span> <span data-ttu-id="c8723-110">In particolare, il servizio Active Directory viene utilizzato per gestire le informazioni sulle directory aziendali per la distribuzione da parte di un server di dominio Windows.</span><span class="sxs-lookup"><span data-stu-id="c8723-110">In particular, the Active Directory service is used to manage enterprise directory information for distribution by a Windows domain server.</span></span>

</dd> <dt>

<span data-ttu-id="c8723-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**mapping del percorso alternativo**</span><span class="sxs-lookup"><span data-stu-id="c8723-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**alternate location mapping**</span></span>
</dt> <dd>

<span data-ttu-id="c8723-112">Un percorso diverso dal percorso originale di un file, in cui il file può essere ripristinato in determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="c8723-112">A path, other than a file's original path, to which the file may be restored under certain conditions.</span></span> <span data-ttu-id="c8723-113">In genere, i mapping dei percorsi alternativi non sono definiti per un singolo file ben definito, ma per una coppia di specifiche di percorso/file e possono essere ricorsivi.</span><span class="sxs-lookup"><span data-stu-id="c8723-113">Typically, alternate location mappings are not defined for a single well-defined file, but for a path/file specification pair, and may be recursive.</span></span>

<span data-ttu-id="c8723-114">Un mapping del percorso alternativo viene usato solo durante un'operazione di ripristino e non deve essere confuso con un percorso alternativo, che viene usato solo durante un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="c8723-114">An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.</span></span> <span data-ttu-id="c8723-115">Vedere anche *percorso alternativo*.</span><span class="sxs-lookup"><span data-stu-id="c8723-115">See also *alternate path*.</span></span>

</dd> <dt>

<span data-ttu-id="c8723-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**percorso alternativo**</span><span class="sxs-lookup"><span data-stu-id="c8723-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**alternate path**</span></span>
</dt> <dd>

<span data-ttu-id="c8723-117">Durante le operazioni di backup, una coppia di specifiche di percorso/file (gestita da un'istanza dell'interfaccia **IVssWMFiledesc** ) ha un percorso alternativo se il descrittore del file (come restituito da **IVssWMFiledesc:: GetAlternateLocation**) è diverso da null.</span><span class="sxs-lookup"><span data-stu-id="c8723-117">During backup operations, a path/file specification pair (handled by an instance of the **IVssWMFiledesc** interface) is said to have an alternate path if its file descriptor (as returned by **IVssWMFiledesc::GetAlternateLocation**) is non-NULL.</span></span> <span data-ttu-id="c8723-118">Da questo percorso, invece del percorso specificato predefinito, i file devono essere copiati quando viene eseguito il backup di un volume.</span><span class="sxs-lookup"><span data-stu-id="c8723-118">It is from this path, rather than the default specified path, that files are to be copied when a volume is backed up.</span></span>

<span data-ttu-id="c8723-119">Un percorso alternativo viene usato solo durante un'operazione di backup e non deve essere confuso con un mapping del percorso alternativo.</span><span class="sxs-lookup"><span data-stu-id="c8723-119">An alternate path is used only during a backup operation and should not be confused with an alternate location mapping.</span></span> <span data-ttu-id="c8723-120">Un mapping del percorso alternativo viene usato solo durante le operazioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c8723-120">An alternate location mapping is used only during restore operations.</span></span> <span data-ttu-id="c8723-121">Vedere anche *mapping del percorso alternativo*.</span><span class="sxs-lookup"><span data-stu-id="c8723-121">See also *alternate location mapping*.</span></span>

</dd> <dt>

<span data-ttu-id="c8723-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**livello applicazione**</span><span class="sxs-lookup"><span data-stu-id="c8723-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**application level**</span></span>
</dt> <dd>

<span data-ttu-id="c8723-123">Utilizzato da VSS per indicare il punto nel corso della creazione di una copia shadow a cui un writer riceve un blocco.</span><span class="sxs-lookup"><span data-stu-id="c8723-123">Used by VSS to indicate the point in the course of the creation of a shadow copy that a writer is notified of a freeze.</span></span> <span data-ttu-id="c8723-124">Vedere anche [*applicazioni di livello back-end*](vssgloss-b.md), [*blocco*](vssgloss-f.md), [*applicazioni di livello front-end*](vssgloss-f.md), [*Copia Shadow*](vssgloss-s.md), [*applicazioni a livello di sistema*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="c8723-124">See also [*back-end level applications*](vssgloss-b.md), [*freeze*](vssgloss-f.md), [*front-end level applications*](vssgloss-f.md), [*shadow copy*](vssgloss-s.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8723-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**copia shadow recuperata automaticamente**</span><span class="sxs-lookup"><span data-stu-id="c8723-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**auto-recovered shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="c8723-126">Una copia shadow che ha eseguito un'elaborazione aggiuntiva da parte di un writer è in uno stato completamente coerente per le azioni di backup o data mining (ad esempio, il rollback di tutte le transazioni non ancora completate nel punto in cui è stata creata la copia shadow). Questo può essere avviato da un writer specificando un flag appropriato dall'enumerazione dei **\_ \_ flag del componente VSS** nel membro **dwComponentFlags** della struttura **\_ COMPONENTINFO VSS** o da un richiedente aggiungendo il flag **VSS \_ VolSnap \_ attr \_ rollback \_ Recovery** al contesto per la copia shadow.</span><span class="sxs-lookup"><span data-stu-id="c8723-126">A shadow copy that has had additional processing by a writer to be in a completely consistent state for backup or data mining actions (for example, rolling back all transactions that did not yet complete at the point that the shadow copy was created.) This can be initiated by a writer by specifying an appropriate flag from the **VSS\_COMPONENT\_FLAGS** enumeration in the **dwComponentFlags** member of the **VSS\_COMPONENTINFO** structure or by a requester by adding the **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** flag to the context for the shadow copy.</span></span> <span data-ttu-id="c8723-127">Il ripristino automatico consente di usare i dati copiati in modalità shadow in un volume di sola lettura, ad data mining, ripristini parziali, ad esempio gli elementi selezionati in un database, o altri scopi.</span><span class="sxs-lookup"><span data-stu-id="c8723-127">Auto-recovery allows the shadow copied data to be used on a read-only volume, for data mining, partial restores (for example selected items in a database), or other purposes.</span></span>

<span data-ttu-id="c8723-128">Vedere anche [*copia shadow trasportabile*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="c8723-128">See also [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8723-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**copia shadow della versione automatica**</span><span class="sxs-lookup"><span data-stu-id="c8723-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**auto-release shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="c8723-130">Copia shadow che verrà eliminata al termine di un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="c8723-130">A shadow copy that will be deleted upon the termination of a backup operation.</span></span> <span data-ttu-id="c8723-131">A livello di codice, ciò significa che la copia shadow verrà eliminata quando viene rilasciata l'interfaccia **IVssBackupComponents** .</span><span class="sxs-lookup"><span data-stu-id="c8723-131">Programmatically, this means the shadow copy will be deleted when the **IVssBackupComponents** interface is released.</span></span> <span data-ttu-id="c8723-132">Una copia shadow con rilascio automatico non può essere persistente.</span><span class="sxs-lookup"><span data-stu-id="c8723-132">An auto-release shadow copy cannot be persistent.</span></span>

<span data-ttu-id="c8723-133">Per impostazione predefinita, tutte le copie shadow sono rilasciate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c8723-133">By default, all shadow copies are auto-release.</span></span> <span data-ttu-id="c8723-134">Vedere anche [*Copia Shadow persistente*](vssgloss-p.md), [*copia shadow trasportabile*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="c8723-134">See also [*persistent shadow copy*](vssgloss-p.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> </dl>

 

 



