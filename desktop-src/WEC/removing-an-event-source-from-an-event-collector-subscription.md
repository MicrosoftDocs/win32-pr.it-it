---
title: Rimozione di un'origine evento da una sottoscrizione avviata dall'agente di raccolta
description: È possibile rimuovere un'origine evento da una sottoscrizione avviata dall'agente di raccolta senza eliminare l'intera sottoscrizione.
ms.assetid: 6c9e0dbf-59a2-4db9-8fb8-0dbfda5cf38b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303e0a708c2b52225af83475674e5f60d1a8418d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856446"
---
# <a name="removing-an-event-source-from-a-collector-initiated-subscription"></a>Rimozione di un'origine evento da una sottoscrizione avviata dall'agente di raccolta

È possibile rimuovere un'origine evento da una sottoscrizione avviata dall'agente di raccolta senza eliminare l'intera sottoscrizione. È necessario essere a conoscenza dell'indirizzo dell'origine evento che si desidera eliminare. È possibile trovare l'indirizzo di un'origine evento associato a una sottoscrizione usando l'esempio C++ illustrato in [visualizzazione delle proprietà di una sottoscrizione dell'agente di raccolta eventi](displaying-the-properties-of-an-event-collector-subscription.md)oppure è possibile digitare il comando seguente al prompt dei comandi:

*sottoscrizione* **wecutil gs**

Per elencare le sottoscrizioni correnti in un computer locale, è possibile usare l'esempio di codice C++ illustrato in [elenco delle sottoscrizioni](listing-event-collector-subscriptions.md)degli agenti di raccolta eventi oppure è possibile digitare il comando seguente al prompt dei comandi:

**wecutil es**

> [!Note]
>
> È possibile usare questo esempio per rimuovere un'origine evento da una sottoscrizione avviata dall'agente di raccolta oppure è possibile digitare il comando seguente al prompt dei comandi:
>
> **wecutil SS** *subscriptionname*  * */ESA: * * * EventSourceAddress* **/res**
>
> *EventSourceAddress* può essere localhost per il computer locale o un nome di dominio completo per un computer remoto.

 

Questo esempio segue una serie di passaggi per rimuovere un'origine evento da una sottoscrizione avviata dall'agente di raccolta.

**Per rimuovere un'origine evento da una sottoscrizione avviata dall'agente di raccolta**

1.  Aprire la sottoscrizione esistente fornendo il nome della sottoscrizione e i diritti di accesso come parametri per la funzione [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) . Per ulteriori informazioni sui diritti di accesso, vedere [**costanti dell'agente di raccolta eventi di Windows**](windows-event-collector-constants.md).
2.  Ottenere la matrice di origini eventi della sottoscrizione chiamando la funzione [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) . Per ulteriori informazioni sulle proprietà di sottoscrizione che possono essere recuperate, vedere l'enumerazione di [**\_ \_ \_ ID proprietà della sottoscrizione EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .
3.  Cercare l'origine evento specificata nella matrice di origini eventi della sottoscrizione chiamando la funzione [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) . Il valore della proprietà **EcSubscriptionEventSourceAddress** sarà localhost per il computer locale o sarà un nome di dominio completo per un computer remoto. Per ulteriori informazioni sulle proprietà dell'origine evento che possono essere recuperate, vedere l'enumerazione dell' **\_ \_ \_ ID proprietà della sottoscrizione EC** .
4.  Eliminare l'origine evento dalla sottoscrizione chiamando la funzione [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) .
5.  Salvare la sottoscrizione chiamando la funzione [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .
6.  Chiudere la sottoscrizione chiamando la funzione [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .

Nell'esempio di codice C++ riportato di seguito viene illustrato come rimuovere un'origine evento da una sottoscrizione di raccolta eventi.


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Subscription Information
DWORD GetSubscriptionProperty(EC_HANDLE hSubscription,  
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty);
DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD arrayIndex, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProper);



void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost";
    BOOL foundEventSource = false;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD deleteEvent = 0; 
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vProperty = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription(lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS,
        EC_OPEN_EXISTING);

    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to remove an event 
    // source from the subscription.
    dwRetVal = GetSubscriptionProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vProperty);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained.
    if (vProperty->Type != EcVarTypeNull  && 
        vProperty->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vProperty->Type == EcVarTypeNull)? NULL: 
        vProperty->PropertyHandleVal;
    if (!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Search for the specified event source in the event source array.
    for (DWORD I = 0; I < dwEventSourceCount; I++)
    {
        dwRetVal = GetEventSourceProperty(hArray, 
            EcSubscriptionEventSourceAddress, 
            I,
            0,
            buffer,
            vProperty);
        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }

        if (vProperty->StringVal == eventSource)
        {
            foundEventSource = true;
            deleteEvent = I;
            break;
        }
    }

    // Step 4: If the event source was found in the array, remove it.
    if (foundEventSource)
    {
        if (!EcRemoveObjectArrayElement(hArray, deleteEvent))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }
    else
    {
        wprintf(L"Could not remove the event source from the subscription.\n");
        goto Cleanup;
    }

    // Step 5: Save the subscription to finalize the removal of the event source.
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 6: Close the subscription.
    Cleanup:
        if (hArray)
            EcClose(hArray);
        if (hSubscription)
            EcClose(hSubscription);

        if (dwRetVal != ERROR_SUCCESS)
        {
            FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
                NULL,
                dwRetVal,
                0,
                (LPWSTR) &lpwszBuffer,
                0,
                NULL);
            
            if (!lpwszBuffer)
            {
                wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." \
                    L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
                return;
            }

            wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n" \
                L"Error Message: %s\n", dwRetVal, lpwszBuffer);

            LocalFree(lpwszBuffer);
        }
}

DWORD GetSubscriptionProperty(EC_HANDLE hSubscription, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty)
{
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hSubscription)
    return ERROR_INVALID_PARAMETER;

    // Get the value for the specified property. 
    if (!EcGetSubscriptionProperty(hSubscription,
        propID,
        flags,
        (DWORD) buffer.size(),
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetSubscriptionProperty(hSubscription,
                propID,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}

DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID,
    DWORD arrayIndex,
    DWORD flags,
    std::vector<BYTE>& buffer,
    PEC_VARIANT& vProperty)
{
    UNREFERENCED_PARAMETER(flags);
    UNREFERENCED_PARAMETER(propID);
    
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hArray)
        return ERROR_INVALID_PARAMETER;

    // Obtain the value for the specified property. 
    if (!EcGetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceAddress, 
        arrayIndex,
        0, 
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetObjectArrayProperty(hArray,
                EcSubscriptionEventSourceAddress,
                arrayIndex,
                0, 
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Visualizzazione delle proprietà di una sottoscrizione di raccolta eventi](displaying-the-properties-of-an-event-collector-subscription.md)
</dt> <dt>

[Elenco delle sottoscrizioni degli agenti di raccolta eventi](listing-event-collector-subscriptions.md)
</dt> <dt>

[Informazioni di riferimento sull'agente di raccolta eventi Windows](windows-event-collector-reference.md)
</dt> </dl>

 

 




