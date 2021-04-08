---
title: Implementazione di CEcho DoProcessOutput
description: Implementazione di CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Plug-in di Windows Media Player, metodo DoProcessOutput di esempio Echo
- plug-in, esempio Echo metodo DoProcessOutput
- plug-in di elaborazione dei segnali digitali, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045348"
---
# <a name="implementing-cechodoprocessoutput"></a><span data-ttu-id="4d1b1-108">Implementazione di CEcho::D oProcessOutput</span><span class="sxs-lookup"><span data-stu-id="4d1b1-108">Implementing CEcho::DoProcessOutput</span></span>

<span data-ttu-id="4d1b1-109">Il metodo **DoProcessOutput** esegue l'elaborazione del segnale digitale.</span><span class="sxs-lookup"><span data-stu-id="4d1b1-109">The **DoProcessOutput** method performs the digital signal processing.</span></span> <span data-ttu-id="4d1b1-110">Si tratta del metodo che apporta le modifiche ai dati forniti da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4d1b1-110">This is the method that makes the changes to the data provided by Windows Media Player.</span></span> <span data-ttu-id="4d1b1-111">Si tratta del risultato di questo metodo che verrà visualizzato come effetto Echo quando il plug-in echo sample è completo.</span><span class="sxs-lookup"><span data-stu-id="4d1b1-111">It is the results of this method that you will hear as an echo effect when your Echo sample plug-in is complete.</span></span>

<span data-ttu-id="4d1b1-112">Per questo esempio, il plug-in elaborerà solo audio a 8 bit o a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="4d1b1-112">For this sample, the plug-in will only process 8-bit or 16-bit audio.</span></span> <span data-ttu-id="4d1b1-113">È necessario apportare alcune modifiche al codice di esempio della procedura guidata plug-in per rimuovere le sezioni che elaborano un audio di profondità di bit superiore.</span><span class="sxs-lookup"><span data-stu-id="4d1b1-113">You will need to make some changes to the plug-in wizard sample code to remove the sections that process higher bit depth audio.</span></span> <span data-ttu-id="4d1b1-114">È tuttavia utile studiare queste sezioni, perché è possibile decidere di aggiungere un'implementazione Echo personalizzata per tali formati.</span><span class="sxs-lookup"><span data-stu-id="4d1b1-114">It is worthwhile to study these sections, however, because you may decide to add your own echo implementation for those formats.</span></span>

<span data-ttu-id="4d1b1-115">Le sezioni seguenti illustrano in dettaglio le modifiche che è necessario apportare al codice:</span><span class="sxs-lookup"><span data-stu-id="4d1b1-115">The following sections detail the changes you need to make to the code:</span></span>

-   [<span data-ttu-id="4d1b1-116">Rimozione del codice per elaborare più di 16 bit</span><span class="sxs-lookup"><span data-stu-id="4d1b1-116">Removing the Code to Process Greater than 16 Bits</span></span>](removing-the-code-to-process-greater-than-16-bits.md)
-   [<span data-ttu-id="4d1b1-117">Elaborazione dei dati audio</span><span class="sxs-lookup"><span data-stu-id="4d1b1-117">Processing the Audio Data</span></span>](processing-the-audio-data.md)
-   [<span data-ttu-id="4d1b1-118">Variabili per l'esecuzione dell'elaborazione</span><span class="sxs-lookup"><span data-stu-id="4d1b1-118">Variables to Perform Processing</span></span>](variables-to-perform-processing.md)
-   [<span data-ttu-id="4d1b1-119">Creazione dell'effetto Echo</span><span class="sxs-lookup"><span data-stu-id="4d1b1-119">Creating the Echo Effect</span></span>](creating-the-echo-effect.md)

## <a name="related-topics"></a><span data-ttu-id="4d1b1-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4d1b1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d1b1-121">**Esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="4d1b1-121">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




