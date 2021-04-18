---
title: Codice di notifica di NM_CUSTOMDRAW (intestazione) (COMmctrl. h)
description: Inviato da un controllo intestazione per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- Codice di notifica di NM_CUSTOMDRAW (intestazione) controlli Windows
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302792"
---
# <a name="nm_customdraw-header-notification-code"></a>\_Codice di notifica di CUSTOMDRAW (intestazione) Nm

Inviato da un controllo intestazione per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno. Il membro **dwItemSpec** di questa struttura contiene l'indice dell'elemento da disegnare e il membro **lItemlParam** di questa struttura contiene l'elemento *lParam* dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_DODEFAULT CDRF**</dt> </dl>         | Il controllo viene disegnato automaticamente. Non invierà alcun messaggio [ \_ CUSTOMDRAW Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                       |
| <dl> <dt>**\_NOTIFYITEMDRAW CDRF**</dt> </dl>    | Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi. Invierà i \_ codici di notifica di CUSTOMDRAW prima e dopo il disegno degli elementi. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                              |
| <dl> <dt>**\_NOTIFYPOSTERASE CDRF**</dt> </dl>   | Il controllo invierà una notifica al padre dopo la cancellazione di un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                              |
| <dl> <dt>**\_NOTIFYPOSTPAINT CDRF**</dt> </dl>   | Il controllo invierà una notifica al padre dopo aver disegnato un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                             |
| <dl> <dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt> </dl> | [Versioni di controllo comuni](common-control-versions.md). Il controllo invierà una notifica all'elemento padre quando viene disegnato un sottoelemento di visualizzazione elenco. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                    |
| <dl> <dt>**\_NEWFONT CDRF**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere. Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md). Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**\_SKIPDEFAULT CDRF**</dt> </dl>       | L'applicazione ha disegnato manualmente l'elemento. L'elemento non viene disegnato dal controllo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Per ulteriori informazioni, vedere [utilizzo del progetto personalizzato](custom-draw.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





