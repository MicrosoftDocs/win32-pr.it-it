---
title: Proprietà State
description: La proprietà State descrive lo stato di un oggetto in un momento specifico. Tutti gli oggetti supportano la proprietà State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e174e938dd6252852ded6de957a54f6f94264aa811bd5bb76094af7bbba61f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564419"
---
# <a name="state-property"></a>Proprietà State

La **proprietà State** descrive lo stato di un oggetto in un momento specifico. Tutti gli oggetti supportano **la proprietà** State.

La **proprietà State** viene recuperata chiamando [**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

Microsoft Active Accessibility fornisce [costanti di stato](object-state-constants.md)dell'oggetto , definite in oleacc.h, che vengono combinate per identificare lo stato di un oggetto. È consigliabile che gli sviluppatori di server usino questi valori di stato predefiniti. Se vengono restituiti valori di stato predefiniti, i client usano [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) per recuperare una stringa localizzata che descrive lo stato.

La grafica a cui viene occasionalmente animata la proprietà **State** deve essere impostata su [**STATE SYSTEM \_ \_ ANIMATED**](object-state-constants.md) e la [**proprietà Role**](role-property.md) su ROLE [**SYSTEM \_ \_ GRAPHIC.**](object-roles.md)

 

 




