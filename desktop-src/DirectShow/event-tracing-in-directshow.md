---
description: Traccia eventi in DirectShow
ms.assetid: e78c4514-25f4-441d-bfd0-6dac4f7567fd
title: Traccia eventi in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c567d8a2e75d838570323d8ad6be04f11502c9c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304394"
---
# <a name="event-tracing-in-directshow"></a><span data-ttu-id="6da4b-103">Traccia eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6da4b-103">Event Tracing in DirectShow</span></span>

<span data-ttu-id="6da4b-104">DirectShow supporta Event Tracing for Windows (ETW), che può essere usato per creare registri eventi per la strumentazione o il debug.</span><span class="sxs-lookup"><span data-stu-id="6da4b-104">DirectShow supports Event Tracing for Windows (ETW), which can be used to create event logs for instrumentation or debugging.</span></span> <span data-ttu-id="6da4b-105">Per ulteriori informazioni su ETW, vedere la documentazione di Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6da4b-105">For more information about ETW, see the Windows SDK documentation.</span></span> <span data-ttu-id="6da4b-106">Per utilizzare gli eventi ETW in un'applicazione DirectShow, è necessario abilitare la traccia e quindi elaborare gli eventi di traccia.</span><span class="sxs-lookup"><span data-stu-id="6da4b-106">To consume ETW events in a DirectShow application, you must enable tracing and then process the trace events.</span></span> <span data-ttu-id="6da4b-107">Seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="6da4b-107">Use the following steps.</span></span>

<span data-ttu-id="6da4b-108">**Impostare le chiavi del registro di sistema necessarie**</span><span class="sxs-lookup"><span data-stu-id="6da4b-108">**Set the Necessary Registry Keys**</span></span>

<span data-ttu-id="6da4b-109">Per abilitare la traccia nel computer dell'utente, impostare innanzitutto le chiavi del registro di sistema seguenti:</span><span class="sxs-lookup"><span data-stu-id="6da4b-109">To enable tracing on the user's computer, first set the following registry keys:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DirectX
    GlitchInstrumentation = 0x00000001 (REG_DWORD)
HKEY_LOCAL_MACHINE\SOFTWARE\DEBUG\Quartz.dll
    PERFLOG = 0x00000001 (REG_DWORD) 
