---
description: Descrive il modo in cui i reparse point abilitano il comportamento file system che si riparte dal comportamento che la maggior parte degli sviluppatori Windows prevede
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Reparse point e operazioni su file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232978"
---
# <a name="reparse-points-and-file-operations"></a><span data-ttu-id="7a309-103">Reparse point e operazioni su file</span><span class="sxs-lookup"><span data-stu-id="7a309-103">Reparse Points and File Operations</span></span>

<span data-ttu-id="7a309-104">I *reparse point* abilitano file System comportamento che si riferisce dal comportamento che la maggior parte degli sviluppatori Windows può essere abituato, pertanto tenere presente questi comportamenti quando si scrivono applicazioni che modificano i file è fondamentale per applicazioni affidabili e affidabili progettate per accedere ai file System che supportano i reparse point.</span><span class="sxs-lookup"><span data-stu-id="7a309-104">*Reparse points* enable file system behavior that departs from the behavior most Windows developers may be accustomed to, therefore being aware of these behaviors when writing applications that manipulate files is vital to robust and reliable applications intended to access file systems that support reparse points.</span></span> <span data-ttu-id="7a309-105">L'ambito di queste considerazioni dipende dall'implementazione specifica e dal comportamento del filtro file system associato di un determinato punto di analisi, che può essere definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7a309-105">The extent of these considerations will depend on the specific implementation and associated file system filter behavior of a particular reparse point, which can be user-defined.</span></span> <span data-ttu-id="7a309-106">Per ulteriori informazioni, vedere [reparse point](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="7a309-106">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="7a309-107">Si considerino gli esempi seguenti relativi alle implementazioni del reparse point NTFS, che includono le cartelle montate, i file collegati e il server di archiviazione remota Microsoft:</span><span class="sxs-lookup"><span data-stu-id="7a309-107">Consider the following examples regarding NTFS reparse point implementations, which include mounted folders, linked files, and the Microsoft Remote Storage Server:</span></span>

-   <span data-ttu-id="7a309-108">Quando si esegue il backup di file con i reparse point, le applicazioni di backup che usano [flussi di file](file-streams.md) devono specificare i **\_ \_ dati di analisi del backup** nella struttura dell' [**\_ \_ ID del flusso Win32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) .</span><span class="sxs-lookup"><span data-stu-id="7a309-108">Backup applications that use [file streams](file-streams.md) should specify **BACKUP\_REPARSE\_DATA** in the [**WIN32\_STREAM\_ID**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) structure when backing up files with reparse points.</span></span>
-   <span data-ttu-id="7a309-109">Per le applicazioni che utilizzano la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) è necessario specificare il flag di **file \_ \_ Open \_ reparse \_ Point** quando si apre il file se si tratta di un reparse point.</span><span class="sxs-lookup"><span data-stu-id="7a309-109">Applications that use the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function should specify the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag when opening the file if it is a reparse point.</span></span> <span data-ttu-id="7a309-110">Per ulteriori informazioni, vedere [creazione e apertura di file](creating-and-opening-files.md).</span><span class="sxs-lookup"><span data-stu-id="7a309-110">For more information, see [Creating and Opening Files](creating-and-opening-files.md).</span></span>
-   <span data-ttu-id="7a309-111">Il processo di [deframmentazione dei file](defragmenting-files.md) richiede una gestione speciale per i reparse point.</span><span class="sxs-lookup"><span data-stu-id="7a309-111">The process of [defragmenting files](defragmenting-files.md) requires special handling for reparse points.</span></span>
-   <span data-ttu-id="7a309-112">Le applicazioni di rilevamento del virus devono cercare i reparse point che indicano i file collegati.</span><span class="sxs-lookup"><span data-stu-id="7a309-112">Virus detection applications should search for reparse points that indicate linked files.</span></span>
-   <span data-ttu-id="7a309-113">La maggior parte delle applicazioni deve eseguire azioni speciali per i file spostati nell'archiviazione a lungo termine, se solo per notificare all'utente che il recupero del file potrebbe richiedere tempo.</span><span class="sxs-lookup"><span data-stu-id="7a309-113">Most applications should take special actions for files that have been moved to long-term storage, if only to notify the user that it may take a while to retrieve the file.</span></span>
-   <span data-ttu-id="7a309-114">La funzione [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) consente di aprire il file o il reparse point, a seconda dell'uso del flag di **file \_ \_ Open \_ reparse \_ Point** .</span><span class="sxs-lookup"><span data-stu-id="7a309-114">The [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) function will either open the file or the reparse point, depending on the use of the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span>
-   <span data-ttu-id="7a309-115">I collegamenti simbolici, come reparse point, presentano alcune [considerazioni di programmazione](symbolic-link-programming-considerations.md) specifiche.</span><span class="sxs-lookup"><span data-stu-id="7a309-115">Symbolic links, as reparse points, have certain [programming considerations](symbolic-link-programming-considerations.md) specific to them.</span></span>
-   <span data-ttu-id="7a309-116">Le attività di gestione del volume per la lettura dei record del journal delle modifiche USN (Update Sequence Number) richiedono una gestione speciale per i reparse point quando si usa il [**\_ record USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e si leggono le strutture [**\_ \_ \_ dei dati journal USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) .</span><span class="sxs-lookup"><span data-stu-id="7a309-116">Volume management activities for reading update sequence number (USN) change journal records require special handling for reparse points when using the [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**READ\_USN\_JOURNAL\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a309-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a309-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a309-118">Determinare se una directory è una cartella montata</span><span class="sxs-lookup"><span data-stu-id="7a309-118">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[<span data-ttu-id="7a309-119">Creazione di cartelle montate</span><span class="sxs-lookup"><span data-stu-id="7a309-119">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[<span data-ttu-id="7a309-120">Effetti dei collegamenti simbolici sulle funzioni di file System</span><span class="sxs-lookup"><span data-stu-id="7a309-120">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
