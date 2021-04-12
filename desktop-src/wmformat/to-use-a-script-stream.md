---
title: Per usare un flusso di script
description: Per usare un flusso di script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, flussi di script
- Formati di sistema avanzati (ASF), flussi di script
- ASF (formato avanzato dei sistemi), flussi di script
- flussi di script, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332556"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="29f08-107">Per usare un flusso di script</span><span class="sxs-lookup"><span data-stu-id="29f08-107">To Use a Script Stream</span></span>

<span data-ttu-id="29f08-108">In questa sezione viene descritto come inviare i dati di script al writer per l'inclusione in un file.</span><span class="sxs-lookup"><span data-stu-id="29f08-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="29f08-109">Per informazioni sull'inclusione di flussi di script nei profili, vedere [configurazione di tipi di flusso arbitrari](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="29f08-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="29f08-110">Ogni script è costituito da due stringhe, una stringa di *tipo* e una stringa di *argomento* .</span><span class="sxs-lookup"><span data-stu-id="29f08-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="29f08-111">I dati di script devono essere formattati prima di essere inviati al writer.</span><span class="sxs-lookup"><span data-stu-id="29f08-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="29f08-112">Le stringhe devono essere concatenate, separate da un carattere **null** e terminate con un carattere **null** .</span><span class="sxs-lookup"><span data-stu-id="29f08-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="29f08-113">Nell'esempio seguente viene illustrato uno script legittimo:</span><span class="sxs-lookup"><span data-stu-id="29f08-113">The following example shows a legitimate script:</span></span>



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="29f08-114">U</span><span class="sxs-lookup"><span data-stu-id="29f08-114">U</span></span>   | <span data-ttu-id="29f08-115">R</span><span class="sxs-lookup"><span data-stu-id="29f08-115">R</span></span>   | <span data-ttu-id="29f08-116">L</span><span class="sxs-lookup"><span data-stu-id="29f08-116">L</span></span>   | <span data-ttu-id="29f08-117">\\0</span><span class="sxs-lookup"><span data-stu-id="29f08-117">\\0</span></span> | <span data-ttu-id="29f08-118">h</span><span class="sxs-lookup"><span data-stu-id="29f08-118">h</span></span>   | <span data-ttu-id="29f08-119">u</span><span class="sxs-lookup"><span data-stu-id="29f08-119">t</span></span>   | <span data-ttu-id="29f08-120">u</span><span class="sxs-lookup"><span data-stu-id="29f08-120">t</span></span>   | <span data-ttu-id="29f08-121">p</span><span class="sxs-lookup"><span data-stu-id="29f08-121">p</span></span>   | <span data-ttu-id="29f08-122">:</span><span class="sxs-lookup"><span data-stu-id="29f08-122">:</span></span>   | /   | /   | <span data-ttu-id="29f08-123">w</span><span class="sxs-lookup"><span data-stu-id="29f08-123">w</span></span>   | <span data-ttu-id="29f08-124">w</span><span class="sxs-lookup"><span data-stu-id="29f08-124">w</span></span>   | <span data-ttu-id="29f08-125">w</span><span class="sxs-lookup"><span data-stu-id="29f08-125">w</span></span>   | <span data-ttu-id="29f08-126">.</span><span class="sxs-lookup"><span data-stu-id="29f08-126">.</span></span>   | <span data-ttu-id="29f08-127">a</span><span class="sxs-lookup"><span data-stu-id="29f08-127">a</span></span>   | <span data-ttu-id="29f08-128">d</span><span class="sxs-lookup"><span data-stu-id="29f08-128">d</span></span>   | <span data-ttu-id="29f08-129">a</span><span class="sxs-lookup"><span data-stu-id="29f08-129">a</span></span>   | <span data-ttu-id="29f08-130">u</span><span class="sxs-lookup"><span data-stu-id="29f08-130">t</span></span>   | <span data-ttu-id="29f08-131">u</span><span class="sxs-lookup"><span data-stu-id="29f08-131">u</span></span>   | <span data-ttu-id="29f08-132">m</span><span class="sxs-lookup"><span data-stu-id="29f08-132">m</span></span>   | <span data-ttu-id="29f08-133">.</span><span class="sxs-lookup"><span data-stu-id="29f08-133">.</span></span>   | <span data-ttu-id="29f08-134">c</span><span class="sxs-lookup"><span data-stu-id="29f08-134">c</span></span>   | <span data-ttu-id="29f08-135">o</span><span class="sxs-lookup"><span data-stu-id="29f08-135">o</span></span>   | <span data-ttu-id="29f08-136">m</span><span class="sxs-lookup"><span data-stu-id="29f08-136">m</span></span>   | <span data-ttu-id="29f08-137">\\0</span><span class="sxs-lookup"><span data-stu-id="29f08-137">\\0</span></span> |



 

<span data-ttu-id="29f08-138">Ogni coppia di comandi di script deve essere scritta come esempio per il writer.</span><span class="sxs-lookup"><span data-stu-id="29f08-138">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="29f08-139">Per ulteriori informazioni sulla scrittura di esempi, vedere [per scrivere esempi](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="29f08-139">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="29f08-140">Quando viene riprodotto il file ASF, i comandi di script vengono recapitati dal lettore (o dal lettore sincrono) nell'ordine temporale della presentazione.</span><span class="sxs-lookup"><span data-stu-id="29f08-140">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="29f08-141">È responsabilità dell'applicazione analizzare le due stringhe e rispondere al comando script.</span><span class="sxs-lookup"><span data-stu-id="29f08-141">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="29f08-142">Quando si usa il DRM per crittografare un file, nessun comando di script può avere un tempo di presentazione pari a 0.</span><span class="sxs-lookup"><span data-stu-id="29f08-142">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="29f08-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29f08-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f08-144">**Uso di comandi script**</span><span class="sxs-lookup"><span data-stu-id="29f08-144">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




