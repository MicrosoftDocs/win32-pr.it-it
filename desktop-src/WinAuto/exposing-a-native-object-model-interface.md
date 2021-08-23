---
title: Esposizione di un'interfaccia del modello a oggetti nativo
description: Se un elemento dell'interfaccia utente supporta un modello a oggetti nativo diverso da Microsoft Active Accessibility o Automazione interfaccia utente, può esporre l'interfaccia personalizzata rispondendo ai messaggi WM GETOBJECT che includono l'identificatore di oggetto \_ OBJID \_ NATIVEOM.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701ed721e8259aa3b707fa1d7a6f2e80b9da13a3760b9850edef22b169d772e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644921"
---
# <a name="exposing-a-native-object-model-interface"></a>Esposizione di un'interfaccia del modello a oggetti nativo

Se un elemento dell'interfaccia utente supporta un modello a oggetti nativo diverso da Microsoft Active Accessibility o Automazione interfaccia utente, può esporre l'interfaccia personalizzata rispondendo ai messaggi [**WM \_ GETOBJECT**](wm-getobject.md) che includono l'identificatore di oggetto [**OBJID \_ NATIVEOM.**](object-identifiers.md) Per rispondere, l'elemento dell'interfaccia utente deve restituire il valore recuperato da una chiamata alla [**funzione LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)

Un client può recuperare un'interfaccia da un elemento dell'interfaccia utente che supporta un modello a oggetti nativo chiamando la funzione [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e specificando [**OBJID \_ NATIVEOM**](object-identifiers.md) come secondo parametro.

 

 




