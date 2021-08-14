---
title: EN_OBJECTPOSITIONS di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Rich Edit quando il controllo legge negli oggetti . Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- EN_OBJECTPOSITIONS del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3be6f3f41877a56396ef021e97130f4c174516160d7243144f10ea1dfd3951b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436691"
---
# <a name="en_objectpositions-notification-code"></a>Codice di notifica EN \_ OBJECTPOSITIONS

Notifica alla finestra padre di un controllo Rich Edit quando il controllo legge negli oggetti . Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**OBJECTPOSITIONS.**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire zero per continuare **l'operazione di** lettura.

Restituire un valore diverso da zero per arrestare **l'operazione di** lettura.

## <a name="remarks"></a>Commenti

Per ricevere un codice di notifica EN OBJECTPOSITIONS, specificare il \_ flag [**ENM \_ OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

