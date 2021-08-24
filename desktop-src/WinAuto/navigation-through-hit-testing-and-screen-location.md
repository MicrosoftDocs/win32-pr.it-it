---
title: Navigazione tramite hit testing e posizione dello schermo
description: Per individuare gli elementi figlio di un oggetto o per determinare le dimensioni di un oggetto, i client possono ottenere punti di test sullo schermo.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34911b13a4c9bad2bfd79cb32d5654265878568ad00475ade08a87a23150b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828274"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>Navigazione tramite hit testing e posizione dello schermo

Per individuare gli elementi figlio di un oggetto o per determinare le dimensioni di un oggetto, i client possono ottenere punti di test sullo schermo. Sono disponibili due metodi:

-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>Uso di IAccessible::accHitTest

Per determinare se un punto si trova all'interno di un oggetto, all'interno del relativo elemento figlio o nessuno dei due, i client chiamano il metodo [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) dell'oggetto padre, passando le coordinate dello schermo del punto di cui eseguire l'hit test. L'elenco seguente descrive alcuni scenari tipici:

-   Se gli elementi figlio dell'oggetto si sovrappongono a un punto specificato, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) recupera l'elemento figlio in primo piano che visivamente sembra occupare lo spazio.
-   Se una finestra copre un elemento figlio o se l'elemento figlio viene ritagliato dall'elemento padre, l'hit testing del punto coperto recupera il figlio anche se non è visibile.
-   Se l'elemento figlio trovato nel punto specificato è un oggetto accessibile, anziché un elemento figlio, il metodo restituisce [**l'interfaccia IDispatch dell'elemento**](idispatch-interface.md) figlio.

## <a name="using-iaccessibleacclocation"></a>Uso di IAccessible::accLocation

Per ottenere la posizione dello schermo di un oggetto o di uno degli elementi figlio dell'oggetto, i client chiamano [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation). Questo metodo restituisce le coordinate del rettangolo di delimitazione dell'oggetto specificato. Se l'oggetto non ha la forma di un rettangolo, il metodo restituisce le coordinate del rettangolo più piccolo che comprende l'intero oggetto.

La figura seguente mostra la relazione tra l'area dell'oggetto non rettangolare e il rettangolo di delimitazione.

![Figura che mostra l'area di un oggetto non rettangolare (un cerchio) e il relativo rettangolo di delimitazione.](images/region.gif)

> [!Note]  
> [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) è più preciso di [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) perché consente ai client di determinare la posizione degli oggetti in base pixel per pixel anziché con rettangoli di delimitazione. Questa precisione è utile, ad esempio, quando un'applicazione raccoglie informazioni tracciando la posizione del puntatore del mouse.

 

 

 




