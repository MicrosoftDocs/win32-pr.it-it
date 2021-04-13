---
title: Recupero di un oggetto IAccessible
description: Microsoft Active Accessibility fornisce funzioni quali AccessibleObjectFromWindow e AccessibleObjectFromPoint che consentono ai client di recuperare gli oggetti accessibili.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328791"
---
# <a name="retrieving-an-iaccessible-object"></a>Recupero di un oggetto IAccessible

Microsoft Active Accessibility fornisce funzioni quali [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) che consentono ai client di recuperare gli oggetti accessibili. Queste funzioni restituiscono un puntatore all'interfaccia [**IDispatch**](idispatch-interface.md) o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) tramite il quale i client ottengono informazioni sull'oggetto accessibile.

Quando un client chiama [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o qualsiasi altra funzione **AccessibleObjectFrom * * * X* che recupera un'interfaccia a un oggetto, Microsoft Active Accessibility invia il messaggio della finestra [**WM \_ GetObject**](wm-getobject.md) alla routine della finestra applicabile all'interno dell'applicazione appropriata. Per fornire informazioni ai client, i server devono rispondere al messaggio **WM \_ GetObject** .

Per raccogliere informazioni specifiche su un elemento dell'interfaccia utente, i client devono prima recuperare un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento. Per recuperare l'oggetto **IAccessible** di un elemento, i client possono usare una delle funzioni seguenti:

-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

**Per recuperare un puntatore di interfaccia IAccessible**

1.  Il client chiama una delle funzioni **AccessibleObjectFrom * * * X* .
2.  Oleacc.dll Invia un messaggio [**WM \_ GetObject**](wm-getobject.md) al server.
3.  Il server determina quale elemento dell'interfaccia utente corrisponde alla richiesta.
4.  Il server restituisce zero per richiedere un proxy di Oleacc.dll,

    Oppure

    Restituisce un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (implementazione nativa). A tale scopo, è necessario:

    -   Costruisce un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento.
    -   Chiama [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) per effettuare il marshalling del puntatore dell'oggetto.
    -   Restituisce LRESULT per Oleacc.dll.

5.  Oleacc.dll esamina il valore restituito da [**WM \_ GetObject**](wm-getobject.md).

    Se è zero, Oleacc.dll costruisce un oggetto proxy e lo restituisce al client.

    Oppure

    Se è diverso da zero, Oleacc.dll chiama [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) per annullare il marshalling del puntatore all'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo e restituirlo al client.

 

 




