---
description: La sessione del logger del kernel NT è una sessione di traccia eventi che registra un set predefinito di eventi del kernel.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Configurazione e avvio della sessione del logger del kernel NT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13cb0d429bc4b0e01e02c33e2686040f0b7454b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980946"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a>Configurazione e avvio della sessione del logger del kernel NT

La sessione del logger del kernel NT è una sessione di traccia eventi che registra un set predefinito di eventi del kernel. Non viene chiamata la funzione [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per abilitare i provider del kernel. Usare invece il membro **EnableFlags** della struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) per specificare gli eventi del kernel che si desidera ricevere. La funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) usa i flag enable specificati per abilitare i provider del kernel.

Esiste una sola sessione del logger di kernel NT. Se la sessione è già in uso, la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) restituisce un errore \_ già \_ esistente.

Per informazioni dettagliate sull'avvio di una sessione di traccia eventi, vedere [configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

Per informazioni dettagliate sull'avvio di una sessione di logger privata, vedere [configurazione e avvio di una sessione di logger privati](configuring-and-starting-a-private-logger-session.md).

Per informazioni dettagliate sull'avvio di una sessione di logger globale, vedere [configurazione e avvio della sessione Global Logger](configuring-and-starting-the-global-logger-session.md).

Per informazioni dettagliate sull'avvio di una sessione di autologger, vedere [configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md).

Nell'esempio seguente viene illustrato come configurare e avviare una sessione del logger del kernel NT che raccoglie gli eventi del kernel TCP/IP di rete e li scrive in un file circolare di 5 MB.


```C++
#define INITGUID  // Include this #define to use SystemTraceControlGuid in Evntrace.h.

#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <strsafe.h>
#include <wmistr.h>
#include <evntrace.h>

#define LOGFILE_PATH L"<FULLPATHTOTHELOGFILE.etl>"

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE SessionHandle = 0;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name,
    // which get appended to the end of the session properties structure.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(LOGFILE_PATH) + sizeof(KERNEL_LOGGER_NAME);
    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    // Set the session properties. You only append the log file name
    // to the properties structure; the StartTrace function appends
    // the session name for you.

    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->Wnode.ClientContext = 1; //QPC clock resolution
    pSessionProperties->Wnode.Guid = SystemTraceControlGuid; 
    pSessionProperties->EnableFlags = EVENT_TRACE_FLAG_NETWORK_TCPIP;
    pSessionProperties->LogFileMode = EVENT_TRACE_FILE_MODE_CIRCULAR;
    pSessionProperties->MaximumFileSize = 5;  // 5 MB
    pSessionProperties->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
    pSessionProperties->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(KERNEL_LOGGER_NAME); 
    StringCbCopy((LPWSTR)((char*)pSessionProperties + pSessionProperties->LogFileNameOffset), sizeof(LOGFILE_PATH), LOGFILE_PATH);

    // Create the trace session.

    status = StartTrace((PTRACEHANDLE)&SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_ALREADY_EXISTS == status)
        {
            wprintf(L"The NT Kernel Logger session is already in use.\n");
        }
        else
        {
            wprintf(L"EnableTrace() failed with %lu\n", status);
        }

        goto cleanup;
    }

    wprintf(L"Press any key to end trace session ");
    _getch();

cleanup:

    if (SessionHandle)
    {
        status = ControlTrace(SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_STOP);

        if (ERROR_SUCCESS != status)
        {
            wprintf(L"ControlTrace(stop) failed with %lu\n", status);
        }
    }

    if (pSessionProperties)
        free(pSessionProperties);
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

[Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
