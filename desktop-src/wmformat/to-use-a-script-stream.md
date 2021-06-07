---
title: Per usare un flusso di script
description: Per usare un flusso di script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, flussi di script
- Advanced Systems Format (ASF), flussi di script
- ASF (Advanced Systems Format), flussi di script
- flussi di script, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444732"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="a0a20-107">Per usare un flusso di script</span><span class="sxs-lookup"><span data-stu-id="a0a20-107">To Use a Script Stream</span></span>

<span data-ttu-id="a0a20-108">Questa sezione descrive come inviare dati script al writer per l'inclusione in un file.</span><span class="sxs-lookup"><span data-stu-id="a0a20-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="a0a20-109">Per informazioni sull'inclusione di flussi di script nei profili, vedere [Configurazione di tipi di flusso arbitrari.](configuring-arbitrary-stream-types.md)</span><span class="sxs-lookup"><span data-stu-id="a0a20-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="a0a20-110">Ogni script è costituito da due stringhe, una *stringa di tipo* e una stringa *di* argomento.</span><span class="sxs-lookup"><span data-stu-id="a0a20-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="a0a20-111">I dati dello script devono essere formattati prima di essere inviati al writer.</span><span class="sxs-lookup"><span data-stu-id="a0a20-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="a0a20-112">Le stringhe devono essere concatenate, separate da un **carattere NULL** e terminate con un **carattere NULL.**</span><span class="sxs-lookup"><span data-stu-id="a0a20-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="a0a20-113">L'esempio seguente illustra uno script legittimo:</span><span class="sxs-lookup"><span data-stu-id="a0a20-113">The following example shows a legitimate script:</span></span>



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="a0a20-114">U</span><span class="sxs-lookup"><span data-stu-id="a0a20-114">U</span></span>   | <span data-ttu-id="a0a20-115">R</span><span class="sxs-lookup"><span data-stu-id="a0a20-115">R</span></span>   | <span data-ttu-id="a0a20-116">L</span><span class="sxs-lookup"><span data-stu-id="a0a20-116">L</span></span>   | &nbsp; | <span data-ttu-id="a0a20-117">h</span><span class="sxs-lookup"><span data-stu-id="a0a20-117">h</span></span>   | <span data-ttu-id="a0a20-118">t</span><span class="sxs-lookup"><span data-stu-id="a0a20-118">t</span></span>   | <span data-ttu-id="a0a20-119">t</span><span class="sxs-lookup"><span data-stu-id="a0a20-119">t</span></span>   | <span data-ttu-id="a0a20-120">p</span><span class="sxs-lookup"><span data-stu-id="a0a20-120">p</span></span>   | <span data-ttu-id="a0a20-121">:</span><span class="sxs-lookup"><span data-stu-id="a0a20-121">:</span></span>   | /   | /   | <span data-ttu-id="a0a20-122">w</span><span class="sxs-lookup"><span data-stu-id="a0a20-122">w</span></span>   | <span data-ttu-id="a0a20-123">w</span><span class="sxs-lookup"><span data-stu-id="a0a20-123">w</span></span>   | <span data-ttu-id="a0a20-124">w</span><span class="sxs-lookup"><span data-stu-id="a0a20-124">w</span></span>   | <span data-ttu-id="a0a20-125">.</span><span class="sxs-lookup"><span data-stu-id="a0a20-125">.</span></span>   | <span data-ttu-id="a0a20-126">a</span><span class="sxs-lookup"><span data-stu-id="a0a20-126">a</span></span>   | <span data-ttu-id="a0a20-127">d</span><span class="sxs-lookup"><span data-stu-id="a0a20-127">d</span></span>   | <span data-ttu-id="a0a20-128">a</span><span class="sxs-lookup"><span data-stu-id="a0a20-128">a</span></span>   | <span data-ttu-id="a0a20-129">t</span><span class="sxs-lookup"><span data-stu-id="a0a20-129">t</span></span>   | <span data-ttu-id="a0a20-130">u</span><span class="sxs-lookup"><span data-stu-id="a0a20-130">u</span></span>   | <span data-ttu-id="a0a20-131">m</span><span class="sxs-lookup"><span data-stu-id="a0a20-131">m</span></span>   | <span data-ttu-id="a0a20-132">.</span><span class="sxs-lookup"><span data-stu-id="a0a20-132">.</span></span>   | <span data-ttu-id="a0a20-133">c</span><span class="sxs-lookup"><span data-stu-id="a0a20-133">c</span></span>   | <span data-ttu-id="a0a20-134">o</span><span class="sxs-lookup"><span data-stu-id="a0a20-134">o</span></span>   | <span data-ttu-id="a0a20-135">m</span><span class="sxs-lookup"><span data-stu-id="a0a20-135">m</span></span>   | &nbsp; |



 

<span data-ttu-id="a0a20-136">Ogni coppia di comandi script deve essere scritta come esempio nel writer.</span><span class="sxs-lookup"><span data-stu-id="a0a20-136">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="a0a20-137">Per altre informazioni sulla scrittura di esempi, vedere [Per scrivere esempi](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a0a20-137">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="a0a20-138">Quando viene riprodotto il file ASF, i comandi script verranno recapitati dal lettore (o lettore sincrono) in ordine di tempo di presentazione.</span><span class="sxs-lookup"><span data-stu-id="a0a20-138">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="a0a20-139">È responsabilità dell'applicazione analizzare le due stringhe e rispondere al comando script.</span><span class="sxs-lookup"><span data-stu-id="a0a20-139">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="a0a20-140">Quando si usa DRM per crittografare un file, nessun comando script può avere un'ora di presentazione di 0.</span><span class="sxs-lookup"><span data-stu-id="a0a20-140">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a0a20-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0a20-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a20-142">**Uso di comandi script**</span><span class="sxs-lookup"><span data-stu-id="a0a20-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




