---
title: Configurazione di flussi VBR
description: Configurazione di flussi VBR
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- flussi, configurazione di flussi VBR
- flussi, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, interfaccia IWMPropertyVault
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956182"
---
# <a name="configuring-vbr-streams"></a><span data-ttu-id="52430-109">Configurazione di flussi VBR</span><span class="sxs-lookup"><span data-stu-id="52430-109">Configuring VBR Streams</span></span>

<span data-ttu-id="52430-110">È possibile utilizzare la codifica a velocità in bit variabile (VBR) per produrre flussi di alta qualità per i file locali o per il download e la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="52430-110">You can use variable bit rate (VBR) encoding to produce high quality streams for local files or for downloading and playing.</span></span> <span data-ttu-id="52430-111">Sono disponibili tre opzioni per VBR: basata sulla qualità (un passaggio), non vincolato (due passaggi) e vincolato (due passaggi).</span><span class="sxs-lookup"><span data-stu-id="52430-111">There are three options for VBR: quality-based (one-pass), unconstrained (two-pass), and constrained (two-pass).</span></span> <span data-ttu-id="52430-112">Per ulteriori informazioni sui tipi di codifica VBR, vedere la pagina relativa alla [codifica con velocità in bit variabile (VBR)](variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="52430-112">For more information about the types of VBR encoding, see [Variable Bit Rate (VBR) Encoding](variable-bit-rate--vbr--encoding.md).</span></span>

<span data-ttu-id="52430-113">È possibile configurare la codifica VBR in un profilo impostando le proprietà con l'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) .</span><span class="sxs-lookup"><span data-stu-id="52430-113">You can configure VBR encoding in a profile by setting properties with the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface.</span></span> <span data-ttu-id="52430-114">Nella tabella seguente vengono descritte le proprietà utilizzate per configurare la codifica VBR.</span><span class="sxs-lookup"><span data-stu-id="52430-114">The following table describes the properties used to configure VBR encoding.</span></span>



| <span data-ttu-id="52430-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52430-115">Property</span></span>                     | <span data-ttu-id="52430-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52430-116">Description</span></span>                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52430-117">**g \_ wszVBREnabled**</span><span class="sxs-lookup"><span data-stu-id="52430-117">**g\_wszVBREnabled**</span></span>         | <span data-ttu-id="52430-118">.</span><span class="sxs-lookup"><span data-stu-id="52430-118">Boolean value.</span></span> <span data-ttu-id="52430-119">Impostare su true per utilizzare la codifica VBR.</span><span class="sxs-lookup"><span data-stu-id="52430-119">Set to True to use VBR encoding.</span></span>                                                   |
| <span data-ttu-id="52430-120">**g \_ wszVBRQuality**</span><span class="sxs-lookup"><span data-stu-id="52430-120">**g\_wszVBRQuality**</span></span>         | <span data-ttu-id="52430-121">Valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="52430-121">**DWORD** value.</span></span> <span data-ttu-id="52430-122">Impostare sul livello di qualità desiderato (da 1 a 100) per la codifica VBR basata sulla qualità.</span><span class="sxs-lookup"><span data-stu-id="52430-122">Set to the desired quality level (1 to 100) for quality-based VBR encoding.</span></span>      |
| <span data-ttu-id="52430-123">**g \_ wszVBRBitrateMax**</span><span class="sxs-lookup"><span data-stu-id="52430-123">**g\_wszVBRBitrateMax**</span></span>      | <span data-ttu-id="52430-124">Valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="52430-124">**DWORD** value.</span></span> <span data-ttu-id="52430-125">Impostare sulla velocità in bit massima, in bit al secondo, per la codifica VBR vincolata.</span><span class="sxs-lookup"><span data-stu-id="52430-125">Set to the maximum bit rate, in bits per second, for constrained VBR encoding.</span></span>   |
| <span data-ttu-id="52430-126">**g \_ wszVBRBufferWindowMax**</span><span class="sxs-lookup"><span data-stu-id="52430-126">**g\_wszVBRBufferWindowMax**</span></span> | <span data-ttu-id="52430-127">Valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="52430-127">**DWORD** value.</span></span> <span data-ttu-id="52430-128">Impostare sulla finestra massima del buffer, in millisecondi, per la codifica VBR vincolata.</span><span class="sxs-lookup"><span data-stu-id="52430-128">Set to the maximum buffer window, in milliseconds, for constrained VBR encoding.</span></span> |



 

<span data-ttu-id="52430-129">Le sezioni seguenti descrivono come usare i diversi tipi di codifica della velocità in bit variabile.</span><span class="sxs-lookup"><span data-stu-id="52430-129">The following sections describe how to use the different types of variable bit rate encoding.</span></span>



| <span data-ttu-id="52430-130">Sezione</span><span class="sxs-lookup"><span data-stu-id="52430-130">Section</span></span>                                                              | <span data-ttu-id="52430-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52430-131">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52430-132">Per configurare Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="52430-132">To Configure Quality-Based VBR</span></span>](to-configure-quality-based-vbr.md) | <span data-ttu-id="52430-133">Viene descritto come usare la codifica della velocità in bit variabile in base a un livello di qualità statico.</span><span class="sxs-lookup"><span data-stu-id="52430-133">Describes how to use variable bit rate encoding based on a static quality level.</span></span>                                   |
| [<span data-ttu-id="52430-134">Per configurare il VBR non vincolato</span><span class="sxs-lookup"><span data-stu-id="52430-134">To Configure Unconstrained VBR</span></span>](to-configure-unconstrained-vbr.md) | <span data-ttu-id="52430-135">Viene descritto come usare la codifica della velocità in bit variabile in base a una velocità in bit media di destinazione senza un valore di picco esplicito.</span><span class="sxs-lookup"><span data-stu-id="52430-135">Describes how to use variable bit rate encoding based on a target average bit rate without an explicit peak value.</span></span> |
| [<span data-ttu-id="52430-136">Per configurare il VBR vincolato</span><span class="sxs-lookup"><span data-stu-id="52430-136">To Configure Constrained VBR</span></span>](to-configure-constrained-vbr.md)     | <span data-ttu-id="52430-137">Viene descritto come usare la codifica della velocità in bit variabile in base a una velocità in bit media di destinazione e a un valore di picco esplicito.</span><span class="sxs-lookup"><span data-stu-id="52430-137">Describes how to use variable bit rate encoding based on a target average bit rate and an explicit peak value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="52430-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52430-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52430-139">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="52430-139">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




