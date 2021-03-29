---
description: Prima di poter scrivere eventi in una sessione di traccia, è necessario registrare il provider.
ms.assetid: 76e7202e-74ce-40a3-a04b-9af5117fe20e
title: Scrittura di eventi basati su manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a1817defe85e68860d8a628a2d3275034ce285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130079"
---
# <a name="writing-manifest-based-events"></a><span data-ttu-id="9266d-103">Scrittura di eventi basati su manifesto</span><span class="sxs-lookup"><span data-stu-id="9266d-103">Writing Manifest-based Events</span></span>

<span data-ttu-id="9266d-104">Prima di poter scrivere eventi in una sessione di traccia, è necessario registrare il provider.</span><span class="sxs-lookup"><span data-stu-id="9266d-104">Before you can write events to a trace session, you must register your provider.</span></span> <span data-ttu-id="9266d-105">La registrazione di un provider indica a ETW che il provider è pronto per la scrittura di eventi in una sessione di traccia.</span><span class="sxs-lookup"><span data-stu-id="9266d-105">Registering a provider tells ETW that your provider is ready to write events to a trace session.</span></span> <span data-ttu-id="9266d-106">Un processo può registrare fino a 1.024 GUID del provider. Tuttavia, è necessario limitare il numero di provider registrati dal processo a uno o due.</span><span class="sxs-lookup"><span data-stu-id="9266d-106">A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that your process registers to one or two.</span></span>

<span data-ttu-id="9266d-107">**Prima di Windows Vista:** Non esiste alcun limite al numero di provider che possono essere registrati da un processo.</span><span class="sxs-lookup"><span data-stu-id="9266d-107">**Prior to Windows Vista:** There is no limit to the number of providers that a process can register.</span></span>

<span data-ttu-id="9266d-108">Per registrare un provider basato su manifesto, chiamare la funzione [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) .</span><span class="sxs-lookup"><span data-stu-id="9266d-108">To register a manifest-based provider, call the [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) function.</span></span> <span data-ttu-id="9266d-109">La funzione registra il GUID del provider e identifica un callback facoltativo che ETW chiama quando un controller Abilita o Disabilita il provider.</span><span class="sxs-lookup"><span data-stu-id="9266d-109">The function registers the provider's GUID and identifies an optional callback that ETW calls when a controller enables or disables the provider.</span></span>

<span data-ttu-id="9266d-110">Prima della chiusura del provider, chiamare la funzione [**EventUnregister**](/windows/desktop/api/Evntprov/nf-evntprov-eventunregister) per rimuovere la registrazione del provider da ETW.</span><span class="sxs-lookup"><span data-stu-id="9266d-110">Before the provider exits, call the [**EventUnregister**](/windows/desktop/api/Evntprov/nf-evntprov-eventunregister) function to remove the provider's registration from ETW.</span></span> <span data-ttu-id="9266d-111">La funzione [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) restituisce l'handle di registrazione passato alla funzione **EventUnregister** .</span><span class="sxs-lookup"><span data-stu-id="9266d-111">The [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) function returns the registration handle that you pass to the **EventUnregister** function.</span></span>

<span data-ttu-id="9266d-112">I provider [basati su manifesto](about-event-tracing.md) non devono implementare una funzione [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback) per ricevere notifiche quando una sessione Abilita o Disabilita il provider.</span><span class="sxs-lookup"><span data-stu-id="9266d-112">[Manifest-based](about-event-tracing.md) providers do not have to implement an [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback) function to receive notifications when a session enables or disables the provider.</span></span> <span data-ttu-id="9266d-113">Il callback è facoltativo e viene usato a scopo informativo. non è necessario specificare o implementare il callback quando si registra il provider.</span><span class="sxs-lookup"><span data-stu-id="9266d-113">The callback is optional and is used for informational purposes; you do not need to specify or implement the callback when registering the provider.</span></span> <span data-ttu-id="9266d-114">Un provider basato su manifesto può semplicemente scrivere eventi e ETW decide se l'evento viene registrato in una sessione di traccia.</span><span class="sxs-lookup"><span data-stu-id="9266d-114">A manifest-based provider can simply write events and ETW will decide if the event gets logged to a trace session.</span></span> <span data-ttu-id="9266d-115">Se un evento richiede l'esecuzione di un lavoro esteso per generare i dati dell'evento, potrebbe essere necessario chiamare prima la funzione [**EventEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventenabled) o [**EventProviderEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventproviderenabled) per verificare che l'evento venga scritto in una sessione prima di eseguire il lavoro.</span><span class="sxs-lookup"><span data-stu-id="9266d-115">If an event requires that you perform extensive work to generate the event's data, you may want to call the [**EventEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventenabled) or [**EventProviderEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventproviderenabled) function first to verify that the event will be written to a session before performing the work.</span></span>

