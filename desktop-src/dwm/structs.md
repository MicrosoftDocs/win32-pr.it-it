---
title: Strutture DWM
description: In questa sezione vengono fornite informazioni sulle strutture di Gestione finestre desktop (DWM).
ms.assetid: 26b36617-54c2-405a-9a7d-bd86fefa94b6
keywords:
- Gestione finestre desktop (DWM), riferimento
- DWM (Gestione finestre desktop), riferimento
- Gestione finestre desktop (DWM), strutture
- DWM (Gestione finestre desktop), strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f212d248c0f70cfd51e6e47b2d37c89d24f630b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044746"
---
# <a name="dwm-structures"></a><span data-ttu-id="51d42-107">Strutture DWM</span><span class="sxs-lookup"><span data-stu-id="51d42-107">DWM Structures</span></span>

<span data-ttu-id="51d42-108">In questa sezione vengono fornite informazioni sulle strutture di Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="51d42-108">This section contains information about the Desktop Window Manager (DWM) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51d42-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="51d42-109">In this section</span></span>



| <span data-ttu-id="51d42-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="51d42-110">Topic</span></span>                                                                     | <span data-ttu-id="51d42-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51d42-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d42-112">**\_BLURBEHIND DWM**</span><span class="sxs-lookup"><span data-stu-id="51d42-112">**DWM\_BLURBEHIND**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)<br/>                      | <span data-ttu-id="51d42-113">Specifica le proprietà Blur-behind di DWM.</span><span class="sxs-lookup"><span data-stu-id="51d42-113">Specifies DWM blur-behind properties.</span></span> <span data-ttu-id="51d42-114">Usato dalla funzione [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) .</span><span class="sxs-lookup"><span data-stu-id="51d42-114">Used by the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function.</span></span><br/>                     |
| [<span data-ttu-id="51d42-115">**\_parametri presenti di DWM \_**</span><span class="sxs-lookup"><span data-stu-id="51d42-115">**DWM\_PRESENT\_PARAMETERS**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_present_parameters)<br/>     | <span data-ttu-id="51d42-116">Specifica i parametri del frame video DWM per la composizione del frame.</span><span class="sxs-lookup"><span data-stu-id="51d42-116">Specifies DWM video frame parameters for frame composition.</span></span> <span data-ttu-id="51d42-117">Usato dalla funzione [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) .</span><span class="sxs-lookup"><span data-stu-id="51d42-117">Used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function.</span></span><br/>   |
| [<span data-ttu-id="51d42-118">**\_Proprietà anteprima \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="51d42-118">**DWM\_THUMBNAIL\_PROPERTIES**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties)<br/> | <span data-ttu-id="51d42-119">Specifica le proprietà dell'anteprima DWM.</span><span class="sxs-lookup"><span data-stu-id="51d42-119">Specifies DWM thumbnail properties.</span></span> <span data-ttu-id="51d42-120">Usato dalla funzione [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) .</span><span class="sxs-lookup"><span data-stu-id="51d42-120">Used by the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function.</span></span><br/>                 |
| [<span data-ttu-id="51d42-121">**\_informazioni sull'intervallo di DWM \_**</span><span class="sxs-lookup"><span data-stu-id="51d42-121">**DWM\_TIMING\_INFO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_timing_info)<br/>                   | <span data-ttu-id="51d42-122">Specifica le informazioni sull'intervallo di composizione DWM.</span><span class="sxs-lookup"><span data-stu-id="51d42-122">Specifies DWM composition timing information.</span></span> <span data-ttu-id="51d42-123">Usato dalla funzione [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) .</span><span class="sxs-lookup"><span data-stu-id="51d42-123">Used by the [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) function.</span></span><br/>         |
| [<span data-ttu-id="51d42-124">**MilMatrix3x2D**</span><span class="sxs-lookup"><span data-stu-id="51d42-124">**MilMatrix3x2D**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-milmatrix3x2d)<br/>                         | <span data-ttu-id="51d42-125">Specifica una matrice 3x2 che descrive una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="51d42-125">Specifies a 3x2 matrix that describes a transform.</span></span> <br/>                                                                                            |
| [<span data-ttu-id="51d42-126">**rapporto senza segno \_**</span><span class="sxs-lookup"><span data-stu-id="51d42-126">**UNSIGNED\_RATIO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-unsigned_ratio)<br/>                      | <span data-ttu-id="51d42-127">Definisce un tipo di dati utilizzato dalle API DWM.</span><span class="sxs-lookup"><span data-stu-id="51d42-127">Defines a data type used by the DWM APIs.</span></span> <span data-ttu-id="51d42-128">Rappresenta un rapporto generico e viene usato per diversi scopi e unità anche all'interno di una singola API.</span><span class="sxs-lookup"><span data-stu-id="51d42-128">It represents a generic ratio and is used for different purposes and units even within a single API.</span></span><br/> |



 

 

 





