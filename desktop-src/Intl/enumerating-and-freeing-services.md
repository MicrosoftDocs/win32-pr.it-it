---
description: Enumerazione e freeing dei servizi
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Enumerazione e freeing dei servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6472851fbf5f7f84a499d2e9e04804279d397f31452d9617a8868e05cb8ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086611"
---
# <a name="enumerating-and-freeing-services"></a>Enumerazione e freeing dei servizi

L'applicazione ELS [**chiama la funzione MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) per determinare i servizi disponibili nel sistema operativo. La funzione può essere usata per enumerare tutti i servizi ELS disponibili o per filtrare i servizi in base ai criteri di ricerca forniti dall'applicazione. Quando i servizi non sono più necessari, l'applicazione chiama [**MappingFreeServices.**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)

## <a name="get-all-supported-services"></a>Ottenere tutti i servizi supportati

Questo esempio di codice illustra l'uso di [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) per enumerare e quindi liberare tutti i servizi disponibili nel sistema operativo. A tale scopo, l'applicazione **passa NULL** per il *parametro pOptions* **di MappingGetServices.**


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

L'esempio seguente illustra l'uso di [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) per enumerare e quindi liberare tutti i servizi della categoria "Rilevamento lingua". Per altre informazioni su questa categoria di servizi, vedere [**Microsoft Rilevamento lingua**](microsoft-language-detection.md).


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

[Uso di Servizi linguistici estesi](using-extended-linguistic-services.md)
</dt> <dt>

[**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



