---
description: I volumi vengono implementati da un driver di dispositivo denominato responsabile del volume.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Informazioni sulla gestione dei volumi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317814"
---
# <a name="about-volume-management"></a><span data-ttu-id="8499d-103">Informazioni sulla gestione dei volumi</span><span class="sxs-lookup"><span data-stu-id="8499d-103">About Volume Management</span></span>

<span data-ttu-id="8499d-104">I volumi vengono implementati da un driver di dispositivo denominato responsabile del volume.</span><span class="sxs-lookup"><span data-stu-id="8499d-104">Volumes are implemented by a device driver called a volume manager.</span></span> <span data-ttu-id="8499d-105">Gli esempi includono FtDisk Manager, gestione dischi logici (LDM) e VERITAS Logical Volume Manager (LVM).</span><span class="sxs-lookup"><span data-stu-id="8499d-105">Examples include the FtDisk Manager, the Logical Disk Manager (LDM), and the VERITAS Logical Volume Manager (LVM).</span></span> <span data-ttu-id="8499d-106">I responsabili del volume forniscono un livello di astrazione fisica, protezione dei dati (tramite una forma di RAID) e prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8499d-106">Volume managers provide a layer of physical abstraction, data protection (using some form of RAID), and performance.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8499d-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8499d-107">In this section</span></span>



| <span data-ttu-id="8499d-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="8499d-108">Topic</span></span>                                                                       | <span data-ttu-id="8499d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8499d-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8499d-110">Riconoscimento del file System</span><span class="sxs-lookup"><span data-stu-id="8499d-110">File System Recognition</span></span>](file-system-recognition.md)<br/>           | <span data-ttu-id="8499d-111">L'obiettivo del riconoscimento file system consiste nel consentire al sistema operativo Windows di disporre di un'opzione aggiuntiva per un file system valido ma non riconosciuto diverso da "RAW".</span><span class="sxs-lookup"><span data-stu-id="8499d-111">The goal of file system recognition is to allow the Windows operating system to have an additional option for a valid but unrecognized file system other than "RAW".</span></span><br/>                                                                                                         |
| [<span data-ttu-id="8499d-112">Denominazione di un volume</span><span class="sxs-lookup"><span data-stu-id="8499d-112">Naming a Volume</span></span>](naming-a-volume.md)<br/>                           | <span data-ttu-id="8499d-113">Un'etichetta è un nome descrittivo assegnato a un volume, in genere da un utente finale, per renderlo più semplice da riconoscere.</span><span class="sxs-lookup"><span data-stu-id="8499d-113">A label is a user-friendly name that is assigned to a volume, usually by an end user, to make it easier to recognize.</span></span> <span data-ttu-id="8499d-114">Un volume può avere un'etichetta, una lettera di unità, entrambi o nessuno.</span><span class="sxs-lookup"><span data-stu-id="8499d-114">A volume can have a label, a drive letter, both, or neither.</span></span> <span data-ttu-id="8499d-115">Per impostare l'etichetta per un volume, utilizzare la funzione [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .</span><span class="sxs-lookup"><span data-stu-id="8499d-115">To set the label for a volume, use the [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) function.</span></span><br/> |
| [<span data-ttu-id="8499d-116">Enumerazione dei volumi</span><span class="sxs-lookup"><span data-stu-id="8499d-116">Enumerating Volumes</span></span>](enumerating-volumes.md)<br/>                   | <span data-ttu-id="8499d-117">Per ottenere un elenco completo dei volumi in un computer o per modificare ogni volume a sua volta, è possibile enumerare i volumi.</span><span class="sxs-lookup"><span data-stu-id="8499d-117">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="8499d-118">Recupero delle informazioni sul volume</span><span class="sxs-lookup"><span data-stu-id="8499d-118">Obtaining Volume Information</span></span>](obtaining-volume-information.md)<br/> | <span data-ttu-id="8499d-119">Prima di accedere a file e directory in un volume specifico, è necessario determinare le funzionalità del file system usando la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) .</span><span class="sxs-lookup"><span data-stu-id="8499d-119">Before you access files and directories on a given volume, you should determine the capabilities of the file system by using the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function.</span></span><br/>                                                                              |
| [<span data-ttu-id="8499d-120">Journal delle modifiche</span><span class="sxs-lookup"><span data-stu-id="8499d-120">Change Journals</span></span>](change-journals.md)<br/>                           | <span data-ttu-id="8499d-121">Quando viene apportata una modifica a un file o a una directory in un volume, il Journal delle modifiche USN per tale volume viene aggiornato con una descrizione della modifica e il nome del file o della directory.</span><span class="sxs-lookup"><span data-stu-id="8499d-121">When any change is made to a file or directory in a volume, the USN change journal for that volume is updated with a description of the change and the name of the file or directory.</span></span><br/>                                                                                        |
| [<span data-ttu-id="8499d-122">Cartelle montate</span><span class="sxs-lookup"><span data-stu-id="8499d-122">Mounted Folders</span></span>](volume-mount-points.md)<br/>                       | <span data-ttu-id="8499d-123">Con le cartelle montate è possibile unificare diversi file System, ad esempio NTFS file system, un file system FAT a 16 bit e un file system ISO-9660 in un'unità CD-ROM in un file system logico in un singolo volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="8499d-123">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span><br/>                                                      |
| [<span data-ttu-id="8499d-124">Tabella file master</span><span class="sxs-lookup"><span data-stu-id="8499d-124">Master File Table</span></span>](master-file-table.md)<br/>                       | <span data-ttu-id="8499d-125">Tutte le informazioni su un file, incluse le dimensioni, gli indicatori di data e ora, le autorizzazioni e il contenuto dei dati, vengono archiviati nelle voci della tabella file master (MFT) o nello spazio esterno alla MFT descritta dalle voci MFT.</span><span class="sxs-lookup"><span data-stu-id="8499d-125">All information about a file, including its size, time and date stamps, permissions, and data content, is stored either in master file table (MFT) entries, or in space outside the MFT that is described by MFT entries.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="8499d-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8499d-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8499d-127">[Riferimento tecnico per dischi e volumi di base](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8499d-127">[Basic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="8499d-128">[Guida di riferimento tecnico ai dischi e ai volumi dinamici](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8499d-128">[Dynamic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="8499d-129">Riferimento per gestione volume</span><span class="sxs-lookup"><span data-stu-id="8499d-129">Volume Management Reference</span></span>](volume-management-reference.md)
</dt> </dl>

 

