---
description: Set di proprietà di avanzamento frame
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Set di proprietà di avanzamento frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746639"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="f5d3e-103">Set di proprietà di avanzamento frame</span><span class="sxs-lookup"><span data-stu-id="f5d3e-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="f5d3e-104">I decodificatori che implementano la ricerca con precisione dei frame in Microsoft DirectShow devono implementare il \_ \_ set di proprietà KSPROPSETID FrameStep, che viene usato insieme all'interfaccia [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .</span><span class="sxs-lookup"><span data-stu-id="f5d3e-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="f5d3e-105">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="f5d3e-105">Property Set GUID</span></span> | <span data-ttu-id="f5d3e-106">\_FrameStep KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="f5d3e-106">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="f5d3e-107">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="f5d3e-107">Property ID</span></span>                              | <span data-ttu-id="f5d3e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5d3e-108">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d3e-109">\_ \_ passaggio FRAMESTEP della proprietà am \_</span><span class="sxs-lookup"><span data-stu-id="f5d3e-109">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="f5d3e-110">Indica al decodificatore di iniziare un'operazione di passaggio e passa una struttura di [**\_ proprietà \_ FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) che specifica il numero di passaggi.</span><span class="sxs-lookup"><span data-stu-id="f5d3e-110">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="f5d3e-111">\_Proprietà am \_ FRAMESTEP \_ Cancel</span><span class="sxs-lookup"><span data-stu-id="f5d3e-111">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="f5d3e-112">Indica al decodificatore di annullare l'operazione del passaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="f5d3e-112">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="f5d3e-113">Nessun dato dell'istanza è associato a questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5d3e-113">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="f5d3e-114">\_Proprietà am \_ FRAMESTEP \_ CANSTEP</span><span class="sxs-lookup"><span data-stu-id="f5d3e-114">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="f5d3e-115">Il decodificatore restituisce \_ OK su questa istruzione per indicare che è in grado di eseguire il frame stepping, S \_ false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f5d3e-115">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="f5d3e-116">Quando questa proprietà è impostata, non vengono passati dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f5d3e-116">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="f5d3e-117">\_Proprietà am \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="f5d3e-117">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="f5d3e-118">Il decodificatore restituisce \_ OK in questa istruzione per indicare che è possibile eseguire più frame alla volta, in \_ caso contrario, s false.</span><span class="sxs-lookup"><span data-stu-id="f5d3e-118">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="f5d3e-119">Quando questa proprietà è impostata, non vengono passati dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f5d3e-119">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f5d3e-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5d3e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5d3e-121">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="f5d3e-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



