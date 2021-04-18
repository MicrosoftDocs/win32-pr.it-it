---
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato uno dei movimenti elencati.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualizzazione movimenti (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317238"
---
# <a name="gesture-visualization"></a><span data-ttu-id="b1cea-103">Visualizzazione movimenti</span><span class="sxs-lookup"><span data-stu-id="b1cea-103">Gesture Visualization</span></span>

<span data-ttu-id="b1cea-104">Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato uno dei movimenti elencati.</span><span class="sxs-lookup"><span data-stu-id="b1cea-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed gestures is detected.</span></span>

<span data-ttu-id="b1cea-105">Queste costanti vengono usate con i parametri **SPI \_ GETGESTUREVISUALIZATION** e **SPI \_ SETGESTUREVISUALIZATION** e la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b1cea-105">These constants are used with the **SPI\_GETGESTUREVISUALIZATION** and **SPI\_SETGESTUREVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="b1cea-106">**Nota**</span><span class="sxs-lookup"><span data-stu-id="b1cea-106">**Note**</span></span>  

<span data-ttu-id="b1cea-107">Per recuperare o impostare le informazioni di visualizzazione della penna, è consigliabile usare i parametri **SPI \_ GETPENVISUALIZATION** e **SPI \_ SETPENVISUALIZATION** e le costanti elencate nella [**visualizzazione Pen**](pen-visualization.md).</span><span class="sxs-lookup"><span data-stu-id="b1cea-107">For retrieving or setting pen visualization info, we recommend that you use the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the constants listed in [**Pen Visualization**](pen-visualization.md).</span></span>

<dl> <dt>

<span data-ttu-id="b1cea-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ disattivato**</span><span class="sxs-lookup"><span data-stu-id="b1cea-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1cea-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="b1cea-109">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="b1cea-110">Specifica che il feedback dell'interfaccia utente per tutti i movimenti è disattivato.</span><span class="sxs-lookup"><span data-stu-id="b1cea-110">Specifies that UI feedback for all gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1cea-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_**</span><span class="sxs-lookup"><span data-stu-id="b1cea-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1cea-112">0x001F</span><span class="sxs-lookup"><span data-stu-id="b1cea-112">0x001F</span></span>
</dt> <dt>



<span data-ttu-id="b1cea-113">Specifica che il feedback dell'interfaccia utente per tutti i movimenti è on.</span><span class="sxs-lookup"><span data-stu-id="b1cea-113">Specifies that UI feedback for all gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1cea-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**\_tocco GESTUREVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="b1cea-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1cea-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="b1cea-115">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="b1cea-116">Specifica il feedback dell'interfaccia utente per il tocco.</span><span class="sxs-lookup"><span data-stu-id="b1cea-116">Specifies UI feedback for a tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1cea-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**\_DOUBLETAP GESTUREVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="b1cea-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1cea-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="b1cea-118">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="b1cea-119">Specifica il feedback dell'interfaccia utente per un doppio tocco.</span><span class="sxs-lookup"><span data-stu-id="b1cea-119">Specifies UI feedback for a double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1cea-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**\_PRESSANDTAP GESTUREVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="b1cea-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION\_PRESSANDTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1cea-121">0x0004</span><span class="sxs-lookup"><span data-stu-id="b1cea-121">0x0004</span></span>
</dt> <dt>



<span data-ttu-id="b1cea-122">Specifica il feedback dell'interfaccia utente per una pressione e un tocco.</span><span class="sxs-lookup"><span data-stu-id="b1cea-122">Specifies UI feedback for a press and tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1cea-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**\_PRESSANDHOLD GESTUREVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="b1cea-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION\_PRESSANDHOLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1cea-124">0x0008</span><span class="sxs-lookup"><span data-stu-id="b1cea-124">0x0008</span></span>
</dt> <dt>



<span data-ttu-id="b1cea-125">Specifica il feedback dell'interfaccia utente per una pressione e un tasto di attesa.</span><span class="sxs-lookup"><span data-stu-id="b1cea-125">Specifies UI feedback for a press and hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1cea-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**\_RIGHTTAP GESTUREVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="b1cea-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION\_RIGHTTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1cea-127">0x0010</span><span class="sxs-lookup"><span data-stu-id="b1cea-127">0x0010</span></span>
</dt> <dt>



<span data-ttu-id="b1cea-128">Specifica il feedback dell'interfaccia utente per il tocco corretto.</span><span class="sxs-lookup"><span data-stu-id="b1cea-128">Specifies UI feedback for a right tap.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1cea-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1cea-129">Requirements</span></span>



| <span data-ttu-id="b1cea-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1cea-130">Requirement</span></span> | <span data-ttu-id="b1cea-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b1cea-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1cea-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1cea-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b1cea-133">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b1cea-133">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b1cea-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1cea-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b1cea-135">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b1cea-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b1cea-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1cea-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1cea-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1cea-137"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1cea-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1cea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1cea-139">Costanti di configurazione</span><span class="sxs-lookup"><span data-stu-id="b1cea-139">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="b1cea-140">**Visualizzazione contatto**</span><span class="sxs-lookup"><span data-stu-id="b1cea-140">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="b1cea-141">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="b1cea-141">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="b1cea-142">Configurazione feedback input</span><span class="sxs-lookup"><span data-stu-id="b1cea-142">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

