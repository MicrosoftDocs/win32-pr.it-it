---
title: Posizionare e spostare rettangoli video nello spazio di composizione
description: Posizionamento e spostamento di rettangoli video nello spazio di composizione
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96955fc2107036299ab6f530eeda76374a0a0315
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909629"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="8f460-103">Posizionare e spostare rettangoli video nello spazio di composizione</span><span class="sxs-lookup"><span data-stu-id="8f460-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="8f460-104">Quando vmR combina più flussi di input, posiziona ogni flusso all'interno di un rettangolo normalizzato, denominato "spazio di composizione".</span><span class="sxs-lookup"><span data-stu-id="8f460-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="8f460-105">All'interno dello spazio di composizione, le coordinate da 0,0, 0,0 a (1,0, 1,0) formano il rettangolo video visibile.</span><span class="sxs-lookup"><span data-stu-id="8f460-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="8f460-106">Tutte le coordinate esterne a questo rettangolo vengono ritagliate.</span><span class="sxs-lookup"><span data-stu-id="8f460-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="8f460-107">Un'applicazione può eseguire effetti speciali con lo spostamento, l'estensione e la riduzione del video da un flusso di input, modificando il rettangolo di destinazione nello spazio di composizione per tale flusso.</span><span class="sxs-lookup"><span data-stu-id="8f460-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="8f460-108">Se le dimensioni del rettangolo specificato sono diverse da quelle del rettangolo video nativo, il video nativo verrà ridotto o adattato.</span><span class="sxs-lookup"><span data-stu-id="8f460-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="8f460-109">Il rettangolo di destinazione viene specificato chiamando il [**metodo IVMRMixerControl::SetOutputRect.**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs)</span><span class="sxs-lookup"><span data-stu-id="8f460-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="8f460-110">Si supponga, ad esempio, che il flusso 0 (che corrisponde al pin 0) contenga il flusso video principale e che il flusso 1 (che corrisponde al pin 1) contenga un video secondario.</span><span class="sxs-lookup"><span data-stu-id="8f460-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="8f460-111">Il flusso 1 può essere posizionato completamente fuori schermo specificando un rettangolo normalizzato di { -1.0f, 0.0f, 0.0f, 1.0f }.</span><span class="sxs-lookup"><span data-stu-id="8f460-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="8f460-112">Il flusso 1 può quindi essere spostato nell'area visibile modificando i lati sinistro e destro del rettangolo nelle chiamate successive a **SetOutputRect:**</span><span class="sxs-lookup"><span data-stu-id="8f460-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



| <span data-ttu-id="8f460-113">Label</span><span class="sxs-lookup"><span data-stu-id="8f460-113">Label</span></span> | <span data-ttu-id="8f460-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8f460-114">Value</span></span> |
|--------|-----------------------------|
| <span data-ttu-id="8f460-115">Tempo</span><span class="sxs-lookup"><span data-stu-id="8f460-115">Time</span></span>   | <span data-ttu-id="8f460-116">Rettangolo</span><span class="sxs-lookup"><span data-stu-id="8f460-116">Rectangle</span></span>                   |
| <span data-ttu-id="8f460-117">t + 0</span><span class="sxs-lookup"><span data-stu-id="8f460-117">t + 0</span></span>  | <span data-ttu-id="8f460-118">{ -1.0f, 0.0f, 0.0f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="8f460-118">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="8f460-119">t + 1</span><span class="sxs-lookup"><span data-stu-id="8f460-119">t + 1</span></span>  | <span data-ttu-id="8f460-120">{ -0.9f, 0.0f, 0.1f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="8f460-120">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="8f460-121">t + 2</span><span class="sxs-lookup"><span data-stu-id="8f460-121">t + 2</span></span>  | <span data-ttu-id="8f460-122">{ -0.8f, 0.0f, 0.2f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="8f460-122">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="8f460-123">...</span><span class="sxs-lookup"><span data-stu-id="8f460-123">...</span></span>    | <span data-ttu-id="8f460-124">...</span><span class="sxs-lookup"><span data-stu-id="8f460-124">...</span></span>                         |
| <span data-ttu-id="8f460-125">t + 10</span><span class="sxs-lookup"><span data-stu-id="8f460-125">t + 10</span></span> | <span data-ttu-id="8f460-126">{ 0.0f, 0.0f, 1.0f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="8f460-126">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![spostamento di un flusso video nello spazio di composizione](images/composition-space.png)

<span data-ttu-id="8f460-128">Al momento t+10, il video dal flusso 1 è completamente visibile.</span><span class="sxs-lookup"><span data-stu-id="8f460-128">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="8f460-129">In questo esempio sono stati mantenute le dimensioni native del flusso 1 durante lo spostamento.</span><span class="sxs-lookup"><span data-stu-id="8f460-129">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="8f460-130">È anche possibile estendere o ridurre il rettangolo per produrre effetti interessanti.</span><span class="sxs-lookup"><span data-stu-id="8f460-130">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="8f460-131">È anche possibile capovolgere il video verticalmente, specificando un valore maggiore per la parte superiore rispetto alla parte inferiore o rispecchiando il video orizzontalmente, specificando un valore maggiore per la parte sinistra rispetto a destra.</span><span class="sxs-lookup"><span data-stu-id="8f460-131">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f460-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f460-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f460-133">Uso della modalità di combinazione vmr</span><span class="sxs-lookup"><span data-stu-id="8f460-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



