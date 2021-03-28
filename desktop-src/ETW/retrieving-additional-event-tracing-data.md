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
# <a name="retrieving-additional-event-tracing-data"></a><span data-ttu-id="faf2c-103">Recupero di dati di traccia eventi aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="faf2c-103">Retrieving Additional Event Tracing Data</span></span>

<span data-ttu-id="faf2c-104">Una volta iniziata una sessione di traccia eventi, è possibile usare [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) per indicare al sistema di restituire dati di traccia eventi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="faf2c-104">Once you have begun an event tracing session, you can use [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to instruct the system to return additional event tracing data.</span></span> <span data-ttu-id="faf2c-105">Le informazioni aggiuntive verranno inserite nella sezione dati estesi della traccia eventi pertinente.</span><span class="sxs-lookup"><span data-stu-id="faf2c-105">The additional information will be placed in the extended data section of the relevant event trace.</span></span>

<span data-ttu-id="faf2c-106">Nella procedura seguente viene descritto come utilizzare la funzione [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) per recuperare dati aggiuntivi da una sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="faf2c-106">The following procedure describes how to use the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function to retrieve additional data from an event tracing session.</span></span>

<span data-ttu-id="faf2c-107">**Per recuperare altri dati di traccia eventi**</span><span class="sxs-lookup"><span data-stu-id="faf2c-107">**To retrieve additional event tracing data**</span></span>

1.  <span data-ttu-id="faf2c-108">Avviare la sessione con una chiamata a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span><span class="sxs-lookup"><span data-stu-id="faf2c-108">Start your session with a call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span></span>

    <span data-ttu-id="faf2c-109">Per ulteriori informazioni, vedere [configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="faf2c-109">For more information, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

2.  <span data-ttu-id="faf2c-110">Chiamare [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) per impostare ulteriori dati di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="faf2c-110">Call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to set additional event tracing data.</span></span>

    <span data-ttu-id="faf2c-111">usare l'enumerazione delle [**\_ informazioni \_ di evento**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) nel parametro *ClassInformation* per descrivere le informazioni aggiuntive che si desidera recuperare.</span><span class="sxs-lookup"><span data-stu-id="faf2c-111">use the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration in the *ClassInformation* parameter to describe the additional information you wish to retrieve.</span></span> <span data-ttu-id="faf2c-112">Nell'esempio seguente viene descritto come chiamare [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), usando l'handle di sessione restituito dalla chiamata a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e il valore **TraceProviderBinaryTracking** dalla **classe di \_ informazioni \_ evento**.</span><span class="sxs-lookup"><span data-stu-id="faf2c-112">The following example describes how to call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), using the session handle returned from the call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and the **TraceProviderBinaryTracking** value from **EVENT\_INFO\_CLASS**.</span></span>

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  <span data-ttu-id="faf2c-113">In alternativa, è possibile usare [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) per recuperare informazioni sulle impostazioni correnti della sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="faf2c-113">Alternately, you can use [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) to retrieve information about the current event tracing session settings.</span></span>

    <span data-ttu-id="faf2c-114">Analogamente a [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) usa l'enumerazione della [**\_ \_ classe di informazioni sugli eventi**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) per descrivere quali informazioni recuperare dal sistema.</span><span class="sxs-lookup"><span data-stu-id="faf2c-114">Like [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) uses the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration to describe what information to retrieve from the system.</span></span>

 

 
