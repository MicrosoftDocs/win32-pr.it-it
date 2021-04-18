---
title: Posizionare e spostare i rettangoli video nello spazio di composizione
description: Posizionamento e trasferimento di rettangoli video nello spazio di composizione
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766d1ae739e46a2c56bfab81b4243c9dcf6f10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303984"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="cffaa-103">Posizionare e spostare i rettangoli video nello spazio di composizione</span><span class="sxs-lookup"><span data-stu-id="cffaa-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="cffaa-104">Quando VMR unisce più flussi di input, posiziona ogni flusso all'interno di un rettangolo normalizzato, denominato "spazio di composizione".</span><span class="sxs-lookup"><span data-stu-id="cffaa-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="cffaa-105">All'interno dello spazio di composizione, le coordinate (0,0, 0,0) in (1,0, 1,0) formano il rettangolo video visibile.</span><span class="sxs-lookup"><span data-stu-id="cffaa-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="cffaa-106">Tutte le coordinate che esulano da questo rettangolo vengono ritagliate.</span><span class="sxs-lookup"><span data-stu-id="cffaa-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="cffaa-107">Un'applicazione può eseguire effetti speciali con lo spostamento, l'allungamento e la compattazione del video da un flusso di input, modificando il rettangolo di destinazione nello spazio di composizione per quel flusso.</span><span class="sxs-lookup"><span data-stu-id="cffaa-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="cffaa-108">Se il rettangolo specificato ha dimensioni diverse rispetto al rettangolo del video nativo, il video nativo verrà compattato o allungato per adattarlo.</span><span class="sxs-lookup"><span data-stu-id="cffaa-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="cffaa-109">Il rettangolo di destinazione viene specificato chiamando il metodo [**IVMRMixerControl:: SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .</span><span class="sxs-lookup"><span data-stu-id="cffaa-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="cffaa-110">Si supponga, ad esempio, che il flusso 0 (che corrisponde al pin 0) contenga il flusso video principale e il flusso 1 (che corrisponde al pin 1) contenga un video secondario.</span><span class="sxs-lookup"><span data-stu-id="cffaa-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="cffaa-111">Il flusso 1 può essere posizionato completamente Offscreen specificando un rettangolo normalizzato di {-1.0 f, 0,0 f, 0,0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="cffaa-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="cffaa-112">Il flusso 1 può quindi essere spostato nell'area visibile modificando il lato sinistro e destro del rettangolo sulle chiamate successive a **SetOutputRect**:</span><span class="sxs-lookup"><span data-stu-id="cffaa-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



|        |                             |
|--------|-----------------------------|
| <span data-ttu-id="cffaa-113">Tempo</span><span class="sxs-lookup"><span data-stu-id="cffaa-113">Time</span></span>   | <span data-ttu-id="cffaa-114">Rettangolo</span><span class="sxs-lookup"><span data-stu-id="cffaa-114">Rectangle</span></span>                   |
| <span data-ttu-id="cffaa-115">t + 0</span><span class="sxs-lookup"><span data-stu-id="cffaa-115">t + 0</span></span>  | <span data-ttu-id="cffaa-116">{-1.0 f, 0,0 f, 0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cffaa-116">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="cffaa-117">t + 1</span><span class="sxs-lookup"><span data-stu-id="cffaa-117">t + 1</span></span>  | <span data-ttu-id="cffaa-118">{-0.9 f, 0,0 f, 0,1 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cffaa-118">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="cffaa-119">t + 2</span><span class="sxs-lookup"><span data-stu-id="cffaa-119">t + 2</span></span>  | <span data-ttu-id="cffaa-120">{-0.8 f, 0,0 f, 0.2 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cffaa-120">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="cffaa-121">...</span><span class="sxs-lookup"><span data-stu-id="cffaa-121">...</span></span>    | <span data-ttu-id="cffaa-122">...</span><span class="sxs-lookup"><span data-stu-id="cffaa-122">...</span></span>                         |
| <span data-ttu-id="cffaa-123">t + 10</span><span class="sxs-lookup"><span data-stu-id="cffaa-123">t + 10</span></span> | <span data-ttu-id="cffaa-124">{0,0 f, 0,0 f, 1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cffaa-124">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![trasferimento di un flusso video nello spazio di composizione](images/composition-space.png)

<span data-ttu-id="cffaa-126">Al momento t + 10, il video del flusso 1 è completamente visibile.</span><span class="sxs-lookup"><span data-stu-id="cffaa-126">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="cffaa-127">In questo esempio, la dimensione nativa del flusso 1 è stata mantenuta mentre era in fase di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="cffaa-127">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="cffaa-128">È anche possibile estendere o ridurre il rettangolo per produrre effetti interessanti.</span><span class="sxs-lookup"><span data-stu-id="cffaa-128">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="cffaa-129">È anche possibile capovolgere il video verticalmente, specificando un valore maggiore per la parte superiore della parte inferiore oppure eseguendo il mirroring del video orizzontalmente, specificando un valore maggiore per il lato sinistro rispetto a quello a destra.</span><span class="sxs-lookup"><span data-stu-id="cffaa-129">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cffaa-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cffaa-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cffaa-131">Uso della modalità di combinazione VMR</span><span class="sxs-lookup"><span data-stu-id="cffaa-131">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



