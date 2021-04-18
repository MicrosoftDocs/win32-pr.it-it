---
description: Quando un'operazione di backup VSS viene eseguita senza il coinvolgimento di un writer, la creazione della copia shadow può ancora verificarsi.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Backup senza partecipazione del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318907"
---
# <a name="backups-without-writer-participation"></a><span data-ttu-id="3b8ec-103">Backup senza partecipazione del writer</span><span class="sxs-lookup"><span data-stu-id="3b8ec-103">Backups without Writer Participation</span></span>

<span data-ttu-id="3b8ec-104">Quando un'operazione di backup VSS viene eseguita senza il coinvolgimento di un writer, la creazione della copia shadow può ancora verificarsi.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-104">When a VSS backup operation is conducted without the involvement of a writer, the shadow copy creation can still occur.</span></span>

<span data-ttu-id="3b8ec-105">Come indicato altrove (vedere [lo stato predefinito della copia shadow](shadow-copies-and-shadow-copy-sets.md)), il risultato di questo tipo di copia shadow è costituito da un volume che riflette lo stato di un disco al momento della copia shadow: i dati nel volume copiato shadow possono riflettere operazioni di I/o incomplete o parziali ed è descritto come in uno [*stato di arresto anomalo*](vssgloss-c.md)del sistema.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-105">As noted elsewhere (see [Default Shadow Copy State](shadow-copies-and-shadow-copy-sets.md)), the result of this type of shadow copy is a volume reflecting the state of a disk at the time of the shadow copy: data on the shadow-copied volume may reflect incomplete or partial I/O operations and is described as being in a [*crash-consistent state*](vssgloss-c.md).</span></span>

<span data-ttu-id="3b8ec-106">Esistono diverse situazioni in cui è necessario che un'applicazione di backup funzioni con i dati copiati shadow coerenti con l'arresto anomalo del sistema:</span><span class="sxs-lookup"><span data-stu-id="3b8ec-106">There are several situations that will require a backup application to work with crash consistent shadow copied data:</span></span>

-   <span data-ttu-id="3b8ec-107">**I dati sono gestiti da applicazioni non compatibili con VSS**</span><span class="sxs-lookup"><span data-stu-id="3b8ec-107">**Data is managed by VSS-unaware applications**</span></span>

    <span data-ttu-id="3b8ec-108">Quasi tutti i sistemi disporranno di alcune applicazioni, ad esempio editor di testo, lettori di posta elettronica, elaboratori di testi e così via, che non sono in grado di ignorare, quindi è sempre probabile che alcuni dati di una copia shadow debbano essere considerati in uno stato coerente con l'arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-108">Almost every system will have some applications—text editors, mail readers, word processors, and so forth—that are VSS unaware, so it is always likely that some of the data on a shadow copy will need to be thought of as being in a crash consistent state.</span></span>

    <span data-ttu-id="3b8ec-109">Questo tipo di dati non è in genere critico dal sistema o dal servizio, pertanto il backup non dovrebbe essere problematico o almeno non più problematico rispetto a un backup convenzionale.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-109">This sort of data is not typically system- or service-critical, so backing it up should not be problematic, or at least no more problematic than during a conventional backup.</span></span>

    <span data-ttu-id="3b8ec-110">Come per i preparativi per i backup convenzionali, se possibile, gli operatori di backup devono tentare di sospendere o terminare tali applicazioni prima di avviare un processo di backup VSS.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-110">As with preparations for conventional backups, if possible, backup operators should attempt to suspend or terminate such applications prior to starting a VSS backup job.</span></span>

-   <span data-ttu-id="3b8ec-111">**Sistema senza writer compatibili con VSS**</span><span class="sxs-lookup"><span data-stu-id="3b8ec-111">**System with no VSS-compatible writers**</span></span>

    <span data-ttu-id="3b8ec-112">Questa situazione può essere relativamente rara poiché la maggior parte dei sistemi di cui è possibile eseguire il backup da un'applicazione di backup VSS avrà una versione di Windows abilitata per VSS, che dovrebbe contenere writer.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-112">This situation may be relatively rare because most systems that can be backed up by a VSS backup application will have a VSS-enabled version of Windows, which should contain writers.</span></span>

    <span data-ttu-id="3b8ec-113">Tuttavia, in alcune circostanze potrebbe verificarsi questo problema, ad esempio se si esegue il backup di un sistema senza supporto VSS, ma il sistema usa un'appliance di rete abilitata per VSS per la relativa archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-113">However, there are certain circumstances where this problem could arise—for instance, if you are backing up a system without VSS support but the system uses a VSS-enabled networked appliance for its storage.</span></span>

    <span data-ttu-id="3b8ec-114">Sebbene il backup dello stato di un sistema da un'immagine coerente con l'arresto anomalo non sia ottimale, potrebbe essere sufficiente che un computer riavvii lo stato operativo.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-114">Although backing up a system's state from a crash-consistent image is not optimal, it may be sufficient for a computer to reboot to an operational status.</span></span> <span data-ttu-id="3b8ec-115">In molti casi, il computer ripristinerà le operazioni di I/O incomplete nei file System e funzionerà normalmente.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-115">In many cases, the computer will recover from any incomplete I/O operations to the file systems and will operate normally.</span></span>

-   <span data-ttu-id="3b8ec-116">**Un richiedente che sceglie di non usare i writer di sistema**</span><span class="sxs-lookup"><span data-stu-id="3b8ec-116">**A requester choosing not to work with the system writers**</span></span>

    <span data-ttu-id="3b8ec-117">Questa circostanza si verifica se un richiedente ha scelto di non aggiungere componenti del writer o disabilitare tutti i writer.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-117">This circumstance would occur if a requester chose to add no writer components, or disabling all writers.</span></span>

    <span data-ttu-id="3b8ec-118">L'esecuzione di backup in questo modo è in genere sconsigliata.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-118">Performing backups in this way is generally discouraged.</span></span> <span data-ttu-id="3b8ec-119">Sebbene il volume copiato dall'ombreggiatura per eseguire il backup potrebbe essere sufficiente per ripristinare un sistema in esecuzione, non è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-119">Although the shadow-copied volume to back up might be sufficient to restore a system to running, it is not desirable.</span></span> <span data-ttu-id="3b8ec-120">Infatti, dato che i writer in esecuzione nel sistema sono progettati con funzionalità per collaborare con VSS e copie shadow, il backup dei dati in questo modo potrebbe causare instabilità.</span><span class="sxs-lookup"><span data-stu-id="3b8ec-120">In fact, given that the writers running on the system are designed with functionality to cooperate with VSS and shadow copies, backing up their data in this way might result in instability.</span></span>

 

 



