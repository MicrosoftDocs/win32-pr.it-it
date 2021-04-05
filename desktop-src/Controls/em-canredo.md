---
title: Messaggio di EM_CANREDO (RichEdit. h)
description: Determina se sono presenti azioni nella coda di rollforward del controllo.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- Controlli di Windows Message EM_CANREDO
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874125"
---
# <a name="em_canredo-message"></a>\_Messaggio CANREDO em

Determina se sono presenti azioni nella coda di rollforward del controllo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se sono presenti azioni nella coda di rollforward del controllo, il valore restituito è un valore diverso da zero.

Se la coda di rollforward è vuota, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Per ripetere l'operazione di annullamento più recente, inviare il messaggio di [**\_ ripetizione em**](em-redo.md) .

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

[**\_GETredoname em**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETundoname**](em-getundoname.md)
</dt> <dt>

[**\_ripetizione em**](em-redo.md)
</dt> <dt>

[**\_Annulla**](em-undo.md)
</dt> </dl>

 

 





