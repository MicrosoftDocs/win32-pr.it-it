---
title: Codice di notifica di NM_CUSTOMDRAW (descrizione comando) (COMmctrl. h)
description: Inviato da un controllo ToolTip per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- NM_CUSTOMDRAW (descrizione comando) il codice di notifica controlli Windows
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
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743978"
---
# <a name="nm_customdraw-tooltip-notification-code"></a>\_Codice di notifica di CUSTOMDRAW Nm (descrizione comando)

Inviato da un controllo ToolTip per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) che contiene informazioni sull'operazione di disegno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_DODEFAULT CDRF**</dt> </dl>         | Il controllo viene disegnato automaticamente. Non invierà alcun codice di [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                |
| <dl> <dt>**\_NOTIFYITEMDRAW CDRF**</dt> </dl>    | Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi. Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                            |
| <dl> <dt>**\_NOTIFYPOSTERASE CDRF**</dt> </dl>   | Il controllo invierà una notifica al padre dopo la cancellazione di un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                 |
| <dl> <dt>**\_NOTIFYPOSTPAINT CDRF**</dt> </dl>   | Il controllo invierà una notifica al padre dopo aver disegnato un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                |
| <dl> <dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt> </dl> | [Versione 4,71](common-control-versions.md). Il controllo invierà una notifica all'elemento padre quando viene disegnato un sottoelemento di visualizzazione elenco. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                  |
| <dl> <dt>**\_NEWFONT CDRF**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. Il controllo utilizzerà il nuovo tipo di carattere. Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md). Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**\_SKIPDEFAULT CDRF**</dt> </dl>       | L'applicazione ha disegnato manualmente l'elemento. L'elemento non viene disegnato dal controllo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di un progetto personalizzato](custom-draw.md)
</dt> </dl>

 

 