```



<span data-ttu-id="6da4b-110">Queste chiavi si applicano ai file binari di rilascio e di debug.</span><span class="sxs-lookup"><span data-stu-id="6da4b-110">These keys apply to both release and debug binaries.</span></span>

<span data-ttu-id="6da4b-111">**Abilitare la traccia nell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="6da4b-111">**Enable Tracing in Your Application**</span></span>

<span data-ttu-id="6da4b-112">Per abilitare la traccia nell'applicazione, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="6da4b-112">To enable tracing in your application, perform the following steps:</span></span>

1.  <span data-ttu-id="6da4b-113">Chiamare **StartTrace** per avviare una nuova sessione di traccia.</span><span class="sxs-lookup"><span data-stu-id="6da4b-113">Call **StartTrace** to start a new tracing session.</span></span>
2.  <span data-ttu-id="6da4b-114">Chiamare **EnableTrace** per abilitare la traccia.</span><span class="sxs-lookup"><span data-stu-id="6da4b-114">Call **EnableTrace** to enable tracing.</span></span> <span data-ttu-id="6da4b-115">Il GUID del provider per DirectShow è GUID \_ dshow \_ CTL.</span><span class="sxs-lookup"><span data-stu-id="6da4b-115">The provider GUID for DirectShow is GUID\_DSHOW\_CTL.</span></span>
3.  <span data-ttu-id="6da4b-116">Prima della chiusura dell'applicazione, chiamare **StopTrace** per chiudere la sessione di traccia.</span><span class="sxs-lookup"><span data-stu-id="6da4b-116">Before the application exits, call **StopTrace** to close the tracing session.</span></span>

<span data-ttu-id="6da4b-117">**Elaborare gli eventi**</span><span class="sxs-lookup"><span data-stu-id="6da4b-117">**Process the Events**</span></span>

<span data-ttu-id="6da4b-118">Per elaborare gli eventi, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="6da4b-118">To process the events, perform the following steps:</span></span>

1.  <span data-ttu-id="6da4b-119">Chiamare **OpenTrace** per aprire la traccia per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6da4b-119">Call **OpenTrace** to open the trace for processing.</span></span>
2.  <span data-ttu-id="6da4b-120">Chiamare **ProcessTrace** per elaborare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="6da4b-120">Call **ProcessTrace** to process the events.</span></span>
3.  <span data-ttu-id="6da4b-121">Nel callback **ProcessTrace** usare il GUID dell'evento per trovare il tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="6da4b-121">In the **ProcessTrace** callback, use the event GUID to find the event type.</span></span> <span data-ttu-id="6da4b-122">Il GUID dell'evento indica la struttura utilizzata per i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="6da4b-122">The event GUID indicates the structure that is used for the event data.</span></span> <span data-ttu-id="6da4b-123">Vedere [GUID dell'evento di traccia](trace-guids.md).</span><span class="sxs-lookup"><span data-stu-id="6da4b-123">See [Trace Event GUIDs](trace-guids.md).</span></span>
4.  <span data-ttu-id="6da4b-124">Chiamare **CloseTrace** per chiudere l'handle di traccia.</span><span class="sxs-lookup"><span data-stu-id="6da4b-124">Call **CloseTrace** to close the trace handle.</span></span>

<span data-ttu-id="6da4b-125">**Codice di esempio**</span><span class="sxs-lookup"><span data-stu-id="6da4b-125">**Example Code**</span></span>

<span data-ttu-id="6da4b-126">Nel codice seguente viene illustrata una classe helper che consente la traccia.</span><span class="sxs-lookup"><span data-stu-id="6da4b-126">The following code shows a helper class that enables tracing.</span></span> <span data-ttu-id="6da4b-127">In questo codice viene illustrato come scrivere eventi in un file di log, che può essere elaborato al termine della sessione.</span><span class="sxs-lookup"><span data-stu-id="6da4b-127">This code shows how to write events to a log file, which can be processed after the session completes.</span></span> <span data-ttu-id="6da4b-128">È anche possibile elaborare gli eventi in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="6da4b-128">You can also process events in real time.</span></span> <span data-ttu-id="6da4b-129">Per ulteriori informazioni, vedere la documentazione ETW nella Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6da4b-129">For more information, refer to the ETW documentation in the Windows SDK.</span></span>


```C++
#include <wmistr.h>
#include <evntrace.h>
#include <perfstruct.h>

// Event classes. These are defined in dxmperf.h.
#ifndef DXMPERF_VIDEOREND
#define DXMPERF_VIDEOREND   0x00000001
#endif

#ifndef AUDIOBREAK_BIT
#define AUDIOBREAK_BIT      0x00000010
#endif

// This structure extends the EVENT_TRACE_PROPERTIES by adding fields
// for the name of the WMI session name and the log file.
struct PERFMON_LOGGERINFO
{
    EVENT_TRACE_PROPERTIES TraceProperties;
    WCHAR wcSessionName[ MAX_PATH ];    // Session name.
    WCHAR wcLogFileName[ MAX_PATH ];    // Log file.
};

// Helper class for DirectShow event tracing.
class CTrace
{
public:
    CTrace() : m_SessionLogger((TRACEHANDLE) INVALID_HANDLE_VALUE)
    {
        ZeroMemory(&m_LogInfo, sizeof(&m_LogInfo));
    }