<span data-ttu-id="9266d-116">In genere, è necessario implementare il callback se il provider richiede che il controller passi i dati del filtro definiti dal provider (vedere il parametro *FilterData* di [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)) al provider oppure il provider usa le informazioni di contesto specificate durante la registrazione (vedere il parametro *CallbackContext* di [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)).</span><span class="sxs-lookup"><span data-stu-id="9266d-116">Typically, you would implement the callback if your provider requires that the controller pass provider-defined filter data (see the *FilterData* parameter of [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)) to the provider, or the provider uses the context information that it specified when it registered itself (see the *CallbackContext* parameter of [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)).</span></span>

<span data-ttu-id="9266d-117">I provider [basati su manifesto](about-event-tracing.md) chiamano la funzione [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) o [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) per scrivere eventi in una sessione.</span><span class="sxs-lookup"><span data-stu-id="9266d-117">[Manifest-based](about-event-tracing.md) providers call the [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) or [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) function to write events to a session.</span></span> <span data-ttu-id="9266d-118">Se i dati dell'evento sono una stringa o se non si definisce un manifesto per il provider e i dati dell'evento sono una singola stringa, chiamare la funzione [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) per scrivere l'evento.</span><span class="sxs-lookup"><span data-stu-id="9266d-118">If your event data is a string, or if you do not define a manifest for your provider and your event data is a single string, call the [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) function to write the event.</span></span> <span data-ttu-id="9266d-119">Per i dati dell'evento che contengono tipi di dati numerici o complessi, chiamare la funzione [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) per registrare l'evento.</span><span class="sxs-lookup"><span data-stu-id="9266d-119">For event data that contains numeric or complex data types, call the [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) function to log the event.</span></span>

<span data-ttu-id="9266d-120">Nell'esempio seguente viene illustrato come preparare i dati dell'evento da scrivere utilizzando la funzione [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) .</span><span class="sxs-lookup"><span data-stu-id="9266d-120">The following example shows how to prepare the event data to be written using the [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) function.</span></span> <span data-ttu-id="9266d-121">L'esempio fa riferimento agli eventi definiti nella [pubblicazione dello schema di eventi per un provider basato su manifesto](publishing-your-event-schema-for-a-manifest-base-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9266d-121">The example references the events defined in [Publishing Your Event Schema for a Manifest-based Provider](publishing-your-event-schema-for-a-manifest-base-provider.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <evntprov.h>
#include "provider.h"  // Generated from manifest

#define SUNDAY     0X1
#define MONDAY     0X2
#define TUESDAY    0X4
#define WEDNESDAY  0X8
#define THURSDAY   0X10
#define FRIDAY     0X20
#define SATURDAY   0X40

enum TRANSFER_TYPE {
  Download = 1,
  Upload,
  UploadReply
};

#define MAX_NAMEDVALUES          5  // Maximum array size
#define MAX_PAYLOAD_DESCRIPTORS  9 + (2 * MAX_NAMEDVALUES)

typedef struct _namedvalue {
  LPWSTR name;
  USHORT value;
} NAMEDVALUE, *PNAMEDVALUE;

