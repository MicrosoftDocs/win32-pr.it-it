---
title: DTN_CLOSEUP di notifica (Commctrl.h)
description: Inviato da un controllo di selezione data e ora quando l'utente chiude il calendario mensile a discesa.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97cd2d799d05afc638b60adc9203eaad80feb159f985df8b3813403bf5ca0d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877721"
---
# <a name="dtn_closeup-notification-code"></a>Codice di notifica DTN \_ CLOSEUP

Inviato da un controllo di selezione data e ora quando l'utente chiude il calendario mensile a discesa. Il calendario mensile viene chiuso quando l'utente sceglie una data dal calendario mensile o fa clic sulla freccia a discesa mentre il calendario è aperto. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni sulla notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

I controlli DTP non mantengono un controllo calendario mensile figlio statico. Il controllo DTP elimina il controllo calendario mensile figlio prima di inviare questo codice di notifica. L'applicazione non deve quindi basarsi su un handle di finestra statico per il calendario mensile figlio del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[ELENCO A DISCESA \_ DTN](dtn-dropdown.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

 





