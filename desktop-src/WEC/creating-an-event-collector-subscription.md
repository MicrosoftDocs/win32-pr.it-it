---
title: Creazione di una sottoscrizione avviata dall'agente di raccolta
description: È possibile sottoscrivere la ricezione di eventi in un computer locale, ovvero l'agente di raccolta eventi, che vengono trasmessi da computer remoti (origini eventi) utilizzando una sottoscrizione avviata dall'agente di raccolta.
ms.assetid: 76f14e01-7a84-4c94-aea6-91189573eb89
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1359033b61d419f1147ca930f30d924b8429e31
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223979"
---
# <a name="creating-a-collector-initiated-subscription"></a><span data-ttu-id="03414-103">Creazione di una sottoscrizione avviata dall'agente di raccolta</span><span class="sxs-lookup"><span data-stu-id="03414-103">Creating a Collector Initiated Subscription</span></span>

<span data-ttu-id="03414-104">È possibile sottoscrivere la ricezione di eventi in un computer locale, ovvero l'agente di raccolta eventi, che vengono trasmessi da computer remoti (origini eventi) utilizzando una sottoscrizione avviata dall'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="03414-104">You can subscribe to receive events on a local computer (the event collector) that are forwarded from remote computers (the event sources) by using a collector-initiated subscription.</span></span> <span data-ttu-id="03414-105">In una sottoscrizione avviata dall'agente di raccolta, la sottoscrizione deve contenere un elenco di tutte le origini evento.</span><span class="sxs-lookup"><span data-stu-id="03414-105">In a collector-initiated subscription, the subscription must contain a list of all the event sources.</span></span> <span data-ttu-id="03414-106">Prima che un computer agente di raccolta possa sottoscrivere gli eventi e un'origine evento remoto può inviare eventi, entrambi i computer devono essere configurati per la raccolta e l'invio di eventi.</span><span class="sxs-lookup"><span data-stu-id="03414-106">Before a collector computer can subscribe to events and a remote event source can forward events, both computers must be configured for event collecting and forwarding.</span></span> <span data-ttu-id="03414-107">Per ulteriori informazioni su come configurare i computer, vedere [configurare i computer per l'invio e la raccolta di eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="03414-107">For more information about how to configure the computers, see [Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).</span></span>

<span data-ttu-id="03414-108">L'esempio di codice seguente segue una serie di passaggi per creare una sottoscrizione avviata dall'agente di raccolta:</span><span class="sxs-lookup"><span data-stu-id="03414-108">The following code example follows a series of steps to create a collector initiated subscription:</span></span>

<span data-ttu-id="03414-109">**Per creare una sottoscrizione avviata dall'agente di raccolta**</span><span class="sxs-lookup"><span data-stu-id="03414-109">**To create a collector initiated subscription**</span></span>

