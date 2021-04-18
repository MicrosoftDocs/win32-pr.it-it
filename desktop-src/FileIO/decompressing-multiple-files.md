---
description: Un'applicazione può decomprimere più file usando le funzioni LZOpenFile, LZCopy e LZClose.
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: Decompressione di più file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310033"
---
# <a name="decompressing-multiple-files"></a><span data-ttu-id="8e35b-103">Decompressione di più file</span><span class="sxs-lookup"><span data-stu-id="8e35b-103">Decompressing Multiple Files</span></span>

<span data-ttu-id="8e35b-104">Un'applicazione può decomprimere più file eseguendo le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e35b-104">An application can decompress multiple files by performing the following tasks:</span></span>

1.  <span data-ttu-id="8e35b-105">Aprire i file di origine chiamando la funzione [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="8e35b-105">Open the source files by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="8e35b-106">Aprire i file di destinazione chiamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="8e35b-106">Open the destination files by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="8e35b-107">Copiare i file di origine nei file di destinazione chiamando la funzione [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .</span><span class="sxs-lookup"><span data-stu-id="8e35b-107">Copy the source files to the destination files by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function.</span></span>
4.  <span data-ttu-id="8e35b-108">Chiudere i file chiamando la funzione [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="8e35b-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



