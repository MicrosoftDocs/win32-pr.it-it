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
# <a name="defining-channels"></a><span data-ttu-id="97a82-104">Definizione di canali</span><span class="sxs-lookup"><span data-stu-id="97a82-104">Defining Channels</span></span>

<span data-ttu-id="97a82-105">Gli eventi possono essere scritti nei canali del log eventi, nei file di log di traccia eventi o in entrambi.</span><span class="sxs-lookup"><span data-stu-id="97a82-105">Events can be written to event log channels, event tracing log files, or both.</span></span> <span data-ttu-id="97a82-106">Un canale è fondamentalmente un sink che raccoglie gli eventi.</span><span class="sxs-lookup"><span data-stu-id="97a82-106">A channel is basically a sink that collects events.</span></span> <span data-ttu-id="97a82-107">Se i destinatari per gli eventi utilizzano consumer di eventi quali Windows Visualizzatore eventi, è necessario definire nuovi canali per raccogliere gli eventi o importare un canale esistente definito da un altro provider.</span><span class="sxs-lookup"><span data-stu-id="97a82-107">If the target audience for your events uses event consumers such as the Windows Event Viewer, you must define new channels to collect your events or import an existing channel that another provider defined.</span></span>

<span data-ttu-id="97a82-108">Per definire canali personalizzati, usare l'elemento **Channel** .</span><span class="sxs-lookup"><span data-stu-id="97a82-108">To define your own channels, use the **channel** element.</span></span> <span data-ttu-id="97a82-109">Per definire un canale importato, usare l'elemento **importChannel** .</span><span class="sxs-lookup"><span data-stu-id="97a82-109">To define an imported channel, use the **importChannel** element.</span></span> <span data-ttu-id="97a82-110">È possibile specificare fino a otto canali in qualsiasi combinazione di canali o canali importati definiti.</span><span class="sxs-lookup"><span data-stu-id="97a82-110">You can specify up to eight channels in any combination of imported channels or channels that you define.</span></span>

<span data-ttu-id="97a82-111">Il canale deve essere di uno dei quattro tipi seguenti: amministratore, operativo, analitico e debug.</span><span class="sxs-lookup"><span data-stu-id="97a82-111">The channel must be of one of four types: Admin, Operational, Analytic, and Debug.</span></span> <span data-ttu-id="97a82-112">Ogni tipo di canale ha un pubblico desiderato, che determina il tipo di eventi scritti sul canale.</span><span class="sxs-lookup"><span data-stu-id="97a82-112">Each channel type has an intended audience, which determines the type of events that you write to the channel.</span></span> <span data-ttu-id="97a82-113">Per una descrizione di ogni tipo, vedere il tipo complesso [**ChannelType**](eventmanifestschema-channeltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="97a82-113">For a description of each type, see the [**ChannelType**](eventmanifestschema-channeltype-complextype.md) complex type.</span></span>

<span data-ttu-id="97a82-114">Per specificare il canale in cui viene scritto un evento, impostare l'attributo del **canale** della definizione dell'evento sullo stesso valore dell'attributo **figlio** della definizione del canale.</span><span class="sxs-lookup"><span data-stu-id="97a82-114">To specify the channel to which an event is written, set the event definition's **channel** attribute to the same value as the channel definition's **chid** attribute.</span></span> <span data-ttu-id="97a82-115">Gli eventi possono essere scritti in un solo canale alla volta, ma possono essere raccolti anche fino a 7 altre sessioni ETW nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="97a82-115">Events can only be written to one channel at a time, but can also be collected by up to 7 other ETW sessions at the same time.</span></span>

<span data-ttu-id="97a82-116">Nell'esempio seguente viene illustrato come importare un canale.</span><span class="sxs-lookup"><span data-stu-id="97a82-116">The following example shows how to import a channel.</span></span> <span data-ttu-id="97a82-117">È necessario impostare gli attributi **figlio** e **Name** .</span><span class="sxs-lookup"><span data-stu-id="97a82-117">You must set the **chid** and **name** attributes.</span></span> <span data-ttu-id="97a82-118">L'attributo **figlio** identifica in modo univoco il canale. ogni identificatore del canale nell'elenco dei canali deve essere univoco.</span><span class="sxs-lookup"><span data-stu-id="97a82-118">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="97a82-119">Impostare l'attributo **Name** sullo stesso nome utilizzato dal provider durante la definizione del canale.</span><span class="sxs-lookup"><span data-stu-id="97a82-119">Set the **name** attribute to the same name that the provider used when it defined the channel.</span></span>


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

<span data-ttu-id="97a82-120">Anche se Winmeta.xml definisce i canali legacy che è possibile importare, è consigliabile non utilizzarli a meno che non si supportino i consumer legacy che utilizzano gli eventi dei canali legacy (ad esempio, applicazione o sistema).</span><span class="sxs-lookup"><span data-stu-id="97a82-120">Although Winmeta.xml defines legacy channels that you can import, you should not use them unless you are supporting legacy consumers that consume events out of the legacy channels (for example, Application or System).</span></span> <span data-ttu-id="97a82-121">Il file di Winmeta.xml è incluso nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="97a82-121">The Winmeta.xml file is included in the Windows SDK.</span></span>

<span data-ttu-id="97a82-122">Nell'esempio seguente viene illustrato come definire un canale.</span><span class="sxs-lookup"><span data-stu-id="97a82-122">The following example shows how to define a channel.</span></span> <span data-ttu-id="97a82-123">È necessario impostare gli attributi **figlio**, **Name** e **Type** .</span><span class="sxs-lookup"><span data-stu-id="97a82-123">You must set the **chid**, **name**, and **type** attributes.</span></span> <span data-ttu-id="97a82-124">L'attributo **figlio** identifica in modo univoco il canale. ogni identificatore del canale nell'elenco dei canali deve essere univoco.</span><span class="sxs-lookup"><span data-stu-id="97a82-124">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="97a82-125">Impostare l'attributo **figlio** su un valore univoco per i canali elencati dal provider. si fa riferimento all'identificatore del canale in una o più definizioni di evento.</span><span class="sxs-lookup"><span data-stu-id="97a82-125">Set the **chid** attribute to a value that is unique for the channels that your provider lists; the channel identifier is referenced in one or more of your event definitions.</span></span> <span data-ttu-id="97a82-126">La convenzione per la denominazione del canale consiste nell'usare il nome del provider e il tipo di canale nel formato *providerName* / *channelType*.</span><span class="sxs-lookup"><span data-stu-id="97a82-126">The convention for naming the channel is to use the provider name and channel type in the form, *providername*/*channeltype*.</span></span>

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
