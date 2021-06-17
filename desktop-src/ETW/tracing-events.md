---
description: Informazioni sulla scrittura di eventi MOF in una sessione di traccia. Iniziare con la registrazione del provider, in modo che sia pronto per scrivere eventi in una sessione di traccia.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Scrittura di eventi MOF (versione classica)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d081c48567851d2fb570dd7bfa5c75e687b524
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112261843"
---
# <a name="writing-mof-classic-events"></a>Scrittura di eventi MOF (versione classica)

Prima di poter scrivere eventi in una sessione di traccia, è necessario registrare il provider. La registrazione di un provider indica a ETW che il provider è pronto per scrivere eventi in una sessione di traccia. Un processo può registrare fino a 1.024 GUID del provider. Tuttavia, è necessario limitare il numero di provider registrati dal processo a uno o due.

**Prima di Windows Vista:** Non esiste alcun limite al numero di provider che un processo può registrare.

Per registrare un provider classico, chiamare la [**funzione RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) La funzione registra il GUID del provider, i GUID della classe di traccia eventi e identifica il callback chiamato da ETW quando un controller abilita o disabilita il provider.

Se il provider chiama la funzione [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) per registrare gli eventi, non è necessario includere la matrice di GUID di classe (può essere **NULL)** quando si chiama la [**funzione RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) È necessario includere la matrice solo se il provider chiama la [**funzione TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) per registrare gli eventi.

**Windows XP e Windows 2000:** È sempre necessario includere la matrice di GUID di classe (non può essere **NULL).**

Dopo che un provider si registra e viene abilitato dal controller, il provider può registrare gli eventi nella sessione di traccia del controller.

Prima che il provider venga chiuso, chiamare la [**funzione UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) per rimuovere la registrazione del provider da ETW. La [**funzione RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) restituisce l'handle di registrazione passato alla **funzione UnregisterTraceGuids.**

Se il provider registra gli eventi solo nella sessione del logger globale, non è necessario registrare il provider con ETW perché il controller del logger globale non abilita o disabilita i provider. Per informazioni dettagliate, [vedere Configurazione e avvio della sessione del logger globale](configuring-and-starting-the-global-logger-session.md).

Tutti [i](about-event-tracing.md) provider classici ,ad eccezione di quelli che tracciano gli eventi nella sessione global Logger, devono implementare la [**funzione ControlCallback.**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) Il provider usa le informazioni nel callback per determinare se è abilitato o disabilitato e quali eventi deve scrivere.

Il provider specifica il nome della funzione di callback quando chiama la [**funzione RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) per registrarsi. ETW chiama la funzione di callback quando il controller chiama la [**funzione EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per abilitare o disabilitare il provider.

[**Nell'implementazione di ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) è necessario chiamare la [**funzione GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) per recuperare l'handle di sessione. l'handle di sessione viene utilizzato quando si chiama [**la funzione TraceEvent.**](/windows/win32/api/evntrace/nf-evntrace-traceevent) È necessario chiamare la [**funzione GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) o [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) nell'implementazione **di ControlCallback** solo se il provider usa il livello di abilitazione o i flag di abilitazione.

Un provider può registrare gli eventi di traccia in una sola sessione, ma non è necessario impedire a più controller di abilitare un singolo provider. Per impedire a un altro controller di reindirizzare gli eventi di traccia alla relativa sessione, è possibile aggiungere logica all'implementazione [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) per confrontare gli handle di sessione e ignorare le richieste di abilitazione da altri controller.

Per registrare gli eventi, [i provider classici](about-event-tracing.md) chiamano la funzione [**TraceEvent.**](/windows/win32/api/evntrace/nf-evntrace-traceevent) Un evento è costituito dalla [**struttura EVENT \_ TRACE \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e da tutti i dati specifici dell'evento aggiunti all'intestazione.

L'intestazione deve contenere le informazioni seguenti:

-   Il **membro Size** deve contenere il numero totale di byte da registrare per l'evento , incluse le dimensioni della struttura EVENT TRACE [**\_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e di tutti i dati specifici dell'evento aggiunti all'intestazione.
-   Il **membro Guid** deve contenere il GUID della classe dell'evento oppure il membro **GuidPtr** deve contenere un puntatore al GUID della classe.

    **Windows XP e Windows 2000:** Il GUID della classe deve essere stato registrato in precedenza usando la [**funzione RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)

-   Il **membro Flags** deve contenere il flag GUID **\_ \_ TRACED WNODE \_ FLAG.** Se si specifica il GUID della classe usando il **membro GuidPtr,** aggiungere anche il flag **PTR WNODE \_ FLAG USE \_ \_ GUID. \_**
-   Il **membro Class.Type** deve contenere il tipo di evento, se si usa MOF per pubblicare il layout dei dati dell'evento.
-   Il **membro Class.Version** deve contenere la versione dell'evento, se si usa MOF per pubblicare il layout dei dati dell'evento. La versione viene usata per distinguere tra revisioni ai dati dell'evento. Impostare il numero di versione iniziale su 0.

Se si scrivono sia il provider che il consumer, è possibile usare una struttura per popolare i dati specifici dell'evento aggiunti all'intestazione. Tuttavia, se si usa MOF per pubblicare i dati specifici dell'evento in modo che qualsiasi consumer possa elaborare l'evento, non è consigliabile usare una struttura per aggiungere i dati specifici dell'evento all'intestazione. Ciò è dovuto al fatto che il compilatore può aggiungere byte aggiuntivi ai dati specifici dell'evento ai fini dell'allineamento dei byte. Poiché la definizione MOF non include i byte aggiuntivi, il consumer può recuperare dati non validi.

È necessario allocare un blocco di memoria per l'evento e copiare ogni elemento di dati dell'evento nella memoria oppure creare una struttura che includa una matrice di [**strutture MOF \_ FIELD.**](/windows/win32/api/evntrace/ns-evntrace-mof_field) La maggior parte delle applicazioni creerà una struttura che include una matrice di **strutture FIELD MOF. \_** Assicurarsi che **Header.Size rifletta** il numero effettivo di **strutture MOF \_ FIELD** effettivamente impostate prima di registrare l'evento. Ad esempio, se l'evento contiene tre campi dati, impostare **Header.Size** su sizeof(EVENT \_ TRACE \_ HEADER) + (sizeof(MOF \_ FIELD) \* 3).

Per informazioni sulla traccia degli eventi correlati, vedere Scrittura di eventi [correlati in uno scenario end-to-end](writing-related-events-in-an-end-to-end-scenario.md).

Nell'esempio seguente viene illustrato come chiamare la [**funzione TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) per registrare gli eventi. L'esempio fa riferimento agli eventi definiti in [Pubblicazione dello schema di eventi per un provider classico.](publishing-your-event-schema-for-a-classic-provider.md)


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



 

 
