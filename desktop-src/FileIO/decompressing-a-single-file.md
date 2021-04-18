---
description: Un'applicazione può decomprimere un singolo file compresso usando le funzioni LZOpenFile, LZCopy e LZClose.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Decompressione di un singolo file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8da6ee4ee80e42d6ff70c3d9c50efdc572f97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310036"
---
# <a name="decompressing-a-single-file"></a><span data-ttu-id="a0c34-103">Decompressione di un singolo file</span><span class="sxs-lookup"><span data-stu-id="a0c34-103">Decompressing a Single File</span></span>

<span data-ttu-id="a0c34-104">Un'applicazione può decomprimere un singolo file compresso eseguendo le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0c34-104">An application can decompress a single compressed file by performing the following tasks:</span></span>

1.  <span data-ttu-id="a0c34-105">Aprire il file di origine chiamando la funzione [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="a0c34-105">Open the source file by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="a0c34-106">Aprire il file di destinazione chiamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="a0c34-106">Open the destination file by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="a0c34-107">Copiare il file di origine nel file di destinazione chiamando la funzione [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) e passando gli handle restituiti da [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="a0c34-107">Copy the source file to the destination file by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function and passing the handles returned by [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
4.  <span data-ttu-id="a0c34-108">Chiudere i file chiamando la funzione [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="a0c34-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



