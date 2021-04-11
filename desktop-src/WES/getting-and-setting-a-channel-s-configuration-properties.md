---
title: Recupero e impostazione delle proprietà di configurazione di un canale
description: Un canale viene inizialmente configurato nel manifesto (vedere Definizione dei canali). Per ottenere le proprietà configurabili di un canale, chiamare la funzione EvtOpenChannelConfig per ottenere un handle per il canale.
ms.assetid: 4ee44dae-b390-4d98-bcef-836b53b04860
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b28e96e45a8b061fac2914b2ef79847cf25a6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044506"
---
# <a name="getting-and-setting-a-channels-configuration-properties"></a><span data-ttu-id="03ee8-104">Recupero e impostazione delle proprietà di configurazione di un canale</span><span class="sxs-lookup"><span data-stu-id="03ee8-104">Getting and Setting a Channel's Configuration Properties</span></span>

<span data-ttu-id="03ee8-105">Un canale viene inizialmente configurato nel manifesto (vedere [definizione dei canali](defining-channels.md)).</span><span class="sxs-lookup"><span data-stu-id="03ee8-105">A channel is initially configured in the manifest (see [Defining Channels](defining-channels.md)).</span></span> <span data-ttu-id="03ee8-106">Per ottenere le proprietà configurabili di un canale, chiamare la funzione [**EvtOpenChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtopenchannelconfig) per ottenere un handle per il canale.</span><span class="sxs-lookup"><span data-stu-id="03ee8-106">To get the configurable properties of a channel, call the [**EvtOpenChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtopenchannelconfig) function to get a handle to the channel.</span></span> <span data-ttu-id="03ee8-107">Chiamare quindi la funzione [**EvtGetChannelConfigProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtgetchannelconfigproperty) per ottenere il valore di una proprietà configurabile del canale.</span><span class="sxs-lookup"><span data-stu-id="03ee8-107">Then, call the [**EvtGetChannelConfigProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtgetchannelconfigproperty) function to get the value of a configurable property of the channel.</span></span> <span data-ttu-id="03ee8-108">Per un elenco di proprietà configurabili, vedere l'enumerazione dell' [**ID della proprietà di \_ configurazione del canale \_ \_ \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id) .</span><span class="sxs-lookup"><span data-stu-id="03ee8-108">For a list of configurable properties, see the [**EVT\_CHANNEL\_CONFIG\_PROPERTY\_ID**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id) enumeration.</span></span> <span data-ttu-id="03ee8-109">Il nome, il valore e le proprietà della stringa del messaggio del canale sono considerati metadati e non possono essere recuperati tramite la funzione **EvtGetChannelConfigProperty** .</span><span class="sxs-lookup"><span data-stu-id="03ee8-109">The channel's name, value, and message string properties are considered metadata and cannot be retrieved using the **EvtGetChannelConfigProperty** function.</span></span> <span data-ttu-id="03ee8-110">Per informazioni dettagliate su come ottenere queste proprietà, vedere [recupero dei metadati di un provider](getting-a-provider-s-metadata-.md).</span><span class="sxs-lookup"><span data-stu-id="03ee8-110">For details on getting these properties, see [Getting a Provider's Metadata](getting-a-provider-s-metadata-.md).</span></span>

