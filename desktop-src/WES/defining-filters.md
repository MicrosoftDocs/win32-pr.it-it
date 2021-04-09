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
# <a name="defining-filters"></a>Definizione di filtri

Un provider può definire i filtri utilizzati da una sessione per filtrare gli eventi in base ai dati dell'evento. Con Level e keywords, ETW determina se l'evento viene scritto nel log. Tuttavia, con i filtri, il provider usa i criteri dei dati del filtro che la sessione di controllo vi passa (vedere la funzione [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) ) per determinare se scrive l'evento nella sessione. I filtri sono applicabili solo quando una sessione di traccia ETW Abilita il provider.

In genere, i provider scrivono solo gli eventi e la sessione identifica i tipi di eventi che vogliono usare il livello e le parole chiave. Se il provider ha definito un filtro di dati per un tipo di evento, la sessione potrebbe utilizzarlo per filtrare gli eventi per quel tipo di evento in base ai dati dell'evento (la semantica del filtro è definita dal provider). Se, ad esempio, il provider genera eventi di processo, è possibile definire un filtro dei dati per filtrare gli eventi di elaborazione in base a un identificatore di processo. La sessione può quindi passare un identificatore del processo come filtro dei dati al provider e ricevere solo eventi di elaborazione per tale identificatore di processo.

Nell'esempio seguente viene illustrato come utilizzare l'elemento **Filter** per definire un filtro. È necessario specificare gli attributi **Name** e **value** del filtro; gli altri attributi sono facoltativi. L'attributo **TID** è obbligatorio se il filtro richiede che la sessione passi i dati del filtro.


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