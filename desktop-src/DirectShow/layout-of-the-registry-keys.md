---
description: Layout delle chiavi del registro di sistema
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Layout delle chiavi del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303710"
---
# <a name="layout-of-the-registry-keys"></a><span data-ttu-id="bd64f-103">Layout delle chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="bd64f-103">Layout of the Registry Keys</span></span>

<span data-ttu-id="bd64f-104">I filtri DirectShow sono registrati in due posizioni:</span><span class="sxs-lookup"><span data-stu-id="bd64f-104">DirectShow filters are registered in two places:</span></span>

-   <span data-ttu-id="bd64f-105">La DLL che contiene il filtro è registrata come server COM del filtro.</span><span class="sxs-lookup"><span data-stu-id="bd64f-105">The DLL that contains the filter is registered as the filter's COM server.</span></span> <span data-ttu-id="bd64f-106">Quando un'applicazione chiama **CoCreateInstance** per creare il filtro, la libreria COM di Microsoft Windows utilizza questa voce del registro di sistema per individuare la dll.</span><span class="sxs-lookup"><span data-stu-id="bd64f-106">When an application calls **CoCreateInstance** to create the filter, the Microsoft Windows COM library uses this registry entry to locate the DLL.</span></span>
-   <span data-ttu-id="bd64f-107">È possibile registrare informazioni aggiuntive sul filtro all'interno di una categoria di filtro.</span><span class="sxs-lookup"><span data-stu-id="bd64f-107">Additional information about the filter can be registered within a filter category.</span></span> <span data-ttu-id="bd64f-108">Queste informazioni consentono a [System Device Enumerator](system-device-enumerator.md) e a [Filter Mapper](filter-mapper.md) di individuare il filtro.</span><span class="sxs-lookup"><span data-stu-id="bd64f-108">This information enables the [System Device Enumerator](system-device-enumerator.md) and the [Filter Mapper](filter-mapper.md) to locate the filter.</span></span>

<span data-ttu-id="bd64f-109">I filtri non sono necessari per registrare le informazioni aggiuntive sul filtro.</span><span class="sxs-lookup"><span data-stu-id="bd64f-109">Filters are not required to register the additional filter information.</span></span> <span data-ttu-id="bd64f-110">Finché la DLL viene registrata come server COM, un'applicazione può creare il filtro e aggiungerlo a un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="bd64f-110">As long as the DLL is registered as the COM server, an application can create the filter and add it to a filter graph.</span></span> <span data-ttu-id="bd64f-111">Tuttavia, se si desidera che il filtro sia individuabile dall'enumeratore del dispositivo di sistema o dal mapper del filtro, è necessario registrare le informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="bd64f-111">However, if you want your filter to be discoverable by the System Device Enumerator or the Filter Mapper, you must register the additional information.</span></span>

<span data-ttu-id="bd64f-112">La voce del registro di sistema per la DLL presenta le chiavi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd64f-112">The registry entry for the DLL has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



<span data-ttu-id="bd64f-113">La voce del registro di sistema per le informazioni sul filtro presenta le chiavi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd64f-113">The registry entry for the filter information has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



<span data-ttu-id="bd64f-114">GUID di una categoria di filtro.</span><span class="sxs-lookup"><span data-stu-id="bd64f-114">is the GUID of a filter category.</span></span> <span data-ttu-id="bd64f-115">(Vedere [categorie di filtro](filter-categories.md)). Le informazioni sul filtro vengono compresse in un formato binario.</span><span class="sxs-lookup"><span data-stu-id="bd64f-115">(See [Filter Categories](filter-categories.md).) The filter information is packed into a binary format.</span></span> <span data-ttu-id="bd64f-116">L'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) decomprime questi dati quando cerca un filtro nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bd64f-116">The [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface unpacks this data when it searches the registry for a filter.</span></span>

<span data-ttu-id="bd64f-117">Tutti i GUID della categoria Filter sono elencati nel registro di sistema nella chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="bd64f-117">All of the filter category GUIDs are listed in the registry under the following key:</span></span>


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



