---
title: TVN_ASYNCDRAW di notifica (Commctrl.h)
description: Inviato da un controllo di visualizzazione albero al relativo elemento padre quando il disegno di un'icona o di una sovrimpressione non è riuscito. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4d929977e1a14a5ada96232fa054c2689d27f1eaa026b64c974d51f5a2c38c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060101"
---
# <a name="tvn_asyncdraw-notification-code"></a>Codice di notifica \_ TVN ASYNCDRAW

Inviato da un controllo di visualizzazione albero al relativo elemento padre quando il disegno di un'icona o di una sovrimpressione non è riuscito. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTVASYNCDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) La **struttura NMTVASYNCDRAW** contiene il motivo per cui il disegno non è riuscito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il controllo visualizzazione albero deve avere lo stile [**esteso TVS \_ EX \_ DRAWIMAGEASYNC.**](tree-view-control-window-extended-styles.md) Si noti che è equivalente al flag LVN ASYNCDRAWN della visualizzazione elenco e \_ al relativo stile corrispondente.

Questo controllo non disegna in modo asincrono. L'oggetto asincrono viene utilizzato nel contesto in cui il controllo visualizzazione albero non estrae in modo sincrono un'immagine se non è disponibile. Ad esempio, l'immagine potrebbe non essere disponibile se il controllo visualizzazione albero usa un elenco di immagini di tipo sparse, poiché l'immagine potrebbe essere scaricata. Quando invece un'immagine non è disponibile, il controllo chiede in modo sincrono all'elemento padre quale azione eseguire inviando all'elemento padre una notifica TVN ASYNCDRAW con una struttura \_ [**NMTVASYNCDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) Il **membro hr** di questa struttura descrive il motivo per cui il disegno del controllo non è riuscito. Un **risultato hr** di E PENDING indica che l'immagine non è presente \_ (l'immagine deve essere estratta). Esito positivo indica che l'immagine è presente ma non alla qualità dell'immagine richiesta.

L'elemento padre **imposta il membro dwRetFlags** della struttura per informare il controllo su come procedere. Ad esempio, l'elemento padre può restituire un'altra immagine, nel membro **iRetImageIndex,** per il controllo da disegnare. In questo caso, l'elemento padre imposta **il membro dwRetFlags** su ADRF \_ DRAWIMAGE. Se il controllo rileva che l'immagine restituita non è stata estratta, è possibile che il controllo invii un'altra \_ notifica TVN ASYNCDRAW.

Se un'immagine non è disponibile, l'idea alla base dell'operazione asincrona è quella di consentire all'elemento padre di eseguire l'estrazione in background in modo che l'estrazione non blocchi il thread dell'interfaccia utente, ad esempio il thread su cui si trova il controllo. L'elemento padre può restituire ADRF \_ DRAWNOTHING al controllo, quindi avviare un thread in background per estrarre l'icona. Dopo l'estrazione, l'elemento padre può impostare l'icona nel controllo treeview con la macro [**TreeView \_ SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) In questo modo la visualizzazione albero invalida l'elemento e infine lo ridisegna con l'immagine estratta nell'elenco di immagini.

Nell'esempio di codice seguente, da utilizzare come parte di un programma più ampio, viene illustrato come un elemento padre può elaborare due possibili codici restituiti in questa notifica da un controllo e decidere quale azione deve eseguire il controllo. **L'impostazione di dwRetFlags** non viene visualizzata.


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





