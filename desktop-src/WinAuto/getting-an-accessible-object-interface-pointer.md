---
title: Recupero di un puntatore a interfaccia a oggetti accessibile
description: Le applicazioni client Microsoft Active Accessibility recuperano i puntatori di interfaccia agli oggetti accessibili utilizzando una delle funzioni seguenti.
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d4006bf073075f2aa47a9911565213050e3d11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300243"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>Recupero di un puntatore a interfaccia a oggetti accessibile

Le applicazioni client Microsoft Active Accessibility recuperano i puntatori di interfaccia agli oggetti accessibili utilizzando una delle funzioni seguenti.

**AccessibleObjectFromEvent**

Molti client cercano informazioni su oggetti accessibili specifici che generano eventi. Poiché l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) è il "gateway" agli oggetti accessibili, i client devono disporre di un modo semplice per associare [winEvents](winevents-overview.md) con l'interfaccia **IAccessible** dell'oggetto che genera gli eventi. Microsoft Active Accessibility fornisce la funzione [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) in modo specifico per questo scopo.

> [!Note]  
> I client con [funzioni hook nel contesto](in-context-hook-functions.md) devono chiamare la funzione [unwindow](/windows/win32/api/winuser/nf-winuser-iswindow) prima di chiamare [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

La funzione [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) accetta gran parte delle stesse informazioni ricevute dalla [*funzione hook*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) di un client. Quando una funzione di hook client riceve una notifica degli eventi, passa i parametri appropriati dagli eventi a **AccessibleObjectFromEvent**.

La funzione recupera l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'elemento dell'interfaccia utente che ha generato l'evento o l'interfaccia dell'oggetto padre dell'elemento. Se viene restituito il puntatore all'interfaccia dell'oggetto padre, il client chiama le proprietà e i metodi del padre per ottenere informazioni sull'elemento figlio che ha generato l'evento.

**AccessibleObjectFromPoint**

Per recuperare l'indirizzo dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) di un oggetto in corrispondenza di un punto specificato sullo schermo, i client utilizzano la funzione [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) .

**AccessibleObjectFromWindow**

Per recuperare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) di un oggetto da un handle di finestra, i client utilizzano la funzione [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

È possibile che i server restituiscano puntatori di interfaccia distinti per lo stesso elemento dell'interfaccia utente ogni volta che viene chiamata la funzione [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) . Per determinare se due puntatori fanno riferimento allo stesso elemento dell'interfaccia utente, gli sviluppatori client devono confrontare le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto, non i puntatori.

 

 