---
title: Collegamenti SIS e reparse point
description: SIS è un driver di filtro NTFS che sostituisce i file duplicati con i collegamenti copy-on-Write (detti collegamenti SIS) che puntano a un singolo file di backup, riducendo il sovraccarico del disco e della cache di tali file.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Backup dei reparse point
- Backup dell'archivio a istanza singola (SIS), collegamenti SIS
- Backup dell'archivio a istanza singola (SIS), reparse point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4987e7c64a83e7d0b02ed91899a182616be7943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118211"
---
# <a name="sis-links-and-reparse-points"></a><span data-ttu-id="18177-106">Collegamenti SIS e reparse point</span><span class="sxs-lookup"><span data-stu-id="18177-106">SIS Links and Reparse Points</span></span>

<span data-ttu-id="18177-107">SIS è un driver di filtro NTFS che sostituisce i file duplicati con i collegamenti copy-on-Write (detti collegamenti SIS) che puntano a un singolo file di backup, riducendo il sovraccarico del disco e della cache di tali file.</span><span class="sxs-lookup"><span data-stu-id="18177-107">SIS is an NTFS filter driver that replaces duplicate files with copy-on-write links (referred to as SIS links) that point to a single backing file, reducing the disk and cache overhead of those files.</span></span> <span data-ttu-id="18177-108">Questo file di backup è contenuto in un [archivio comune](the-sis-common-store-and-common-store-files.md).</span><span class="sxs-lookup"><span data-stu-id="18177-108">This backing file is contained in a [common store](the-sis-common-store-and-common-store-files.md).</span></span> <span data-ttu-id="18177-109">L'implementazione dell'architettura SIS usa i [reparse point](/windows/desktop/FileIO/reparse-points) contenenti informazioni sui collegamenti SIS.</span><span class="sxs-lookup"><span data-stu-id="18177-109">The implementation of the SIS architecture makes use of [reparse points](/windows/desktop/FileIO/reparse-points) that contain information about the SIS links.</span></span>

<span data-ttu-id="18177-110">I collegamenti SIS vengono implementati come file sparse, in genere con la maggior parte degli intervalli del file non allocato e un reparse point.</span><span class="sxs-lookup"><span data-stu-id="18177-110">SIS links are implemented as sparse files, usually with most ranges of the file unallocated, and a reparse point.</span></span> <span data-ttu-id="18177-111">La struttura e il contenuto di un punto di analisi è opaco per le applicazioni di backup e ripristino. Tuttavia, le applicazioni inviano e recuperano i dati all'interno di tali reparse point da e verso le funzioni API SIS che elaborano le informazioni in esse contenute.</span><span class="sxs-lookup"><span data-stu-id="18177-111">The structure and contents of a reparse point is opaque to your backup and restore applications; however, your applications send and retrieve the data within these reparse points to and from SIS API functions that process the information in them.</span></span> <span data-ttu-id="18177-112">Le informazioni in un reparse point si riferiscono a un singolo file di backup che contiene i dati del file effettivi.</span><span class="sxs-lookup"><span data-stu-id="18177-112">The information in a reparse point refers to a single backing file that contains the actual file data.</span></span> <span data-ttu-id="18177-113">Questo file di backup è denominato [file di archivio comune](the-sis-common-store-and-common-store-files.md)ed è presente nell'archivio comune.</span><span class="sxs-lookup"><span data-stu-id="18177-113">This backing file is called a [common-store file](the-sis-common-store-and-common-store-files.md), and it exists in the common store.</span></span>

<span data-ttu-id="18177-114">Quando si ripristina un collegamento SIS, l'applicazione di ripristino deve eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="18177-114">When restoring a SIS link, your restore application should perform the following steps:</span></span>

1.  <span data-ttu-id="18177-115">Determinare il file o i file dell'archivio comune a cui punta il collegamento SIS.</span><span class="sxs-lookup"><span data-stu-id="18177-115">Determine the common-store file or files to which the SIS link points.</span></span>
2.  <span data-ttu-id="18177-116">Se il file o i file non sono presenti nell'archivio comune, ripristinare il file o i file insieme al collegamento SIS.</span><span class="sxs-lookup"><span data-stu-id="18177-116">If the file or files do not exist in the common store, restore the file or files along with the SIS link.</span></span>
3.  <span data-ttu-id="18177-117">Se il collegamento SIS punta a un file o a un file di archivio comune esistente sul disco, ripristinare solo il collegamento SIS.</span><span class="sxs-lookup"><span data-stu-id="18177-117">If the SIS link points to a common-store file or files that exist on the disk, then restore only the SIS link.</span></span> <span data-ttu-id="18177-118">Si ricordi che i dati nei file di archivio comuni non cambiano mai. Pertanto, se un file di archivio comune si trova ancora sul disco al momento del ripristino, avrà lo stesso contenuto del momento in cui è stato eseguito il backup e non è necessario sovrascriverlo.</span><span class="sxs-lookup"><span data-stu-id="18177-118">Recall that the data in common-store files never changes, so if a given common-store file is still on the disk at restore time, it has the same contents as when it was backed up and there is no need to overwrite it.</span></span>

<span data-ttu-id="18177-119">L'unico overhead aggiuntivo necessario per i backup assistiti da SIS è che l'applicazione di backup deve eseguire il backup del collegamento SIS e dei dati associati ai file di supporto.</span><span class="sxs-lookup"><span data-stu-id="18177-119">The only additional overhead required for SIS-assisted backups is that your backup application must back up the SIS link and the data associated with the backing files.</span></span> <span data-ttu-id="18177-120">Tutte le operazioni di backup e ripristino SIS sono locali in un volume specifico.</span><span class="sxs-lookup"><span data-stu-id="18177-120">All SIS backup and restore operations are local to a specific volume.</span></span>

 

 