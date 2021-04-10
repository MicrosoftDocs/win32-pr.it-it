---
description: Se un esperto non riesce in fase di esecuzione, se si usano Network Monitor funzioni per la gestione della memoria, Network Monitor libera la memoria allocata.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966773"
---
# <a name="managing-memory"></a><span data-ttu-id="4ae92-103">Gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="4ae92-103">Managing Memory</span></span>

<span data-ttu-id="4ae92-104">Se un esperto non riesce in fase di esecuzione, se si usano Network Monitor funzioni per la gestione della memoria, Network Monitor libera la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="4ae92-104">Should an expert fail during run time, if you use Network Monitor functions for memory management, Network Monitor will free allocated memory.</span></span> <span data-ttu-id="4ae92-105">Tuttavia, quando si scrive un esperto, potrebbe essere necessario acquisire le risorse di sistema e le informazioni sulla struttura dei dati.</span><span class="sxs-lookup"><span data-stu-id="4ae92-105">However, when you write an expert, it might be necessary to acquire system resources and data structure information.</span></span> <span data-ttu-id="4ae92-106">Ad esempio, l'esperto di COALESCE del protocollo Network Monitor acquisisce un handle di file per compilare una nuova acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4ae92-106">For example, the Network Monitor Protocol Coalesce Expert acquires a file handle to build a new capture.</span></span> <span data-ttu-id="4ae92-107">Ogni esperto deve creare una propria gestione **try/catch** in modo che l'esperto possa liberare risorse acquisite.</span><span class="sxs-lookup"><span data-stu-id="4ae92-107">Each expert must build its own **try/catch** handling so that the expert can free resources it acquired.</span></span>

<span data-ttu-id="4ae92-108">Quando la memoria viene allocata, usare le funzioni di memoria esistenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ae92-108">When memory is allocated, use the following existing memory functions:</span></span>

-   [<span data-ttu-id="4ae92-109">**ExpertAllocMemory**</span><span class="sxs-lookup"><span data-stu-id="4ae92-109">**ExpertAllocMemory**</span></span>](expertallocmemory.md)
-   [<span data-ttu-id="4ae92-110">**ExpertReallocMemory**</span><span class="sxs-lookup"><span data-stu-id="4ae92-110">**ExpertReallocMemory**</span></span>](expertreallocmemory.md)

 

 



