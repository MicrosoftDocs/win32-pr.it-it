---
description: Prima di poter scrivere eventi in una sessione di traccia, è necessario registrare il provider.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Scrittura di eventi MOF (classico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3d041e2792540d4a05637bcffdb67e1164a95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980906"
---
# <a name="writing-mof-classic-events"></a><span data-ttu-id="40582-103">Scrittura di eventi MOF (classico)</span><span class="sxs-lookup"><span data-stu-id="40582-103">Writing MOF (Classic) Events</span></span>

<span data-ttu-id="40582-104">Prima di poter scrivere eventi in una sessione di traccia, è necessario registrare il provider.</span><span class="sxs-lookup"><span data-stu-id="40582-104">Before you can write events to a trace session, you must register your provider.</span></span> <span data-ttu-id="40582-105">La registrazione di un provider indica a ETW che il provider è pronto per la scrittura di eventi in una sessione di traccia.</span><span class="sxs-lookup"><span data-stu-id="40582-105">Registering a provider tells ETW that your provider is ready to write events to a trace session.</span></span> <span data-ttu-id="40582-106">Un processo può registrare fino a 1.024 GUID del provider. Tuttavia, è necessario limitare il numero di provider registrati dal processo a uno o due.</span><span class="sxs-lookup"><span data-stu-id="40582-106">A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that your process registers to one or two.</span></span>

<span data-ttu-id="40582-107">**Prima di Windows Vista:** Non esiste alcun limite al numero di provider che possono essere registrati da un processo.</span><span class="sxs-lookup"><span data-stu-id="40582-107">**Prior to Windows Vista:** There is no limit to the number of providers that a process can register.</span></span>

<span data-ttu-id="40582-108">Per registrare un provider classico, chiamare la funzione [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="40582-108">To register a classic provider, call the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="40582-109">La funzione registra il GUID del provider, i GUID della classe di traccia eventi e identifica il callback che ETW chiama quando un controller Abilita o Disabilita il provider.</span><span class="sxs-lookup"><span data-stu-id="40582-109">The function registers the provider's GUID, event trace class GUIDs, and identifies the callback that ETW calls when a controller enables or disables the provider.</span></span>

<span data-ttu-id="40582-110">Se il provider chiama la funzione [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) per registrare gli eventi, non è necessario includere la matrice di GUID di classe (può essere **null**) quando si chiama la funzione [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="40582-110">If the provider calls the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events, you do not need to include the array of class GUIDs (can be **NULL**) when calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="40582-111">È sufficiente includere la matrice se il provider chiama la funzione [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="40582-111">You only need to include the array if the provider calls the [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) function to log events.</span></span>

<span data-ttu-id="40582-112">**Windows XP e windows 2000:** È sempre necessario includere la matrice di GUID di classe (non può essere **null**).</span><span class="sxs-lookup"><span data-stu-id="40582-112">**Windows XP and Windows 2000:** You always need to include the array of class GUIDs (cannot be **NULL**).</span></span>

<span data-ttu-id="40582-113">Dopo che un provider si è registrato e viene abilitato dal controller, il provider può registrare gli eventi nella sessione di traccia del controller.</span><span class="sxs-lookup"><span data-stu-id="40582-113">After a provider registers itself and is enabled by the controller, the provider can log events to the controller's trace session.</span></span>

<span data-ttu-id="40582-114">Prima della chiusura del provider, chiamare la funzione [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) per rimuovere la registrazione del provider da ETW.</span><span class="sxs-lookup"><span data-stu-id="40582-114">Before the provider exits, call the [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) function to remove the provider's registration from ETW.</span></span> <span data-ttu-id="40582-115">La funzione [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) restituisce l'handle di registrazione passato alla funzione **UnregisterTraceGuids** .</span><span class="sxs-lookup"><span data-stu-id="40582-115">The [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function returns the registration handle that you pass to the **UnregisterTraceGuids** function.</span></span>

<span data-ttu-id="40582-116">Se il provider registra gli eventi solo nella sessione globale del logger, non è necessario registrare il provider con ETW perché il controller globale del logger non Abilita o Disabilita i provider.</span><span class="sxs-lookup"><span data-stu-id="40582-116">If your provider logs events to the Global Logger session only, you do not have to register your provider with ETW because the Global Logger controller does not enable or disable providers.</span></span> <span data-ttu-id="40582-117">Per informazioni dettagliate, vedere [configurazione e avvio della sessione Global Logger](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="40582-117">For details, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="40582-118">Tutti i provider [classici](about-event-tracing.md) (ad eccezione di quelli che tracciano gli eventi nella sessione Global Logger) devono implementare la funzione [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) .</span><span class="sxs-lookup"><span data-stu-id="40582-118">All [classic](about-event-tracing.md) providers (except those that trace events to the Global Logger session) must implement the [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) function.</span></span> <span data-ttu-id="40582-119">Il provider utilizza le informazioni nel callback per determinare se è abilitato o disabilitato e quali eventi devono essere scritti.</span><span class="sxs-lookup"><span data-stu-id="40582-119">The provider uses the information in the callback to determine if it is enabled or disabled and which events it should write.</span></span>

<span data-ttu-id="40582-120">Il provider specifica il nome della funzione di callback quando chiama la funzione [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="40582-120">The provider specifies the name of the callback function when it calls the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register itself.</span></span> <span data-ttu-id="40582-121">ETW chiama la funzione di callback quando il controller chiama la funzione [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per abilitare o disabilitare il provider.</span><span class="sxs-lookup"><span data-stu-id="40582-121">ETW calls the callback function when the controller calls the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable or disable the provider.</span></span>

<span data-ttu-id="40582-122">Nell'implementazione di [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) è necessario chiamare la funzione [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) per recuperare l'handle di sessione. usare l'handle di sessione quando si chiama la funzione [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) .</span><span class="sxs-lookup"><span data-stu-id="40582-122">In your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation, you must call the [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) function to retrieve the session handle; you use the session handle when calling the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="40582-123">È sufficiente chiamare la funzione [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) o la funzione [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) nell'implementazione di **ControlCallback** se il provider usa i flag enable level o Enable.</span><span class="sxs-lookup"><span data-stu-id="40582-123">You only need to call the [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) function or the [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) function in your **ControlCallback** implementation if your provider uses the enable level or enable flags.</span></span>

<span data-ttu-id="40582-124">Un provider può registrare gli eventi di traccia in una sola sessione, ma non è necessario impedire a più controller di abilitare un singolo provider.</span><span class="sxs-lookup"><span data-stu-id="40582-124">A provider can log trace events to only one session, but there is nothing to prevent multiple controllers from enabling a single provider.</span></span> <span data-ttu-id="40582-125">Per impedire a un altro controller di reindirizzare gli eventi di traccia alla relativa sessione, è possibile aggiungere la logica all'implementazione di [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) per confrontare gli handle di sessione e ignorare le richieste di abilitazione da altri controller.</span><span class="sxs-lookup"><span data-stu-id="40582-125">To prevent another controller from redirecting your trace events to its session, you may want to add logic to your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation to compare session handles and ignore enable requests from other controllers.</span></span>

<span data-ttu-id="40582-126">Per registrare gli eventi, i provider [classici](about-event-tracing.md) chiamano la funzione [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) .</span><span class="sxs-lookup"><span data-stu-id="40582-126">To log events, [classic](about-event-tracing.md) providers call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="40582-127">Un evento è costituito dalla struttura dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e da tutti i dati specifici degli eventi aggiunti all'intestazione.</span><span class="sxs-lookup"><span data-stu-id="40582-127">An event consists of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and any event-specific data that is appended to the header.</span></span>

<span data-ttu-id="40582-128">L'intestazione deve contenere le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="40582-128">The header must contain the following information:</span></span>

-   <span data-ttu-id="40582-129">Il membro **size** deve contenere il numero totale di byte da registrare per l'evento (incluse le dimensioni della struttura dell' [**\_ \_ intestazione di traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e di tutti i dati specifici degli eventi aggiunti all'intestazione).</span><span class="sxs-lookup"><span data-stu-id="40582-129">The **Size** member must contain the total number of bytes to be recorded for the event (including the size of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and of any event-specific data that is appended to the header).</span></span>
-   <span data-ttu-id="40582-130">Il membro **GUID** deve contenere il GUID della classe dell'evento (oppure il membro **GuidPtr** deve contenere un puntatore al GUID della classe).</span><span class="sxs-lookup"><span data-stu-id="40582-130">The **Guid** member must contain the class GUID of the event (or the **GuidPtr** member must contain a pointer to the class GUID).</span></span>

    <span data-ttu-id="40582-131">**Windows XP e windows 2000:** Il GUID della classe deve essere stato registrato in precedenza tramite la funzione [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="40582-131">**Windows XP and Windows 2000:** The class GUID must have been registered previously using the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span>

-   <span data-ttu-id="40582-132">Il membro **Flags** deve contenere il flag **\_ \_ \_ GUID tracciato del flag WNODE** .</span><span class="sxs-lookup"><span data-stu-id="40582-132">The **Flags** member must contain the **WNODE\_FLAG\_TRACED\_GUID** flag.</span></span> <span data-ttu-id="40582-133">Se si specifica il GUID della classe usando il membro **GuidPtr** , aggiungere anche il flag **WNODE \_ \_ use \_ GUID \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="40582-133">If you specify the class GUID using the **GuidPtr** member, also add the **WNODE\_FLAG\_USE\_GUID\_PTR** flag.</span></span>
-   <span data-ttu-id="40582-134">Il membro **Class. Type** deve contenere il tipo di evento, se si usa MOF per pubblicare il layout dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="40582-134">The **Class.Type** member must contain the event type, if you use MOF to publish the layout of your event data.</span></span>
-   <span data-ttu-id="40582-135">Il membro **Class. Version** deve contenere la versione dell'evento, se si usa MOF per pubblicare il layout dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="40582-135">The **Class.Version** member must contain the event version, if you use MOF to publish the layout of your event data.</span></span> <span data-ttu-id="40582-136">La versione viene utilizzata per distinguere tra le revisioni e i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="40582-136">The version is used to distinguish between revisions to the event data.</span></span> <span data-ttu-id="40582-137">Impostare il numero di versione iniziale su 0.</span><span class="sxs-lookup"><span data-stu-id="40582-137">Set the initial version number to 0.</span></span>

<span data-ttu-id="40582-138">Se si scrivono sia il provider che il consumer, è possibile usare una struttura per popolare i dati specifici dell'evento aggiunti all'intestazione.</span><span class="sxs-lookup"><span data-stu-id="40582-138">If you write both the provider and the consumer, you can use a structure to populate the event-specific data that is appended to the header.</span></span> <span data-ttu-id="40582-139">Tuttavia, se si utilizza MOF per pubblicare i dati specifici dell'evento in modo che qualsiasi consumer possa elaborare l'evento, è consigliabile non utilizzare una struttura per aggiungere i dati specifici dell'evento all'intestazione.</span><span class="sxs-lookup"><span data-stu-id="40582-139">However, if you use MOF to publish the event-specific data so that any consumer can process the event, you should not use a structure to append the event-specific data to the header.</span></span> <span data-ttu-id="40582-140">Questo perché il compilatore può aggiungere byte aggiuntivi ai dati specifici dell'evento per scopi di allineamento dei byte.</span><span class="sxs-lookup"><span data-stu-id="40582-140">This is because the compiler may add extra bytes to the event-specific data for byte alignment purposes.</span></span> <span data-ttu-id="40582-141">Poiché la definizione MOF non tiene conto dei byte aggiuntivi, il consumer può recuperare dati non validi.</span><span class="sxs-lookup"><span data-stu-id="40582-141">Because the MOF definition does not account for the extra bytes, the consumer may retrieve data that is not valid.</span></span>

<span data-ttu-id="40582-142">È necessario allocare un blocco di memoria per l'evento e copiare ogni elemento di dati evento nella memoria oppure creare una struttura che includa una matrice di strutture di [**\_ campo MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) . la maggior parte delle applicazioni creerà una struttura che include una matrice di strutture di **\_ campi MOF** .</span><span class="sxs-lookup"><span data-stu-id="40582-142">You should either allocate a block of memory for the event and copy each event data item to the memory, or create a structure that includes an array of [**MOF\_FIELD**](/windows/win32/api/evntrace/ns-evntrace-mof_field) structures; most applications will create a structure that includes an array of **MOF\_FIELD** structures.</span></span> <span data-ttu-id="40582-143">Verificare che **header. Size** rifletta il numero effettivo di strutture di **\_ campo MOF** effettivamente impostate prima di registrare l'evento.</span><span class="sxs-lookup"><span data-stu-id="40582-143">Make sure that **Header.Size** reflects the actual number of **MOF\_FIELD** structures that are actually set before logging the event.</span></span> <span data-ttu-id="40582-144">Se, ad esempio, l'evento contiene tre campi dati, impostare **header. Size** su sizeof ( \_ intestazione della traccia eventi \_ ) + (sizeof ( \_ campo MOF) \* 3).</span><span class="sxs-lookup"><span data-stu-id="40582-144">For example, if the event contains three data fields, set **Header.Size** to sizeof(EVENT\_TRACE\_HEADER) + (sizeof(MOF\_FIELD) \* 3).</span></span>

<span data-ttu-id="40582-145">Per informazioni sulla traccia degli eventi correlati, vedere [scrittura di eventi correlati in uno scenario end-to-end](writing-related-events-in-an-end-to-end-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="40582-145">For information on tracing related events, see [Writing Related Events in an End-to-End Scenario](writing-related-events-in-an-end-to-end-scenario.md).</span></span>

<span data-ttu-id="40582-146">Nell'esempio seguente viene illustrato come chiamare la funzione [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="40582-146">The following example shows how to call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events.</span></span> <span data-ttu-id="40582-147">L'esempio fa riferimento agli eventi definiti nella [pubblicazione dello schema di eventi per un provider classico](publishing-your-event-schema-for-a-classic-provider.md).</span><span class="sxs-lookup"><span data-stu-id="40582-147">The example references the events defined in [Publishing Your Event Schema for a Classic Provider](publishing-your-event-schema-for-a-classic-provider.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

// GUID that identifies the category of events that the provider can log. 
// The GUID is also used in the event MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {B49D5931-AD85-4070-B1B1-3F81F1532875}
static const GUID MyCategoryGuid = 
{ 0xb49d5931, 0xad85, 0x4070, { 0xb1, 0xb1, 0x3f, 0x81, 0xf1, 0x53, 0x28, 0x75 } };

// GUID that identifies the provider that you are registering.
// The GUID is also used in the provider MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };

// Identifies the event type within the MyCategoryGuid category 
// of events to be logged. This is the same value as the EventType 
// qualifier that is defined in the event type MOF class for one of 
// the MyCategoryGuid category of events.

#define MY_EVENT_TYPE 1

// Event passed to TraceEvent

typedef struct _event
{
    EVENT_TRACE_HEADER Header;
    MOF_FIELD Data[MAX_MOF_FIELDS];  // Event-specific data
} MY_EVENT, *PMY_EVENT;

#define MAX_INDICES            3
#define MAX_SIGNATURE_LEN      32
#define EVENT_DATA_FIELDS_CNT  6

// Application data to be traced for Version 1 of the MOF class.

typedef struct _evtdata
{
    LONG Cost;
    DWORD Indices[MAX_INDICES];
    WCHAR Signature[MAX_SIGNATURE_LEN];
    BOOL IsComplete;
    GUID ID;
    DWORD Size;
}EVENT_DATA, *PEVENT_DATA;

// GUID used as the value for EVENT_DATA.ID.

// {25BAEDA9-C81A-4889-8764-184FE56750F2}
static const GUID tempID = 
{ 0x25baeda9, 0xc81a, 0x4889, { 0x87, 0x64, 0x18, 0x4f, 0xe5, 0x67, 0x50, 0xf2 } };

// Global variables to store tracing state information.

TRACEHANDLE g_SessionHandle = 0; // The handle to the session that enabled the provider.
ULONG g_EnableFlags = 0; // Determines which class of events to log.
UCHAR g_EnableLevel = 0; // Determines the severity of events to log.
BOOL g_TraceOn = FALSE;  // Used by the provider to determine whether it should log events.

ULONG WINAPI ControlCallback(WMIDPREQUESTCODE RequestCode, PVOID Context, ULONG* Reserved, PVOID Header);

// For this example to log the event, run the session example
// to enable the provider before running this example.

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_DATA EventData;
    MY_EVENT MyEvent; 
    TRACEHANDLE RegistrationHandle = 0; 
    TRACE_GUID_REGISTRATION EventClassGuids[] = {
        (LPGUID)&MyCategoryGuid, NULL
        };

    // Register the provider and specify the control callback function
    // that receives the enable/disable notifications.

    status = RegisterTraceGuids(
        (WMIDPREQUEST)ControlCallback,
        NULL,
        (LPGUID)&ProviderGuid,
        sizeof(EventClassGuids)/sizeof(TRACE_GUID_REGISTRATION),
        EventClassGuids,
        NULL,
        NULL,
        &RegistrationHandle
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegisterTraceGuids failed with %lu\n", status);
        goto cleanup;
    }

    // Set the event-specific data.

    EventData.Cost = 32;
    EventData.ID = tempID;
    EventData.Indices[0] = 4;
    EventData.Indices[1] = 5;
    EventData.Indices[2] = 6;
    EventData.IsComplete = TRUE;
    wcscpy_s(EventData.Signature, MAX_SIGNATURE_LEN, L"Signature");
    EventData.Size = 1024;

    // Log the event if the provider is enabled and the session
    // passed a severity level value >= TRACE_LEVEL_ERROR (or zero).
    // If your provider generates more than one class of events, you
    // would also need to check g_EnableFlags.

    if (g_TraceOn && (0 == g_EnableLevel || TRACE_LEVEL_ERROR <= g_EnableLevel))
    {
        // Initialize the event data structure.

        ZeroMemory(&MyEvent, sizeof(MY_EVENT));
        MyEvent.Header.Size = sizeof(EVENT_TRACE_HEADER) + (sizeof(MOF_FIELD) * EVENT_DATA_FIELDS_CNT);
        MyEvent.Header.Flags = WNODE_FLAG_TRACED_GUID | WNODE_FLAG_USE_MOF_PTR;
        MyEvent.Header.Guid = MyCategoryGuid;
        MyEvent.Header.Class.Type = MY_EVENT_TYPE;
        MyEvent.Header.Class.Version = 1;
        MyEvent.Header.Class.Level = g_EnableLevel;

        // Load the event data. You can also use the DEFINE_TRACE_MOF_FIELD
        // macro defined in evntrace.h to set the MOF_FIELD members. For example,
        // DEFINE_TRACE_MOF_FIELD(&EventData.Data[0], &EventData.Cost, sizeof(EventData.Cost), 0);

        MyEvent.Data[0].DataPtr = (ULONG64) &(EventData.Cost);
        MyEvent.Data[0].Length = sizeof(EventData.Cost);
        MyEvent.Data[1].DataPtr = (ULONG64) &(EventData.Indices);
        MyEvent.Data[1].Length = sizeof(EventData.Indices);
        MyEvent.Data[2].DataPtr = (ULONG64) &(EventData.Signature);
        MyEvent.Data[2].Length = (ULONG)(wcslen(EventData.Signature) + 1) * sizeof(WCHAR);
        MyEvent.Data[3].DataPtr = (ULONG64) &(EventData.IsComplete);
        MyEvent.Data[3].Length = sizeof(EventData.IsComplete);
        MyEvent.Data[4].DataPtr = (ULONG64) &(EventData.ID);
        MyEvent.Data[4].Length = sizeof(EventData.ID);
        MyEvent.Data[5].DataPtr = (ULONG64) &(EventData.Size);
        MyEvent.Data[5].Length = sizeof(EventData.Size);

        // Write the event.

        status = TraceEvent(g_SessionHandle, &(MyEvent.Header));

        if (ERROR_SUCCESS != status)
        {
            // Decide how you want to handle failures. Typically, you do not
            // want to terminate the application because you failed to
            // log an event. If the error is a memory failure, you may
            // may want to log a message to the system event log or turn
            // off logging.

            wprintf(L"TraceEvent() event failed with %lu\n", status);
            g_TraceOn = FALSE;
        }
    }

cleanup:

    if (RegistrationHandle)
    {
        UnregisterTraceGuids(RegistrationHandle);
    }
}


// The callback function that receives enable/disable notifications
// from one or more ETW sessions. Because more than one session
// can enable the provider, this example ignores requests from other 
// sessions if it is already enabled.

ULONG WINAPI ControlCallback(
    WMIDPREQUESTCODE RequestCode,
    PVOID Context,
    ULONG* Reserved, 
    PVOID Header
    )
{
    UNREFERENCED_PARAMETER(Context);
    UNREFERENCED_PARAMETER(Reserved);

    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE TempSessionHandle = 0; 

    switch (RequestCode)
    {
        case WMI_ENABLE_EVENTS:  // Enable the provider.
        {
            SetLastError(0);

            // If the provider is already enabled to a provider, ignore 
            // the request. Get the session handle of the enabling session.
            // You need the session handle to call the TraceEvent function.
            // The session could be enabling the provider or it could be
            // updating the level and enable flags.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (0 == g_SessionHandle)
            {
                g_SessionHandle = TempSessionHandle;
            }
            else if (g_SessionHandle != TempSessionHandle)
            {
                break;
            }

            // Get the severity level of the events that the
            // session wants you to log.

            g_EnableLevel = GetTraceEnableLevel(g_SessionHandle); 
            if (0 == g_EnableLevel)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable level means to your provider.
                    // For this example, it means log all events.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableLevel failed with, %lu.\n", status);
                    break;
                } 
            }

            // Get the enable flags that indicate the events that the
            // session wants you to log. The provider determines the
            // flags values. How it articulates the flag values and 
            // meanings to perspective sessions is up to it.

            g_EnableFlags = GetTraceEnableFlags(g_SessionHandle);
            if (0 == g_EnableFlags)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable flags value means to your provider.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableFlags failed with, %lu.\n", status);
                    break;
                }
            }

            g_TraceOn = TRUE;
            break;
        }
 
        case WMI_DISABLE_EVENTS:  // Disable the provider.
        {
            // Disable the provider only if the request is coming from the
            // session that enabled the provider.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (g_SessionHandle == TempSessionHandle)
            {
                g_TraceOn = FALSE;
                g_SessionHandle = 0;
            }
            break;
        }

        default:
        {
            status = ERROR_INVALID_PARAMETER;
            break;
        }
    }

    return status;
}
```



 

 