1.  <span data-ttu-id="03414-110">Aprire la sottoscrizione fornendo il nome della sottoscrizione e i diritti di accesso come parametri della funzione [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="03414-110">Open the subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="03414-111">Per ulteriori informazioni sui diritti di accesso, vedere [**costanti dell'agente di raccolta eventi di Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="03414-111">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="03414-112">Impostare le proprietà della sottoscrizione chiamando la funzione [**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) .</span><span class="sxs-lookup"><span data-stu-id="03414-112">Set the properties of the subscription by calling the [**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) function.</span></span> <span data-ttu-id="03414-113">Per ulteriori informazioni sulle proprietà di sottoscrizione che è possibile impostare, vedere l'enumerazione di [**\_ \_ \_ ID proprietà della sottoscrizione EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .</span><span class="sxs-lookup"><span data-stu-id="03414-113">For more information about subscription properties that can be set, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="03414-114">Salvare la sottoscrizione chiamando la funzione [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .</span><span class="sxs-lookup"><span data-stu-id="03414-114">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
4.  <span data-ttu-id="03414-115">Chiudere la sottoscrizione chiamando la funzione [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="03414-115">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="03414-116">Per ulteriori informazioni sull'aggiunta di un'origine evento, vedere [aggiunta di un'origine evento a una sottoscrizione dell'agente di raccolta eventi](adding-an-event-source-to-an-event-collector-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="03414-116">For more information about adding an event source, see [Adding an Event Source to an Event Collector Subscription](adding-an-event-source-to-an-event-collector-subscription.md).</span></span>

<span data-ttu-id="03414-117">Nell'esempio di codice C++ riportato di seguito viene illustrato come creare una sottoscrizione avviata dall'agente di raccolta:</span><span class="sxs-lookup"><span data-stu-id="03414-117">The following C++ code example shows how to create a collector-initiated subscription:</span></span>


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <string>
#include <xstring>
#include <conio.h>
#include <EvColl.h>
#include <vector>
#include <wincred.h>
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "wecapi.lib")

// Track properties of the Subscription.
typedef struct _SUBSCRIPTION_COLLECTOR_INITIATED
{
    std::wstring Name;
    std::wstring Description;
    std::wstring URI;
    std::wstring Query;
    std::wstring DestinationLog;
    std::wstring Password;
    std::wstring UserName;
    EC_SUBSCRIPTION_CONFIGURATION_MODE ConfigMode;
    EC_SUBSCRIPTION_DELIVERY_MODE DeliveryMode;
    EC_SUBSCRIPTION_TYPE SubscriptionType;
    DWORD MaxItems;
    DWORD MaxLatencyTime;
    DWORD HeartbeatInerval;
    EC_SUBSCRIPTION_CONTENT_FORMAT ContentFormat;
    EC_SUBSCRIPTION_CREDENTIALS_TYPE CredentialsType;
    BOOL SubscriptionStatus;
} SUBSCRIPTION_COLLECTOR_INITIATED;

// Subscription Information
DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);


void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwRetVal = ERROR_SUCCESS;
    EC_HANDLE hSubscription = 0;
    EC_VARIANT vPropertyValue;
    std::vector<BYTE> buffer;
    PEC_VARIANT vProperty = NULL;
    SUBSCRIPTION_COLLECTOR_INITIATED sub;

    sub.Name = L"TestSubscription-CollectorInitiated";
    sub.Description = L"A subscription that collects events that are published in\n" \
        L"the Microsoft-Windows-TaskScheduler/Operational log and forwards them\n" \
        L"to the ForwardedEvents log.";
    sub.URI = L"http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog";
    sub.Query = L"<QueryList>" \
        L"<Query Path=\"Microsoft-Windows-TaskScheduler/Operational\">" \
        L"<Select>*</Select>" \
        L"</Query>" \
        L"</QueryList>";
    sub.DestinationLog = L"ForwardedEvents";
    sub.ConfigMode = EcConfigurationModeCustom;
    sub.MaxItems = 5;
    sub.MaxLatencyTime = 10000;
    sub.HeartbeatInerval = 10000;
    sub.DeliveryMode = EcDeliveryModePull;
    sub.ContentFormat = EcContentFormatRenderedText;
    sub.CredentialsType = EcSubscriptionCredDefault;
    sub.SubscriptionStatus = true;
    sub.SubscriptionType = EcSubscriptionTypeCollectorInitiated;

    std::wstring eventSource = L"localhost"; 
    BOOL status = true;
    PEC_VARIANT vEventSource = NULL;
    DWORD dwEventSourceCount;
    EC_VARIANT vSourceProperty;

    // Create a handle to access the event sources array.
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // The subscription name, URI, and query string must be defined to create 
    // the subscription.
    if ( sub.Name.empty() || sub.URI.empty() || sub.Query.empty() )
    {
        dwRetVal = ERROR_INVALID_PARAMETER;
        goto Cleanup;
    }

    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(sub.Name.c_str(),
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_CREATE_NEW);
    if ( !hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Define the subscription properties.
    // Set the Description property that contains a description
    // of the subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Description.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionDescription,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the subscription type property (collector initiated).
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.SubscriptionType;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionType,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the URI property that specifies the URI of all the event sources.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.URI.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionURI,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Query property that defines the query used by the event
    // source to select events that are forwarded to the event collector.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Query.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionQuery,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Log File property that specifies where the forwarded events
    // will be stored.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.DestinationLog.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionLogFile,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the ConfigurationMode property that specifies the mode in which events 
    // are delivered.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ConfigMode;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionConfigurationMode,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // If the Configuration Mode is Custom, set the DeliveryMode, DeliveryMaxItems,
    // HeartbeatInterval, and DeliveryMaxLatencyTime properties.
    if ( sub.ConfigMode == EcConfigurationModeCustom)
    {
        // Set the DeliveryMode property that defines how events are delivered. 
        // Events can be delivered through either a push or pull model.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.DeliveryMode;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMode,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxItems property that specifies the maximum number of 
        // events that can be batched when forwarded from the event sources.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxItems;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxItems,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the HeartbeatInterval property that defines the time interval, in 
        // seconds, that is observed between the heartbeat messages.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.HeartbeatInerval;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionHeartbeatInterval,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxLatencyTime property that specifies how long, in 
        // seconds, the event source should wait before forwarding events.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxLatencyTime;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxLatencyTime,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // Set the ContentFormat property that specifies the format for the event content.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ContentFormat;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionContentFormat,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the CredentialsType property that specifies the type of credentials 
    // used in the event subscription.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.CredentialsType;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionCredentialsType,
        0, 
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Enabled property that is used to enable or disable the subscription
    // or to obtain the current status of a subscription.
    vPropertyValue.Type = EcVarTypeBoolean;
    vPropertyValue.BooleanVal = sub.SubscriptionStatus;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionEnabled,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the user name and password used to connect to the event sources    
    wcout << "Enter credentials used to connect to the event sources. " << endl <<
        "Enter user name: " << endl;
    wcin >> sub.UserName;
    cout << "Enter password: " << endl;

    wchar_t c;
    while( (c = _getwch()) && c != '\n' && c != '\r' && sub.Password.length() < 512)
    {sub.Password.append(1, c);}

    // Set the CommonUserName property that is used by the local and remote 
    // computers to authenticate the user with the source of the events. This 
    // property is used across all the event sources available for this subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.UserName.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionCommonUserName,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the CommonPassword property that is used by the local and remote 
    // computers to authenticate the user with the source of the events.
    // Use Credential Manager Functions to handle Password information.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Password.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionCommonPassword,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }    

    //  When you have finished using the credentials,
    //  erase them from memory.
    sub.UserName.erase();
    sub.Password.erase();


    //----------------------------------------------
    // Add event sources.
    // Ensure that a handle to the event sources array has been obtained.

    //Initialize the Event Sources Array
    dwRetVal = GetProperty( hSubscription, 
        EcSubscriptionEventSources, 
        0, 
        buffer, 
        vEventSource);

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

    // Set the properties of the event source
    // Set the EventSourceAddress property that specifies the address
    // of the event forwarding computer, this property can be localhost 
    // or a fully-qualified domain name.
    vSourceProperty.Type = EcVarTypeString;
    vSourceProperty.StringVal = eventSource.c_str();
    if (!EcSetObjectArrayProperty( hArray,
        EcSubscriptionEventSourceAddress,
        dwEventSourceCount,
        0,
        &vSourceProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }    

    // Set the EventSourceEnabled property that enables the event source
    // to forward events.
    vSourceProperty.Type = EcVarTypeBoolean;
    vSourceProperty.BooleanVal = status;
    if (!EcSetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceEnabled,
        dwEventSourceCount,
        0,
        &vSourceProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    //----------------------------------------------
    // Step 3: Save the subscription.
    // Save the subscription with the associated properties
    // This will create the subscription and store it in the 
    // subscription repository 
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Close the subscription.
Cleanup:
    if(hSubscription)
        EcClose(hSubscription);
    if(hArray)
        EcClose(hArray);

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
            L" Error Message: %s\n", dwRetVal, lpwszBuffer);

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
        &dwBufferSize) )
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
```



<span data-ttu-id="03414-118">**Verificare che la sottoscrizione funzioni correttamente**</span><span class="sxs-lookup"><span data-stu-id="03414-118">**Validate that the subscription works correctly**</span></span>

1.  <span data-ttu-id="03414-119">Sul computer dell'agente di raccolta eventi completare la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="03414-119">On the event collector computer complete the following procedure:</span></span>

    1.  <span data-ttu-id="03414-120">Eseguire il comando seguente da un prompt dei comandi con privilegi elevati per ottenere lo stato di runtime della sottoscrizione:</span><span class="sxs-lookup"><span data-stu-id="03414-120">Run the following command from an elevated privilege command prompt to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="03414-121">\**wecutil gr\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="03414-121">**wecutil gr** *<subscriptionID>*</span></span>

    2.  <span data-ttu-id="03414-122">Verificare che l'origine evento sia connessa.</span><span class="sxs-lookup"><span data-stu-id="03414-122">Verify that the event source has connected.</span></span> <span data-ttu-id="03414-123">Potrebbe essere necessario attendere fino al termine dell'intervallo di aggiornamento specificato nei criteri dopo aver creato la sottoscrizione per la connessione dell'origine evento.</span><span class="sxs-lookup"><span data-stu-id="03414-123">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3.  <span data-ttu-id="03414-124">Eseguire il comando seguente per ottenere le informazioni sulla sottoscrizione:</span><span class="sxs-lookup"><span data-stu-id="03414-124">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="03414-125">\**wecutil gs\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="03414-125">**wecutil gs** *<subscriptionID>*</span></span>

    4.  <span data-ttu-id="03414-126">Ottenere il valore DeliveryMaxItems dalle informazioni sulla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="03414-126">Get the DeliveryMaxItems value from the subscription information.</span></span>

2.  <span data-ttu-id="03414-127">Nel computer di origine evento, generare gli eventi che corrispondono alla query della sottoscrizione di eventi.</span><span class="sxs-lookup"><span data-stu-id="03414-127">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="03414-128">Per l'invio degli eventi è necessario che venga generato il numero DeliveryMaxItems di eventi.</span><span class="sxs-lookup"><span data-stu-id="03414-128">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3.  <span data-ttu-id="03414-129">Sul computer dell'agente di raccolta eventi, verificare che gli eventi siano stati trasmessi al log ForwardedEvents o al log specificato nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="03414-129">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03414-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03414-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="03414-131">[Configurare i computer per l'invio e la raccolta di eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="03414-131">[Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="03414-132">Aggiunta di un'origine evento a una sottoscrizione dell'agente di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="03414-132">Adding an Event Source to an Event Collector Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="03414-133">Informazioni di riferimento sull'agente di raccolta eventi Windows</span><span class="sxs-lookup"><span data-stu-id="03414-133">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 