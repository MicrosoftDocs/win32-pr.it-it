---
title: Messaggio di EM_GETBIDIOPTIONS (RichEdit. h)
description: Indica lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- Controlli di Windows Message EM_GETBIDIOPTIONS
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120015"
---
# <a name="em_getbidioptions-message"></a>\_Messaggio GETBIDIOPTIONS em

Indica lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) che riceve lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Questo messaggio imposta i valori dei membri **wMask** e **wEffects** sul valore dello stato corrente delle opzioni bidirezionali nel controllo Rich Edit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**\_SETBIDIOPTIONS em**](em-setbidioptions.md)
</dt> </dl>

 

 





