---
title: EM_CANUNDO messaggio (Winuser.h)
description: Determina se sono presenti azioni nella coda di annullamento di un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- EM_CANUNDO dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b1cb56b07232c6b55a85b7387cf7b2fafd40ac29e5dc0520b45e1aa50cadcb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915991"
---
# <a name="em_canundo-message"></a>Messaggio \_ EM CANUNDO

Determina se sono presenti azioni nella coda di annullamento di un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se sono presenti azioni nella coda di annullamento del controllo, il valore restituito è diverso da zero.

Se la coda di annullamento è vuota, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Se la coda di annullamento non è vuota, è possibile inviare il messaggio [**EM \_ UNDO**](em-undo.md) al controllo per annullare l'operazione più recente.

**Controlli di modifica e Rich Edit 1.0:** La coda di annullamento contiene solo l'operazione più recente.

**Rich Edit 2.0 e versioni successive:** La coda di annullamento può contenere più operazioni.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





