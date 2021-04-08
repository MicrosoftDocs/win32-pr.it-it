---
title: Esposizione di un'interfaccia del modello a oggetti nativa
description: Se un elemento dell'interfaccia utente supporta un modello a oggetti nativo diverso da Microsoft Active Accessibility o automazione interfaccia utente, può esporre l'interfaccia personalizzata rispondendo a \_ messaggi WM GetObject che includono l' \_ identificatore di oggetto NATIVEOM di ObjID.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044944"
---
# <a name="exposing-a-native-object-model-interface"></a><span data-ttu-id="8222e-103">Esposizione di un'interfaccia del modello a oggetti nativa</span><span class="sxs-lookup"><span data-stu-id="8222e-103">Exposing a Native Object Model Interface</span></span>

<span data-ttu-id="8222e-104">Se un elemento dell'interfaccia utente supporta un modello a oggetti nativo diverso da Microsoft Active Accessibility o automazione interfaccia utente, può esporre l'interfaccia personalizzata rispondendo a messaggi [**WM \_ GetObject**](wm-getobject.md) che includono l'identificatore di oggetto [**\_ NATIVEOM di ObjID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="8222e-104">If a UI element supports a native object model other than Microsoft Active Accessibility or UI Automation, it can expose the custom interface by responding to [**WM\_GETOBJECT**](wm-getobject.md) messages that include the [**OBJID\_NATIVEOM**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="8222e-105">Per rispondere, l'elemento dell'interfaccia utente deve restituire il valore recuperato da una chiamata alla funzione [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="8222e-105">To respond, the UI element should return the value retrieved by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

<span data-ttu-id="8222e-106">Un client può recuperare un'interfaccia da un elemento dell'interfaccia utente che supporta un modello a oggetti nativo chiamando la funzione [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e specificando [**objid \_ NATIVEOM**](object-identifiers.md) come secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="8222e-106">A client can retrieve an interface from a UI element that supports a native object model by calling the [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) function and specifying [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

 

 




