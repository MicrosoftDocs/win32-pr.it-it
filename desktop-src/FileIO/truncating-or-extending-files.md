---
description: Un'applicazione può troncare o estendere un file chiamando SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Troncamento o estensione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316763"
---
# <a name="truncating-or-extending-files"></a><span data-ttu-id="e7829-103">Troncamento o estensione di file</span><span class="sxs-lookup"><span data-stu-id="e7829-103">Truncating or Extending Files</span></span>

<span data-ttu-id="e7829-104">Un'applicazione può troncare o estendere un file chiamando [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span><span class="sxs-lookup"><span data-stu-id="e7829-104">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span> <span data-ttu-id="e7829-105">Questa funzione imposta il marcatore di fine file sulla posizione corrente del puntatore del file.</span><span class="sxs-lookup"><span data-stu-id="e7829-105">This function sets the end-of-file marker to the current position of the file pointer.</span></span>

<span data-ttu-id="e7829-106">Si noti che quando un file viene esteso, il contenuto tra i percorsi di fine file obsoleti e nuovi non è definito.</span><span class="sxs-lookup"><span data-stu-id="e7829-106">Note that when a file is extended, the contents between the old and new end-of-file locations are not defined.</span></span>

 

 



