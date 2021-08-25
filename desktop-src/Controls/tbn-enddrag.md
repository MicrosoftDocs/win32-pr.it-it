---
title: TBN_ENDDRAG di notifica (Commctrl.h)
description: Notifica alla finestra padre della barra degli strumenti che l'utente ha interrotto il trascinamento di un pulsante in una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- TBN_ENDDRAG codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff6cfff7448f452223681ef1ebf720e0330c1fee52ba48862411978d53a0616
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876871"
---
# <a name="tbn_enddrag-notification-code"></a>Codice di \_ notifica TBN ENDDRAG

Notifica alla finestra padre della barra degli strumenti che l'utente ha interrotto il trascinamento di un pulsante in una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Il **membro iItem** contiene l'identificatore di comando del pulsante trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





