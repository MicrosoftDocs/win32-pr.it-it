---
title: Usare OBJID \_ NATIVEOM per esporre un'interfaccia nativa per una finestra
description: Questa tecnica consente ai client di ottenere un oggetto personalizzato per una finestra. I server possono utilizzare questa operazione per esporre un puntatore a un oggetto documento personalizzato per una finestra.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2c5c6ec194ca643475444feb5839c02d3fa890
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104398173"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a>Usare OBJID \_ NATIVEOM per esporre un'interfaccia nativa per una finestra

Questa tecnica consente ai client di ottenere un oggetto personalizzato per una finestra. I server possono utilizzare questa operazione per esporre un puntatore a un oggetto documento personalizzato per una finestra.

**Per esporre un'interfaccia del modello a oggetti nativo per una finestra (Server)**

1.  Gestire il messaggio [**WM \_ GetObject**](wm-getobject.md) nella routine della finestra. Quando il valore *lParam* è [**objid \_ NATIVEOM**](object-identifiers.md), restituisce un puntatore di interfaccia all'oggetto personalizzato utilizzando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).
2.  Rilasciare il puntatore di interfaccia dopo aver chiamato [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), se appropriato. Per ulteriori informazioni, vedere **LresultFromObject**.

I client possono ottenere un puntatore a questo oggetto personalizzato.

**Per ottenere un puntatore per un oggetto personalizzato per una finestra (client)**

-   Chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e passare [**objid \_ NATIVEOM**](object-identifiers.md) come secondo parametro.

Per questa tecnica si notino i problemi seguenti:

-   Questa tecnica è simile alla restituzione di un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , fatta eccezione per l'ID oggetto utilizzato e il fatto che [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) restituisce un oggetto personalizzato anziché **IAccessible**.
-   Gli sviluppatori di server possono dover pubblicare informazioni che consentono ai client di identificare in modo univoco il **HWND** in modo che possano trovarlo prima di chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) sul relativo handle di finestra.
-   Non implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nell'oggetto personalizzato restituito. In caso contrario, OLEACC lo considererà come un **IAccessible** standard e potrebbe impedire l'uso delle interfacce personalizzate.
-   Per poter essere utilizzati tra i processi, potrebbe essere necessario registrare le interfacce sull'oggetto restituito con Component Object Model (COM).

Questa tecnica è supportata da diversi componenti Microsoft Office. Per ulteriori informazioni, vedere [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

 

 




