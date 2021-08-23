---
title: EM_GETBIDIOPTIONS messaggio (Richedit.h)
description: Indica lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- EM_GETBIDIOPTIONS dei messaggi Windows controlli
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
ms.openlocfilehash: 90b377e0fd3a439737fea9efbc403d2ccc64d6cf78eab1c7e31feeffd6c4b0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019909"
---
# <a name="em_getbidioptions-message"></a>Messaggio \_ EM GETBIDIOPTIONS

Indica lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) che riceve lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo messaggio imposta i valori dei membri **wMask** e **wEffects** sul valore dello stato corrente delle opzioni bidirezionali nel controllo Rich Edit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | Rich Edit 3.0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**OPZIONI DI OFFERTA**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ SETBIDIOPTIONS**](em-setbidioptions.md)
</dt> </dl>

 

 





