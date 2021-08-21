---
title: Definizione di filtri
description: Un provider può definire filtri utilizzati da una sessione per filtrare gli eventi in base ai dati degli eventi.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d9d065fe3a46fc22114cfb4aed5b5b51d9a89eafa3280e2e258199e06aad3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056019"
---
# <a name="defining-filters"></a>Definizione di filtri

Un provider può definire filtri utilizzati da una sessione per filtrare gli eventi in base ai dati degli eventi. Con level e keywords, ETW determina se l'evento viene scritto nel log. Tuttavia, con i filtri, il provider usa i criteri dei dati di filtro passati dalla sessione di controllo (vedere la [*funzione EnableCallback)*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) per determinare se scrive l'evento in tale sessione. I filtri sono applicabili solo quando una sessione di traccia ETW abilita il provider.

In genere, i provider scrivono solo eventi e la sessione identifica i tipi di eventi che desiderano usando parole chiave e livello. Se il provider ha definito un filtro dati per un tipo di evento, la sessione potrebbe usarlo per filtrare gli eventi per tale tipo di evento in base ai dati dell'evento (la semantica del filtro è definita dal provider). Ad esempio, se il provider genera eventi di elaborazione, è possibile definire un filtro dati che filtra gli eventi del processo in base a un identificatore di processo. La sessione può quindi passare un identificatore di processo come dati di filtro al provider e ricevere solo eventi di elaborazione per tale identificatore di processo.

Nell'esempio seguente viene illustrato come usare **l'elemento filter** per definire un filtro. È necessario specificare gli attributi nome **e** **valore del** filtro. gli altri attributi sono facoltativi. **L'attributo tid** è obbligatorio se il filtro richiede che la sessione passi i dati del filtro.


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