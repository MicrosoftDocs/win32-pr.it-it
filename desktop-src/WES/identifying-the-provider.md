---
title: Identificazione del provider
description: Un manifesto può identificare uno o più provider. Per identificare un provider, usare l'elemento provider .
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbce9b07aa8a2322311397ae9a48b3d72d60b784e5c55b028afc9772b53f63d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470922"
---
# <a name="identifying-the-provider"></a>Identificazione del provider

Un manifesto può identificare uno o più provider. Per identificare un provider, usare **l'elemento provider** . È necessario specificare gli **attributi name**, **guid**, **resourceFileName**, **messageFileName** e **symbol.** Se si localizza il manifesto, è necessario specificare anche l'attributo **del** messaggio, che i consumer usano come nome visualizzato del provider. Se non si specifica l'attributo **del messaggio,** i consumer utilizzano il valore dell'attributo name. 

È possibile identificare fino a 16 provider nel manifesto. Se si desidera identificare più di 16 provider, è necessario includere la sezione **messageTable** del manifesto che i diciassette e i provider devono usare per assegnare valori di risorsa per le stringhe di messaggio definite. La tabella dei messaggi non deve includere stringhe di messaggio definite dai provider da 1 a 16.

Nell'esempio seguente viene illustrato come utilizzare **l'elemento provider** per identificare un provider.


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
