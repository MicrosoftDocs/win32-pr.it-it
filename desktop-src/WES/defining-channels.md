---
title: Definizione di canali
description: Gli eventi possono essere scritti nei canali del log eventi, nei file di log di traccia eventi o in entrambi. Un canale è fondamentalmente un sink che raccoglie gli eventi.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3c73697aa11e7b63ace0ece33be23ca7a1b883
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104117471"
---
# <a name="defining-channels"></a>Definizione di canali

Gli eventi possono essere scritti nei canali del log eventi, nei file di log di traccia eventi o in entrambi. Un canale è fondamentalmente un sink che raccoglie gli eventi. Se i destinatari per gli eventi utilizzano consumer di eventi quali Windows Visualizzatore eventi, è necessario definire nuovi canali per raccogliere gli eventi o importare un canale esistente definito da un altro provider.

Per definire canali personalizzati, usare l'elemento **Channel** . Per definire un canale importato, usare l'elemento **importChannel** . È possibile specificare fino a otto canali in qualsiasi combinazione di canali o canali importati definiti.

Il canale deve essere di uno dei quattro tipi seguenti: amministratore, operativo, analitico e debug. Ogni tipo di canale ha un pubblico desiderato, che determina il tipo di eventi scritti sul canale. Per una descrizione di ogni tipo, vedere il tipo complesso [**ChannelType**](eventmanifestschema-channeltype-complextype.md) .

Per specificare il canale in cui viene scritto un evento, impostare l'attributo del **canale** della definizione dell'evento sullo stesso valore dell'attributo **figlio** della definizione del canale. Gli eventi possono essere scritti in un solo canale alla volta, ma possono essere raccolti anche fino a 7 altre sessioni ETW nello stesso momento.

Nell'esempio seguente viene illustrato come importare un canale. È necessario impostare gli attributi **figlio** e **Name** . L'attributo **figlio** identifica in modo univoco il canale. ogni identificatore del canale nell'elenco dei canali deve essere univoco. Impostare l'attributo **Name** sullo stesso nome utilizzato dal provider durante la definizione del canale.


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

                <channels>
                    <channel chid="c1"
                             name="Microsoft-Windows-BaseProvider/Admin"
                             symbol="CHANNEL_BASEPROVIDER_ADMIN"
                             type="Admin"/>
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

Anche se Winmeta.xml definisce i canali legacy che è possibile importare, è consigliabile non utilizzarli a meno che non si supportino i consumer legacy che utilizzano gli eventi dei canali legacy (ad esempio, applicazione o sistema). Il file di Winmeta.xml è incluso nel Windows SDK.

Nell'esempio seguente viene illustrato come definire un canale. È necessario impostare gli attributi **figlio**, **Name** e **Type** . L'attributo **figlio** identifica in modo univoco il canale. ogni identificatore del canale nell'elenco dei canali deve essere univoco. Impostare l'attributo **figlio** su un valore univoco per i canali elencati dal provider. si fa riferimento all'identificatore del canale in una o più definizioni di evento. La convenzione per la denominazione del canale consiste nell'usare il nome del provider e il tipo di canale nel formato *providerName* / *channelType*.

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

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
