---
title: Aggiunta di un'origine evento a una sottoscrizione avviata dall'agente di raccolta
description: Per ricevere un evento inoltrato da una sottoscrizione di eventi, è possibile creare una sottoscrizione avviata dall'agente di raccolta nel computer locale.
ms.assetid: f0100938-1702-4ef7-b20e-a0e8df224d18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905dd9b5a250f9ab12397f851f79a8374c6847235acb34013972dea445f3622b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344212"
---
# <a name="adding-an-event-source-to-a-collector-initiated-subscription"></a>Aggiunta di un'origine evento a una sottoscrizione avviata dall'agente di raccolta

Per ricevere un evento inoltrato da una sottoscrizione di eventi, è possibile creare una sottoscrizione avviata dall'agente di raccolta nel computer locale. Per altre informazioni su come creare una sottoscrizione avviata dall'agente di raccolta, vedere l'esempio di codice C++ illustrato in [Creazione di una sottoscrizione dell'agente di raccolta eventi](creating-an-event-collector-subscription.md).

Dopo aver creato una sottoscrizione avviata dall'agente di raccolta, è possibile aggiungere origini eventi alla sottoscrizione. È necessario aggiungere almeno un'origine eventi a una sottoscrizione per raccogliere gli eventi.

> [!Note]
>
> È possibile usare questo esempio di codice per aggiungere un'origine evento a una sottoscrizione oppure digitare il comando seguente al prompt dei comandi:
>
> **wecutil ss** *SubscriptionName* **/esa:**_EventSourceAddress_ **/aes /ese**
>
> *EventSourceAddress* può essere localhost per il computer locale o un nome di dominio completo per un computer remoto.

 

Per altre informazioni su come aggiungere origini eventi a una sottoscrizione avviata dall'origine, vedere [Impostazione di una sottoscrizione avviata dall'origine](setting-up-a-source-initiated-subscription.md).

Questo esempio segue una serie di passaggi per aggiungere un'origine evento a una sottoscrizione avviata dall'agente di raccolta.

**Per aggiungere un'origine evento a una sottoscrizione avviata dall'agente di raccolta**

1.  Aprire la sottoscrizione esistente specificando il nome della sottoscrizione e i diritti di accesso come parametri per la [**funzione EcOpenSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) Per altre informazioni sui diritti di accesso, vedere [**Costanti dell'agente**](windows-event-collector-constants.md)Windows eventi .
2.  Ottenere la matrice di origini eventi della sottoscrizione chiamando la [**funzione EcGetSubscriptionProperty.**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) Per altre informazioni sulle proprietà della sottoscrizione che possono essere recuperate, vedere l'enumerazione [**EC \_ SUBSCRIPTION PROPERTY \_ \_ ID.**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)
3.  Aggiungere una nuova origine evento alla matrice di origini eventi della sottoscrizione chiamando la [**funzione EcInsertObjectArrayElement.**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
4.  Impostare le proprietà dell'origine evento chiamando la [**funzione EcSetObjectArrayProperty.**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) La **proprietà EcSubscriptionEventSourceAddress** è impostata su un indirizzo per il computer locale (Localhost) o su un nome di dominio completo per un computer remoto. Per altre informazioni sulle proprietà dell'origine evento che è possibile impostare, vedere l'enumerazione **EC \_ SUBSCRIPTION PROPERTY \_ \_ ID.**
5.  Salvare la sottoscrizione chiamando la [**funzione EcSaveSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
6.  Chiudere la sottoscrizione chiamando la [**funzione EcClose.**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)

L'esempio di codice C++ seguente illustra come aggiungere un'origine evento a una sottoscrizione avviata dall'agente di raccolta:


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);

void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost"; 
    BOOL status = true;
    std::wstring eventSourceUserName;
    std::wstring eventSourcePassword;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vEventSource = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_VARIANT vProperty;

    // Create a handle to access the event sources array.
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription( lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to add a new event 
    // source to the subscription.
    dwRetVal = GetProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vEventSource);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained. 
    if (vEventSource->Type != EcVarTypeNull  && 
        vEventSource->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vEventSource->Type == EcVarTypeNull)? NULL: 
        vEventSource->PropertyHandleVal;
    if(!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }
    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Add a new event source to the event source array.
    if (!EcInsertObjectArrayElement(hArray,
        dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Set the properties of the event source
    // Set the EventSourceAddress property that specifies the address
    // of the event forwarding computer, this property can be localhost 
    // or a fully-qualified domain name.
    vProperty.Type = EcVarTypeString;
    vProperty.StringVal = eventSource.c_str();
    if (!EcSetObjectArrayProperty( hArray,
        EcSubscriptionEventSourceAddress,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the credentials.
    wcout << "Enter credentials used to connect to the event source " <<
        eventSource << ". " << endl <<
        "Enter user name: " << endl;
    wcin >> eventSourceUserName;
    cout << "Enter password: " << endl;

    wchar_t c;
    while( (c = _getwch()) && c != '\n' && c != '\r' && eventSourcePassword.length() < 512)
    {eventSourcePassword.append(1, c);}

    // Set the EventSourceUserName property that specifies the user
    // that can retrieve events from the event source.
    if (eventSourceUserName.length() > 0)
    {
        vProperty.Type = EcVarTypeString;
        vProperty.StringVal = eventSourceUserName.c_str();
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourceUserName,
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the EventSourcePassword property that defines the password
        // for the previously-defined user.
        vProperty.StringVal = (eventSourcePassword.length() > 0) ? 
            eventSourcePassword.c_str() : L"";
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourcePassword, 
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // When you have finished using the credentials,
    // erase them.
    eventSourceUserName.erase();
    eventSourcePassword.erase();


    // Set the EventSourceEnabled property that enables the event source
    // to forward events.
    vProperty.Type = EcVarTypeBoolean;
    vProperty.BooleanVal = status;
    if (!EcSetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceEnabled,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 5: Save the subscription to enable the event source.
    if (!EcSaveSubscription(hSubscription, NULL))
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
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u\n  Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }
        wprintf(L"\nFailed to Perform Operation. Error Code: %u\n Error Message: %s\n", dwRetVal, lpwszBuffer);
        LocalFree(lpwszBuffer);
    }
}

DWORD GetProperty(EC_HANDLE hSubscription,
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
                &dwBufferSize) )
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

[Configurare i computer per l'inoltro e la raccolta di eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))
</dt> <dt>

[Creazione di una sottoscrizione dell'agente di raccolta eventi](creating-an-event-collector-subscription.md)
</dt> <dt>

[Windows Informazioni di riferimento sull'agente di raccolta eventi](windows-event-collector-reference.md)
</dt> </dl>

 

 