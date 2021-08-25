---
title: Definizione dei livelli di gravità
description: I livelli vengono usati per raggruppare gli eventi e in genere indicano la gravità o il livello di dettaglio di un evento.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3c3c5e663e476f98bef5c9be3f20cae5e0e88a74a7996f6f515d1d92599eb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863681"
---
# <a name="defining-severity-levels"></a>Definizione dei livelli di gravità

I livelli vengono usati per raggruppare gli eventi e in genere indicano la gravità o il livello di dettaglio di un evento. Per definire un livello, usare **l'elemento level.** Il Winmeta.xml file definisce i livelli di gravità di uso comune seguenti:

-   win:Critical
-   win:Error
-   win:Warning
-   win:Informational
-   win:Verbose

I consumer usano i livelli per eseguire query per gli eventi che contengono un valore di livello specifico. Una sessione di traccia ETW può anche usare i livelli per limitare gli eventi scritti nel file di log di traccia eventi. Gli eventi con un valore di livello uguale o minore del valore del livello specificato vengono scritti nel file di log. Ad esempio, se la sessione ha specificato il valore del livello per win:Warning, il file di log conterrà eventi di avviso, errore ed eventi critici.

Nell'esempio seguente viene illustrato come definire un livello. È necessario specificare gli attributi nome **e** **valore del** livello. Il valore **dell'attributo value** deve essere compreso nell'intervallo compreso tra 16 e 255. Gli **attributi del** simbolo e **del** messaggio sono facoltativi.


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

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>
                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
