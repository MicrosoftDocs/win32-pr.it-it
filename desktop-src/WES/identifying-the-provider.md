---
title: Identificazione del provider
description: Un manifesto può identificare uno o più provider. Per identificare un provider, utilizzare l'elemento provider.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45941a540f8804beccc408435fc202593ddad601
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104516675"
---
# <a name="identifying-the-provider"></a>Identificazione del provider

Un manifesto può identificare uno o più provider. Per identificare un provider, utilizzare l'elemento **provider** . È necessario specificare gli attributi **Name**, **GUID**, **resourceFileName**, **messageFileName** e **Symbol** . Se si localizza il manifesto, è necessario specificare anche l'attributo del **messaggio** , utilizzato dai consumer come Visualizza il nome del provider. Se non si specifica l'attributo **Message** , i consumer utilizzeranno il valore dell'attributo **Name** .

Nel manifesto è possibile identificare fino a 16 provider. Se si desidera identificare più di 16 provider, è necessario includere la sezione **messageTable** del manifesto che i provider XVII e su devono usare per assegnare i valori delle risorse per le stringhe di messaggio che definiscono: la tabella messaggi non deve includere stringhe di messaggio che provider da 1 a 16 definito.

Nell'esempio seguente viene illustrato come utilizzare l'elemento **provider** per identificare un provider.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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
