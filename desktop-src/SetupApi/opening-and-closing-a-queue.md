---
description: Prima di poter accodare le operazioni sui file, è necessario aprire una coda di file. La chiamata della funzione SetupOpenFileQueue restituisce un handle a un file di coda. Questo handle viene usato dalle funzioni di coda successive per fare riferimento alla coda aperta e aggiungervi operazioni o eseguirne l'analisi.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Apertura e chiusura di una coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315316"
---
# <a name="opening-and-closing-a-queue"></a><span data-ttu-id="1e986-105">Apertura e chiusura di una coda</span><span class="sxs-lookup"><span data-stu-id="1e986-105">Opening and Closing a Queue</span></span>

<span data-ttu-id="1e986-106">Prima di poter accodare le operazioni sui file, è necessario aprire una coda di file.</span><span class="sxs-lookup"><span data-stu-id="1e986-106">Before you can queue file operations, you must open a file queue.</span></span> <span data-ttu-id="1e986-107">La chiamata della funzione [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) restituisce un handle a un file di coda.</span><span class="sxs-lookup"><span data-stu-id="1e986-107">Calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function returns a handle to a queue file.</span></span> <span data-ttu-id="1e986-108">Questo handle viene usato dalle funzioni di coda successive per fare riferimento alla coda aperta e aggiungervi operazioni o eseguirne l'analisi.</span><span class="sxs-lookup"><span data-stu-id="1e986-108">This handle is used by subsequent queue functions to reference the open queue and add operations to it or scan it.</span></span>

<span data-ttu-id="1e986-109">Dopo che tutte le operazioni sui file specificate sono state accodate e ne è stato eseguito il commit, è necessario chiamare la funzione [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) per rilasciare le risorse allocate durante la chiamata a [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="1e986-109">After all the specified file operations have been queued and committed, you must call the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function to release resources allocated during the call to [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span>

> [!Note]  
> <span data-ttu-id="1e986-110">La funzione [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) non esegue il commit della coda di file.</span><span class="sxs-lookup"><span data-stu-id="1e986-110">The [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function does not commit the file queue.</span></span> <span data-ttu-id="1e986-111">Tutte le operazioni di cui non è stato eseguito il commit quando viene chiamato **SetupCloseFileQueue** non verranno eseguite.</span><span class="sxs-lookup"><span data-stu-id="1e986-111">Any operations that are uncommitted when **SetupCloseFileQueue** is called will not be performed.</span></span>

 

 

 



