---
title: Costanti RF (CommCtrl. h)
description: Queste costanti vengono usate come valori restituiti da un controllo in risposta a un codice di \_ notifica CUSTOMDRAW di nm.
ms.assetid: 6b05e27e-5d18-46f2-b326-2a5148597852
topic_type:
- apiref
api_name:
- CDRF_DODEFAULT
- CDRF_NEWFONT
- CDRF_SKIPDEFAULT
- CDRF_DOERASE
- CDRF_NOTIFYPOSTPAINT
- CDRF_NOTIFYITEMDRAW
- CDRF_NOTIFYSUBITEMDRAW
- CDRF_NOTIFYPOSTERASE
- CDRF_SKIPPOSTPAINT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ec83b8f8238e4236bbee3f7091c228c552efb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327684"
---
# <a name="rf-constants"></a>Costanti RF

Queste costanti vengono usate come valori restituiti da un controllo in risposta a un codice di notifica [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) .



| Costante/valore                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CDRF_DODEFAULT"></span><span id="cdrf_dodefault"></span><dl> <dt>**CDRF \_**</dt> <dt>0x00000000</dt> DODEFAULT </dl>                         | Il controllo viene disegnato automaticamente. Non invierà alcun codice di [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno. Questo errore si verifica quando il **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                               |
| <span id="CDRF_NEWFONT"></span><span id="cdrf_newfont"></span><dl> <dt>**CDRF \_**</dt> <dt>0x00000002</dt> NEWFONT </dl>                               | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere. Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere modifica di tipi di carattere e colori. Questo errore si verifica quando il **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                      |
| <span id="CDRF_SKIPDEFAULT"></span><span id="cdrf_skipdefault"></span><dl> <dt>**CDRF \_**</dt> <dt>0x00000004</dt> SKIPDEFAULT </dl>                   | L'applicazione ha disegnato manualmente l'elemento. L'elemento non viene disegnato dal controllo. Questo errore si verifica quando il **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                          |
| <span id="CDRF_DOERASE"></span><span id="cdrf_doerase"></span><dl> <dt>**CDRF \_**</dt> <dt>0x00000008</dt> DOERASE </dl>                               | **Windows Vista e versioni successive.** Il controllo trarrà lo sfondo.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CDRF_NOTIFYPOSTPAINT"></span><span id="cdrf_notifypostpaint"></span><dl> <dt>**CDRF \_**</dt> <dt>0x00000010</dt> NOTIFYPOSTPAINT </dl>       | Il controllo invierà una notifica al padre dopo aver disegnato un elemento. Questo errore si verifica quando il **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                                                                                               |
| <span id="CDRF_NOTIFYITEMDRAW"></span><span id="cdrf_notifyitemdraw"></span><dl> <dt>**CDRF \_**</dt> <dt>0x00000020</dt> NOTIFYITEMDRAW </dl>          | Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi. Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi. Questo errore si verifica quando il **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PrePaint.<br/>                                                                                                                           |
| <span id="CDRF_NOTIFYSUBITEMDRAW"></span><span id="cdrf_notifysubitemdraw"></span><dl> <dt>**CDRF \_**</dt> <dt>0x00000020</dt> NOTIFYSUBITEMDRAW </dl> | **Internet Explorer 4,0 e versioni successive.** Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi. Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi. Questo errore si verifica quando il **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PrePaint. Questo flag è identico a **CDRF \_ NOTIFYITEMDRAW** e il relativo utilizzo è dipendente dal contesto.<br/> |
| <span id="CDRF_NOTIFYPOSTERASE"></span><span id="cdrf_notifyposterase"></span><dl> <dt>**CDRF \_**</dt> <dt>0x00000040</dt> NOTIFYPOSTERASE </dl>       | Il controllo invierà una notifica al padre dopo la cancellazione di un elemento. Questo errore si verifica quando il **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                                                                                                |
| <span id="CDRF_SKIPPOSTPAINT"></span><span id="cdrf_skippostpaint"></span><dl> <dt>**CDRF \_**</dt> <dt>0x00000100</dt> SKIPPOSTPAINT </dl>             | **Windows Vista e versioni successive.** Il controllo non trarrà il rettangolo di attivazione.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Commenti

Queste costanti sono definite in commctrl. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione dell'aspetto di un controllo mediante il progetto personalizzato](custom-draw.md)
</dt> </dl>

 

 





