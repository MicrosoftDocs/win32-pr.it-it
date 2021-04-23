---
description: Set di proprietà Frame Stepping
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Set di proprietà Frame Stepping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908449"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="0108b-103">Set di proprietà Frame Stepping</span><span class="sxs-lookup"><span data-stu-id="0108b-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="0108b-104">I decodificatori che implementano la ricerca accurata dei frame in Microsoft DirectShow devono implementare il set di proprietà \_ AM KSPROPSETID FrameStep, che viene usato insieme \_ all'interfaccia [**IVideoFrameStep.**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)</span><span class="sxs-lookup"><span data-stu-id="0108b-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



| <span data-ttu-id="0108b-105">Label</span><span class="sxs-lookup"><span data-stu-id="0108b-105">Label</span></span> | <span data-ttu-id="0108b-106">Valore</span><span class="sxs-lookup"><span data-stu-id="0108b-106">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="0108b-107">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="0108b-107">Property Set GUID</span></span> | <span data-ttu-id="0108b-108">AM \_ KSPROPSETID \_ FrameStep</span><span class="sxs-lookup"><span data-stu-id="0108b-108">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="0108b-109">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="0108b-109">Property ID</span></span>                              | <span data-ttu-id="0108b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0108b-110">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0108b-111">AM \_ PROPERTY \_ FRAMESTEP \_ STEP</span><span class="sxs-lookup"><span data-stu-id="0108b-111">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="0108b-112">Indica al decodificatore di iniziare un'operazione di passaggio e passa una struttura [**\_ AM PROPERTY \_ FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) che specifica il numero di passaggi.</span><span class="sxs-lookup"><span data-stu-id="0108b-112">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="0108b-113">AM \_ PROPERTY \_ FRAMESTEP \_ CANCEL</span><span class="sxs-lookup"><span data-stu-id="0108b-113">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="0108b-114">Indica al decodificatore di annullare l'operazione del passaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="0108b-114">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="0108b-115">Nessun dato dell'istanza è associato a questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0108b-115">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="0108b-116">AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEP</span><span class="sxs-lookup"><span data-stu-id="0108b-116">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="0108b-117">Il decodificatore restituisce S OK in questa istruzione per indicare che è possibile eseguire l'esecuzione delle istruzioni dei \_ frame, S \_ FALSE in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0108b-117">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="0108b-118">Quando questa proprietà è impostata, non viene passato alcun dato dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0108b-118">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="0108b-119">AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="0108b-119">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="0108b-120">Il decodificatore restituisce S OK in questa istruzione per indicare che può eseguire più fotogrammi \_ alla volta, S \_ FALSE in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0108b-120">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="0108b-121">Quando questa proprietà è impostata, non viene passato alcun dato dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0108b-121">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0108b-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0108b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0108b-123">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="0108b-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



