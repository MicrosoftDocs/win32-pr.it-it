---
description: Enumerazione e liberazione di servizi
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Enumerazione e liberazione di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859abe590ccaf2f71df676d5989778d5b391be57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317156"
---
# <a name="enumerating-and-freeing-services"></a><span data-ttu-id="9565a-103">Enumerazione e liberazione di servizi</span><span class="sxs-lookup"><span data-stu-id="9565a-103">Enumerating and Freeing Services</span></span>

<span data-ttu-id="9565a-104">L'applicazione ELS chiama la funzione [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) per determinare i servizi disponibili nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9565a-104">The ELS application calls the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function to determine the services that are available on the operating system.</span></span> <span data-ttu-id="9565a-105">La funzione può essere utilizzata per enumerare tutti i servizi ELS disponibili o per filtrare i servizi in base ai criteri di ricerca forniti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9565a-105">The function can be used either to enumerate all available ELS services, or to filter the services based on application-provided search criteria.</span></span> <span data-ttu-id="9565a-106">Quando i servizi non sono più necessari, l'applicazione chiama [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span><span class="sxs-lookup"><span data-stu-id="9565a-106">When services are no longer needed, the application calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span></span>

## <a name="get-all-supported-services"></a><span data-ttu-id="9565a-107">Ottenere tutti i servizi supportati</span><span class="sxs-lookup"><span data-stu-id="9565a-107">Get All Supported Services</span></span>

<span data-ttu-id="9565a-108">Questo esempio di codice illustra l'uso di [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) per enumerare e quindi liberare tutti i servizi disponibili nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9565a-108">This code example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all available services on the operating system.</span></span> <span data-ttu-id="9565a-109">A tale scopo, l'applicazione passa **null** per il parametro *pOptions* di **MappingGetServices**.</span><span class="sxs-lookup"><span data-stu-id="9565a-109">To do this, the application passes **NULL** for the *pOptions* parameter of **MappingGetServices**.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    // Get all installed ELS services.
    Result = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="get-specific-services"></a><span data-ttu-id="9565a-110">Ottenere servizi specifici</span><span class="sxs-lookup"><span data-stu-id="9565a-110">Get Specific Services</span></span>

<span data-ttu-id="9565a-111">Nell'esempio seguente viene illustrato l'utilizzo di [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) per enumerare e quindi liberare tutti i servizi della categoria "rilevamento lingua".</span><span class="sxs-lookup"><span data-stu-id="9565a-111">The next example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all services of category "Language Detection".</span></span> <span data-ttu-id="9565a-112">Per ulteriori informazioni su questa categoria di servizi, vedere [**Microsoft rilevamento lingua**](microsoft-language-detection.md).</span><span class="sxs-lookup"><span data-stu-id="9565a-112">For more information about this service category, see [**Microsoft Language Detection**](microsoft-language-detection.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);

    // Use the Language Auto-Detection category to enumerate
    // all language detection services.
    EnumOptions.pszCategory = L"Language Detection";

    // Execute the enumeration:
    Result = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="9565a-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9565a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9565a-114">Uso di servizi linguistici estesi</span><span class="sxs-lookup"><span data-stu-id="9565a-114">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="9565a-115">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="9565a-115">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[<span data-ttu-id="9565a-116">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="9565a-116">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



