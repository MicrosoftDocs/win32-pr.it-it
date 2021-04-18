---
description: Le funzioni di installazione gestiscono gli armadi internamente. Per enumerare ed estrarre in modo esplicito i file da un file CAB, è possibile chiamare la funzione SetupIterateCabinet.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Uso dei file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316607"
---
# <a name="using-cabinet-files"></a><span data-ttu-id="622a6-104">Uso dei file CAB</span><span class="sxs-lookup"><span data-stu-id="622a6-104">Using Cabinet Files</span></span>

<span data-ttu-id="622a6-105">Le funzioni di installazione gestiscono gli armadi internamente.</span><span class="sxs-lookup"><span data-stu-id="622a6-105">The setup functions handle cabinets internally.</span></span> <span data-ttu-id="622a6-106">Per enumerare ed estrarre in modo esplicito i file da un file CAB, è possibile chiamare la funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="622a6-106">To explicitly enumerate and extract files from a cabinet, you can call the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

<span data-ttu-id="622a6-107">Nell'argomento seguente viene descritta l'elaborazione del file CAB interna alle funzioni di installazione e come usare [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="622a6-107">The following topic describes the cabinet processing internal to the setup functions and how to use [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="622a6-108">Vengono inoltre descritte le notifiche inviate da **SetupIterateCabinet** e il formato necessario di una routine di callback del cabinet per elaborare tali notifiche.</span><span class="sxs-lookup"><span data-stu-id="622a6-108">Also discussed are the notifications sent by **SetupIterateCabinet** and the required format of a cabinet callback routine to process those notifications.</span></span>

-   [<span data-ttu-id="622a6-109">Estrazione di file da file CAB</span><span class="sxs-lookup"><span data-stu-id="622a6-109">Extracting Files From Cabinets</span></span>](extracting-files-from-cabinets.md)
-   [<span data-ttu-id="622a6-110">Creazione di una routine di callback del cabinet</span><span class="sxs-lookup"><span data-stu-id="622a6-110">Creating a Cabinet Callback Routine</span></span>](creating-a-cabinet-callback-routine.md)

 

 



