---
title: Codice di notifica EN_SEARCHWEB (CommCtrl. h)
description: Inviato quando un controllo di modifica perde lo stato attivo della tastiera. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un \_ messaggio di notifica WM.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- Controlli di Windows per il codice di notifica EN_SEARCHWEB
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475388"
---
# <a name="en_searchweb-notification-code"></a>\_Codice di notifica en SEARCHWEB

Inviato dopo che un controllo di modifica ha eseguito una ricerca Web quando è abilitata la funzionalità "Cerca sul Web", vedere [EM_ENABLESEARCHWEB](em-enablesearchweb.md). La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il controllo di modifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10, 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_ENABLESEARCHWEB em**](em-enablesearchweb.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_notifica WM**](wm-notify.md)
</dt> </dl>

 

 





