---
title: Messaggio di EM_SETEVENTMASK (RichEdit. h)
description: Imposta la maschera di eventi per un controllo Rich Edit. La maschera eventi specifica i codici di notifica che il controllo Invia alla finestra padre.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- Controlli di Windows Message EM_SETEVENTMASK
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
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478568"
---
# <a name="em_seteventmask-message"></a>\_Messaggio SETEVENTMASK em

Imposta la maschera di eventi per un controllo Rich Edit. La maschera eventi specifica i codici di notifica che il controllo Invia alla finestra padre.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova maschera eventi per il controllo Rich Edit. Per un elenco di maschere di eventi, vedere [**flag di maschera eventi del controllo Rich Edit**](rich-edit-control-event-mask-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce la maschera eventi precedente.

## <a name="remarks"></a>Commenti

La maschera di eventi predefinita (prima che sia impostato) è ENM \_ None.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETEVENTMASK em**](em-geteventmask.md)
</dt> <dt>

[**Flag di maschera eventi controllo Rich Edit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





