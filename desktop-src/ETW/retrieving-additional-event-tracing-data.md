---
description: Una volta iniziata una sessione di traccia eventi, è possibile usare TraceSetInformation per indicare al sistema di restituire dati di traccia eventi aggiuntivi.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Recupero di dati di traccia eventi aggiuntivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef864de40b924e0210603646d5ba5430d5d9b643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966873"
---
# <a name="retrieving-additional-event-tracing-data"></a>Recupero di dati di traccia eventi aggiuntivi

Una volta iniziata una sessione di traccia eventi, è possibile usare [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) per indicare al sistema di restituire dati di traccia eventi aggiuntivi. Le informazioni aggiuntive verranno inserite nella sezione dati estesi della traccia eventi pertinente.

Nella procedura seguente viene descritto come utilizzare la funzione [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) per recuperare dati aggiuntivi da una sessione di traccia eventi.

**Per recuperare altri dati di traccia eventi**

1.  Avviare la sessione con una chiamata a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).

    Per ulteriori informazioni, vedere [configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

2.  Chiamare [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) per impostare ulteriori dati di traccia eventi.

    usare l'enumerazione delle [**\_ informazioni \_ di evento**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) nel parametro *ClassInformation* per descrivere le informazioni aggiuntive che si desidera recuperare. Nell'esempio seguente viene descritto come chiamare [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), usando l'handle di sessione restituito dalla chiamata a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e il valore **TraceProviderBinaryTracking** dalla **classe di \_ informazioni \_ evento**.

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  In alternativa, è possibile usare [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) per recuperare informazioni sulle impostazioni correnti della sessione di traccia eventi.

    Analogamente a [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) usa l'enumerazione della [**\_ \_ classe di informazioni sugli eventi**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) per descrivere quali informazioni recuperare dal sistema.

 

 
