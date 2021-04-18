---
description: Per ottenere un elenco completo dei volumi in un computer o per modificare ogni volume a sua volta, è possibile enumerare i volumi.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Enumerazione dei volumi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313884"
---
# <a name="enumerating-volumes"></a><span data-ttu-id="d1be0-103">Enumerazione dei volumi</span><span class="sxs-lookup"><span data-stu-id="d1be0-103">Enumerating Volumes</span></span>

<span data-ttu-id="d1be0-104">Per ottenere un elenco completo dei volumi in un computer o per modificare ogni volume a sua volta, è possibile enumerare i volumi.</span><span class="sxs-lookup"><span data-stu-id="d1be0-104">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span> <span data-ttu-id="d1be0-105">All'interno di un volume, è possibile [analizzare le cartelle montate](enumerating-volume-mount-points.md) o altri oggetti nel volume.</span><span class="sxs-lookup"><span data-stu-id="d1be0-105">Within a volume, you can [scan for mounted folders](enumerating-volume-mount-points.md) or other objects on the volume.</span></span>

<span data-ttu-id="d1be0-106">Tre funzioni consentono a un'applicazione di enumerare i volumi in un computer:</span><span class="sxs-lookup"><span data-stu-id="d1be0-106">Three functions allow an application to enumerate volumes on a computer:</span></span>

-   [<span data-ttu-id="d1be0-107">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="d1be0-107">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [<span data-ttu-id="d1be0-108">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="d1be0-108">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [<span data-ttu-id="d1be0-109">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="d1be0-109">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

<span data-ttu-id="d1be0-110">Queste tre funzioni funzionano in modo molto simile alle funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="d1be0-110">These three functions operate in a manner very similar to the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span>

<span data-ttu-id="d1be0-111">Inizia una ricerca di volumi con [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="d1be0-111">Begin a search for volumes with [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span> <span data-ttu-id="d1be0-112">Se la ricerca ha esito positivo, elaborare i risultati in base alla progettazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1be0-112">If the search is successful, process the results according to the design of your application.</span></span> <span data-ttu-id="d1be0-113">Usare quindi [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in un ciclo per individuare ed elaborare ogni volume successivo.</span><span class="sxs-lookup"><span data-stu-id="d1be0-113">Then use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in a loop to locate and process each subsequent volume.</span></span> <span data-ttu-id="d1be0-114">Quando viene esaurita la quantità di volumi, chiudere la ricerca con [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span><span class="sxs-lookup"><span data-stu-id="d1be0-114">When the supply of volumes is exhausted, close the search with [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span></span>

<span data-ttu-id="d1be0-115">Non è consigliabile presupporre alcuna correlazione tra l'ordine dei volumi restituiti da queste funzioni e l'ordine dei volumi restituiti da altre funzioni o strumenti.</span><span class="sxs-lookup"><span data-stu-id="d1be0-115">You should not assume any correlation between the order of the volumes that are returned by these functions and the order of the volumes that are returned by other functions or tools.</span></span> <span data-ttu-id="d1be0-116">In particolare, non presupporre alcuna correlazione tra l'ordine del volume e le lettere di unità assegnate dal BIOS (se presente) o dall'amministratore del disco.</span><span class="sxs-lookup"><span data-stu-id="d1be0-116">In particular, do not assume any correlation between volume order and drive letters as assigned by the BIOS (if any) or the Disk Administrator.</span></span>

<span data-ttu-id="d1be0-117">Vedere [esempi di cartelle montate](volume-mount-point-examples.md) per un esempio su come enumerare i volumi in un computer.</span><span class="sxs-lookup"><span data-stu-id="d1be0-117">See [Mounted Folder Examples](volume-mount-point-examples.md) for an example of how to enumerate the volumes on a computer.</span></span>

 

 



