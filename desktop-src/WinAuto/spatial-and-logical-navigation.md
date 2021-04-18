---
title: Navigazione spaziale e logica
description: I client recuperano informazioni su un oggetto che è a livello di spazio o logicamente vicino a un altro oggetto all'interno dello stesso contenitore chiamando IAccessible accNavigate e specificando una delle costanti di navigazione.
ms.assetid: a1ebb50e-76cf-472d-bb0f-3f5bf5ed30d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e49772a267e49d723a04005dcbc8a369510b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300294"
---
# <a name="spatial-and-logical-navigation"></a>Navigazione spaziale e logica

I client recuperano le informazioni su un oggetto che è a livello di spazio o logicamente vicino a un altro oggetto all'interno dello stesso contenitore chiamando [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) e specificando una delle [costanti di navigazione](navigation-constants.md).

Con i client di *navigazione spaziale* passare a un oggetto in base alla relativa posizione sullo schermo. I client si spostano verso l'alto, verso il basso, a sinistra o a destra dall'oggetto corrente per ottenere informazioni su un altro oggetto all'interno dello stesso contenitore.

Con i client di *navigazione logica* passare all'oggetto che precede o segue logicamente un altro oggetto, come determinato dal server. I client passano a tutti gli elementi figlio di un oggetto in due modi:

-   Avviare la navigazione con [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) , quindi chiamare ripetutamente il metodo con [**NAVDIR \_ Next**](navigation-constants.md).
-   Avviare la navigazione con [**NAVDIR \_ LastChild**](navigation-constants.md) e chiamare ripetutamente il metodo con [**NAVDIR \_ precedente**](navigation-constants.md).

Indipendentemente dalla direzione, la navigazione visita ogni elemento figlio visibile che appartiene all'oggetto padre. Gli elementi figlio invisibili possono essere ignorati con la navigazione logica. Ogni elemento figlio viene inoltre visitato una sola volta e lo spostamento non viene eseguito in ciclo. Ovvero, il metodo ha esito negativo se un client tenta di spostarsi prima del primo oggetto o dopo l'ultimo oggetto.

La navigazione spaziale e logica sono correlate. Ad esempio, in una barra degli strumenti orizzontale, la chiamata al metodo con [**NAVDIR \_ right**](navigation-constants.md) dovrebbe produrre gli stessi risultati della chiamata al metodo con [**NAVDIR \_ Next**](navigation-constants.md).

L'oggetto iniziale della navigazione è l'oggetto stesso **o uno degli elementi figlio dell'oggetto, tranne quando** viene specificato [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) o [**NAVDIR \_ LastChild**](navigation-constants.md) . in questo caso, la navigazione deve iniziare dall'oggetto stesso.

Se un client passa da un oggetto accessibile a un elemento dell'interfaccia utente di pari livello oppure se il membro **LVAL** di *varStart* è **CHILDID \_ self** e il flag specificato *in NavDir* è un qualsiasi flag di navigazione eccetto [**navdir \_ FIRSTCHILD**](navigation-constants.md) o [**navdir \_ LastChild**](navigation-constants.md), il risultato in *pvarEnd* è un ID figlio o un'interfaccia [**IDispatch**](idispatch-interface.md) . Se *pvarEnd* contiene un ID figlio, i client devono innanzitutto ottenere un puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del padre per spostarsi da questo elemento dell'interfaccia utente o per ottenere ulteriori informazioni su di esso. Per ottenere l'oggetto padre, i client chiamano la proprietà [**IAccessible:: Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) dell'oggetto di pari livello o l'oggetto iniziale della navigazione.

Si noti che i client devono disporre di informazioni su tutti gli oggetti mobili chiamando la funzione [**EnumChildWindows**](/windows/desktop/api/winuser/nf-winuser-enumchildwindows) . Poiché un oggetto mobile non viene ritagliato nell'elemento padre, i client non dispongono di informazioni sulla relazione gerarchica tra due oggetti vicini sullo schermo.

Il grafico seguente è un esempio di oggetto mobile che non viene ritagliato nell'elemento padre.

![screenshot della finestra aperta che è mobile sopra una finestra di Microsoft Developer Studio di dimensioni maggiori](images/floatob.gif)

## <a name="establishing-the-order-in-logical-navigation"></a>Definizione dell'ordine nell'esplorazione logica

Nella navigazione logica gli sviluppatori che progettano gli oggetti stabiliscono le relazioni tra di essi. La navigazione logica è più soggettiva rispetto alla navigazione spaziale. Inoltre, l'ordine nell'esplorazione logica non corrisponde all'ordine utilizzato con gli ID figlio.

Per gli oggetti che dispongono di posizioni dello schermo, gli sviluppatori del server devono stabilire l'ordine di navigazione nel modo in cui la maggior parte degli utenti considera logica. Nei paesi/aree di lingua inglese, ad esempio, ciò significa un ordine da sinistra a destra, dall'alto verso il basso.

L'ordine di navigazione logico deve essere l'ordine di navigazione della tastiera parallelo. Ad esempio, una finestra di dialogo contiene i pulsanti **OK** e **Annulla** push e alcuni controlli di modifica. Un client che chiama [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) per passare all'oggetto successivo o precedente nella finestra di dialogo viene spostato nello stesso ordine in cui si preme TAB o MAIUSC + TAB per spostare lo stato attivo tra gli elementi.

Per gli oggetti che non hanno definito posizioni dello schermo, l'ordine logico viene deciso dagli sviluppatori del server e gli sviluppatori client non devono fare supposizioni. Ad esempio, è accettabile per gli oggetti non visibili, ad esempio gli oggetti che sono solo temporaneamente nascosti, da sparpagliare con gli oggetti visibili.

 

 