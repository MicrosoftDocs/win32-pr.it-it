---
description: Descrive uno schema di raccolta a dispersione per la lettura o la scrittura di blocchi di dati non contigui in un'unica operazione.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lettura o scrittura nei file utilizzando uno schema di Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315929"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a><span data-ttu-id="43ffe-103">Lettura o scrittura nei file utilizzando uno schema di Scatter-Gather</span><span class="sxs-lookup"><span data-stu-id="43ffe-103">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>

<span data-ttu-id="43ffe-104">Uno schema di raccolta a dispersione usa il sistema operativo per recapitare in una sola operazione più blocchi discreti di dati, ad esempio i record del database, da un file a buffer separati non contigui in memoria.</span><span class="sxs-lookup"><span data-stu-id="43ffe-104">A scatter-gather scheme uses the operating system to deliver in one operation multiple discrete chunks of data (such as database records) from a file to separate, noncontiguous buffers in memory.</span></span> <span data-ttu-id="43ffe-105">Uno schema a dispersione-raccolta scrive anche i dati da buffer non contigui in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="43ffe-105">A scatter-gather scheme also writes the data from noncontiguous buffers in one operation.</span></span>

<span data-ttu-id="43ffe-106">Un'applicazione può implementare uno schema di raccolta a dispersione usando le funzioni [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="43ffe-106">An application can implement a scatter-gather scheme by using the [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) functions.</span></span>

 

 



