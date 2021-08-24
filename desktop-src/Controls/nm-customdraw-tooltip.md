---
title: NM_CUSTOMDRAW (descrizione comando) codice di notifica (Commctrl.h)
description: Inviato da un controllo descrizione comando per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- NM_CUSTOMDRAW di notifica (descrizione comando) Windows controlli
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
ms.openlocfilehash: cc75a12bdf216c03892656f25dd41ba93c35346cf5aead08758f917fec29bb8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816381"
---
# <a name="nm_customdraw-tooltip-notification-code"></a>Codice \_ di notifica NM CUSTOMDRAW (descrizione comando)

Inviato da un controllo descrizione comando per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) che contiene informazioni sull'operazione di disegno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il **membro dwDrawStage** della struttura [**NMCUSTOMDRAW associata**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) contiene un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Il controllo disegna se stesso. Non invierà altri codici di [notifica NM \_ CUSTOMDRAW](nm-customdraw.md) per questo ciclo di disegno. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ PREPAINT.<br/>                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Il controllo invierà una notifica all'elemento padre di qualsiasi operazione di disegno correlata all'elemento. Invierà i [codici di notifica DI NM \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo gli elementi di disegno. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ PREPAINT.<br/>                                            |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Il controllo invierà una notifica all'elemento padre dopo la cancellazione di un elemento. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Il controllo invierà una notifica all'elemento padre dopo il disegno di un elemento. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versione 4.71](common-control-versions.md). Il controllo invierà una notifica all'elemento padre quando viene disegnato un elemento secondario della visualizzazione elenco. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ PREPAINT.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. Il controllo userà il nuovo tipo di carattere. Per altre informazioni sulla modifica dei tipi di carattere, vedere [Modifica di tipi di carattere e colori](custom-draw.md). Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**SKIPDEFAULT DI CDRF \_**</dt> </dl>       | L'applicazione ha creato l'elemento manualmente. Il controllo non disegna l'elemento. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso del disegno personalizzato](custom-draw.md)
</dt> </dl>

 

 