<span data-ttu-id="03ee8-111">È possibile configurare molte delle proprietà del canale in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="03ee8-111">You can configure many of the channel's properties at run time.</span></span> <span data-ttu-id="03ee8-112">L'enumerazione dell' [**ID della proprietà di \_ configurazione del canale \_ \_ \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id) identifica le proprietà che non è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="03ee8-112">The [**EVT\_CHANNEL\_CONFIG\_PROPERTY\_ID**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id) enumeration identifies those properties that you cannot set.</span></span> <span data-ttu-id="03ee8-113">Per configurare le proprietà del canale, l'utente deve appartenere al gruppo Administrators ed essere in esecuzione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="03ee8-113">To configure channel properties, the user must be in the administrators group and be running with elevated privileges.</span></span> <span data-ttu-id="03ee8-114">Per impostare le proprietà configurabili di un canale, chiamare la funzione [**EvtOpenChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtopenchannelconfig) per ottenere un handle per il canale.</span><span class="sxs-lookup"><span data-stu-id="03ee8-114">To set the configurable properties of a channel, call the [**EvtOpenChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtopenchannelconfig) function to get a handle to the channel.</span></span> <span data-ttu-id="03ee8-115">Chiamare quindi la funzione [**EvtSetChannelConfigProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtsetchannelconfigproperty) per impostare il valore di una proprietà configurabile.</span><span class="sxs-lookup"><span data-stu-id="03ee8-115">Then, call the [**EvtSetChannelConfigProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtsetchannelconfigproperty) function to set the value of a configurable property.</span></span> <span data-ttu-id="03ee8-116">Dopo aver impostato le proprietà configurabili, chiamare la funzione [**EvtSaveChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtsavechannelconfig) per salvare e applicare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="03ee8-116">After setting the configurable properties, call the [**EvtSaveChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtsavechannelconfig) function to save and apply the changes.</span></span>

<span data-ttu-id="03ee8-117">Vedere le sezioni seguenti per esempi che illustrano come ottenere e impostare le proprietà del canale:</span><span class="sxs-lookup"><span data-stu-id="03ee8-117">See the following sections for examples that show how to get and set channel properties:</span></span>

