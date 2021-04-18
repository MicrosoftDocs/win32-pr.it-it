---
title: Ora di presentazione
description: Ora di presentazione
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows Media Format SDK, tempi di presentazione
- Formato avanzato dei sistemi (ASF), tempi di presentazione
- ASF (formato avanzato dei sistemi), tempi di presentazione
- tempi di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331708"
---
# <a name="presentation-time"></a><span data-ttu-id="08f1d-107">Ora di presentazione</span><span class="sxs-lookup"><span data-stu-id="08f1d-107">Presentation Time</span></span>

<span data-ttu-id="08f1d-108">Un'ora di presentazione è una misurazione del tempo dal primo campione del primo flusso in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="08f1d-108">A presentation time is a measurement of time from the first sample of the first stream in an ASF file.</span></span> <span data-ttu-id="08f1d-109">Questa misurazione, oltre alla maggior parte delle altre misurazioni del tempo usato dagli oggetti di questo SDK, si trova in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="08f1d-109">This measurement, as well as most other measurements of time used by the objects of this SDK, is in 100-nanosecond units.</span></span> <span data-ttu-id="08f1d-110">I tempi di presentazione sono importanti perché consentono la sincronizzazione dei vari flussi in un file.</span><span class="sxs-lookup"><span data-stu-id="08f1d-110">Presentation times are important because they enable the various streams in a file to be synchronized.</span></span> <span data-ttu-id="08f1d-111">È necessario fornire un'ora di presentazione per ogni esempio di input passato al writer.</span><span class="sxs-lookup"><span data-stu-id="08f1d-111">You must supply a presentation time for each input sample you pass to the writer.</span></span> <span data-ttu-id="08f1d-112">A ogni oggetto dati nella sezione dati di un file ASF è associato un tempo di presentazione.</span><span class="sxs-lookup"><span data-stu-id="08f1d-112">Every data object in the data section of an ASF file has a presentation time associated with it.</span></span> <span data-ttu-id="08f1d-113">Ogni esempio di output recuperato dal lettore dispone anche di un'ora di presentazione.</span><span class="sxs-lookup"><span data-stu-id="08f1d-113">Every output sample retrieved by the reader also has a presentation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08f1d-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08f1d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08f1d-115">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="08f1d-115">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="08f1d-116">**Input, flussi e output**</span><span class="sxs-lookup"><span data-stu-id="08f1d-116">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="08f1d-117">**Esempi di supporti**</span><span class="sxs-lookup"><span data-stu-id="08f1d-117">**Media Samples**</span></span>](media-samples.md)
</dt> </dl>

 

 




