---
title: Aggiunta di un'origine evento a una sottoscrizione avviata dall'agente di raccolta
description: Per ricevere un evento trasmesso da una sottoscrizione di eventi, è possibile creare una sottoscrizione avviata dall'agente di raccolta nel computer locale.
ms.assetid: f0100938-1702-4ef7-b20e-a0e8df224d18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c639b496a00f56a38a0f9f8e72b9d099e58c17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046893"
---
# <a name="adding-an-event-source-to-a-collector-initiated-subscription"></a><span data-ttu-id="d8d6b-103">Aggiunta di un'origine evento a una sottoscrizione avviata dall'agente di raccolta</span><span class="sxs-lookup"><span data-stu-id="d8d6b-103">Adding an Event Source to a Collector Initiated Subscription</span></span>

<span data-ttu-id="d8d6b-104">Per ricevere un evento trasmesso da una sottoscrizione di eventi, è possibile creare una sottoscrizione avviata dall'agente di raccolta nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d8d6b-104">To receive a forwarded event from an event subscription, you can create a collector-initiated subscription on the local computer.</span></span> <span data-ttu-id="d8d6b-105">Per ulteriori informazioni su come creare una sottoscrizione avviata dall'agente di raccolta, vedere l'esempio di codice C++ illustrato in [creazione di una sottoscrizione di raccolta eventi](creating-an-event-collector-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="d8d6b-105">For more information about how to create a collector initiated subscription, see the C++ code example shown in [Creating an Event Collector Subscription](creating-an-event-collector-subscription.md).</span></span>

<span data-ttu-id="d8d6b-106">Dopo la creazione di una sottoscrizione avviata dall'agente di raccolta, è possibile aggiungere origini eventi alla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d8d6b-106">After a collector-initiated subscription has been created, you can add event sources to the subscription.</span></span> <span data-ttu-id="d8d6b-107">Per raccogliere gli eventi, è necessario aggiungere almeno un'origine evento a una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d8d6b-107">You must add at least one event source to a subscription to collect events.</span></span>

> [!Note]
>
> <span data-ttu-id="d8d6b-108">Questo esempio di codice può essere usato per aggiungere un'origine evento a una sottoscrizione oppure è possibile digitare il comando seguente al prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="d8d6b-108">You can use this code example to add an event source to a subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="d8d6b-109">**wecutil SS** *subscriptionname*  \* */ESA: \* \* \* EventSourceAddress* **/AES/ESE**</span><span class="sxs-lookup"><span data-stu-id="d8d6b-109">**wecutil ss** *SubscriptionName* \**/esa:\*\*\*EventSourceAddress* **/aes /ese**</span></span>
>
> <span data-ttu-id="d8d6b-110">*EventSourceAddress* può essere localhost per il computer locale o un nome di dominio completo per un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="d8d6b-110">*EventSourceAddress* can be either localhost for the local computer or a fully qualified domain name for a remote computer.</span></span>

 

<span data-ttu-id="d8d6b-111">Per altre informazioni su come aggiungere origini eventi a una sottoscrizione avviata dall'origine, vedere [configurazione di una sottoscrizione avviata dall'origine](setting-up-a-source-initiated-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="d8d6b-111">For more information about how to add event sources to a source initiated subscription, see [Setting up a Source Initiated Subscription](setting-up-a-source-initiated-subscription.md).</span></span>

<span data-ttu-id="d8d6b-112">Questo esempio segue una serie di passaggi per aggiungere un'origine evento a una sottoscrizione avviata dall'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="d8d6b-112">This example follows a series of steps to add an event source to a collector initiated subscription.</span></span>

<span data-ttu-id="d8d6b-113">**Per aggiungere un'origine evento a una sottoscrizione avviata dall'agente di raccolta**</span><span class="sxs-lookup"><span data-stu-id="d8d6b-113">**To add an event source to a collector initiated subscription**</span></span>

1.  <span data-ttu-id="d8d6b-114">Aprire la sottoscrizione esistente fornendo il nome della sottoscrizione e i diritti di accesso come parametri per la funzione [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="d8d6b-114">Open the existing subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="d8d6b-115">Per ulteriori informazioni sui diritti di accesso, vedere [**costanti dell'agente di raccolta eventi di Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d8d6b-115">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="d8d6b-116">Ottenere la matrice di origini eventi della sottoscrizione chiamando la funzione [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) .</span><span class="sxs-lookup"><span data-stu-id="d8d6b-116">Get the event sources array of the subscription by calling the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) function.</span></span> <span data-ttu-id="d8d6b-117">Per ulteriori informazioni sulle proprietà di sottoscrizione che possono essere recuperate, vedere l'enumerazione di [**\_ \_ \_ ID proprietà della sottoscrizione EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .</span><span class="sxs-lookup"><span data-stu-id="d8d6b-117">For more information about subscription properties that can be retrieved, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="d8d6b-118">Aggiungere una nuova origine evento alla matrice di origini eventi della sottoscrizione chiamando la funzione [**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) .</span><span class="sxs-lookup"><span data-stu-id="d8d6b-118">Add a new event source to the event sources array of the subscription by calling the [**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) function.</span></span>
4.  <span data-ttu-id="d8d6b-119">Impostare le proprietà dell'origine evento chiamando la funzione [**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) .</span><span class="sxs-lookup"><span data-stu-id="d8d6b-119">Set the event source properties by calling the [**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) function.</span></span> <span data-ttu-id="d8d6b-120">La proprietà **EcSubscriptionEventSourceAddress** è impostata su un indirizzo per il computer locale (localhost) o su un nome di dominio completo per un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="d8d6b-120">The **EcSubscriptionEventSourceAddress** property is either set to an address for the local computer (Localhost) or to a fully qualified domain name for a remote computer.</span></span> <span data-ttu-id="d8d6b-121">Per ulteriori informazioni sulle proprietà dell'origine evento che è possibile impostare, vedere l'enumerazione dell' **\_ \_ \_ ID proprietà della sottoscrizione EC** .</span><span class="sxs-lookup"><span data-stu-id="d8d6b-121">For more information about event source properties that can be set, see the **EC\_SUBSCRIPTION\_PROPERTY\_ID** enumeration.</span></span>
5.  <span data-ttu-id="d8d6b-122">Salvare la sottoscrizione chiamando la funzione [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .</span><span class="sxs-lookup"><span data-stu-id="d8d6b-122">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
6.  <span data-ttu-id="d8d6b-123">Chiudere la sottoscrizione chiamando la funzione [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="d8d6b-123">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="d8d6b-124">Nell'esempio di codice C++ riportato di seguito viene illustrato come aggiungere un'origine evento a una sottoscrizione avviata dall'agente di raccolta:</span><span class="sxs-lookup"><span data-stu-id="d8d6b-124">The following C++ code example shows how to add an event source to a collector initiated subscription:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d8d6b-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8d6b-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d8d6b-126">[Configurare i computer per l'invio e la raccolta di eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="d8d6b-126">[Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="d8d6b-127">Creazione di una sottoscrizione di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="d8d6b-127">Creating an Event Collector Subscription</span></span>](creating-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="d8d6b-128">Informazioni di riferimento sull'agente di raccolta eventi Windows</span><span class="sxs-lookup"><span data-stu-id="d8d6b-128">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 