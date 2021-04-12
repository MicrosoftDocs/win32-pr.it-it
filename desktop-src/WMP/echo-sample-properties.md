---
title: Proprietà di esempio Echo
description: Proprietà di esempio Echo
ms.assetid: 16f6f963-d746-42dc-872f-6f4db296cab9
keywords:
- Plug-in di Windows Media Player, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ae368a75817320e346dab7e3061fb6b3d7d490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396362"
---
# <a name="echo-sample-properties"></a><span data-ttu-id="c2abf-108">Proprietà di esempio Echo</span><span class="sxs-lookup"><span data-stu-id="c2abf-108">Echo Sample Properties</span></span>

<span data-ttu-id="c2abf-109">L'esempio Echo espone due proprietà: il ritardo e il livello di effetto (Wet Mix).</span><span class="sxs-lookup"><span data-stu-id="c2abf-109">The Echo sample exposes two properties: the delay time and the effect level (wet mix).</span></span> <span data-ttu-id="c2abf-110">Il valore per il livello di segnale secco (mix secco) viene sempre derivato dal valore Wet Mix.</span><span class="sxs-lookup"><span data-stu-id="c2abf-110">The value for the dry signal level (dry mix) is always derived from the wet mix value.</span></span> <span data-ttu-id="c2abf-111">È necessario modificare il codice esistente e aggiungere un nuovo codice per rendere accessibili queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c2abf-111">You need to modify existing code and add some new code to make these properties accessible.</span></span>

<span data-ttu-id="c2abf-112">Le sezioni seguenti illustrano come modificare il codice delle proprietà:</span><span class="sxs-lookup"><span data-stu-id="c2abf-112">The following sections explain how to modify the properties code:</span></span>

-   [<span data-ttu-id="c2abf-113">Funzionamento delle proprietà</span><span class="sxs-lookup"><span data-stu-id="c2abf-113">How Properties Work</span></span>](how-properties-work.md)
-   [<span data-ttu-id="c2abf-114">Variabili per archiviare le proprietà</span><span class="sxs-lookup"><span data-stu-id="c2abf-114">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="c2abf-115">Modifica della proprietà scale</span><span class="sxs-lookup"><span data-stu-id="c2abf-115">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="c2abf-116">Aggiunta della proprietà Wet Mix</span><span class="sxs-lookup"><span data-stu-id="c2abf-116">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="c2abf-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2abf-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2abf-118">**Esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="c2abf-118">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