void wmain(void)
{
    DWORD status = ERROR_SUCCESS;
    REGHANDLE RegistrationHandle = NULL; 
    EVENT_DATA_DESCRIPTOR Descriptors[MAX_PAYLOAD_DESCRIPTORS]; 
    DWORD i = 0;

    // Data to load into event descriptors

    USHORT Scores[3] = {45, 63, 21};
    ULONG pImage = (ULONG)&Scores;
    DWORD TransferType = Upload;
    DWORD Day = MONDAY | TUESDAY;
    LPWSTR Path = L"c:\\path\\folder\\file.ext";
    BYTE Cert[11] = {0x2, 0x4, 0x8, 0x10, 0x20, 0x30, 0x40, 0x50, 0x60, 0x0, 0x1};
    PBYTE Guid = (PBYTE) &ProviderGuid;
    USHORT ArraySize = MAX_NAMEDVALUES;
    BOOL IsLocal = TRUE;
    NAMEDVALUE NamedValues[MAX_NAMEDVALUES] = { 
        {L"Bill", 1},
        {L"Bob", 2},
        {L"William", 3},
        {L"Robert", 4},
        {L"", 5}
        };

    status = EventRegister(
        &ProviderGuid,      // GUID that identifies the provider
        NULL,               // Callback not used
        NULL,               // Context noot used
        &RegistrationHandle // Used when calling EventWrite and EventUnregister
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"EventRegister failed with %lu\n", status);
        goto cleanup;
    }
  
    // Load the array of data descriptors for the TransferEvent event. 
    // Add the data to the array in the order of the <data> elements
    // defined in the event's template. 
   
    EventDataDescCreate(&Descriptors[i++], &pImage, sizeof(ULONG));
    EventDataDescCreate(&Descriptors[i++], Scores, sizeof(Scores));
    EventDataDescCreate(&Descriptors[i++], Guid, sizeof(GUID));
    EventDataDescCreate(&Descriptors[i++], Cert, sizeof(Cert));
    EventDataDescCreate(&Descriptors[i++], &IsLocal, sizeof(BOOL));
    EventDataDescCreate(&Descriptors[i++], Path, (ULONG)(wcslen(Path) + 1) * sizeof(WCHAR));
    EventDataDescCreate(&Descriptors[i++], &ArraySize, sizeof(USHORT));

    // If your event contains a structure, you should write each member
    // of the structure separately. If the structure contained integral data types
    // such as DWORDs and the data types were aligned on an 8-byte boundary, you 
    // could use the following call to write the structure, however, you are 
    // encouraged to write the members separately.
    //
    // EventDataDescCreate(&EvtData, struct, sizeof(struct));
    //
    // Because the array of structures in this example contains both strings 
    // and numbers, you must write each member of the structure separately.

    for (int j = 0; j < MAX_NAMEDVALUES; j++)
    {
        EventDataDescCreate(&Descriptors[i++], NamedValues[j].name, (ULONG)(wcslen(NamedValues[j].name)+1) * sizeof(WCHAR) );
        EventDataDescCreate(&Descriptors[i++], &(NamedValues[j].value), sizeof(USHORT) );
    }

    EventDataDescCreate(&Descriptors[i++], &Day, sizeof(DWORD));
    EventDataDescCreate(&Descriptors[i++], &TransferType, sizeof(DWORD));

    // Write the event. You do not have to verify if your provider is enabled before
    // writing the event. ETW will write the event to any session that enabled
    // the provider. If no session enabled the provider, the event is not 
    // written. If you need to perform extra work to write an event that you
    // would not otherwise do, you may want to call the EventEnabled function
    // before performing the extra work. The EventEnabled function tells you if a
    // session has enabled your provider, so you know if you need to perform the 
    // extra work or not.

    status = EventWrite(
        RegistrationHandle,              // From EventRegister
        &TransferEvent,                  // EVENT_DESCRIPTOR generated from the manifest
        (ULONG)MAX_PAYLOAD_DESCRIPTORS,  // Size of the array of EVENT_DATA_DESCRIPTORs
        &Descriptors[0]                  // Array of descriptors that contain the event data
        );

    if (status != ERROR_SUCCESS) 
    {
        wprintf(L"EventWrite failed with 0x%x", status);
    }

cleanup:

    EventUnregister(RegistrationHandle);
}
```



<span data-ttu-id="9266d-122">Quando si compila il manifesto (vedere [compilazione di un manifesto di strumentazione](../wes/compiling-an-instrumentation-manifest.md)) usato nell'esempio precedente, viene creato il file di intestazione seguente (a cui si fa riferimento nell'esempio precedente).</span><span class="sxs-lookup"><span data-stu-id="9266d-122">When you compile the manifest (see [Compiling an Instrumentation Manifest](../wes/compiling-an-instrumentation-manifest.md)) that the example above uses, it creates the following header file (referenced in the example above).</span></span>


```C++
//**********************************************************************`
//* This is an include file generated by Message Compiler.             *`
//*                                                                    *`
//* Copyright (c) Microsoft Corporation. All Rights Reserved.          *`
//**********************************************************************`
#pragma once
//+
// Provider Microsoft-Windows-ETWProvider Event Count 1
//+
EXTERN_C __declspec(selectany) const GUID ProviderGuid = {0xd8909c24, 0x5be9, 0x4502, {0x98, 0xca, 0xab, 0x7b, 0xdc, 0x24, 0x89, 0x9d}};
//
// Keyword
//
#define READ_KEYWORD 0x1
#define WRITE_KEYWORD 0x2
#define LOCAL_KEYWORD 0x4
#define REMOTE_KEYWORD 0x8

//
// Event Descriptors
//
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR TransferEvent = {0x1, 0x0, 0x0, 0x4, 0x0, 0x0, 0x5};
#define TransferEvent_value 0x1
#define MSG_Provider_Name                    0x90000001L
#define MSG_Event_WhenToTransfer             0xB0000001L
#define MSG_Map_Download                     0xD0000001L
#define MSG_Map_Upload                       0xD0000002L
#define MSG_Map_UploadReply                  0xD0000003L
#define MSG_Map_Sunday                       0xF0000001L
#define MSG_Map_Monday                       0xF0000002L
#define MSG_Map_Tuesday                      0xF0000003L
#define MSG_Map_Wednesday                    0xF0000004L
#define MSG_Map_Thursday                     0xF0000005L
#define MSG_Map_Friday                       0xF0000006L
#define MSG_Map_Saturday                     0xF0000007L
```



 

 
