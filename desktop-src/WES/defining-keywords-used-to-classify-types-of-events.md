---
title: Definizione di parole chiave utilizzate per classificare i tipi di eventi
description: I provider usano parole chiave per classificare diversi tipi di eventi.
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "103858093"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a><span data-ttu-id="f4569-103">Definizione di parole chiave utilizzate per classificare i tipi di eventi</span><span class="sxs-lookup"><span data-stu-id="f4569-103">Defining Keywords Used to Classify Types of Events</span></span>

<span data-ttu-id="f4569-104">I provider usano parole chiave per classificare diversi tipi di eventi.</span><span class="sxs-lookup"><span data-stu-id="f4569-104">Providers use keywords to classify different types of events.</span></span> <span data-ttu-id="f4569-105">Ad esempio, è possibile creare una parola chiave per tutti gli eventi di lettura e quindi applicare la parola chiave Read a qualsiasi evento che esegue un'operazione di lettura, ad esempio la lettura da un file o un registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f4569-105">For example, you can create a keyword for all read events and then apply the read keyword to any event that performs a read operation such as reading from a file or registry.</span></span> <span data-ttu-id="f4569-106">I consumer possono quindi utilizzare i valori di bit della parola chiave per filtrare per la classificazione di eventi diversa.</span><span class="sxs-lookup"><span data-stu-id="f4569-106">Consumers could then use the keyword bit values to filter for different classification of events.</span></span> <span data-ttu-id="f4569-107">Ad esempio, il consumer può richiedere tutti gli eventi di lettura o tutti gli eventi di lettura dall'attività X (se si raggruppano anche gli eventi per attività).</span><span class="sxs-lookup"><span data-stu-id="f4569-107">For example, the consumer could request all read events or all read events from task X (if you also group events by task).</span></span> <span data-ttu-id="f4569-108">Per definire una parola chiave, usare l'elemento **keyword** .</span><span class="sxs-lookup"><span data-stu-id="f4569-108">To define a keyword, use the **keyword** element.</span></span>

<span data-ttu-id="f4569-109">Una sessione di traccia ETW può utilizzare le parole chiave, nello stesso modo in cui viene utilizzato il livello, per limitare gli eventi che il servizio ETW scrive nel file di log di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="f4569-109">An ETW tracing session can use the keywords (in the same way that it uses level) to limit the events that the ETW service writes to its event tracing log file.</span></span> <span data-ttu-id="f4569-110">Una sessione di traccia può abilitare il provider utilizzando due set di maschere di maschera di parole chiave: maschera di bit "any" in cui viene scritto l'evento se uno dei bit della parola chiave dell'evento corrisponde a uno dei bit impostati in questa maschera e una maschera di bit "All" dove per gli eventi corrispondenti al caso "any", l'evento viene scritto solo se tutti i bit della maschera "All" sono presenti nella maschera di bit della parola chiave dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f4569-110">A tracing session can enable the provider using two sets of keyword bitmasks: an "Any" bitmask where the event is written if any of the event's keyword bits match any of the bits set in this mask, and an "All" bitmask where for those events that matched the "Any" case, the event is written only if all of the bits in the "All" mask exist in the event's keyword bitmask.</span></span>

<span data-ttu-id="f4569-111">Se, ad esempio, il provider definisce un evento che specifica una parola chiave Read (bit 0) e una parola chiave Local Access (bit 1), e un secondo evento che specifica una parola chiave Read (bit 0) e una parola chiave Remote Access (bit 2), è possibile impostare la maschera di bit "any" su 1 per ricevere tutti gli eventi di lettura oppure impostare la maschera di bit "any" su 1 e la maschera di bit "All" su 3 per ricevere solo le letture locali.</span><span class="sxs-lookup"><span data-stu-id="f4569-111">For example, if the provider defines an event that specifies a read keyword (bit 0) and a local access keyword (bit 1), and a second event that specifies a read keyword (bit 0) and a remote access keyword (bit 2), you could set the "Any" bitmask to 1 to receive all read events, or you could set the "Any" bitmask to 1 and "All" bitmask to 3 to receive only local reads.</span></span>

<span data-ttu-id="f4569-112">È necessario specificare gli attributi **Name** e **mask** della parola chiave.</span><span class="sxs-lookup"><span data-stu-id="f4569-112">You must specify the keyword's **name** and **mask** attributes.</span></span> <span data-ttu-id="f4569-113">La maschera deve impostare un solo bit, tra il bit 0 e il bit 47.</span><span class="sxs-lookup"><span data-stu-id="f4569-113">The mask must set only one bit, between bit 0 and bit 47.</span></span> <span data-ttu-id="f4569-114">Sono riservati BITS da 48 a 64.</span><span class="sxs-lookup"><span data-stu-id="f4569-114">Bits 48 through 64 are reserved.</span></span>

<span data-ttu-id="f4569-115">Gli attributi **Symbol** e **Message** sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="f4569-115">The **symbol** and **message** attributes are optional.</span></span>

<span data-ttu-id="f4569-116">Nell'esempio seguente viene illustrato come definire una parola chiave.</span><span class="sxs-lookup"><span data-stu-id="f4569-116">The following example shows how to define a keyword.</span></span>

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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

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
