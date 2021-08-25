---
title: EN_SEARCHWEB di notifica (CommCtrl.h)
description: Inviato quando un controllo di modifica perde lo stato attivo della tastiera. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio WM \_ NOTIFY.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB del codice di notifica Windows controlli
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
ms.openlocfilehash: 606f53427426e4c9d20c2e4c12245569ed1d8a53ed7ea29162516f6d65fd1baa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047471"
---
# <a name="en_searchweb-notification-code"></a>EN \_ SEARCH Codice di notifica WEB

Inviato dopo che un controllo di modifica ha eseguito una ricerca Web quando è abilitata la funzionalità "Cerca nel [Web", vedere EM_ENABLESEARCHWEB](em-enablesearchweb.md). La finestra padre del controllo di modifica riceve questo codice di notifica tramite un [**messaggio WM \_ NOTIFY.**](wm-notify.md)


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

Puntatore a una [**struttura NMSEARCHWEB.**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2019 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





