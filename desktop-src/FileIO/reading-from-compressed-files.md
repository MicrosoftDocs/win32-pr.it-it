---
description: Un'applicazione può decomprimere un file compresso una parte alla volta usando le funzioni LZSeek e LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lettura da file compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315930"
---
# <a name="reading-from-compressed-files"></a><span data-ttu-id="1f79e-103">Lettura da file compressi</span><span class="sxs-lookup"><span data-stu-id="1f79e-103">Reading from Compressed Files</span></span>

<span data-ttu-id="1f79e-104">Oltre a decomprimere un file completo in un'unica operazione, un'applicazione può decomprimere un file compresso una parte alla volta usando le funzioni [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) e [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) .</span><span class="sxs-lookup"><span data-stu-id="1f79e-104">In addition to decompressing a complete file in a single operation, an application can decompress a compressed file a portion at a time by using the [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) and [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) functions.</span></span> <span data-ttu-id="1f79e-105">Queste funzioni sono particolarmente utili quando è necessario estrarre parti di file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1f79e-105">These functions are particularly useful when it is necessary to extract parts of large files.</span></span> <span data-ttu-id="1f79e-106">Un produttore di tipi di carattere, ad esempio, può disporre di file compressi contenenti metriche di tipo carattere oltre ai dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="1f79e-106">For example, a font manufacturer may have compressed files containing font metrics in addition to character data.</span></span> <span data-ttu-id="1f79e-107">Per usare le informazioni contenute in questi file, un'applicazione deve decomprimere il file. Tuttavia, la maggior parte delle applicazioni utilizzerà solo una parte del file in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="1f79e-107">To use the information in these files, an application would need to decompress the file; however, most applications would use only part of the file at any particular time.</span></span> <span data-ttu-id="1f79e-108">Per ottenere informazioni sulle metriche dei tipi di carattere, l'applicazione estrae i dati dall'intestazione.</span><span class="sxs-lookup"><span data-stu-id="1f79e-108">To get information about font metrics, the application would extract data from the header.</span></span> <span data-ttu-id="1f79e-109">Per ottenere informazioni dal testo, l'applicazione riposiziona il puntatore del file chiamando **LZSeek** ed estrae i dati di tipo carattere chiamando **LZRead**.</span><span class="sxs-lookup"><span data-stu-id="1f79e-109">To get information from the text, the application would reposition the file pointer by calling **LZSeek** and extract character data by calling **LZRead**.</span></span>

 

 



