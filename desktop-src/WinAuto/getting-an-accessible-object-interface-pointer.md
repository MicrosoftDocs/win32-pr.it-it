---
title: Recupero di un puntatore a interfaccia a oggetti accessibile
description: Microsoft Active Accessibility applicazioni client recuperano puntatori a interfaccia a oggetti accessibili usando una delle funzioni seguenti.
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ea0d7936671a68c140c6d22fdc3afdad0db0899c9c2cbc51637dcf36d9ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994201"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>Recupero di un puntatore a interfaccia a oggetti accessibile

Microsoft Active Accessibility applicazioni client recuperano puntatori a interfaccia a oggetti accessibili usando una delle funzioni seguenti.

**AccessibleObjectFromEvent**

Molti client ricercano informazioni su oggetti accessibili specifici che generano eventi. Poiché [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) è il "gateway" per gli oggetti accessibili, i client devono avere un modo semplice per associare [WinEvents](winevents-overview.md) **all'interfaccia IAccessible** dell'oggetto che genera gli eventi. Microsoft Active Accessibility la funzione [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) specificatamente a questo scopo.

> [!Note]  
> I client [con funzioni hook nel](in-context-hook-functions.md) contesto devono chiamare la funzione [IsWindow](/windows/win32/api/winuser/nf-winuser-iswindow) prima di [**chiamare AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

La [**funzione AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) accetta molte delle stesse informazioni ricevute dalla funzione [*hook di*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) un client. Quando una funzione hook client riceve una notifica degli eventi, passa i parametri appropriati dagli eventi a **AccessibleObjectFromEvent**.

La funzione recupera [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'elemento dell'interfaccia utente che ha generato l'evento o l'interfaccia dell'oggetto padre dell'elemento. Se viene restituito il puntatore a interfaccia dell'oggetto padre, il client chiama le proprietà e i metodi dell'elemento padre per ottenere informazioni sull'elemento figlio che ha generato l'evento.

**AccessibleObjectFromPoint**

Per recuperare l'indirizzo [**dell'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) di un oggetto in un punto specificato sullo schermo, i client usano la [**funzione AccessibleObjectFromPoint.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

**AccessibleObjectFromWindow**

Per recuperare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) di un oggetto da un handle di finestra, i client usano la [**funzione AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

È possibile che i server restituiranno puntatori a interfaccia distinti per lo stesso elemento dell'interfaccia utente ogni volta che viene chiamata la funzione [**AccessibleObjectFromEvent,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) Per determinare se due puntatori fanno riferimento allo stesso elemento dell'interfaccia utente, gli sviluppatori client devono confrontare le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto, non i puntatori.

 

 