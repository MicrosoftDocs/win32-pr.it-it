---
title: Dispositivi di scorrimento (Windows Multimedia)
description: Dispositivi di scorrimento
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- mixer audio, controlli
- mixer audio, dispositivi di scorrimento
- mixer, controlli
- mixer, dispositivi di scorrimento
- scorrimento (controlli)
- Struttura MIXERCONTROLDETAILS_SIGNED
- controllo Pan
- Controllo Pan QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400110"
---
# <a name="sliders-windows-multimedia"></a><span data-ttu-id="944a7-111">Dispositivi di scorrimento (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="944a7-111">Sliders (Windows Multimedia)</span></span>

<span data-ttu-id="944a7-112">I controlli dispositivo di scorrimento sono in genere controlli orizzontali che possono essere modificati a sinistra o a destra.</span><span class="sxs-lookup"><span data-stu-id="944a7-112">The slider controls are typically horizontal controls that can be adjusted to the left or right.</span></span> <span data-ttu-id="944a7-113">Questi controlli utilizzano la struttura con [**\_ firma MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) per recuperare e impostare le proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="944a7-113">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="944a7-114">Nella tabella seguente vengono descritti i tipi di dispositivi di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="944a7-114">The following table describes the types of sliders.</span></span>



| <span data-ttu-id="944a7-115">Controllo</span><span class="sxs-lookup"><span data-stu-id="944a7-115">Control</span></span>    | <span data-ttu-id="944a7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="944a7-116">Description</span></span>                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="944a7-117">Slider</span><span class="sxs-lookup"><span data-stu-id="944a7-117">Slider</span></span>     | <span data-ttu-id="944a7-118">Ha un intervallo compreso tra-32.768 e 32.767.</span><span class="sxs-lookup"><span data-stu-id="944a7-118">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="944a7-119">Il driver del mixer definisce i limiti di questo controllo.</span><span class="sxs-lookup"><span data-stu-id="944a7-119">The mixer driver defines the limits of this control.</span></span>                               |
| <span data-ttu-id="944a7-120">Dettaglio</span><span class="sxs-lookup"><span data-stu-id="944a7-120">Pan</span></span>        | <span data-ttu-id="944a7-121">Ha un intervallo compreso tra-32.768 e 32.767.</span><span class="sxs-lookup"><span data-stu-id="944a7-121">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="944a7-122">Il driver del mixer definisce i limiti di questo controllo, con 0 come valore medio.</span><span class="sxs-lookup"><span data-stu-id="944a7-122">The mixer driver defines the limits of this control, with 0 as the midrange value.</span></span> |
| <span data-ttu-id="944a7-123">Panoramica di QSound</span><span class="sxs-lookup"><span data-stu-id="944a7-123">QSound Pan</span></span> | <span data-ttu-id="944a7-124">Fornisce il controllo audio espanso tramite QSound.</span><span class="sxs-lookup"><span data-stu-id="944a7-124">Provides expanded sound control through QSound.</span></span> <span data-ttu-id="944a7-125">Questo controllo ha un intervallo compreso tra-15 e 15.</span><span class="sxs-lookup"><span data-stu-id="944a7-125">This control has a range of –15 through 15.</span></span>                               |



 

 

 