    // Start: Starts a trace session.
    HRESULT Start(WCHAR *wszLogFile)
    {
        const WCHAR* wszSessionName = L"PerfMon_DirectShow"; 
        HRESULT hr = S_OK;
        ULONG result; 

        ZeroMemory(&m_LogInfo, sizeof(m_LogInfo));
        
        EVENT_TRACE_PROPERTIES& prop = m_LogInfo.TraceProperties;

        prop.Wnode.BufferSize = sizeof(m_LogInfo);  // Size of the structure.
        prop.Wnode.Flags = WNODE_FLAG_TRACED_GUID;  // Must be this value.

        // Use the QPC (high resolution timer).
        prop.Wnode.ClientContext = 1;        

        prop.Wnode.Guid = GUID_DSHOW_CTL;           // Event provider GUID.
        prop.LogFileMode = 
            EVENT_TRACE_FILE_MODE_CIRCULAR | EVENT_TRACE_USE_PAGED_MEMORY; 
        prop.EnableFlags = 
            EVENT_TRACE_FLAG_PROCESS;   // Process events.

        // Set the offset from the start of the structure to the log file name.
        prop.LogFileNameOffset = 
            sizeof(m_LogInfo.TraceProperties) + sizeof(m_LogInfo.wcSessionName);  

        // Set the offset from the start of the structure to the session name.
        prop.LoggerNameOffset = sizeof(m_LogInfo.TraceProperties); 

        // Copy the names into the structure.
        StringCchCopy(m_LogInfo.wcSessionName, MAX_PATH, wszSessionName);
        StringCchCopy(m_LogInfo.wcLogFileName, MAX_PATH, wszLogFile);

        // Start the trace.
        result = StartTrace(
            &m_SessionLogger, 
            m_LogInfo.wcSessionName, 
            &m_LogInfo.TraceProperties
            );

        if (result == ERROR_SUCCESS)
        {
            result = EnableTrace(
                TRUE,                                   // Enable.
                AUDIOBREAK_BIT | DXMPERF_VIDEOREND,     // Event classes.
                TRACE_LEVEL_VERBOSE,                    // Trace level.
                &GUID_DSHOW_CTL,                        // Event provider.
                m_SessionLogger                         // Session handle.
                );
        }
        if (result != ERROR_SUCCESS)
        { 
            hr = __HRESULT_FROM_WIN32(result);
        }
        return hr;
    }

    HRESULT Stop()
    {
        HRESULT hr = S_OK;

        // Stop the trace.
        if (m_SessionLogger != (TRACEHANDLE)INVALID_HANDLE_VALUE)
        {
            LONG result = 0;

            result = EnableTrace(FALSE, 0, 0, &GUID_DSHOW_CTL, m_SessionLogger);
            if (result == ERROR_SUCCESS)
            {
                result = StopTrace(
                    m_SessionLogger, 
                    m_LogInfo.wcSessionName, 
                    &m_LogInfo.TraceProperties);
            }

            m_SessionLogger = (TRACEHANDLE)INVALID_HANDLE_VALUE;
            if (result != ERROR_SUCCESS)
            { 
                hr = __HRESULT_FROM_WIN32(result);
            }
        }
        return hr;
    }

protected:
    TRACEHANDLE         m_SessionLogger;
    PERFMON_LOGGERINFO  m_LogInfo;
};
```



<span data-ttu-id="6da4b-130">Il codice seguente illustra come elaborare il registro eventi:</span><span class="sxs-lookup"><span data-stu-id="6da4b-130">The following code shows how to process the event log:</span></span>


```C++
// Callback for event processing.
VOID WINAPI EventCallback(PEVENT_TRACE pEvent)
{
    PERFINFO_DSHOW_STREAMTRACE  *pStreamTrace = NULL;
    PERFINFO_DSHOW_AVREND       *pVideoRender = NULL;
    PERFINFO_DSHOW_AUDIOBREAK   *pAudioBreak = NULL;

    if (pEvent->Header.Guid == GUID_STREAMTRACE) 
    {
        pStreamTrace = (PPERFINFO_DSHOW_STREAMTRACE)pEvent->MofData;

        switch (pStreamTrace->id)
        {
            // TODO: Handle the event.
        }
    }
    else if(pEvent->Header.Guid == GUID_VIDEOREND)
    {      
        pVideoRender = (PPERFINFO_DSHOW_AVREND)pEvent->MofData;
        // TODO: Handle the event.
    }
    else if(pEvent->Header.Guid == GUID_AUDIOBREAK)
    {
        pAudioBreak = (PPERFINFO_DSHOW_AUDIOBREAK)pEvent->MofData;
        // TODO: Handle the event.
    }
}

void ProcessTraceEvents(WCHAR *wszLogFile)
{
    ULONG result = 0;        
    EVENT_TRACE_LOGFILE logfile;

    ZeroMemory(&logfile, sizeof(logfile));
    logfile.LogFileName = wszLogFile;
    logfile.EventCallback  = EventCallback;   

    TRACEHANDLE handle = OpenTrace(&logfile);
    if (handle != (TRACEHANDLE)INVALID_HANDLE_VALUE)
    {
        result = ProcessTrace(&handle, 1, NULL, NULL);
        CloseTrace(handle);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="6da4b-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6da4b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6da4b-132">Debug in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6da4b-132">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



