---
title: Considerazioni di progettazione per gli oggetti proxy
description: Il proxy e la progettazione degli oggetti accessibili dipendono dalla progettazione degli elementi dell'interfaccia utente del server. Indipendentemente dalla progettazione, un elemento dell'interfaccia utente deve notificare all'oggetto proxy immediatamente prima che venga eliminato definitivamente, in modo che l'oggetto proxy gestisca le chiamate dai client in modo appropriato.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044302"
---
# <a name="design-considerations-for-proxy-objects"></a>Considerazioni di progettazione per gli oggetti proxy

Il proxy e la progettazione degli oggetti accessibili dipendono dalla progettazione degli elementi dell'interfaccia utente del server. Indipendentemente dalla progettazione, un elemento dell'interfaccia utente deve notificare all'oggetto proxy immediatamente prima che venga eliminato definitivamente, in modo che l'oggetto proxy gestisca le chiamate dai client in modo appropriato.

Nell'elenco seguente vengono descritte due possibilità di progettazione:

-   Inserire il codice che implementa l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nello stesso modulo del codice che implementa l'elemento dell'interfaccia utente se il codice dell'interfaccia utente è facilmente estendibile. In questo caso, il proxy è "leggero" nel senso che tutto ciò che esegue è il monitoraggio della durata dell'oggetto accessibile, l'inoltro delle chiamate all'oggetto accessibile e la restituzione dei risultati.
-   Inserire il codice che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nello stesso modulo del codice che implementa l'oggetto proxy. In questo caso, l'oggetto accessibile utilizza funzioni interne per ottenere informazioni sull'elemento dell'interfaccia utente.

## <a name="trackbar-controls"></a>Controlli TrackBar

Quando si implementano i controlli TrackBar, utilizzare il tipo di oggetto TrackBar **\_ invertito** per fornire informazioni più significative. Questo stile inverte la scala utilizzata da [**IAccessible:: Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

Per gli TrackBar verticali senza questo stile, [**IAccessible:: Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) restituisce zero (0) quando il cursore TrackBar si trova nella parte superiore del controllo; i valori aumentano quando si scorre il cursore verso il basso. Con lo stile **TBS \_ invertito** , **IAccessible:: Get \_ accValue** restituisce 100 (100) quando il cursore TrackBar si trova nella parte superiore; i numeri diminuiscono quando si sposta il cursore del controllo TrackBar verso il basso.

Per gli TrackBar orizzontali senza questo stile, viene restituito zero (0) quando il cursore TrackBar si trova all'estremità sinistra del controllo; i valori aumentano quando si sposta il cursore del controllo TrackBar a destra. Con lo stile **TBS \_ invertito** , [**IAccessible:: Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) restituisce 100 (100) quando il cursore TrackBar si trova a sinistra; i valori diminuiscono quando si sposta il cursore del controllo TrackBar a destra.

 

 




