---
title: Proprietà State
description: La proprietà state descrive lo stato di un oggetto in un momento specifico. Tutti gli oggetti supportano la proprietà state.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856861"
---
# <a name="state-property"></a><span data-ttu-id="eea49-104">Proprietà State</span><span class="sxs-lookup"><span data-stu-id="eea49-104">State Property</span></span>

<span data-ttu-id="eea49-105">La proprietà **state** descrive lo stato di un oggetto in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="eea49-105">The **State** property describes an object's status at a moment in time.</span></span> <span data-ttu-id="eea49-106">Tutti gli oggetti supportano la proprietà **state** .</span><span class="sxs-lookup"><span data-stu-id="eea49-106">All objects support the **State** property.</span></span>

<span data-ttu-id="eea49-107">La proprietà **state** viene recuperata chiamando [**IAccessible:: Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span><span class="sxs-lookup"><span data-stu-id="eea49-107">The **State** property is retrieved by calling [**IAccessible::get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span></span>

<span data-ttu-id="eea49-108">Microsoft Active Accessibility fornisce [costanti di stato dell'oggetto](object-state-constants.md), definite in oleacc. h, che vengono combinate per identificare lo stato di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="eea49-108">Microsoft Active Accessibility provides [object state constants](object-state-constants.md), defined in oleacc.h, that are combined to identify an object's state.</span></span> <span data-ttu-id="eea49-109">È consigliabile che gli sviluppatori di server usino questi valori di stato predefiniti.</span><span class="sxs-lookup"><span data-stu-id="eea49-109">It is recommended that server developers use these predefined state values.</span></span> <span data-ttu-id="eea49-110">Se vengono restituiti valori di stato predefiniti, i client utilizzano [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) per recuperare una stringa localizzata che descrive lo stato.</span><span class="sxs-lookup"><span data-stu-id="eea49-110">If predefined state values are returned, clients use [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) to retrieve a localized string that describes the state.</span></span>

<span data-ttu-id="eea49-111">Per gli elementi grafici a cui è stata animata occasionalmente la proprietà **state** è impostata su [**state \_ System \_ Animated**](object-state-constants.md) e la proprietà [**Role**](role-property.md) impostata sull' [**\_ \_ elemento Graphic del sistema Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="eea49-111">Graphics that are occasionally animated should have the **State** property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md) and the [**Role**](role-property.md) property set to [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

 

 




