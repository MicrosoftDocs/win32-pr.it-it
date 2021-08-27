---
title: EM_SETEVENTMASK messaggio (Richedit.h)
description: Imposta la maschera evento per un controllo Rich Edit. La maschera eventi specifica i codici di notifica che il controllo invia alla finestra padre.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244274d969473531bae7c1d124af24a88d6b98d9db8bdbe073d054a3a9e36ac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048501"
---
# <a name="em_seteventmask-message"></a>Messaggio \_ EM SETEVENTMASK

Imposta la maschera evento per un controllo Rich Edit. La maschera eventi specifica i codici di notifica che il controllo invia alla finestra padre.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova maschera evento per il controllo Rich Edit. Per un elenco di maschere evento, vedere Flag di maschera eventi del [**controllo Rich Edit.**](rich-edit-control-event-mask-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce la maschera evento precedente.

## <a name="remarks"></a>Commenti

La maschera di evento predefinita (prima dell'impostazione di qualsiasi) è ENM \_ NONE.

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

[**EM \_ GETEVENTMASK**](em-geteventmask.md)
</dt> <dt>

[**Flag di maschera eventi del controllo Rich Edit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





