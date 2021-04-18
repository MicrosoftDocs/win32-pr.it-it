---
description: La creazione di una cartella montata è un processo in due passaggi.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Creazione di cartelle montate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319066"
---
# <a name="creating-mounted-folders"></a><span data-ttu-id="63eaa-103">Creazione di cartelle montate</span><span class="sxs-lookup"><span data-stu-id="63eaa-103">Creating Mounted Folders</span></span>

<span data-ttu-id="63eaa-104">La creazione di una cartella montata è un processo in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="63eaa-104">Creating a mounted folder is a two-step process.</span></span> <span data-ttu-id="63eaa-105">In primo luogo, chiamare [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) con il punto di montaggio (lettera di unità, percorso GUID volume o cartella montata) del volume da assegnare alla cartella montata.</span><span class="sxs-lookup"><span data-stu-id="63eaa-105">First, call [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) with the mount point (drive letter, volume GUID path, or mounted folder) of the volume to be assigned to the mounted folder.</span></span> <span data-ttu-id="63eaa-106">Usare quindi la funzione [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) per associare il percorso GUID del volume restituito alla directory desiderata in un altro volume.</span><span class="sxs-lookup"><span data-stu-id="63eaa-106">Then use the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function to associate the returned volume GUID path with the desired directory on another volume.</span></span> <span data-ttu-id="63eaa-107">Per un esempio di codice, vedere [creazione di una cartella montata](mounting-a-volume-at-a-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="63eaa-107">For example code, see [Creating a Mounted Folder](mounting-a-volume-at-a-mount-point.md).</span></span>

<span data-ttu-id="63eaa-108">L'applicazione può designare qualsiasi directory vuota in un volume diverso dalla radice come cartella montata.</span><span class="sxs-lookup"><span data-stu-id="63eaa-108">Your application can designate any empty directory on a volume other than the root as a mounted folder.</span></span> <span data-ttu-id="63eaa-109">Quando si chiama la funzione [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , tale directory diventa la cartella montata.</span><span class="sxs-lookup"><span data-stu-id="63eaa-109">When you call the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, that directory becomes the mounted folder.</span></span> <span data-ttu-id="63eaa-110">È possibile assegnare lo stesso volume a più cartelle montate.</span><span class="sxs-lookup"><span data-stu-id="63eaa-110">You can assign the same volume to multiple mounted folders.</span></span>

<span data-ttu-id="63eaa-111">Una volta stabilita, la cartella montata viene gestita automaticamente tramite il riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="63eaa-111">After the mounted folder has been established, it is maintained through computer restarts automatically.</span></span>

<span data-ttu-id="63eaa-112">Se si verifica un errore in un volume, non sarà più possibile accedere ai volumi assegnati alle cartelle montate in tale volume tramite le cartelle montate.</span><span class="sxs-lookup"><span data-stu-id="63eaa-112">If a volume fails, any volumes that have been assigned to mounted folders on that volume can no longer be accessed through those mounted folders.</span></span> <span data-ttu-id="63eaa-113">Si supponga, ad esempio, di avere due volumi, C: e D: e che D: sia associato alla cartella montata C: \\ mountd \\ .</span><span class="sxs-lookup"><span data-stu-id="63eaa-113">For example, suppose you have two volumes, C: and D:, and that D: is associated with the mounted folder C:\\MountD\\.</span></span> <span data-ttu-id="63eaa-114">Se il volume C: ha esito negativo, non è più possibile accedere al volume D: tramite il percorso C: \\ mountd \\ .</span><span class="sxs-lookup"><span data-stu-id="63eaa-114">If volume C: fails, volume D: can no longer be accessed through the path C:\\MountD\\.</span></span>

<span data-ttu-id="63eaa-115">Solo i volumi di file system NTFS possono avere cartelle montate, ma i volumi di destinazione per le cartelle montate possono essere volumi non NTFS.</span><span class="sxs-lookup"><span data-stu-id="63eaa-115">Only NTFS file system volumes can have mounted folders, but the target volumes for the mounted folders can be non-NTFS volumes.</span></span>

<span data-ttu-id="63eaa-116">Le cartelle montate vengono implementate usando i reparse point e sono soggette alle restrizioni.</span><span class="sxs-lookup"><span data-stu-id="63eaa-116">Mounted folders are implemented by using reparse points and are subject to their restrictions.</span></span> <span data-ttu-id="63eaa-117">Per ulteriori informazioni, vedere [reparse point](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="63eaa-117">For more information, see [Reparse Points](reparse-points.md).</span></span> <span data-ttu-id="63eaa-118">Non è necessario modificare i reparse point per usare le cartelle montate; funzioni come [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) gestiscono tutti i dettagli dei reparse point.</span><span class="sxs-lookup"><span data-stu-id="63eaa-118">It is not necessary to manipulate reparse points to use mounted folders; functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) handle all the reparse point details for you.</span></span>

<span data-ttu-id="63eaa-119">Poiché le cartelle montate sono directory, è possibile rinominarle, rimuoverle, spostarle e modificarle in altro modo, come per le altre directory.</span><span class="sxs-lookup"><span data-stu-id="63eaa-119">Because mounted folders are directories, you can rename, remove, move, and otherwise manipulate them, as you would other directories.</span></span>

<span data-ttu-id="63eaa-120">Nota: la documentazione di TechNet usa il termine *unità montate* per fare riferimento alle *cartelle montate*.</span><span class="sxs-lookup"><span data-stu-id="63eaa-120">(Note: The TechNet documentation uses the term *mounted drives* to refer to *mounted folders*.)</span></span>

 

 



