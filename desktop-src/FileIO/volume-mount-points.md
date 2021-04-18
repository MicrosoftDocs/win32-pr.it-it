---
description: Con le cartelle montate è possibile unificare diversi file System, ad esempio NTFS file system, un file system FAT a 16 bit e un file system ISO-9660 in un'unità CD-ROM in un file system logico in un singolo volume NTFS.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Cartelle montate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313871"
---
# <a name="mounted-folders"></a><span data-ttu-id="36a36-103">Cartelle montate</span><span class="sxs-lookup"><span data-stu-id="36a36-103">Mounted Folders</span></span>

<span data-ttu-id="36a36-104">Il file system NTFS supporta le cartelle montate.</span><span class="sxs-lookup"><span data-stu-id="36a36-104">The NTFS file system supports mounted folders.</span></span> <span data-ttu-id="36a36-105">Una *cartella montata* è un'associazione tra un volume e una directory in un altro volume.</span><span class="sxs-lookup"><span data-stu-id="36a36-105">A *mounted folder* is an association between a volume and a directory on another volume.</span></span> <span data-ttu-id="36a36-106">Quando viene creata una cartella montata, gli utenti e le applicazioni possono accedere al volume di destinazione usando il percorso della cartella montata o la lettera di unità del volume.</span><span class="sxs-lookup"><span data-stu-id="36a36-106">When a mounted folder is created, users and applications can access the target volume either by using the path to the mounted folder or by using the volume's drive letter.</span></span> <span data-ttu-id="36a36-107">Ad esempio, un utente può creare una cartella montata per associare l'unità D: con la \\ cartella c: mnt \\ DDrive nell'unità C. Dopo aver creato la cartella montata, l'utente può usare il percorso "C: \\ mnt \\ DDrive" per accedere all'unità D: come se fosse una cartella nell'unità C:.</span><span class="sxs-lookup"><span data-stu-id="36a36-107">For example, a user can create a mounted folder to associate drive D: with the C:\\Mnt\\DDrive folder on drive C. After creating the mounted folder, the user can use the "C:\\Mnt\\DDrive" path to access drive D: as if it were a folder on drive C:.</span></span>

<span data-ttu-id="36a36-108">Con le cartelle montate è possibile unificare diversi file System, ad esempio NTFS file system, un file system FAT a 16 bit e un file system ISO-9660 in un'unità CD-ROM in un file system logico in un singolo volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="36a36-108">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span> <span data-ttu-id="36a36-109">Né gli utenti né le applicazioni necessitano di informazioni sul volume di destinazione in cui si trova un file specifico.</span><span class="sxs-lookup"><span data-stu-id="36a36-109">Neither users nor applications need information about the target volume on which a specific file is located.</span></span> <span data-ttu-id="36a36-110">Tutte le informazioni necessarie per individuare un file specificato sono un percorso completo utilizzando una cartella montata nel volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="36a36-110">All the information they need to locate a specified file is a complete path using a mounted folder on the NTFS volume.</span></span> <span data-ttu-id="36a36-111">I volumi possono essere ridisposti, sostituiti o suddivisi in molti volumi senza che utenti o applicazioni debbano modificare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="36a36-111">Volumes can be rearranged, substituted, or subdivided into many volumes without users or applications needing to change settings.</span></span>

<span data-ttu-id="36a36-112">Per informazioni sulle cartelle montate, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="36a36-112">For information on mounted folders, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="36a36-113">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="36a36-113">In this section</span></span>



| <span data-ttu-id="36a36-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="36a36-114">Topic</span></span>                                                                                                                         | <span data-ttu-id="36a36-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36a36-115">Description</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36a36-116">Creazione di cartelle montate</span><span class="sxs-lookup"><span data-stu-id="36a36-116">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)<br/>                                                  | <span data-ttu-id="36a36-117">La creazione di una cartella montata è un processo in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="36a36-117">Creating a mounted folder is a two-step process.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="36a36-118">Enumerazione di cartelle montate</span><span class="sxs-lookup"><span data-stu-id="36a36-118">Enumerating Mounted Folders</span></span>](enumerating-volume-mount-points.md)<br/>                                                 | <span data-ttu-id="36a36-119">Funzioni da utilizzare per enumerare le cartelle montate in un volume.</span><span class="sxs-lookup"><span data-stu-id="36a36-119">Functions to use to enumerate mounted folders on a volume.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="36a36-120">Determinare se una directory è una cartella montata</span><span class="sxs-lookup"><span data-stu-id="36a36-120">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | <span data-ttu-id="36a36-121">Come determinare se una directory specificata è una cartella montata.</span><span class="sxs-lookup"><span data-stu-id="36a36-121">How to determine whether a specified directory is a mounted folder.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="36a36-122">Assegnazione di una lettera di unità a un volume</span><span class="sxs-lookup"><span data-stu-id="36a36-122">Assigning a Drive Letter to a Volume</span></span>](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | <span data-ttu-id="36a36-123">È possibile assegnare una lettera di unità (ad esempio, X: \) a un volume locale usando la funzione [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , a condizione che non sia già stato assegnato un volume a tale lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="36a36-123">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span><br/> |
| [<span data-ttu-id="36a36-124">Funzioni cartella montata</span><span class="sxs-lookup"><span data-stu-id="36a36-124">Mounted Folder Functions</span></span>](volume-mount-point-functions.md)<br/>                                                       | <span data-ttu-id="36a36-125">Funzioni utilizzate per gestire le cartelle montate.</span><span class="sxs-lookup"><span data-stu-id="36a36-125">Functions used to manage mounted folders.</span></span><br/>                                                                                                                                                                        |



 

<span data-ttu-id="36a36-126">Per esempi, vedere [esempi di cartelle montate](volume-mount-point-examples.md).</span><span class="sxs-lookup"><span data-stu-id="36a36-126">For examples, see [Mounted Folder Examples](volume-mount-point-examples.md).</span></span>

 

 




