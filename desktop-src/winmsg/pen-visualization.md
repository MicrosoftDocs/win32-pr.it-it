---
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato uno dei movimenti penna elencati.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualizzazione penna (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529161"
---
# <a name="pen-visualization"></a><span data-ttu-id="b6748-103">Visualizzazione penna</span><span class="sxs-lookup"><span data-stu-id="b6748-103">Pen Visualization</span></span>

<span data-ttu-id="b6748-104">Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato uno dei movimenti penna elencati.</span><span class="sxs-lookup"><span data-stu-id="b6748-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed pen gestures is detected.</span></span>

<span data-ttu-id="b6748-105">Queste costanti vengono usate con i parametri **SPI \_ GETPENVISUALIZATION** e **SPI \_ SETPENVISUALIZATION** e la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b6748-105">These constants are used with the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="b6748-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ disattivato**</span><span class="sxs-lookup"><span data-stu-id="b6748-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6748-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="b6748-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="b6748-108">Specifica che il feedback dell'interfaccia utente per tutti i movimenti di penna è disattivato.</span><span class="sxs-lookup"><span data-stu-id="b6748-108">Specifies that UI feedback for all pen gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6748-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_**</span><span class="sxs-lookup"><span data-stu-id="b6748-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6748-110">0x0023</span><span class="sxs-lookup"><span data-stu-id="b6748-110">0x0023</span></span>
</dt> <dt>



<span data-ttu-id="b6748-111">Specifica che il feedback dell'interfaccia utente per tutti i movimenti di penna è on.</span><span class="sxs-lookup"><span data-stu-id="b6748-111">Specifies that UI feedback for all pen gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6748-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**\_tocco PENVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="b6748-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6748-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="b6748-113">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="b6748-114">Specifica il feedback dell'interfaccia utente per un tocco della penna.</span><span class="sxs-lookup"><span data-stu-id="b6748-114">Specifies UI feedback for a pen tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6748-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**\_DOUBLETAP PENVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="b6748-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6748-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="b6748-116">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="b6748-117">Specifica il feedback dell'interfaccia utente per un tocco di penna doppio.</span><span class="sxs-lookup"><span data-stu-id="b6748-117">Specifies UI feedback for a pen double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6748-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**\_cursore PENVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="b6748-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION\_CURSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6748-119">0x0020</span><span class="sxs-lookup"><span data-stu-id="b6748-119">0x0020</span></span>
</dt> <dt>



<span data-ttu-id="b6748-120">Specifica il feedback dell'interfaccia utente per il cursore della penna.</span><span class="sxs-lookup"><span data-stu-id="b6748-120">Specifies UI feedback for the pen cursor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6748-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6748-121">Requirements</span></span>



| <span data-ttu-id="b6748-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6748-122">Requirement</span></span> | <span data-ttu-id="b6748-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b6748-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6748-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6748-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6748-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b6748-125">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b6748-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6748-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6748-127">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="b6748-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6748-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6748-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6748-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6748-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6748-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6748-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6748-131">Costanti di configurazione</span><span class="sxs-lookup"><span data-stu-id="b6748-131">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="b6748-132">**Visualizzazione contatto**</span><span class="sxs-lookup"><span data-stu-id="b6748-132">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="b6748-133">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="b6748-133">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="b6748-134">Configurazione feedback input</span><span class="sxs-lookup"><span data-stu-id="b6748-134">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

