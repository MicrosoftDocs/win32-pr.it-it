---
title: Considerazioni sulla progettazione per gli oggetti proxy
description: La progettazione del proxy e degli oggetti accessibili dipende dalla progettazione degli elementi dell'interfaccia utente del server. Indipendentemente dalla progettazione, un elemento dell'interfaccia utente deve notificare il proprio oggetto proxy immediatamente prima che venga eliminato definitivamente in modo che l'oggetto proxy gestisca le chiamate dai client in modo appropriato.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cd96056f89e1efc18da3e299a76e92c85166efd7067e54f972a69eb8786d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830072"
---
# <a name="design-considerations-for-proxy-objects"></a>Considerazioni sulla progettazione per gli oggetti proxy

La progettazione del proxy e degli oggetti accessibili dipende dalla progettazione degli elementi dell'interfaccia utente del server. Indipendentemente dalla progettazione, un elemento dell'interfaccia utente deve notificare il proprio oggetto proxy immediatamente prima che venga eliminato definitivamente in modo che l'oggetto proxy gestisca le chiamate dai client in modo appropriato.

L'elenco seguente descrive due possibilità di progettazione:

-   Inserire il codice che implementa [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nello stesso modulo del codice che implementa l'elemento dell'interfaccia utente se il codice dell'interfaccia utente è facilmente estendibile. In questo caso, il proxy è "leggero" nel senso che tutto ciò che fa è monitorare l'intervallo di vita dell'oggetto accessibile, inoltrare le chiamate all'oggetto accessibile e restituire i risultati.
-   Inserire il codice che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nello stesso modulo del codice che implementa l'oggetto proxy. In questo caso, l'oggetto accessibile usa funzioni interne per ottenere informazioni sull'elemento dell'interfaccia utente.

## <a name="trackbar-controls"></a>Controlli Trackbar

Quando si implementano i controlli trackbar, usare lo stile del trackbar **TBS \_ REVERSED** per fornire informazioni più significative. Questo stile inverte la scala usata da [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

Per i trackbar verticali senza questo stile, [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) restituisce zero (0) quando il cursore del trackbar si trova nella parte superiore del controllo. I valori aumentano quando si scorre il cursore verso il basso. Con lo stile **TBS \_ REVERSED,** **IAccessible::get \_ accValue** restituisce 100 (100) quando il cursore del trackbar si trova nella parte superiore. I numeri diminuiscono quando si sposta il cursore del trackbar verso il basso.

Per i trackbar orizzontali senza questo stile, viene restituito zero (0) quando il cursore del trackbar si trova all'estremità sinistra del controllo; I valori aumentano man mano che si sposta il cursore del trackbar verso destra. Con lo stile **TBS \_ REVERSED,** [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) restituisce 100 (100) quando il cursore del trackbar si trova a sinistra. I valori diminuiscono quando si sposta il cursore del trackbar a destra.

 

 




