---
title: Definizione dei canali
description: Gli eventi possono essere scritti nei canali del registro eventi, nei file di log di traccia eventi o in entrambi. Un canale è fondamentalmente un sink che raccoglie eventi.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c2f932616a131e478c100996fd0b76034b3cccdebf4e3714fd5b9b38ba9678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032481"
---
# <a name="defining-channels"></a>Definizione dei canali

Gli eventi possono essere scritti nei canali del registro eventi, nei file di log di traccia eventi o in entrambi. Un canale è fondamentalmente un sink che raccoglie eventi. Se il pubblico di destinazione per gli eventi usa consumer di eventi come il Windows Visualizzatore eventi, è necessario definire nuovi canali per raccogliere gli eventi o importare un canale esistente definito da un altro provider.

Per definire canali personalizzati, usare **l'elemento channel.** Per definire un canale importato, usare **l'elemento importChannel.** È possibile specificare fino a otto canali in qualsiasi combinazione di canali importati o canali definiti.

Il canale deve essere di uno dei quattro tipi: Admin, Operational, Analytic e Debug. Ogni tipo di canale ha un pubblico previsto, che determina il tipo di eventi che si scrivono nel canale. Per una descrizione di ogni tipo, vedere il [**tipo complesso ChannelType.**](eventmanifestschema-channeltype-complextype.md)

Per specificare il canale in cui viene scritto un  evento, impostare l'attributo channel della definizione di evento sullo stesso valore dell'attributo **chid della definizione del** canale. Gli eventi possono essere scritti in un solo canale alla volta, ma possono essere raccolti anche da un massimo di 7 altre sessioni ETW contemporaneamente.

L'esempio seguente illustra come importare un canale. È necessario impostare gli **attributi chid** **e name.** **L'attributo chid** identifica in modo univoco il canale. Ogni identificatore di canale nell'elenco di canali deve essere univoco. Impostare **l'attributo** name sullo stesso nome usato dal provider quando ha definito il canale.


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

Anche Winmeta.xml definisce canali legacy che è possibile importare, non è consigliabile usarli a meno che non si supportino consumer legacy che utilizzano eventi dai canali legacy (ad esempio, applicazione o sistema). Il Winmeta.xml file è incluso in Windows SDK.

L'esempio seguente illustra come definire un canale. È necessario impostare gli **attributi chid**, **name** e **type.** **L'attributo chid** identifica in modo univoco il canale. Ogni identificatore di canale nell'elenco di canali deve essere univoco. Impostare **l'attributo chid** su un valore univoco per i canali elencati dal provider. Viene fatto riferimento all'identificatore di canale in una o più definizioni di evento. La convenzione per la denominazione del canale è usare il nome del provider e il tipo di canale nel formato *providername* / *channeltype*.

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
