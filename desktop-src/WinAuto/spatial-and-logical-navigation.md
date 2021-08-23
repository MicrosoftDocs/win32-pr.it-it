---
title: Navigazione spaziale e logica
description: I client recuperano informazioni su un oggetto spaziale o logicamente vicino a un altro oggetto all'interno dello stesso contenitore chiamando IAccessible accNavigate e specificando una delle costanti di navigazione.
ms.assetid: a1ebb50e-76cf-472d-bb0f-3f5bf5ed30d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d762352c41f2adc764ac40c052632922a25ca995b9f2ec2f5008c668d0332bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052504"
---
# <a name="spatial-and-logical-navigation"></a>Navigazione spaziale e logica

I client recuperano informazioni su un oggetto spaziale o logicamente vicino a un altro oggetto all'interno dello stesso contenitore chiamando [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) e specificando una delle costanti [di navigazione](navigation-constants.md).

Con *la navigazione spaziale,* i client passano a un oggetto in base alla relativa posizione sullo schermo. I client si spostano verso l'alto, verso il basso, verso sinistra o verso destra dall'oggetto corrente per ottenere informazioni su un altro oggetto all'interno dello stesso contenitore.

Con *la navigazione logica,* i client passano all'oggetto che precede o segue logicamente un altro oggetto, come determinato dal server. I client passano a tutti gli elementi figlio di un oggetto in due modi:

-   Avviare la navigazione con [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) e quindi chiamare ripetutamente il metodo con [**NAVDIR \_ NEXT.**](navigation-constants.md)
-   Avviare la navigazione con [**NAVDIR \_ LASTCHILD e**](navigation-constants.md) chiamare ripetutamente il metodo con [**NAVDIR \_ PREVIOUS.**](navigation-constants.md)

Indipendentemente dalla direzione, la navigazione visita ogni elemento figlio visibile appartenente all'oggetto padre. Gli elementi figlio invisibili possono essere ignorati con la navigazione logica. Inoltre, ogni elemento figlio viene visitato una sola volta e la navigazione non scorre in ciclo. Ciò significa che il metodo ha esito negativo se un client tenta di spostarsi prima del primo oggetto o dopo l'ultimo oggetto.

La navigazione spaziale e logica è correlata. Ad esempio, in una barra degli strumenti orizzontale la chiamata al metodo con [**NAVDIR \_ RIGHT**](navigation-constants.md) dovrebbe produrre gli stessi risultati della chiamata al metodo con [**NAVDIR \_ NEXT.**](navigation-constants.md)

L'oggetto iniziale della navigazione è l'oggetto da esso creato o uno degli elementi figlio **dell'oggetto,** tranne quando viene specificato [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) o [**NAVDIR \_ LASTCHILD.**](navigation-constants.md) In questo caso, la navigazione deve iniziare dall'oggetto stesso.

Se un client passa da un oggetto accessibile a un elemento dell'interfaccia utente di pari livello o se il membro **lVal** di *varStart* è **CHILDID \_ SELF** e il flag specificato in *navDir* è qualsiasi flag di navigazione ad eccezione di [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) o [**NAVDIR \_ LASTCHILD,**](navigation-constants.md)il risultato in *pvarEnd* è un ID figlio o [**un'interfaccia IDispatch.**](idispatch-interface.md) Se *pvarEnd* contiene un ID figlio, i client devono prima ottenere un puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'elemento padre per spostarsi da questo elemento dell'interfaccia utente o per ottenere altre informazioni. Per ottenere l'oggetto padre, i client chiamano la proprietà [**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) dell'oggetto di pari livello o l'oggetto iniziale della navigazione.

Si noti che i client devono avere informazioni su tutti gli oggetti mobili chiamando la [**funzione EnumChildWindows.**](/windows/desktop/api/winuser/nf-winuser-enumchildwindows) Poiché un oggetto mobile non viene ritagliato in base all'elemento padre, i client non dispongono di informazioni sulla relazione gerarchica tra due oggetti vicini l'uno all'altro sullo schermo.

L'immagine seguente è un esempio di oggetto mobile che non viene ritagliato in base all'elemento padre.

![Screenshot della finestra aperta mobile sopra una finestra più grande di Microsoft Developer Studio](images/floatob.gif)

## <a name="establishing-the-order-in-logical-navigation"></a>Definizione dell'ordine nella navigazione logica

Nella navigazione logica gli sviluppatori che progettano gli oggetti stabiliscono le relazioni tra di essi. La navigazione logica è più soggettiva della navigazione spaziale. Inoltre, l'ordine nella navigazione logica non corrisponde all'ordine usato con gli ID figlio.

Per gli oggetti con posizioni dello schermo, gli sviluppatori di server devono stabilire l'ordine di navigazione nel modo in cui la maggior parte degli utenti considera logica. Nei paesi/aree geografiche di lingua inglese, ad esempio, questo significa un ordinamento da sinistra a destra e dall'alto verso il basso.

L'ordine di spostamento logico deve essere parallelo all'ordine di navigazione tramite tastiera. Ad esempio, una finestra di dialogo **contiene i** pulsanti di comando OK e **Annulla** e alcuni controlli di modifica. Un client che chiama [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) per passare all'oggetto successivo o precedente nella finestra di dialogo si sposta nello stesso ordine in cui un utente preme TAB o MAIUSC+TAB per spostare lo stato attivo tra gli elementi.

Per gli oggetti che non dispongono di posizioni dello schermo definite, l'ordine logico viene deciso dagli sviluppatori di server e gli sviluppatori client non devono fare supposizioni. Ad esempio, è accettabile che gli oggetti non visibili, ad esempio gli oggetti che sono solo temporaneamente nascosti, siano interconnessi con oggetti visibili.

 

 