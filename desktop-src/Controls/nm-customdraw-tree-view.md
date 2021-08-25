---
title: NM_CUSTOMDRAW di notifica (visualizzazione albero) (Commctrl.h)
description: Inviato da un controllo di visualizzazione albero per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- NM_CUSTOMDRAW di notifica (visualizzazione struttura ad albero) Windows controlli
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9571d8461b43cebe047d80933af53a0c1aa1b865ede6280b8de2a33b74a60f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088841"
---
# <a name="nm_customdraw-tree-view-notification-code"></a>Codice \_ di notifica NM CUSTOMDRAW (visualizzazione albero)

Inviato da un controllo di visualizzazione albero per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) che contiene e riceve informazioni sull'operazione di disegno. Il **membro dwItemSpec** del membro **nmcd** di questa struttura contiene l'handle dell'elemento da disegnare. Il **membro lItemlParam** del **membro nmcd** di questa struttura contiene *il parametro lParam* dell'elemento da disegnare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il **membro dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata contiene un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Il controllo disegna se stesso. Non invia codici [NM \_ CUSTOMDRAW](nm-customdraw.md) aggiuntivi per questo ciclo di disegno. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Il controllo notifica all'elemento padre qualsiasi operazione di disegno correlata all'elemento. Invia i [codici di notifica NM \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo gli elementi di disegno. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Il controllo invia una notifica all'elemento padre dopo la cancellazione di un elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Il controllo invia una notifica all'elemento padre dopo il disegno di un elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versione 4.71.](common-control-versions.md) Il controllo notifica all'elemento padre quando viene disegnato un elemento secondario della visualizzazione elenco. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. Il controllo userà il nuovo tipo di carattere. Per altre informazioni sulla modifica dei tipi di carattere, vedere Modifica [dei tipi di carattere e dei colori.](custom-draw.md) Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | L'applicazione ha creato l'elemento manualmente. Il controllo non disegna l'elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

[Versione 5.80.](common-control-versions.md) Se si modifica il tipo di carattere tramite la restituzione di [**CDRF \_ NEWFONT**](cdrf-constants.md), il controllo visualizzazione albero potrebbe visualizzare testo ritagliato. Questo comportamento è necessario per la compatibilità con le versioni precedenti dei controlli comuni. Se si vuole modificare il tipo di carattere di un controllo di visualizzazione albero, si otterrà un risultato migliore se si invia un messaggio [**\_ CCM SETVERSION**](ccm-setversion.md) con il valore *wParam* impostato su 5 prima di aggiungere elementi al controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso del disegno personalizzato](custom-draw.md)
</dt> </dl>

 

 





