---
title: Scrittura in un file
description: Scrittura in un file
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- AVIFileWriteData (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298525"
---
# <a name="writing-to-a-file"></a><span data-ttu-id="6543a-104">Scrittura in un file</span><span class="sxs-lookup"><span data-stu-id="6543a-104">Writing to a File</span></span>

<span data-ttu-id="6543a-105">È possibile scrivere informazioni aggiuntive in un file che è stato aperto con privilegi di scrittura tramite la funzione [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) .</span><span class="sxs-lookup"><span data-stu-id="6543a-105">You can write supplementary information to a file that has been opened with write privileges by using the [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) function.</span></span> <span data-ttu-id="6543a-106">Questa funzione copia le informazioni da un buffer fornito dall'applicazione e le inserisce in uno o più blocchi del file.</span><span class="sxs-lookup"><span data-stu-id="6543a-106">This function copies the information from an application-supplied buffer and places it in one or more chunks in the file.</span></span> <span data-ttu-id="6543a-107">Il blocco "INFO" è un tipo di blocco RIFF comune in cui la funzione archivia informazioni supplementari.</span><span class="sxs-lookup"><span data-stu-id="6543a-107">The "INFO" chunk is a common RIFF chunk type in which the function stores supplementary information.</span></span> <span data-ttu-id="6543a-108">Per una descrizione dei file RIFF e dei relativi blocchi di dati, vedere [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="6543a-108">For a description of RIFF files and their data chunks, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

 

 




