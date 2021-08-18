---
description: Per recuperare un elenco di provider che hanno installato il manifesto o le classi MOF nel computer, chiamare la funzione TdhEnumerateProviders.
ms.assetid: 79a29a55-e211-4921-ac78-a21ef8ef238f
title: Enumerazione dei provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b93bcecbd1713a2945ea97703a77ab33629987f989505dea9498d03b7cb17c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755071"
---
# <a name="enumerating-providers"></a>Enumerazione dei provider

Per recuperare un elenco di provider che hanno installato il manifesto o le classi MOF nel computer, chiamare la [**funzione TdhEnumerateProviders.**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviders)

Nell'esempio seguente viene illustrato come enumerare i provider.


```C++
#include <windows.h>
#include <stdio.h>
#include <tdh.h>

#pragma comment(lib, "tdh.lib")

#define MAX_GUID_SIZE 39

void wmain(void)
{
    DWORD status = ERROR_SUCCESS;
    PROVIDER_ENUMERATION_INFO* penum = NULL;    // Buffer that contains provider information
    PROVIDER_ENUMERATION_INFO* ptemp = NULL;
    DWORD BufferSize = 0;                       // Size of the penum buffer
    HRESULT hr = S_OK;                          // Return value for StringFromGUID2
    WCHAR StringGuid[MAX_GUID_SIZE];
    DWORD RegisteredMOFCount = 0;
    DWORD RegisteredManifestCount = 0;

    // Retrieve the required buffer size.

    status = TdhEnumerateProviders(penum, &BufferSize);

    // Allocate the required buffer and call TdhEnumerateProviders. The list of 
    // providers can change between the time you retrieved the required buffer 
    // size and the time you enumerated the providers, so call TdhEnumerateProviders
    // in a loop until the function does not return ERROR_INSUFFICIENT_BUFFER.

    while (ERROR_INSUFFICIENT_BUFFER == status)
    {
        ptemp = (PROVIDER_ENUMERATION_INFO*)realloc(penum, BufferSize);
        if (NULL == ptemp)
        {
            wprintf(L"Allocation failed (size=%lu).\n", BufferSize);
            goto cleanup;
        }

        penum = ptemp;
        ptemp = NULL;

        status = TdhEnumerateProviders(penum, &BufferSize);
    }

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"TdhEnumerateProviders failed with %lu.\n", status);
    }
    else
    {
        // Loop through the list of providers and print the provider's name, GUID, 
        // and the source of the information (MOF class or instrumentation manifest).

        for (DWORD i = 0; i < penum->NumberOfProviders; i++)
        {
            hr = StringFromGUID2(penum->TraceProviderInfoArray[i].ProviderGuid, StringGuid, ARRAYSIZE(StringGuid));

            if (FAILED(hr))
            {
                wprintf(L"StringFromGUID2 failed with 0x%x\n", hr);
                goto cleanup;
            }

            wprintf(L"Provider name: %s\nProvider GUID: %s\nSource: %s\n\n",
                (LPWSTR)((PBYTE)(penum)+penum->TraceProviderInfoArray[i].ProviderNameOffset),
                StringGuid,
                (penum->TraceProviderInfoArray[i].SchemaSource) ? L"WMI MOF class" : L"XML manifest");

            (penum->TraceProviderInfoArray[i].SchemaSource) ? RegisteredMOFCount++ : RegisteredManifestCount++;
        }

        wprintf(L"\nThere are %d registered providers; %lu are registered via MOF class and\n%lu are registered via a manifest.\n",
            penum->NumberOfProviders,
            RegisteredMOFCount,
            RegisteredManifestCount);
    }

cleanup:

    if (penum)
    {
        free(penum);
        penum = NULL;
    }
}
```



 

 



