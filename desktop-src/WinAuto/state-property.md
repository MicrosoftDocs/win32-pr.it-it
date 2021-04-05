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
# <a name="state-property"></a>Proprietà State

La proprietà **state** descrive lo stato di un oggetto in un momento specifico. Tutti gli oggetti supportano la proprietà **state** .

La proprietà **state** viene recuperata chiamando [**IAccessible:: Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

Microsoft Active Accessibility fornisce [costanti di stato dell'oggetto](object-state-constants.md), definite in oleacc. h, che vengono combinate per identificare lo stato di un oggetto. È consigliabile che gli sviluppatori di server usino questi valori di stato predefiniti. Se vengono restituiti valori di stato predefiniti, i client utilizzano [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) per recuperare una stringa localizzata che descrive lo stato.

Per gli elementi grafici a cui è stata animata occasionalmente la proprietà **state** è impostata su [**state \_ System \_ Animated**](object-state-constants.md) e la proprietà [**Role**](role-property.md) impostata sull' [**\_ \_ elemento Graphic del sistema Role**](object-roles.md).

 

 




