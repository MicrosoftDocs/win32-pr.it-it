---
description: Per ottenere la dimensione compressa di un file, usare la funzione GetCompressedFileSize.
ms.assetid: c6bfd221-f125-48b4-b38b-822a23639c40
title: Recupero delle dimensioni di un file compresso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4954a53184e55341838fef7cd70f01639f13bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527048"
---
# <a name="obtaining-the-size-of-a-compressed-file"></a><span data-ttu-id="4871d-103">Recupero delle dimensioni di un file compresso</span><span class="sxs-lookup"><span data-stu-id="4871d-103">Obtaining the Size of a Compressed File</span></span>

<span data-ttu-id="4871d-104">Utilizzare la funzione [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) per ottenere la dimensione compressa di un file.</span><span class="sxs-lookup"><span data-stu-id="4871d-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the compressed size of a file.</span></span> <span data-ttu-id="4871d-105">Se il file è compresso, le dimensioni compresse saranno inferiori alle dimensioni non compresse.</span><span class="sxs-lookup"><span data-stu-id="4871d-105">If the file is compressed, its compressed size will be less than its uncompressed size.</span></span> <span data-ttu-id="4871d-106">Usare la funzione [**Filesize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) per determinare la dimensione non compressa di un file.</span><span class="sxs-lookup"><span data-stu-id="4871d-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the uncompressed size of a file.</span></span>

 

 



