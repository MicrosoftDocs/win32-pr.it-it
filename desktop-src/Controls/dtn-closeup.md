---
title: Codice di notifica DTN_CLOSEUP (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) quando l'utente chiude il calendario mensile a discesa.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- Controlli di Windows per il codice di notifica DTN_CLOSEUP
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
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742831"
---
# <a name="dtn_closeup-notification-code"></a>\_Codice di notifica closeup DTN

Inviato da un controllo di selezione data e ora (DTP) quando l'utente chiude il calendario mensile a discesa. Il calendario mensile viene chiuso quando l'utente sceglie una data del calendario mensile o fa clic sulla freccia a discesa mentre il calendario è aperto. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sulla notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

I controlli DTP non gestiscono un controllo calendario mensile figlio statico. Il controllo DTP Elimina il controllo di calendario mensile figlio prima di inviare il codice di notifica. Quindi, l'applicazione non deve basarsi su un handle di finestra statico per il calendario mensile figlio del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[\_elenco a discesa DTN](dtn-dropdown.md)
</dt> <dt>

[**\_GETMONTHCAL DTM**](dtm-getmonthcal.md)
</dt> </dl>

 

 





