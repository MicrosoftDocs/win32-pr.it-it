---
description: Scrittura dei filtri di acquisizione
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Scrittura dei filtri di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313389"
---
# <a name="writing-capture-filters"></a><span data-ttu-id="a9f58-103">Scrittura dei filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="a9f58-103">Writing Capture Filters</span></span>

<span data-ttu-id="a9f58-104">La scrittura di un filtro di acquisizione audio o video per DirectShow non è consigliata.</span><span class="sxs-lookup"><span data-stu-id="a9f58-104">Writing an audio or video capture filter for DirectShow is not recommended.</span></span> <span data-ttu-id="a9f58-105">DirectShow fornisce invece il supporto automatico per i dispositivi di acquisizione audio e video, usando i filtri wrapper e l' [enumeratore di dispositivi di sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="a9f58-105">Instead, DirectShow provides automatic support for audio and video capture devices, using wrapper filters and the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="a9f58-106">Per ulteriori informazioni sull'implementazione di un driver di dispositivo, consultare la documentazione di Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="a9f58-106">For more information about implementing a device driver, refer to the Windows Driver Kit (WDK) documentation.</span></span>

<span data-ttu-id="a9f58-107">Questa sezione è destinata solo agli sviluppatori che devono acquisire alcuni tipi di dati personalizzati da un dispositivo hardware insolito.</span><span class="sxs-lookup"><span data-stu-id="a9f58-107">This section is intended only for developers who need to capture some kind of custom data from an unusual hardware device.</span></span>

<span data-ttu-id="a9f58-108">In questo articolo sono contenute le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9f58-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="a9f58-109">Requisiti PIN per i filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="a9f58-109">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
-   [<span data-ttu-id="a9f58-110">Implementazione di un pin di anteprima (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="a9f58-110">Implementing a Preview Pin (Optional)</span></span>](implementing-a-preview-pin--optional.md)
-   [<span data-ttu-id="a9f58-111">Produzione di dati in un filtro di acquisizione</span><span class="sxs-lookup"><span data-stu-id="a9f58-111">Producing Data in a Capture Filter</span></span>](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a><span data-ttu-id="a9f58-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9f58-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9f58-113">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="a9f58-113">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



