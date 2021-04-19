---
title: Modifica di set di impostazioni
description: Modifica di set di impostazioni
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- Visualizzazioni, esempio Glow
- Visualizzazioni personalizzate, esempio Glow
- Guida per programmatori, visualizzazioni
- esempi, visualizzazione bagliore
- Esempio di visualizzazione bagliore
- Visualizzazioni, set di impostazioni
- Visualizzazioni personalizzate, set di impostazioni
- impostazioni predefinite nelle visualizzazioni, esempio Glow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298199"
---
# <a name="changing-presets"></a><span data-ttu-id="95133-111">Modifica di set di impostazioni</span><span class="sxs-lookup"><span data-stu-id="95133-111">Changing Presets</span></span>

<span data-ttu-id="95133-112">Le sezioni di codice del set di impostazioni seguenti sono state modificate per consentire tre set di impostazioni:</span><span class="sxs-lookup"><span data-stu-id="95133-112">The following preset code sections were changed to allow three presets:</span></span>

## <a name="getpresettitle"></a><span data-ttu-id="95133-113">GetPresetTitle</span><span class="sxs-lookup"><span data-stu-id="95133-113">GetPresetTitle</span></span>

<span data-ttu-id="95133-114">Questo codice è stato inserito al posto del codice del set di impostazioni generato:</span><span class="sxs-lookup"><span data-stu-id="95133-114">This code was inserted in place of the generated preset code:</span></span>


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a><span data-ttu-id="95133-115">Enumerazioni</span><span class="sxs-lookup"><span data-stu-id="95133-115">Enumerations</span></span>

<span data-ttu-id="95133-116">L'enumerazione seguente in Glow. h è stata modificata in modo da consentire tre set di impostazioni:</span><span class="sxs-lookup"><span data-stu-id="95133-116">The following enumeration in Glow.h was changed to allow three presets:</span></span>


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a><span data-ttu-id="95133-117">Intestazione della risorsa</span><span class="sxs-lookup"><span data-stu-id="95133-117">Resource Header</span></span>

<span data-ttu-id="95133-118">Le risorse seguenti sono state definite in Resource. h per consentire tre set di impostazioni:</span><span class="sxs-lookup"><span data-stu-id="95133-118">The following resources were defined in Resource.h to allow three presets:</span></span>


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



<span data-ttu-id="95133-119">Si noti che è necessario modificare anche il numero di risorsa del **\_ \_ \_ \_ valore SYMED successivo di APS** in 106.</span><span class="sxs-lookup"><span data-stu-id="95133-119">Note that you must also change the resource number of **\_APS\_NEXT\_SYMED\_VALUE** to 106.</span></span>

## <a name="resource-file"></a><span data-ttu-id="95133-120">File di risorse</span><span class="sxs-lookup"><span data-stu-id="95133-120">Resource File</span></span>

<span data-ttu-id="95133-121">È necessario modificare le seguenti stringhe nel file Glowdll. RC per consentire tre set di impostazioni e assegnare loro i nomi:</span><span class="sxs-lookup"><span data-stu-id="95133-121">The following strings must be changed in the Glowdll.rc file to allow three presets and give them names:</span></span>


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a><span data-ttu-id="95133-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95133-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95133-123">**Esempio Glow**</span><span class="sxs-lookup"><span data-stu-id="95133-123">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




