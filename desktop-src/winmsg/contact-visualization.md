---
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato un contatto di input.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualizzazione contatto (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348191"
---
# <a name="contact-visualization"></a><span data-ttu-id="36a08-103">Visualizzazione contatto</span><span class="sxs-lookup"><span data-stu-id="36a08-103">Contact Visualization</span></span>

<span data-ttu-id="36a08-104">Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato un contatto di input.</span><span class="sxs-lookup"><span data-stu-id="36a08-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when an input contact is detected.</span></span>

<span data-ttu-id="36a08-105">Queste costanti vengono usate con i parametri **SPI \_ GETCONTACTVISUALIZATION** e **SPI \_ SETCONTACTVISUALIZATION** e la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="36a08-105">These constants are used with the **SPI\_GETCONTACTVISUALIZATION** and **SPI\_SETCONTACTVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="36a08-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ disattivato**</span><span class="sxs-lookup"><span data-stu-id="36a08-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a08-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="36a08-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="36a08-108">Specifica che il feedback dell'interfaccia utente per tutti i contatti è disattivato.</span><span class="sxs-lookup"><span data-stu-id="36a08-108">Specifies UI feedback for all contacts is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36a08-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_**</span><span class="sxs-lookup"><span data-stu-id="36a08-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a08-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="36a08-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="36a08-111">Specifica che il feedback dell'interfaccia utente per tutti i contatti è on.</span><span class="sxs-lookup"><span data-stu-id="36a08-111">Specifies UI feedback for all contacts is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36a08-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**\_PRESENTATIONMODE CONTACTVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="36a08-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION\_PRESENTATIONMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a08-113">0x0002</span><span class="sxs-lookup"><span data-stu-id="36a08-113">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="36a08-114">Specifica che il feedback dell'interfaccia utente per tutti i contatti è acceso con gli oggetti visivi in modalità presentazione.</span><span class="sxs-lookup"><span data-stu-id="36a08-114">Specifies UI feedback for all contacts is on with presentation mode visuals.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36a08-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36a08-115">Requirements</span></span>



| <span data-ttu-id="36a08-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="36a08-116">Requirement</span></span> | <span data-ttu-id="36a08-117">Valore</span><span class="sxs-lookup"><span data-stu-id="36a08-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="36a08-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36a08-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36a08-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="36a08-119">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="36a08-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36a08-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36a08-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="36a08-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="36a08-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36a08-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36a08-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="36a08-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a08-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36a08-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a08-125">Costanti di configurazione</span><span class="sxs-lookup"><span data-stu-id="36a08-125">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="36a08-126">**Visualizzazione movimenti**</span><span class="sxs-lookup"><span data-stu-id="36a08-126">**Gesture Visualization**</span></span>](gesture-visualization.md)
</dt> <dt>

[<span data-ttu-id="36a08-127">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="36a08-127">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="36a08-128">Configurazione feedback input</span><span class="sxs-lookup"><span data-stu-id="36a08-128">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

