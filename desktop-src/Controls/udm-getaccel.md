---
title: UDM_GETACCEL messaggio (Commctrl.h)
description: Recupera informazioni sull'accelerazione per un controllo di scorrimento.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3603f364a6caa4f4726460e4b5b71e0d79564fbe9178414576fbed2ce5f5777d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132191"
---
# <a name="udm_getaccel-message"></a>Messaggio GETACCEL di UDM \_

Recupera informazioni sull'accelerazione per un controllo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi nella matrice specificata da *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di [**strutture UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) che ricevono informazioni sull'accelerazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di tasti di scelta rapida attualmente impostati per il controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UDM \_ SETACCEL**](udm-setaccel.md)
</dt> </dl>

 

 





