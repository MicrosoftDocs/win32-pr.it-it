---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20cabdfa5260f65d1176f6f1d12ac1d805b9dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343571"
---
# <a name="b-volume-shadow-copy-service"></a><span data-ttu-id="574b2-103">B (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="574b2-103">B (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="574b2-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="574b2-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="574b2-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**applicazioni di livello back-end**</span><span class="sxs-lookup"><span data-stu-id="574b2-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**back-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="574b2-106">Indica il punto al quale un writer riceve una notifica di blocco da parte del servizio Copia Shadow del volume.</span><span class="sxs-lookup"><span data-stu-id="574b2-106">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="574b2-107">I writer inizializzati come applicazioni di livello back-end vengono informati dopo che i writer sono stati inizializzati come applicazioni di livello front-end e prima di quelli inizializzati come applicazioni a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="574b2-107">Writers that are initialized as back-end level applications are notified after writers initialized as front-end level applications and prior to those initialized as system-level applications.</span></span> <span data-ttu-id="574b2-108">Vedere anche [*a livello di applicazione*](vssgloss-a.md), applicazioni di [*livello front-end*](vssgloss-f.md), [*applicazioni a livello di sistema*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="574b2-108">See also [*application level*](vssgloss-a.md), [*front-end level applications*](vssgloss-f.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="574b2-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**Evento BackupComplete**</span><span class="sxs-lookup"><span data-stu-id="574b2-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete event**</span></span>
</dt> <dd>

<span data-ttu-id="574b2-110">Evento VSS che indica il completamento di un backup VSS.</span><span class="sxs-lookup"><span data-stu-id="574b2-110">A VSS event indicating that a VSS backup has completed.</span></span> <span data-ttu-id="574b2-111">Questo evento deve essere seguito da un evento BackupShutdown sotto il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="574b2-111">This event should be followed by a BackupShutdown event under normal operation.</span></span> <span data-ttu-id="574b2-112">Vedere anche *evento BackupShutdown*.</span><span class="sxs-lookup"><span data-stu-id="574b2-112">See also *BackupShutdown event*.</span></span>

</dd> <dt>

<span data-ttu-id="574b2-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Documento componenti di backup**</span><span class="sxs-lookup"><span data-stu-id="574b2-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Backup Components Document**</span></span>
</dt> <dd>

<span data-ttu-id="574b2-114">Documento XML creato da un richiedente (usando l'interfaccia **IVssBackupComponents** ) nel corso della configurazione di un'operazione di ripristino o di backup.</span><span class="sxs-lookup"><span data-stu-id="574b2-114">An XML document created by a requester (using the **IVssBackupComponents** interface) in the course of setting up a restore or backup operation.</span></span> <span data-ttu-id="574b2-115">Il documento dei componenti di backup contiene un elenco dei componenti inclusi in modo esplicito, da uno o più writer, che partecipano a un'operazione di backup o di ripristino.</span><span class="sxs-lookup"><span data-stu-id="574b2-115">The Backup Components Document contains a list of those explicitly included components, from one or more writers, participating in a backup or restore operation.</span></span> <span data-ttu-id="574b2-116">Non contiene informazioni sui componenti inclusi in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="574b2-116">It does not contain implicitly included component information.</span></span> <span data-ttu-id="574b2-117">Al contrario, un documento di metadati del writer contiene solo i componenti del writer che possono partecipare a un backup.</span><span class="sxs-lookup"><span data-stu-id="574b2-117">In contrast, a Writer Metadata Document contains only writer components that may participate in a backup.</span></span>

<span data-ttu-id="574b2-118">Un documento relativo ai componenti di backup può essere salvato su disco.</span><span class="sxs-lookup"><span data-stu-id="574b2-118">A Backup Components Document can be saved to disk.</span></span> <span data-ttu-id="574b2-119">Vedere anche [*inclusione esplicita del componente*](vssgloss-e.md), [*inclusione di componenti impliciti*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="574b2-119">See also [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="574b2-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**set di backup**</span><span class="sxs-lookup"><span data-stu-id="574b2-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**backup set**</span></span>
</dt> <dd>

<span data-ttu-id="574b2-121">File di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="574b2-121">Those files to be backed up.</span></span> <span data-ttu-id="574b2-122">Include i file selezionati per inclusione in un componente, quelli indicati dalle istruzioni di inclusione a livello di writer, meno i file che sono stati inclusi in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="574b2-122">It includes files selected by inclusion in a component, those indicated by writer-level include statements, less those files that have been explicitly included.</span></span>

</dd> <dt>

<span data-ttu-id="574b2-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**Evento BackupShutdown**</span><span class="sxs-lookup"><span data-stu-id="574b2-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown event**</span></span>
</dt> <dd>

<span data-ttu-id="574b2-124">Evento VSS che indica che un'applicazione di backup conforme è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="574b2-124">A VSS event indicating that a compliant backup application has shut down.</span></span> <span data-ttu-id="574b2-125">In genere, questo è preceduto da un evento BackupComplete.</span><span class="sxs-lookup"><span data-stu-id="574b2-125">Normally, this is preceded by a BackupComplete event.</span></span> <span data-ttu-id="574b2-126">Tuttavia, se un backup termina in modo imprevisto, questo evento può essere generato senza un evento BackupComplete precedente.</span><span class="sxs-lookup"><span data-stu-id="574b2-126">However, if a backup terminates unexpectedly, this event can be generated without a preceding BackupComplete event.</span></span> <span data-ttu-id="574b2-127">Vedere anche *Evento BackupComplete*.</span><span class="sxs-lookup"><span data-stu-id="574b2-127">See also *BackupComplete event*.</span></span>

</dd> <dt>

<span data-ttu-id="574b2-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**timbro di backup**</span><span class="sxs-lookup"><span data-stu-id="574b2-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**backup stamp**</span></span>
</dt> <dd>

<span data-ttu-id="574b2-129">Stringa contenente le informazioni relative al momento in cui si è verificata una copia di backup.</span><span class="sxs-lookup"><span data-stu-id="574b2-129">A string containing information as to when a backup took place.</span></span> <span data-ttu-id="574b2-130">VSS non impone alcuna restrizione al formato di questa stringa, ad eccezione del fatto che è comprensibile per tutte le istanze del writer di una determinata classe.</span><span class="sxs-lookup"><span data-stu-id="574b2-130">VSS places no restriction on the format of this string, except that it be intelligible to all the writer instances of a given class.</span></span> <span data-ttu-id="574b2-131">Può contenere informazioni su data e ora, numeri di sequenza logici o qualsiasi altra informazione che consenta a un writer della stessa classe di determinare il momento in cui viene eseguita l'ultimo backup.</span><span class="sxs-lookup"><span data-stu-id="574b2-131">It may contain time and date information, logical sequence numbers, or any other information that will allow a writer of the same class to determine when the last backup has take place.</span></span>

</dd> </dl>

 

 



