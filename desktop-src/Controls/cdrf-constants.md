---
title: Costanti RF (CommCtrl.h)
description: Queste costanti vengono usate come valori restituiti da un controllo in risposta a un codice di notifica NM \_ CUSTOMDRAW.
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
ms.openlocfilehash: 817bab7c2ec41134d71c92ada94c62475b01cc2db96a9f8c74ecb2c7b9274451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770381"
---
# <a name="rf-constants"></a>Costanti RF

Queste costanti vengono usate come valori restituiti da un controllo in risposta a un [codice di notifica NM \_ CUSTOMDRAW.](nm-customdraw.md)



| Costante/valore                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CDRF_DODEFAULT"></span><span id="cdrf_dodefault"></span><dl> <dt>**CDRF \_ DoDEFAULT**</dt> <dt>0x00000000</dt> </dl>                         | Il controllo verrà di disegno. Non invierà codici di notifica [NM \_ CUSTOMDRAW](nm-customdraw.md) aggiuntivi per questo ciclo di disegno. Questo errore si verifica **quando dwDrawStage** della [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                               |
| <span id="CDRF_NEWFONT"></span><span id="cdrf_newfont"></span><dl> <dt>**CDRF \_ NEWFONT**</dt> <dt>0x00000002</dt> </dl>                               | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. Il controllo userà il nuovo tipo di carattere. Per altre informazioni sulla modifica dei tipi di carattere, vedere Modifica di tipi di carattere e colori. Questo errore si verifica **quando dwDrawStage** della [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                      |
| <span id="CDRF_SKIPDEFAULT"></span><span id="cdrf_skipdefault"></span><dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> <dt>0x00000004</dt> </dl>                   | L'applicazione ha estratto l'elemento manualmente. Il controllo non disegna l'elemento. Questo errore si verifica **quando dwDrawStage** della [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                          |
| <span id="CDRF_DOERASE"></span><span id="cdrf_doerase"></span><dl> <dt>**CDRF \_ DoERASE**</dt> <dt>0x00000008</dt> </dl>                               | **Windows Vista e versioni successive.** Il controllo disegna lo sfondo.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CDRF_NOTIFYPOSTPAINT"></span><span id="cdrf_notifypostpaint"></span><dl> <dt>**CDRF \_ NotifyPOSTPAINT**</dt> <dt>0x00000010</dt> </dl>       | Il controllo invierà una notifica all'elemento padre dopo il disegno di un elemento. Questo errore si verifica **quando dwDrawStage** della [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                               |
| <span id="CDRF_NOTIFYITEMDRAW"></span><span id="cdrf_notifyitemdraw"></span><dl> <dt>**CDRF \_ NOTIFICAITEMDRAW**</dt> <dt>0x00000020</dt> </dl>          | Il controllo invierà una notifica all'elemento padre di qualsiasi operazione di disegno correlata all'elemento. Invierà codici [di notifica NM \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo gli elementi di disegno. Questo errore si verifica **quando dwDrawStage** della [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                           |
| <span id="CDRF_NOTIFYSUBITEMDRAW"></span><span id="cdrf_notifysubitemdraw"></span><dl> <dt>**CDRF \_ NOTIFICASUBITEMDRAW**</dt> <dt>0x00000020</dt> </dl> | **Internet Explorer 4.0 e versioni successive.** Il controllo invierà una notifica all'elemento padre di qualsiasi operazione di disegno correlata all'elemento. Invierà codici [di notifica NM \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo gli elementi di disegno. Questo errore si verifica **quando dwDrawStage** della [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PREPAINT. Questo flag è identico a **CDRF \_ NOTIFYITEMDRAW** e il relativo utilizzo dipende dal contesto.<br/> |
| <span id="CDRF_NOTIFYPOSTERASE"></span><span id="cdrf_notifyposterase"></span><dl> <dt>**CDRF \_ NotifyPOSTERASE**</dt> <dt>0x00000040</dt> </dl>       | Il controllo invierà una notifica all'elemento padre dopo la cancellazione di un elemento. Questo errore si verifica **quando dwDrawStage** della [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                                |
| <span id="CDRF_SKIPPOSTPAINT"></span><span id="cdrf_skippostpaint"></span><dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> <dt>0x00000100</dt> </dl>             | **Windows Vista e versioni successive.** Il controllo non disegna il rettangolo di attivazione.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Commenti

Queste costanti sono definite in Commctrl.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione dell'aspetto di un controllo tramite disegno personalizzato](custom-draw.md)
</dt> </dl>

 

 





