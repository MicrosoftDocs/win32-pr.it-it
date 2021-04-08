---
description: La funzione Filesize recupera le dimensioni di un file.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Determinazione delle dimensioni di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7205c47fe25b223dbcc12322516ff2b162fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967631"
---
# <a name="determining-the-size-of-a-file"></a><span data-ttu-id="13b5e-103">Determinazione delle dimensioni di un file</span><span class="sxs-lookup"><span data-stu-id="13b5e-103">Determining the Size of a File</span></span>

<span data-ttu-id="13b5e-104">La funzione [**Filesize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera le dimensioni di un file.</span><span class="sxs-lookup"><span data-stu-id="13b5e-104">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span>

<span data-ttu-id="13b5e-105">Poiché l'implementazione del file system NTFS dei file consente più flussi all'interno di un file, qualsiasi applicazione scritta che accede ai file deve tenere conto della possibilità che l'autore del file possa includere più flussi nel file.</span><span class="sxs-lookup"><span data-stu-id="13b5e-105">Because the NTFS file system implementation of files allows for multiple streams within a file, any application you write that accesses files must account for the possibility that the creator of the file can include multiple streams in the file.</span></span> <span data-ttu-id="13b5e-106">Se non vengono controllati più flussi in un file, l'applicazione può sottovalutare la dimensione totale del file, tra gli altri errori.</span><span class="sxs-lookup"><span data-stu-id="13b5e-106">If multiple streams are not checked for in a file, the application can underestimate the total size of the file, among other errors.</span></span>

 

 



