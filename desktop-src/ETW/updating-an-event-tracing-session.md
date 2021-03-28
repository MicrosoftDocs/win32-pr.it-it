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
# <a name="updating-an-event-tracing-session"></a>Aggiornamento di una sessione di traccia eventi

Per aggiornare le proprietà di una sessione di traccia eventi, chiamare la funzione [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) usando il codice di controllo dell' **aggiornamento del \_ \_ controllo \_ di traccia eventi** . È possibile specificare la sessione da aggiornare utilizzando un handle di sessione ottenuto da una chiamata precedente a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)o un nome di sessione. Le proprietà della sessione di traccia eventi vengono aggiornate utilizzando i valori specificati nella struttura [**delle \_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) . È possibile aggiornare solo un subset di proprietà. Per un elenco delle proprietà che è possibile aggiornare, vedere il parametro *Properties* della funzione **ControlTrace** .

Se la chiamata [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) ha esito positivo, la struttura delle [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) viene aggiornata in modo da riflettere i nuovi valori delle proprietà. La struttura conterrà anche le nuove statistiche di esecuzione per la sessione di traccia eventi.

Nell'esempio seguente viene illustrato come aggiornare la sessione di traccia eventi del kernel. Nell'esempio viene eseguita una query per i valori correnti della proprietà e viene aggiornata la struttura prima di aggiornare la sessione.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione e avvio di una sessione di logger privata](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
