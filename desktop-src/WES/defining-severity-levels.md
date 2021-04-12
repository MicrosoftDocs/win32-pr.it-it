---
title: Definizione di livelli di gravità
description: I livelli vengono usati per raggruppare gli eventi e indicano in genere la gravità o il livello di dettaglio di un evento.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8e2e979e75057a77cca267e540b3ec5469562f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104398795"
---
# <a name="defining-severity-levels"></a>Definizione di livelli di gravità

I livelli vengono usati per raggruppare gli eventi e indicano in genere la gravità o il livello di dettaglio di un evento. Per definire un livello, usare l'elemento **Level** . Il file di Winmeta.xml definisce i livelli di gravità usati di frequente seguenti:

-   win:Critical
-   win:Error
-   win:Warning
-   win:Informational
-   win:Verbose

I consumer utilizzano i livelli per eseguire query per gli eventi che contengono un valore di livello specifico. Una sessione di traccia ETW può inoltre utilizzare livelli per limitare gli eventi scritti nel file di log di traccia eventi; gli eventi con un valore di livello uguale o inferiore al valore del livello specificato vengono scritti nel file di log. Se, ad esempio, nella sessione è stato specificato il valore level per Win: Warning, il file di log conterrà avvisi, errori ed eventi critici.

Nell'esempio seguente viene illustrato come definire un livello. È necessario specificare gli attributi **Name** e **value** del livello. Il valore dell'attributo **value** deve essere compreso tra 16 e 255. Gli attributi **Symbol** e **Message** sono facoltativi.


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
