---
title: Costanti ed enumerazioni di DWM
description: In questa sezione vengono fornite informazioni sulle costanti e sulle enumerazioni utilizzate nelle API di Gestione finestre desktop (DWM).
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Gestione finestre desktop (DWM), riferimento
- DWM (Gestione finestre desktop), riferimento
- Gestione finestre desktop (DWM), costanti
- DWM (Gestione finestre desktop), costanti
- Gestione finestre desktop (DWM), enumerazioni
- DWM (Gestione finestre desktop), enumerazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711185"
---
# <a name="dwm-constants-and-enumerations"></a><span data-ttu-id="ef227-109">Costanti ed enumerazioni di DWM</span><span class="sxs-lookup"><span data-stu-id="ef227-109">DWM Constants and Enumerations</span></span>

<span data-ttu-id="ef227-110">In questa sezione vengono fornite informazioni sulle costanti e sulle enumerazioni utilizzate nelle API di Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="ef227-110">This section contains information about the constants and enumerations used in the Desktop Window Manager (DWM) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef227-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ef227-111">In this section</span></span>



| <span data-ttu-id="ef227-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="ef227-112">Topic</span></span>                                                                                     | <span data-ttu-id="ef227-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef227-113">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef227-114">**Sfocature di DWM dietro costanti**</span><span class="sxs-lookup"><span data-stu-id="ef227-114">**DWM Blur Behind Constants**</span></span>](dwm-bb-constants.md)<br/>                          | <span data-ttu-id="ef227-115">Flag utilizzati dalla struttura [**\_ BLURBEHIND di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) per indicare quali membri contengono informazioni valide.</span><span class="sxs-lookup"><span data-stu-id="ef227-115">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span><br/>                                                                    |
| [<span data-ttu-id="ef227-116">**Le costanti di composizione sono abilitate da DWM**</span><span class="sxs-lookup"><span data-stu-id="ef227-116">**DWM Enable Composition Constants**</span></span>](dwm-ec-constants.md)<br/>                   | <span data-ttu-id="ef227-117">Flag utilizzati dalla funzione [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  per modificare lo stato della composizione di DWM.</span><span class="sxs-lookup"><span data-stu-id="ef227-117">Flags used by the [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  function to change the state of DWM composition.</span></span><br/>                                                                             |
| [<span data-ttu-id="ef227-118">**\_ \_ campionamento frame di origine DWM \_**</span><span class="sxs-lookup"><span data-stu-id="ef227-118">**DWM\_SOURCE\_FRAME\_SAMPLING**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | <span data-ttu-id="ef227-119">Flag utilizzati dalla funzione [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) per specificare il tipo di campionamento dei frame.</span><span class="sxs-lookup"><span data-stu-id="ef227-119">Flags used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function to specify the frame sampling type.</span></span><br/>                                                                            |
| [<span data-ttu-id="ef227-120">**\_requisiti della \_ finestra della scheda DWM \_**</span><span class="sxs-lookup"><span data-stu-id="ef227-120">**DWM\_TAB\_WINDOW\_REQUIREMENTS**</span></span>](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | <span data-ttu-id="ef227-121">Restituito da DwmGetUnmetTabRequirements per indicare i requisiti necessari a una finestra per inserire le schede nella barra del titolo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef227-121">Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.</span></span><br/>                                                                    |
| [<span data-ttu-id="ef227-122">**\_Costanti TNP di DWM**</span><span class="sxs-lookup"><span data-stu-id="ef227-122">**DWM\_TNP Constants**</span></span>](dwm-tnp-constants.md)<br/>                                | <span data-ttu-id="ef227-123">Flag utilizzati dalla struttura [**delle \_ \_ proprietà di anteprima di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) per indicare quali membri contengono informazioni valide.</span><span class="sxs-lookup"><span data-stu-id="ef227-123">Flags used by the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) structure to indicate which of its members contain valid information.</span></span><br/>                                               |
| [<span data-ttu-id="ef227-124">**DWMFLIP3DWINDOWPOLICY**</span><span class="sxs-lookup"><span data-stu-id="ef227-124">**DWMFLIP3DWINDOWPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | <span data-ttu-id="ef227-125">Flag utilizzati dalla funzione [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) per specificare i criteri della finestra di Flip3D.</span><span class="sxs-lookup"><span data-stu-id="ef227-125">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the Flip3D window policy.</span></span><br/>                                                                               |
| [<span data-ttu-id="ef227-126">**DWMNCRENDERINGPOLICY**</span><span class="sxs-lookup"><span data-stu-id="ef227-126">**DWMNCRENDERINGPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | <span data-ttu-id="ef227-127">Flag utilizzati dalla funzione [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) per specificare i criteri di rendering dell'area non client.</span><span class="sxs-lookup"><span data-stu-id="ef227-127">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the non-client area rendering policy.</span></span><br/>                                                                   |
| [<span data-ttu-id="ef227-128">**\_destinazione OWNEDWINDOW \_ DWMTRANSITION**</span><span class="sxs-lookup"><span data-stu-id="ef227-128">**DWMTRANSITION\_OWNEDWINDOW\_TARGET**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | <span data-ttu-id="ef227-129">Identifica la destinazione.</span><span class="sxs-lookup"><span data-stu-id="ef227-129">Identifies the target.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="ef227-130">**DWMWINDOWATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="ef227-130">**DWMWINDOWATTRIBUTE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | <span data-ttu-id="ef227-131">Flag utilizzati dalle funzioni [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) per specificare gli attributi della finestra per il rendering non client.</span><span class="sxs-lookup"><span data-stu-id="ef227-131">Flags used by the [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions to specify window attributes for non-client rendering.</span></span><br/> |
| [<span data-ttu-id="ef227-132">**tipo di movimento \_**</span><span class="sxs-lookup"><span data-stu-id="ef227-132">**GESTURE\_TYPE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | <span data-ttu-id="ef227-133">Identifica il tipo di movimento specificato in [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span><span class="sxs-lookup"><span data-stu-id="ef227-133">Identifies the gesture type specified in [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span></span><br/>                                                                                                               |



 

 

 





