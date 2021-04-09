---
title: Definizione di filtri
description: Un provider può definire i filtri utilizzati da una sessione per filtrare gli eventi in base ai dati dell'evento.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dd2a21b9c4e01ebc4a32a160b24022c79197b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118318"
---
# <a name="defining-filters"></a><span data-ttu-id="34689-103">Definizione di filtri</span><span class="sxs-lookup"><span data-stu-id="34689-103">Defining Filters</span></span>

<span data-ttu-id="34689-104">Un provider può definire i filtri utilizzati da una sessione per filtrare gli eventi in base ai dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="34689-104">A provider can define filters that a session uses to filter events based on event data.</span></span> <span data-ttu-id="34689-105">Con Level e keywords, ETW determina se l'evento viene scritto nel log.</span><span class="sxs-lookup"><span data-stu-id="34689-105">With level and keywords, ETW determines whether the event is written to the log.</span></span> <span data-ttu-id="34689-106">Tuttavia, con i filtri, il provider usa i criteri dei dati del filtro che la sessione di controllo vi passa (vedere la funzione [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) ) per determinare se scrive l'evento nella sessione.</span><span class="sxs-lookup"><span data-stu-id="34689-106">However, with filters, the provider uses the filter data criteria that the controlling session passes to it (see the [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) function) to determine whether it writes the event to that session.</span></span> <span data-ttu-id="34689-107">I filtri sono applicabili solo quando una sessione di traccia ETW Abilita il provider.</span><span class="sxs-lookup"><span data-stu-id="34689-107">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="34689-108">In genere, i provider scrivono solo gli eventi e la sessione identifica i tipi di eventi che vogliono usare il livello e le parole chiave.</span><span class="sxs-lookup"><span data-stu-id="34689-108">Typically, providers just write events, and the session identifies the types of events that it wants using level and keywords.</span></span> <span data-ttu-id="34689-109">Se il provider ha definito un filtro di dati per un tipo di evento, la sessione potrebbe utilizzarlo per filtrare gli eventi per quel tipo di evento in base ai dati dell'evento (la semantica del filtro è definita dal provider).</span><span class="sxs-lookup"><span data-stu-id="34689-109">If the provider defined a data filter for an event type, the session could use it to filter out events for that event type based on the event data (the semantics of the filter is defined by the provider).</span></span> <span data-ttu-id="34689-110">Se, ad esempio, il provider genera eventi di processo, è possibile definire un filtro dei dati per filtrare gli eventi di elaborazione in base a un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="34689-110">For example, if your provider generates process events, you could define a data filter that filtered process events based on a process identifier.</span></span> <span data-ttu-id="34689-111">La sessione può quindi passare un identificatore del processo come filtro dei dati al provider e ricevere solo eventi di elaborazione per tale identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="34689-111">The session could then pass a process identifier as filter data to the provider and receive only process events for that process identifier.</span></span>

<span data-ttu-id="34689-112">Nell'esempio seguente viene illustrato come utilizzare l'elemento **Filter** per definire un filtro.</span><span class="sxs-lookup"><span data-stu-id="34689-112">The following example shows how to use the **filter** element to define a filter.</span></span> <span data-ttu-id="34689-113">È necessario specificare gli attributi **Name** e **value** del filtro; gli altri attributi sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="34689-113">You must specify the filter's **name** and **value** attributes; the other attributes are optional.</span></span> <span data-ttu-id="34689-114">L'attributo **TID** è obbligatorio se il filtro richiede che la sessione passi i dati del filtro.</span><span class="sxs-lookup"><span data-stu-id="34689-114">The **tid** attribute is required if the filter requires that the session pass filter data.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```