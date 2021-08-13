---
title: HDN_FILTERBTNCLICK di notifica (Commctrl.h)
description: Notifica la finestra padre del controllo intestazione quando si fa clic sul pulsante di filtro o in risposta a un messaggio \_ HDM SETITEM. Codice di notifica inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ba216c9946854ccfc6a651db90ab1dd5ed106dfca6ddf568d485c33dae70ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435511"
---
# <a name="hdn_filterbtnclick-notification-code"></a>Codice di notifica \_ HDN FILTERBTNCLICK

Notifica la finestra padre del controllo intestazione quando si fa clic sul pulsante di filtro o in risposta a un [**messaggio \_ HDM SETITEM.**](hdm-setitem.md) Codice di notifica inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) che contiene informazioni sul controllo intestazione e sul pulsante del filtro di intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si restituisce **TRUE,** verrà inviato un codice di notifica [ \_ FILTERCHANGE HDN](hdn-filterchange.md) alla finestra padre del controllo intestazione. Questo codice di notifica offre alla finestra padre la possibilità di sincronizzare gli elementi dell'interfaccia utente. Restituisce **FALSE** se non si vuole inviare la notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





