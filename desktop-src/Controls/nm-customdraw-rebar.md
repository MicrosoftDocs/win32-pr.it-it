---
title: NM_CUSTOMDRAW di notifica (rebar) (Commctrl.h)
description: Inviato dal controllo Rebar per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- NM_CUSTOMDRAW di notifica (rebar) Windows controlli
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
ms.openlocfilehash: 376bb9627d159dbb24080c2e475072dae357062975158d39f269e1cb7a4e3405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914871"
---
# <a name="nm_customdraw-rebar-notification-code"></a>Codice \_ di notifica NM CUSTOMDRAW (rebar)

Inviato dal controllo Rebar per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno. Il **membro dwItemSpec** di questa struttura contiene l'identificatore della banda da disegnare. Il **membro lItemlParam** di questa struttura contiene *lParam* della banda da disegnare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il **membro dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata contiene un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Il controllo verrà di disegno. Non invierà notifiche [NM \_ CUSTOMDRAW](nm-customdraw.md) aggiuntive per questo ciclo di disegno. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                    |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Il controllo invierà una notifica all'elemento padre di qualsiasi operazione di disegno correlata all'elemento. Invierà codici [di notifica NM \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo gli elementi di disegno. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                           |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Il controllo invierà una notifica all'elemento padre dopo la cancellazione di un elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Il controllo invierà una notifica all'elemento padre dopo il disegno di un elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                               |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | Il controllo invierà una notifica all'elemento padre di qualsiasi operazione di disegno correlata all'elemento. Invierà codici [di notifica NM \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo gli elementi di disegno. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                           |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. Il controllo userà il nuovo tipo di carattere. Per altre informazioni sulla modifica dei tipi di carattere, vedere Modifica [dei tipi di carattere e dei colori.](custom-draw.md) Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | L'applicazione ha estratto l'elemento manualmente. Il controllo non disegna l'elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                          |



 

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

 

 





