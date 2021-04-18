---
title: Codice di notifica TVN_ASYNCDRAW (COMmctrl. h)
description: Inviato da un controllo di visualizzazione albero al relativo elemento padre quando il disegno di un'icona o di una sovrapposizione non riesce. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- Controlli di Windows per il codice di notifica TVN_ASYNCDRAW
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
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302510"
---
# <a name="tvn_asyncdraw-notification-code"></a>\_Codice di notifica ASYNCDRAW di TVN

Inviato da un controllo di visualizzazione albero al relativo elemento padre quando il disegno di un'icona o di una sovrapposizione non riesce. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) . La struttura **NMTVASYNCDRAW** contiene il motivo per cui il progetto non è riuscito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il controllo di visualizzazione albero deve avere lo stile esteso [**\_ \_ DRAWIMAGEASYNC TV ex**](tree-view-control-window-extended-styles.md) . Si noti che questa operazione equivale al flag ASYNCDRAWN LVN di visualizzazione elenco \_ e allo stile corrispondente.

Questo controllo non viene disegnato in modo asincrono. Il valore asincrono viene usato nel contesto in cui il controllo di visualizzazione albero non estrae in modo sincrono un'immagine se non è disponibile. Ad esempio, l'immagine potrebbe non essere disponibile se il controllo di visualizzazione albero utilizza un elenco di immagini di tipo sparse, poiché l'immagine potrebbe essere scaricata. Al contrario, quando un'immagine non è disponibile, il controllo chiede in modo sincrono all'elemento padre quale azione intraprendere inviando al padre una \_ notifica ASYNCDRAW di TVN con una struttura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) . Il membro **HR** di questa struttura descrive il motivo per cui il progetto del controllo ha avuto esito negativo. Un risultato **HR** di E \_ in sospeso indica che l'immagine non è presente (l'immagine deve essere estratta). Success indica che l'immagine è presente ma non con la qualità dell'immagine richiesta.

Il padre imposta il membro **dwRetFlags** della struttura per informare il controllo come procedere. Ad esempio, l'elemento padre può restituire un'altra immagine, nel membro **iRetImageIndex** , per il controllo da creare. In questo caso, l'elemento padre imposta il membro **dwRetFlags** su ADRF \_ DRAWIMAGE. Se il controllo rileva che l'immagine restituita non è stata estratta, è \_ possibile che il controllo invii un'altra notifica ASYNCDRAW di TVN.

Se un'immagine non è disponibile, l'idea dietro asincrona consiste nel consentire all'elemento padre di eseguire l'estrazione in background, in modo che l'estrazione non blocchi il thread dell'interfaccia utente, ovvero il thread su cui si trova il controllo. L'elemento padre può restituire ADRF \_ DRAWNOTHING al controllo, quindi avviare un thread in background per estrarre l'icona. Una volta estratto, l'elemento padre può impostare l'icona nel controllo TreeView con la macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem). In questo modo, la visualizzazione albero non invalida l'elemento e infine lo ridisegna con l'immagine estratta nell'elenco immagini.

L'esempio di codice seguente, da usare come parte di un programma più ampio, Mostra come un elemento padre può elaborare due possibili codici restituiti in questa notifica da un controllo e decidere quale azione deve assumere il controllo. L'impostazione di **dwRetFlags** non viene visualizzata.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





