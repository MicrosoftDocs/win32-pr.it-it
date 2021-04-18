---
title: Navigazione tramite hit testing e posizione dello schermo
description: Per individuare gli elementi figlio di un oggetto o per determinare le dimensioni di un oggetto, i client possono colpire i punti di test sullo schermo.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298113"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>Navigazione tramite hit testing e posizione dello schermo

Per individuare gli elementi figlio di un oggetto o per determinare le dimensioni di un oggetto, i client possono colpire i punti di test sullo schermo. Sono disponibili due metodi:

-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>Utilizzo di IAccessible:: accHitTest

Per determinare se un punto si trova all'interno di un oggetto, all'interno del relativo elemento figlio o nessuno dei due, i client chiamano il metodo [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) dell'oggetto padre, passando le coordinate dello schermo del punto da sottoporre a hit test. Nell'elenco seguente vengono descritti alcuni scenari tipici:

-   Se gli elementi figlio dell'oggetto si sovrappongono in corrispondenza di un punto specificato, [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) Recupera il figlio più alto che sembra occupare lo spazio.
-   Se una finestra copre un elemento figlio o se l'elemento figlio viene ritagliato dall'elemento padre, l'hit testing del punto interessato recupera l'elemento figlio anche se non è visibile.
-   Se l'elemento figlio trovato in corrispondenza del punto specificato è un oggetto accessibile, anziché un elemento figlio, il metodo restituisce l'interfaccia [**IDispatch**](idispatch-interface.md) del figlio.

## <a name="using-iaccessibleacclocation"></a>Utilizzo di IAccessible:: accLocation

Per ottenere la posizione dello schermo di un oggetto o di uno degli elementi figlio dell'oggetto, i client chiamano [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation). Questo metodo restituisce le coordinate del rettangolo di delimitazione dell'oggetto specificato. Se l'oggetto non ha una forma come un rettangolo, il metodo restituisce le coordinate del rettangolo più piccolo che include l'intero oggetto.

La figura seguente mostra la relazione tra l'area dell'oggetto non rettangolare e il rettangolo di delimitazione.

![illustrazione che mostra un'area dell'oggetto non rettangolare (un cerchio) e il relativo rettangolo di delimitazione.](images/region.gif)

> [!Note]  
> [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) è più preciso di [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) perché consente ai client di determinare la posizione degli oggetti in base al pixel anziché ai rettangoli di delimitazione. Questa precisione è utile, ad esempio, quando un'applicazione raccoglie informazioni monitorando la posizione del puntatore del mouse.

 

 

 




