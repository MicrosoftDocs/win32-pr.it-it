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
# <a name="enumerating-and-freeing-services"></a>Enumerazione e liberazione di servizi

L'applicazione ELS chiama la funzione [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) per determinare i servizi disponibili nel sistema operativo. La funzione può essere utilizzata per enumerare tutti i servizi ELS disponibili o per filtrare i servizi in base ai criteri di ricerca forniti dall'applicazione. Quando i servizi non sono più necessari, l'applicazione chiama [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).

## <a name="get-all-supported-services"></a>Ottenere tutti i servizi supportati

Questo esempio di codice illustra l'uso di [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) per enumerare e quindi liberare tutti i servizi disponibili nel sistema operativo. A tale scopo, l'applicazione passa **null** per il parametro *pOptions* di **MappingGetServices**.


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



## <a name="get-specific-services"></a>Ottenere servizi specifici

Nell'esempio seguente viene illustrato l'utilizzo di [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) per enumerare e quindi liberare tutti i servizi della categoria "rilevamento lingua". Per ulteriori informazioni su questa categoria di servizi, vedere [**Microsoft rilevamento lingua**](microsoft-language-detection.md).


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di servizi linguistici estesi](using-extended-linguistic-services.md)
</dt> <dt>

[**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



