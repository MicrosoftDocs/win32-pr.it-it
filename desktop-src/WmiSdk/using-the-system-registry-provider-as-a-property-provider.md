---
description: È possibile utilizzare il provider del registro di sistema come istanza o provider di proprietà.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Usare il provider del registro di sistema come provider di proprietà
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315186"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a><span data-ttu-id="5ea47-103">Usare il provider del registro di sistema come provider di proprietà</span><span class="sxs-lookup"><span data-stu-id="5ea47-103">Use the System Registry Provider as a Property Provider</span></span>

<span data-ttu-id="5ea47-104">È possibile utilizzare il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) come istanza o provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ea47-104">You can use the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) as either an instance or a property provider.</span></span>

<span data-ttu-id="5ea47-105">Se si sceglie di accedere alle interfacce del provider di proprietà, è necessario contrassegnare le classi WMI per indicare l'intenzione.</span><span class="sxs-lookup"><span data-stu-id="5ea47-105">If you choose to access the property provider interfaces, you must mark your WMI classes to indicate your intention.</span></span>

<span data-ttu-id="5ea47-106">**Per utilizzare il provider del registro di sistema come provider di proprietà**</span><span class="sxs-lookup"><span data-stu-id="5ea47-106">**To use the system registry provider as a property provider**</span></span>

-   <span data-ttu-id="5ea47-107">Definire la classe WMI con i qualificatori standard **DynProps**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)e **PropertyContext** .</span><span class="sxs-lookup"><span data-stu-id="5ea47-107">Define your WMI class with the **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** standard qualifiers.</span></span>

    <span data-ttu-id="5ea47-108">Il qualificatore **DynProps** identifica una classe come avente proprietà gestite dal provider di proprietà identificato dal qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="5ea47-108">The **DynProps** qualifier identifies a class as having properties that are maintained by the property provider identified by the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span> <span data-ttu-id="5ea47-109">Il qualificatore **PropertyContext** specifica il nome del valore del registro di sistema da archiviare con la proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ea47-109">The **PropertyContext** qualifier specifies the name of the registry value to be stored by the property.</span></span> <span data-ttu-id="5ea47-110">Il formato del qualificatore **PropertyContext** è uguale al formato del qualificatore **ClassContext** con valori *valueName* e *Expression* aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5ea47-110">The format of the **PropertyContext** qualifier is the same as the format of the **ClassContext** qualifier with additional *valuename* and *expression* values.</span></span>

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    <span data-ttu-id="5ea47-111">*ValueName* ed *Expression* sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="5ea47-111">Both *valuename* and *expression* are optional.</span></span> <span data-ttu-id="5ea47-112">L'impostazione *valueName* viene usata solo se il valore del registro di sistema ha un nome.</span><span class="sxs-lookup"><span data-stu-id="5ea47-112">The *valuename* setting is only used if the registry value has a name.</span></span> <span data-ttu-id="5ea47-113">L' *espressione* è inoltre facoltativa e viene utilizzata per i dati del descrittore di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ea47-113">The *expression* is also optional and is used for resource descriptor data.</span></span> <span data-ttu-id="5ea47-114">Per ulteriori informazioni, vedere [Descrizione di una risorsa per il registro di sistema](describing-a-resource-for-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="5ea47-114">For more information, see [Describing a Resource for the Registry](describing-a-resource-for-the-registry.md).</span></span>

    <span data-ttu-id="5ea47-115">Nell'esempio di codice seguente viene illustrato il modo in cui la classe utilizza il provider del registro di sistema come provider di proprietà per mantenere le proprietà colonne.</span><span class="sxs-lookup"><span data-stu-id="5ea47-115">The following code example shows how the class uses the System Registry provider as a property provider to maintain its nonkey properties.</span></span>

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 
