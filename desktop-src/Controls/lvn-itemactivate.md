---
title: LVN_ITEMACTIVATE di notifica (Commctrl.h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente attiva un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21b02406157a13d2fcf110c15e692211b26b3f9da31741489e317e6b2c68309
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105051"
---
# <a name="lvn_itemactivate-notification-code"></a>Codice di notifica LVN \_ ITEMACTIVATE

Inviato da un controllo di visualizzazione elenco quando l'utente attiva un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

[Versione 4.71.](common-control-versions.md) Puntatore a [**una struttura NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) che contiene informazioni su questo codice di notifica.

[Versione 4.70](common-control-versions.md) e precedenti. Puntatore a una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che riceve questo codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

Per ottenere gli elementi da attivare, l'applicazione ricevente deve usare il messaggio [**LVM \_ GETSELECTEDCOUNT**](lvm-getselectedcount.md) per recuperare il numero di elementi selezionati e quindi inviare il messaggio [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) con **LVNI \_ SELECTED** fino a quando non vengono recuperati tutti gli elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





