---
title: Interazione con WinEvents
description: Il tempo di esecuzione dell'annotazione dinamica non invierà WinEvents; è responsabilità dell'annotatore inviare gli eventi appropriati, quando necessario. Se è necessario inviare WinEvents, assicurarsi di inviarli dopo aver eseguito l'annotazione.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aedd09a22371f91a92eca891c77f6c424583b5
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "106299343"
---
# <a name="interaction-with-winevents"></a><span data-ttu-id="ffc41-104">Interazione con WinEvents</span><span class="sxs-lookup"><span data-stu-id="ffc41-104">Interaction with WinEvents</span></span>

<span data-ttu-id="ffc41-105">Il tempo di esecuzione dell'annotazione dinamica non invierà [winEvents](winevents-infrastructure.md); è responsabilità dell'annotatore inviare gli eventi appropriati, quando necessario.</span><span class="sxs-lookup"><span data-stu-id="ffc41-105">The Dynamic Annotation run time will not send [WinEvents](winevents-infrastructure.md); it is the annotator's responsibility to send appropriate events, when necessary.</span></span> <span data-ttu-id="ffc41-106">Se è necessario inviare WinEvents, assicurarsi di inviarli dopo aver eseguito l'annotazione.</span><span class="sxs-lookup"><span data-stu-id="ffc41-106">If you need to send WinEvents, be sure to send them after the annotation has taken place.</span></span>

<span data-ttu-id="ffc41-107">Se ad esempio si usa [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) per impostare la proprietà [**Name**](name-property.md) di un elemento, inviare un evento [**\_ \_ NAMECHANGE dell'oggetto evento**](event-constants.md) per quell'oggetto dopo la restituzione di **SetPropValue** .</span><span class="sxs-lookup"><span data-stu-id="ffc41-107">For example, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the [**Name**](name-property.md) property of an element, send an [**EVENT\_OBJECT\_NAMECHANGE**](event-constants.md) event for that object after **SetPropValue** returns.</span></span>

<span data-ttu-id="ffc41-108">Tuttavia, se si usa [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) per impostare ValueMap per un dispositivo di scorrimento, non è necessario alcun evento perché l'impostazione di ValueMap non comporta la modifica del valore del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="ffc41-108">However, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the ValueMap for a slider, no events are required because setting the ValueMap does not change the slider's value.</span></span>

 

 




