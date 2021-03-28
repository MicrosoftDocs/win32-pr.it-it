---
description: Per aggiornare le proprietà di una sessione di traccia eventi, chiamare la funzione ControlTrace usando il \_ codice di controllo dell'aggiornamento del controllo di traccia eventi \_ \_ .
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: Aggiornamento di una sessione di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e580c2e84dec6682e5fad323fe0cad427300a21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966872"
---
# <a name="updating-an-event-tracing-session"></a><span data-ttu-id="2a6e1-103">Aggiornamento di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="2a6e1-103">Updating an Event Tracing Session</span></span>

<span data-ttu-id="2a6e1-104">Per aggiornare le proprietà di una sessione di traccia eventi, chiamare la funzione [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) usando il codice di controllo dell' **aggiornamento del \_ \_ controllo \_ di traccia eventi** .</span><span class="sxs-lookup"><span data-stu-id="2a6e1-104">To update the properties of an event tracing session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function using the **EVENT\_TRACE\_CONTROL\_UPDATE** control code.</span></span> <span data-ttu-id="2a6e1-105">È possibile specificare la sessione da aggiornare utilizzando un handle di sessione ottenuto da una chiamata precedente a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)o un nome di sessione.</span><span class="sxs-lookup"><span data-stu-id="2a6e1-105">You can specify the session to update using a session handle obtained from an earlier call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), or a session name.</span></span> <span data-ttu-id="2a6e1-106">Le proprietà della sessione di traccia eventi vengono aggiornate utilizzando i valori specificati nella struttura [**delle \_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="2a6e1-106">The properties of the event tracing session are updated using the values specified in the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span> <span data-ttu-id="2a6e1-107">È possibile aggiornare solo un subset di proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a6e1-107">You can update only a subset of the properties.</span></span> <span data-ttu-id="2a6e1-108">Per un elenco delle proprietà che è possibile aggiornare, vedere il parametro *Properties* della funzione **ControlTrace** .</span><span class="sxs-lookup"><span data-stu-id="2a6e1-108">For a list of the properties you can update, see the *Properties* parameter of the **ControlTrace** function.</span></span>

<span data-ttu-id="2a6e1-109">Se la chiamata [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) ha esito positivo, la struttura delle [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) viene aggiornata in modo da riflettere i nuovi valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a6e1-109">If the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) call is successful, the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is updated to reflect the new property values.</span></span> <span data-ttu-id="2a6e1-110">La struttura conterrà anche le nuove statistiche di esecuzione per la sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="2a6e1-110">The structure will also contain the new run statistics for the event tracing session.</span></span>

<span data-ttu-id="2a6e1-111">Nell'esempio seguente viene illustrato come aggiornare la sessione di traccia eventi del kernel.</span><span class="sxs-lookup"><span data-stu-id="2a6e1-111">The following example shows how to update the kernel event tracing session.</span></span> <span data-ttu-id="2a6e1-112">Nell'esempio viene eseguita una query per i valori correnti della proprietà e viene aggiornata la struttura prima di aggiornare la sessione.</span><span class="sxs-lookup"><span data-stu-id="2a6e1-112">The example queries for the current property values and updates the structure before updating the session.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

#define MAX_SESSION_NAME_LEN 1024
#define MAX_LOGFILE_PATH_LEN 1024

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name.
    // This example specifies the maximum size for the session name 
    // and log file name.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + 
        (MAX_SESSION_NAME_LEN * sizeof(WCHAR)) + 
        (MAX_LOGFILE_PATH_LEN * sizeof(WCHAR));

    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;

    // Query for the kernel trace session's current property values.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_QUERY);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_WMI_INSTANCE_NOT_FOUND == status)
        {
            wprintf(L"The Kernel Logger is not running.\n");
        }
        else
        {
            wprintf(L"ControlTrace(query) failed with %lu\n", status);
        }

        goto cleanup;
    }

    // Update the enable flags to also enable the Process and Thread providers.

    pSessionProperties->LogFileNameOffset = 0;  // Zero tells ETW not to update the file name
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->EnableFlags |= EVENT_TRACE_FLAG_PROCESS | EVENT_TRACE_FLAG_THREAD;

    // Update the session's properties.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_UPDATE);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"ControlTrace(update) failed with %lu.\n", status);
        goto cleanup;
    }

    wprintf(L"\nUpdated session");

cleanup:

    if (pSessionProperties)
    {
        free(pSessionProperties);
        pSessionProperties = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="2a6e1-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a6e1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a6e1-114">Configurazione e avvio di una sessione di logger privata</span><span class="sxs-lookup"><span data-stu-id="2a6e1-114">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="2a6e1-115">Configurazione e avvio di una sessione SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="2a6e1-115">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="2a6e1-116">Configurazione e avvio di una sessione di autologger</span><span class="sxs-lookup"><span data-stu-id="2a6e1-116">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="2a6e1-117">Configurazione e avvio di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="2a6e1-117">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="2a6e1-118">Configurazione e avvio della sessione del logger del kernel NT</span><span class="sxs-lookup"><span data-stu-id="2a6e1-118">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