-   [<span data-ttu-id="03ee8-118">Enumerazione dei canali</span><span class="sxs-lookup"><span data-stu-id="03ee8-118">Enumerating channels</span></span>](#enumerating-channels)
-   [<span data-ttu-id="03ee8-119">Recupero delle proprietà del canale</span><span class="sxs-lookup"><span data-stu-id="03ee8-119">Getting channel properties</span></span>](#getting-and-setting-a-channels-configuration-properties)
-   [<span data-ttu-id="03ee8-120">Impostazione delle proprietà del canale</span><span class="sxs-lookup"><span data-stu-id="03ee8-120">Setting channel properties</span></span>](#getting-and-setting-a-channels-configuration-properties)

## <a name="enumerating-channels"></a><span data-ttu-id="03ee8-121">Enumerazione dei canali</span><span class="sxs-lookup"><span data-stu-id="03ee8-121">Enumerating channels</span></span>

<span data-ttu-id="03ee8-122">Nell'esempio seguente viene illustrato come enumerare i canali registrati nel computer.</span><span class="sxs-lookup"><span data-stu-id="03ee8-122">The following example shows how to enumerate the channels that are registered on the computer.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")


void main(void)
{
    EVT_HANDLE hChannels = NULL;
    LPWSTR pBuffer = NULL;
    LPWSTR pTemp = NULL;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    // Get a handle to an enumerator that contains all the names of the 
    // channels registered on the computer.
    hChannels = EvtOpenChannelEnum(NULL, 0);

    if (NULL == hChannels)
    {
        wprintf(L"EvtOpenChannelEnum failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"List of Channels\n\n");

    // Enumerate through the list of channel names. If the buffer is not big
    // enough reallocate the buffer. To get the configuration information for
    // a channel, call the EvtOpenChannelConfig function.
    while (true)
    {
        if (!EvtNextChannelPath(hChannels, dwBufferSize, pBuffer, &dwBufferUsed))
        {
            status = GetLastError();

            if (ERROR_NO_MORE_ITEMS == status)
            {
                break;
            }
            else if (ERROR_INSUFFICIENT_BUFFER == status)
            {
                dwBufferSize = dwBufferUsed;
                pTemp = (LPWSTR)realloc(pBuffer, dwBufferSize * sizeof(WCHAR));
                if (pTemp)
                {
                    pBuffer = pTemp;
                    pTemp = NULL;
                    EvtNextChannelPath(hChannels, dwBufferSize, pBuffer, &dwBufferUsed);
                }
                else
                {
                    wprintf(L"realloc failed\n");
                    status = ERROR_OUTOFMEMORY;
                    goto cleanup;
                }
            }
            else
            {
                wprintf(L"EvtNextChannelPath failed with %lu.\n", status);
            }
        }

        wprintf(L"%s\n", pBuffer);
    }

cleanup:

    if (hChannels)
        EvtClose(hChannels);

    if (pBuffer)
        free(pBuffer);
}
```



## <a name="getting-channel-properties"></a><span data-ttu-id="03ee8-123">Recupero delle proprietà del canale</span><span class="sxs-lookup"><span data-stu-id="03ee8-123">Getting channel properties</span></span>

<span data-ttu-id="03ee8-124">Nell'esempio seguente viene illustrato come ottenere le proprietà configurabili di un canale.</span><span class="sxs-lookup"><span data-stu-id="03ee8-124">The following example shows how to get the configurable properties of a channel.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")
#pragma comment(lib, "ole32.lib")

LPWSTR pwcsChannelTypes[] = {L"Admin", L"Operational", L"Analytic", L"Debug"};
LPWSTR pwcsIsolationTypes[] = {L"Application", L"System", L"Custom"};
LPWSTR pwcsClockTypes[] = {L"System", L"QPC"};

DWORD PrintChannelProperties(EVT_HANDLE hChannel);
DWORD PrintChannelProperty(int Id, PEVT_VARIANT pProperty);

void main(void)
{
    EVT_HANDLE hChannel = NULL;
    DWORD status = ERROR_SUCCESS;
    LPWSTR pwsChannelName = L"<name of channel goes here>";

    hChannel = EvtOpenChannelConfig(NULL, pwsChannelName, 0);

    if (NULL == hChannel) // Fails with 15007 (ERROR_EVT_CHANNEL_NOT_FOUND) if the channel is not found
    {
        wprintf(L"EvtOpenChannelConfig failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    status = PrintChannelProperties(hChannel);

cleanup:

    if (hChannel)
        EvtClose(hChannel);
}

// Print the channel's configuration properties. Use the EVT_CHANNEL_CONFIG_PROPERTY_ID
// enumeration values to loop through all the properties.
DWORD PrintChannelProperties(EVT_HANDLE hChannel)
{
    PEVT_VARIANT pProperty = NULL;  // Buffer that receives the property value
    PEVT_VARIANT pTemp = NULL;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    for (int Id = 0; Id < EvtChannelConfigPropertyIdEND; Id++)
    {
        // Get the specified property. If the buffer is too small, reallocate it.
        if  (!EvtGetChannelConfigProperty(hChannel, (EVT_CHANNEL_CONFIG_PROPERTY_ID)Id, 0, dwBufferSize, pProperty, &dwBufferUsed))
        {
            status = GetLastError();
            if (ERROR_INSUFFICIENT_BUFFER == status)
            {
                dwBufferSize = dwBufferUsed;
                pTemp = (PEVT_VARIANT)realloc(pProperty, dwBufferSize);
                if (pTemp)
                {
                    pProperty = pTemp;
                    pTemp = NULL;
                    EvtGetChannelConfigProperty(hChannel, (EVT_CHANNEL_CONFIG_PROPERTY_ID)Id, 0, dwBufferSize, pProperty, &dwBufferUsed);
                }
                else
                {
                    wprintf(L"realloc failed\n");
                    status = ERROR_OUTOFMEMORY;
                    goto cleanup;
                }
            }

            if (ERROR_SUCCESS != (status = GetLastError()))
            {
                wprintf(L"EvtGetChannelConfigProperty failed with %d\n", GetLastError());
                goto cleanup;
            }
        }

        if (status = PrintChannelProperty(Id, pProperty))
            break;
    }

cleanup:

    if (pProperty)
        free(pProperty);

    return status;
}

// Print the property value.
DWORD PrintChannelProperty(int Id, PEVT_VARIANT pProperty)
{
    DWORD status = ERROR_SUCCESS;
    WCHAR wszSessionGuid[50];
    LPWSTR lpws = NULL;

    switch(Id)
    {
        case EvtChannelConfigEnabled:
            wprintf(L"Enabled: %s\n", (TRUE == pProperty->BooleanVal) ? L"TRUE" : L"FALSE");
            break;

        case EvtChannelConfigIsolation:
            wprintf(L"Isolation: %s\n", pwcsIsolationTypes[pProperty->UInt32Val]);
            break;

        case EvtChannelConfigType:
            wprintf(L"Type: %s\n", pwcsChannelTypes[pProperty->UInt32Val]);
            break;

        // This will contain a value if the channel is imported.
        case EvtChannelConfigOwningPublisher:
            wprintf(L"Publisher that defined the channel: %s\n", pProperty->StringVal);
            break;

        case EvtChannelConfigClassicEventlog:
            wprintf(L"ClassicEventlog: %s\n", (TRUE == pProperty->BooleanVal) ? L"TRUE" : L"FALSE");
            break;

        case EvtChannelConfigAccess:
            wprintf(L"Access: %s\n", pProperty->StringVal);
            break;

        case EvtChannelLoggingConfigRetention:
            wprintf(L"Retention: %s\n", (TRUE == pProperty->BooleanVal) ? L"TRUE (Sequential)" : L"FALSE (Circular)");
            break;

        case EvtChannelLoggingConfigAutoBackup:
            wprintf(L"AutoBackup: %s\n", (TRUE == pProperty->BooleanVal) ? L"TRUE" : L"FALSE"); 
            break;

        case EvtChannelLoggingConfigMaxSize:
            wprintf(L"MaxSize: %I64u MB\n", pProperty->UInt64Val / (1024*1024));
            break;

        case EvtChannelLoggingConfigLogFilePath:
            wprintf(L"LogFilePath: %s\n", pProperty->StringVal);
            break;

        case EvtChannelPublishingConfigLevel:
            if (EvtVarTypeNull == pProperty->Type)
                wprintf(L"Level: \n");
            else
                wprintf(L"Level: %lu\n", pProperty->UInt32Val);

            break;

        // The upper 8 bits can contain reserved bit values, so do not include them
        // when checking to see if any keywords are set.
        case EvtChannelPublishingConfigKeywords:
            if (EvtVarTypeNull == pProperty->Type)
                wprintf(L"Keywords: \n");
            else
                wprintf(L"Keywords: %I64u\n", pProperty->UInt64Val & 0x00FFFFFFFFFFFFFF);

            break;

        case EvtChannelPublishingConfigControlGuid:
            if (EvtVarTypeNull == pProperty->Type)
                wprintf(L"ControlGuid: \n");
            else
            {
                StringFromGUID2(*(pProperty->GuidVal), wszSessionGuid, sizeof(wszSessionGuid)/sizeof(WCHAR));
                wprintf(L"ControlGuid: %s\n", wszSessionGuid);
            }

            break;

        case EvtChannelPublishingConfigBufferSize:
            wprintf(L"BufferSize: %lu KB\n", pProperty->UInt32Val);
            break;

        case EvtChannelPublishingConfigMinBuffers:
            wprintf(L"MinBuffers: %lu\n", pProperty->UInt32Val);
            break;

        case EvtChannelPublishingConfigMaxBuffers:
            wprintf(L"MaxBuffers: %lu\n", pProperty->UInt32Val);
            break;

        case EvtChannelPublishingConfigLatency:
            wprintf(L"Latency: %lu (sec)\n", pProperty->UInt32Val / 1000); // 1 ms
            break;

        case EvtChannelPublishingConfigClockType:
            wprintf(L"ClockType: %s\n", pwcsClockTypes[pProperty->UInt32Val]);
            break;

        case EvtChannelPublishingConfigSidType:
            wprintf(L"Include security ID (SID): %s\n", (EvtChannelSidTypeNone == pProperty->UInt32Val) ? L"No" : L"Yes");
            break;

        case EvtChannelPublisherList:

            wprintf(L"List of providers that import this channel: \n");
            for (DWORD i = 0; i < pProperty->Count; i++)
            {
                wprintf(L"  %s\n", pProperty->StringArr[i]);
            }

            break;

        case EvtChannelPublishingConfigFileMax:
            wprintf(L"FileMax: %lu\n", pProperty->UInt32Val);
            break;

        default:
            wprintf(L"Unknown property Id: %d\n", Id);
    }
    
    return status;
}
```



## <a name="setting-channel-properties"></a><span data-ttu-id="03ee8-125">Impostazione delle proprietà del canale</span><span class="sxs-lookup"><span data-stu-id="03ee8-125">Setting channel properties</span></span>

<span data-ttu-id="03ee8-126">Nell'esempio seguente viene illustrato come impostare le proprietà configurabili di un canale.</span><span class="sxs-lookup"><span data-stu-id="03ee8-126">The following example shows how to set the configurable properties of a channel.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>
#include <winmeta.h>

// For this example, including the keywords that were defined in the header file 
// that the message compiler generated for the manifest.
//
// Keywords
//
#define READ_KEYWORD 0x10
#define WRITE_KEYWORD 0x20
// #include "myprovider.h"  // Contains the keywords defined for my provider

#pragma comment(lib, "wevtapi.lib")

void main(void)
{
    EVT_HANDLE hChannel = NULL;
    DWORD status = ERROR_SUCCESS;
    EVT_VARIANT ChannelProperty;
    DWORD dwBufferSize = sizeof(EVT_VARIANT);
    DWORD dwBufferUsed = 0;

    hChannel = EvtOpenChannelConfig(NULL, L"<name of channel goes here>", 0);
    if (NULL == hChannel)
    {
        wprintf(L"EvtOpenChannelConfig failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    RtlZeroMemory(&ChannelProperty, dwBufferSize);
    ChannelProperty.Type = EvtVarTypeBoolean;
    ChannelProperty.BooleanVal = FALSE;
    if  (!EvtSetChannelConfigProperty(hChannel, EvtChannelConfigEnabled, 0, &ChannelProperty))
    {
        wprintf(L"EvtSetChannelConfigProperty for Enabled property failed with %lu\n", GetLastError());
        goto cleanup;
    }

    RtlZeroMemory(&ChannelProperty, dwBufferSize);
    ChannelProperty.Type = EvtVarTypeUInt32;
    ChannelProperty.UInt32Val = WINEVENT_LEVEL_WARNING;  // Found in winmeta.h
    if  (!EvtSetChannelConfigProperty(hChannel, EvtChannelPublishingConfigLevel, 0, &ChannelProperty))
    {
        wprintf(L"EvtSetChannelConfigProperty for Level failed with %lu\n", GetLastError());
        goto cleanup;
    }

    RtlZeroMemory(&ChannelProperty, dwBufferSize);
    ChannelProperty.Type = EvtVarTypeUInt64;
    ChannelProperty.UInt64Val = READ_KEYWORD | WRITE_KEYWORD;
    if  (!EvtSetChannelConfigProperty(hChannel, EvtChannelPublishingConfigKeywords, 0, &ChannelProperty))
    {
        wprintf(L"EvtSetChannelConfigProperty for Keywords failed with %lu\n", GetLastError());
        goto cleanup;
    }

    RtlZeroMemory(&ChannelProperty, dwBufferSize);
    ChannelProperty.Type = EvtVarTypeBoolean;
    ChannelProperty.BooleanVal = TRUE;
    if  (!EvtSetChannelConfigProperty(hChannel, EvtChannelConfigEnabled, 0, &ChannelProperty))
    {
        wprintf(L"EvtSetChannelConfigProperty for Enabled property failed with %lu\n", GetLastError());
        goto cleanup;
    }

    // The user needs to be in the administrators group and be running with
    // elevated permissions for this call to work.
    if (!EvtSaveChannelConfig(hChannel, 0))
    {
        wprintf(L"EvtSaveChannelConfig failed with %lu\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"Channel properties updated.\n");

cleanup:

    if (hChannel)
        EvtClose(hChannel);
}
```



 

 




