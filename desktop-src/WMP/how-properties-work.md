---
title: Funzionamento delle proprietà
description: Funzionamento delle proprietà
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Plug-in di Windows Media Player, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711563"
---
# <a name="how-properties-work"></a><span data-ttu-id="d5562-108">Funzionamento delle proprietà</span><span class="sxs-lookup"><span data-stu-id="d5562-108">How Properties Work</span></span>

<span data-ttu-id="d5562-109">I valori delle proprietà vengono archiviati in variabili membro.</span><span class="sxs-lookup"><span data-stu-id="d5562-109">Property values are stored in member variables.</span></span>

<span data-ttu-id="d5562-110">Le proprietà vengono rese accessibili dalle coppie di metodi.</span><span class="sxs-lookup"><span data-stu-id="d5562-110">Properties are made accessible by method pairs.</span></span> <span data-ttu-id="d5562-111">Un metodo fornisce l'implementazione per specificare il valore della proprietà. il nome inizia con put \_ .</span><span class="sxs-lookup"><span data-stu-id="d5562-111">One method provides the implementation to specify the property value; its name starts with put\_.</span></span> <span data-ttu-id="d5562-112">L'altro metodo fornisce l'implementazione per recuperare il valore della proprietà. il nome inizia con Get \_ .</span><span class="sxs-lookup"><span data-stu-id="d5562-112">The other method provides the implementation to retrieve the property value; its name starts with get\_.</span></span> <span data-ttu-id="d5562-113">La definizione dell'interfaccia è in Echo. idl.</span><span class="sxs-lookup"><span data-stu-id="d5562-113">The interface definition is in Echo.idl.</span></span> <span data-ttu-id="d5562-114">I prototipi dei metodi di proprietà si trovano in Echo. h.</span><span class="sxs-lookup"><span data-stu-id="d5562-114">The property method prototypes are in Echo.h.</span></span> <span data-ttu-id="d5562-115">Sono implementati in Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="d5562-115">They are implemented in Echo.cpp.</span></span>

<span data-ttu-id="d5562-116">Nelle tre sezioni successive verrà illustrato come modificare i metodi di proprietà esistenti in base alle proprie esigenze e come aggiungere i metodi per una proprietà aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="d5562-116">The next three sections will show you how to modify the existing property methods to suit your needs and how to add the methods for an additional property.</span></span>

-   [<span data-ttu-id="d5562-117">Variabili per archiviare le proprietà</span><span class="sxs-lookup"><span data-stu-id="d5562-117">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="d5562-118">Modifica della proprietà scale</span><span class="sxs-lookup"><span data-stu-id="d5562-118">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="d5562-119">Aggiunta della proprietà Wet Mix</span><span class="sxs-lookup"><span data-stu-id="d5562-119">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="d5562-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5562-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5562-121">**Proprietà di esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="d5562-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




