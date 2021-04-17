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
# <a name="identifying-the-provider"></a><span data-ttu-id="bae9f-104">Identificazione del provider</span><span class="sxs-lookup"><span data-stu-id="bae9f-104">Identifying the Provider</span></span>

<span data-ttu-id="bae9f-105">Un manifesto può identificare uno o più provider.</span><span class="sxs-lookup"><span data-stu-id="bae9f-105">A manifest can identify one or more providers.</span></span> <span data-ttu-id="bae9f-106">Per identificare un provider, utilizzare l'elemento **provider** .</span><span class="sxs-lookup"><span data-stu-id="bae9f-106">To identify a provider, use the **provider** element.</span></span> <span data-ttu-id="bae9f-107">È necessario specificare gli attributi **Name**, **GUID**, **resourceFileName**, **messageFileName** e **Symbol** .</span><span class="sxs-lookup"><span data-stu-id="bae9f-107">You must specify the **name**, **guid**, **resourceFileName**, **messageFileName**, and **symbol** attributes.</span></span> <span data-ttu-id="bae9f-108">Se si localizza il manifesto, è necessario specificare anche l'attributo del **messaggio** , utilizzato dai consumer come Visualizza il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="bae9f-108">If you localize your manifest, you should also specify the **message** attribute, which consumers use as the display the name of the provider.</span></span> <span data-ttu-id="bae9f-109">Se non si specifica l'attributo **Message** , i consumer utilizzeranno il valore dell'attributo **Name** .</span><span class="sxs-lookup"><span data-stu-id="bae9f-109">If you do not specify the **message** attribute, consumers use the value of the **name** attribute.</span></span>

<span data-ttu-id="bae9f-110">Nel manifesto è possibile identificare fino a 16 provider.</span><span class="sxs-lookup"><span data-stu-id="bae9f-110">You can identify up to 16 providers in the manifest.</span></span> <span data-ttu-id="bae9f-111">Se si desidera identificare più di 16 provider, è necessario includere la sezione **messageTable** del manifesto che i provider XVII e su devono usare per assegnare i valori delle risorse per le stringhe di messaggio che definiscono: la tabella messaggi non deve includere stringhe di messaggio che provider da 1 a 16 definito.</span><span class="sxs-lookup"><span data-stu-id="bae9f-111">If you want to identify more than 16 providers, you must include the **messageTable** section of the manifest that the seventeenth and on providers must use to assign resource values for the message strings that they define—the message table must not include any message strings that providers 1 through 16 defined.</span></span>

<span data-ttu-id="bae9f-112">Nell'esempio seguente viene illustrato come utilizzare l'elemento **provider** per identificare un provider.</span><span class="sxs-lookup"><span data-stu-id="bae9f-112">The following example shows how to use the **provider** element to identify a provider.</span></span>


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
