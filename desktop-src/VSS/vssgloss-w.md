---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526268"
---
# <a name="w-volume-shadow-copy-service"></a><span data-ttu-id="cd544-103">W (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="cd544-103">W (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="cd544-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="cd544-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="cd544-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Protezione file di Windows**</span><span class="sxs-lookup"><span data-stu-id="cd544-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="cd544-106">Servizio di sistema che protegge i file speciali del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cd544-106">A system service that protects special operating system files.</span></span> <span data-ttu-id="cd544-107">Se uno di questi file viene eliminato o sovrascritto, la protezione dei file di Windows sostituisce il file con quello originale dalla relativa cache.</span><span class="sxs-lookup"><span data-stu-id="cd544-107">If one of these files is deleted or overwritten, Windows File Protection replaces the file with the original from its cache.</span></span>

</dd> <dt>

<span data-ttu-id="cd544-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**Writer**</span><span class="sxs-lookup"><span data-stu-id="cd544-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**writer**</span></span>
</dt> <dd>

<span data-ttu-id="cd544-109">Applicazione che coordina le operazioni di I/O con la copia shadow VSS e le operazioni correlate alla copia shadow, ad esempio backup e ripristini, in modo che i dati contenuti nel volume copiato Shadow siano in uno stato coerente.</span><span class="sxs-lookup"><span data-stu-id="cd544-109">An application that coordinates its I/O operations with VSS shadow copy and shadow copy related operations (such as backups and restores) so that their data contained on the shadow copied volume is in a consistent state.</span></span>

<span data-ttu-id="cd544-110">Per supportare questo coordinamento, un writer deve implementare un'istanza di una classe derivata dalla classe di base astratta **CVssWriter** per comunicare con l'infrastruttura VSS.</span><span class="sxs-lookup"><span data-stu-id="cd544-110">To support this coordination, a writer must implement an instance of a class derived from the abstract base class **CVssWriter** to communicate with the VSS infrastructure.</span></span> <span data-ttu-id="cd544-111">Vedere anche [*Copia Shadow*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="cd544-111">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd544-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**classe Writer**</span><span class="sxs-lookup"><span data-stu-id="cd544-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**writer class**</span></span>
</dt> <dd>

<span data-ttu-id="cd544-113">Identificatore univoco globale (GUID) fornito da un writer durante l'inizializzazione per indicare che appartiene a un tipo specificato di writer.</span><span class="sxs-lookup"><span data-stu-id="cd544-113">A globally unique identifier (GUID) supplied by a writer during initialization to indicate that it belongs to a given type of writers.</span></span> <span data-ttu-id="cd544-114">Ad esempio, più implementazioni di un writer possono condividere lo stesso ID di classe Writer.</span><span class="sxs-lookup"><span data-stu-id="cd544-114">For instance, multiple implementations of a writer could share the same writer class ID.</span></span>

<span data-ttu-id="cd544-115">I writer della stessa classe possono essere distinti dalle istanze del writer.</span><span class="sxs-lookup"><span data-stu-id="cd544-115">Writers of the same class may be distinguished by their writer instances.</span></span> <span data-ttu-id="cd544-116">È spetta a uno sviluppatore di applicazioni specificare le classi writer.</span><span class="sxs-lookup"><span data-stu-id="cd544-116">It is up to an application developer to specify writer classes.</span></span> <span data-ttu-id="cd544-117">Vedere anche *istanza del writer*.</span><span class="sxs-lookup"><span data-stu-id="cd544-117">See also *writer instance*.</span></span>

</dd> <dt>

<span data-ttu-id="cd544-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**istanza writer**</span><span class="sxs-lookup"><span data-stu-id="cd544-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**writer instance**</span></span>
</dt> <dd>

<span data-ttu-id="cd544-119">Identificatore univoco globale (GUID) fornito da VSS per ogni processo del writer eseguito in un sistema.</span><span class="sxs-lookup"><span data-stu-id="cd544-119">A globally unique identifier (GUID) supplied by VSS for each writer process running on a system.</span></span> <span data-ttu-id="cd544-120">Ogni volta che viene avviato il writer, viene generato un valore univoco per l'istanza del writer.</span><span class="sxs-lookup"><span data-stu-id="cd544-120">A unique value for the writer instance is generated each time the writer starts.</span></span>

</dd> <dt>

<span data-ttu-id="cd544-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Documento di metadati del writer**</span><span class="sxs-lookup"><span data-stu-id="cd544-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Writer Metadata Document**</span></span>
</dt> <dd>

<span data-ttu-id="cd544-122">Documento XML creato da un writer (usando l'interfaccia **IVssCreateWriterMetadata** ) che contiene informazioni sullo stato e sui componenti del writer.</span><span class="sxs-lookup"><span data-stu-id="cd544-122">An XML document created by a writer (using the **IVssCreateWriterMetadata** interface) containing information about the writer's state and components.</span></span> <span data-ttu-id="cd544-123">Un richiedente può eseguire query sui documenti di metadati del writer (usando l'interfaccia **IVssExamineWriterMetadata** ) quando si esegue un'operazione di ripristino o di backup.</span><span class="sxs-lookup"><span data-stu-id="cd544-123">A requester can query Writer Metadata Documents (using the **IVssExamineWriterMetadata** interface) when performing a restore or backup operation.</span></span>

<span data-ttu-id="cd544-124">Un documento di metadati del writer contiene l'elenco di tutti i componenti di un writer, ciascuno dei quali può partecipare a un backup.</span><span class="sxs-lookup"><span data-stu-id="cd544-124">A Writer Metadata Document contains the list of all of a writer's components, any one of which might participate in a backup.</span></span> <span data-ttu-id="cd544-125">Questo comportamento è diverso dal documento relativo ai componenti di backup del richiedente, che contiene solo i componenti inclusi in modo esplicito per un'operazione di backup o ripristino.</span><span class="sxs-lookup"><span data-stu-id="cd544-125">This differs from the requester's Backup Components Document, which contains only those components explicitly included for a backup or restore operation.</span></span>

<span data-ttu-id="cd544-126">Una volta creato, il documento di metadati del writer deve essere visualizzato come oggetto di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cd544-126">Once constructed, the Writer Metadata Document should be viewed as a read-only object.</span></span> <span data-ttu-id="cd544-127">Può essere salvato su disco.</span><span class="sxs-lookup"><span data-stu-id="cd544-127">It can be saved to disk.</span></span> <span data-ttu-id="cd544-128">Vedere anche [*documento sui componenti di backup*](vssgloss-b.md), [*inclusione di componenti espliciti*](vssgloss-e.md), [*inclusione di componenti impliciti*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="cd544-128">See also [*Backup Components Document*](vssgloss-b.md), [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> </dl>

 

 



