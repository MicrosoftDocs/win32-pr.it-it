---
title: Modifica della pagina delle proprietà di esempio Echo
description: Modifica della pagina delle proprietà di esempio Echo
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395735"
---
# <a name="modifying-the-echo-sample-property-page"></a><span data-ttu-id="26a43-108">Modifica della pagina delle proprietà di esempio Echo</span><span class="sxs-lookup"><span data-stu-id="26a43-108">Modifying the Echo Sample Property Page</span></span>

<span data-ttu-id="26a43-109">L'implementazione predefinita della pagina delle proprietà fornita dall'esempio di plug-in della procedura guidata per il plug-in di Windows Media Player contiene un singolo controllo casella di modifica che riceve il fattore di scala dall'utente.</span><span class="sxs-lookup"><span data-stu-id="26a43-109">The default property page implementation provided by the Windows Media Player Plug-in Wizard DSP plug-in sample contains a single edit box control that receives the scale factor from the user.</span></span> <span data-ttu-id="26a43-110">È necessario modificare la pagina delle proprietà per ricevere i due valori di proprietà usati dall'esempio Echo.</span><span class="sxs-lookup"><span data-stu-id="26a43-110">You need to modify the property page to receive the two property values used by the Echo sample.</span></span>

<span data-ttu-id="26a43-111">Per una panoramica delle pagine delle proprietà del plug-in DSP, vedere [implementazione di un plug-in DSP audio](implementing-an-audio-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="26a43-111">For an overview of DSP plug-in property pages, see [Implementing an Audio DSP Plug-in](implementing-an-audio-dsp-plug-in.md).</span></span>

<span data-ttu-id="26a43-112">Le sezioni seguenti illustrano il processo di modifica della pagina delle proprietà di esempio:</span><span class="sxs-lookup"><span data-stu-id="26a43-112">The following sections step you through the process of modifying the sample property page:</span></span>

-   [<span data-ttu-id="26a43-113">Modifica della risorsa della finestra di dialogo Echo</span><span class="sxs-lookup"><span data-stu-id="26a43-113">Modifying the Echo Dialog Resource</span></span>](modifying-the-echo-dialog-resource.md)
-   [<span data-ttu-id="26a43-114">Aggiunta e modifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="26a43-114">Adding and Modifying the Events</span></span>](adding-and-modifying-the-events.md)
-   [<span data-ttu-id="26a43-115">Modo in cui l'esempio Echo rende permanente i dati</span><span class="sxs-lookup"><span data-stu-id="26a43-115">How the Echo Sample Persists Data</span></span>](how-the-echo-sample-persists-data.md)
-   [<span data-ttu-id="26a43-116">Implementazione di CEchoPropPage:: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="26a43-116">Implementing CEchoPropPage::OnInitDialog</span></span>](implementing-cechoproppage--oninitdialog.md)
-   [<span data-ttu-id="26a43-117">Implementazione di CEchoPropPage:: Apply</span><span class="sxs-lookup"><span data-stu-id="26a43-117">Implementing CEchoPropPage::Apply</span></span>](implementing-cechoproppage--apply.md)
-   [<span data-ttu-id="26a43-118">Implementazione di CEcho:: FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="26a43-118">Implementing CEcho::FinalConstruct</span></span>](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a><span data-ttu-id="26a43-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26a43-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26a43-120">**Esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="26a43-120">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




