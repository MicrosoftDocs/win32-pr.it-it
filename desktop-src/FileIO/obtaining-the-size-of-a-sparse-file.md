---
description: Ottenere la dimensione allocata o la dimensione totale per un file usando la funzione GetCompressedFileSize o Filesize.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Recupero delle dimensioni di un file sparse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879698"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a><span data-ttu-id="1c4a8-103">Recupero delle dimensioni di un file sparse</span><span class="sxs-lookup"><span data-stu-id="1c4a8-103">Obtaining the Size of a Sparse File</span></span>

<span data-ttu-id="1c4a8-104">Utilizzare la funzione [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) per ottenere la dimensione effettiva allocata sul disco per un file sparse.</span><span class="sxs-lookup"><span data-stu-id="1c4a8-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the actual size allocated on disk for a sparse file.</span></span> <span data-ttu-id="1c4a8-105">Il totale non include le dimensioni delle aree deallocate perché sono state riempite con zeri.</span><span class="sxs-lookup"><span data-stu-id="1c4a8-105">This total does not include the size of the regions which were deallocated because they were filled with zeros.</span></span> <span data-ttu-id="1c4a8-106">Usare la funzione [**Filesize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) per determinare la dimensione totale di un file, incluse le dimensioni delle aree sparse deallocate.</span><span class="sxs-lookup"><span data-stu-id="1c4a8-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the total size of a file, including the size of the sparse regions that were deallocated.</span></span>

 

 



