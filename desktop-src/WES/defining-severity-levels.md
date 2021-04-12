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
# <a name="defining-severity-levels"></a><span data-ttu-id="c7238-103">Definizione di livelli di gravità</span><span class="sxs-lookup"><span data-stu-id="c7238-103">Defining Severity Levels</span></span>

<span data-ttu-id="c7238-104">I livelli vengono usati per raggruppare gli eventi e indicano in genere la gravità o il livello di dettaglio di un evento.</span><span class="sxs-lookup"><span data-stu-id="c7238-104">Levels are used to group events and typically indicate the severity or verbosity of an event.</span></span> <span data-ttu-id="c7238-105">Per definire un livello, usare l'elemento **Level** .</span><span class="sxs-lookup"><span data-stu-id="c7238-105">To define a level, use the **level** element.</span></span> <span data-ttu-id="c7238-106">Il file di Winmeta.xml definisce i livelli di gravità usati di frequente seguenti:</span><span class="sxs-lookup"><span data-stu-id="c7238-106">The Winmeta.xml file defines the following commonly used severity levels:</span></span>

-   <span data-ttu-id="c7238-107">win:Critical</span><span class="sxs-lookup"><span data-stu-id="c7238-107">win:Critical</span></span>
-   <span data-ttu-id="c7238-108">win:Error</span><span class="sxs-lookup"><span data-stu-id="c7238-108">win:Error</span></span>
-   <span data-ttu-id="c7238-109">win:Warning</span><span class="sxs-lookup"><span data-stu-id="c7238-109">win:Warning</span></span>
-   <span data-ttu-id="c7238-110">win:Informational</span><span class="sxs-lookup"><span data-stu-id="c7238-110">win:Informational</span></span>
-   <span data-ttu-id="c7238-111">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="c7238-111">win:Verbose</span></span>

<span data-ttu-id="c7238-112">I consumer utilizzano i livelli per eseguire query per gli eventi che contengono un valore di livello specifico.</span><span class="sxs-lookup"><span data-stu-id="c7238-112">Consumers use levels to query for events that contain a specific level value.</span></span> <span data-ttu-id="c7238-113">Una sessione di traccia ETW può inoltre utilizzare livelli per limitare gli eventi scritti nel file di log di traccia eventi; gli eventi con un valore di livello uguale o inferiore al valore del livello specificato vengono scritti nel file di log.</span><span class="sxs-lookup"><span data-stu-id="c7238-113">An ETW tracing session can also use levels to limit the events that are written to the event tracing log file; events with a level value equal to or less than the specified level value are written to the log file.</span></span> <span data-ttu-id="c7238-114">Se, ad esempio, nella sessione è stato specificato il valore level per Win: Warning, il file di log conterrà avvisi, errori ed eventi critici.</span><span class="sxs-lookup"><span data-stu-id="c7238-114">For example, if the session specified the level value for win:Warning, the log file would contain warning, error, and critical events.</span></span>

<span data-ttu-id="c7238-115">Nell'esempio seguente viene illustrato come definire un livello.</span><span class="sxs-lookup"><span data-stu-id="c7238-115">The following example shows how to define a level.</span></span> <span data-ttu-id="c7238-116">È necessario specificare gli attributi **Name** e **value** del livello.</span><span class="sxs-lookup"><span data-stu-id="c7238-116">You must specify the level's **name** and **value** attributes.</span></span> <span data-ttu-id="c7238-117">Il valore dell'attributo **value** deve essere compreso tra 16 e 255.</span><span class="sxs-lookup"><span data-stu-id="c7238-117">The value of the **value** attribute must be in the range from 16 through 255.</span></span> <span data-ttu-id="c7238-118">Gli attributi **Symbol** e **Message** sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="c7238-118">The **symbol** and **message** attributes are optional.</span></span>


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
