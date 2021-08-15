---
description: Dopo aver avviato una sessione di traccia eventi, è possibile usare TraceSetInformation per indicare al sistema di restituire dati di traccia eventi aggiuntivi.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Recupero di dati di traccia eventi aggiuntivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae65e516a63154fb76d3d558e02e9533e58e119e977f851c2404f0a218ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393899"
---
# <a name="retrieving-additional-event-tracing-data"></a>Recupero di dati di traccia eventi aggiuntivi

Dopo aver avviato una sessione di traccia eventi, è possibile usare [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) per indicare al sistema di restituire dati di traccia eventi aggiuntivi. Le informazioni aggiuntive verranno inserite nella sezione dei dati estesi della traccia eventi pertinente.

La procedura seguente descrive come usare la funzione [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) per recuperare dati aggiuntivi da una sessione di traccia eventi.

**Per recuperare dati di traccia eventi aggiuntivi**

1.  Avviare la sessione con una chiamata a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).

    Per altre informazioni, vedere [Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

2.  Chiamare [**TraceSetInformation per**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) impostare dati di traccia eventi aggiuntivi.

    Usare [**l'enumerazione EVENT \_ INFO \_ CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) nel *parametro ClassInformation* per descrivere le informazioni aggiuntive da recuperare. Nell'esempio seguente viene descritto come chiamare [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), usando l'handle di sessione restituito dalla chiamata a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e il **valore TraceProviderBinaryTracking** di **EVENT INFO \_ \_ CLASS**.

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  In alternativa, è possibile usare [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) per recuperare informazioni sulle impostazioni correnti della sessione di traccia eventi.

    Come [**TraceSetInformation,**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) usa l'enumerazione [**EVENT INFO \_ \_ CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) per descrivere le informazioni da recuperare dal sistema.

 

 
