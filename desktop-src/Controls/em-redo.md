---
title: Messaggio di EM_REDO (RichEdit. h)
description: Invia un \_ messaggio di ripetizione em a un controllo Rich Edit per ripetere l'azione successiva nella coda di rollforward del controllo.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- Controlli di Windows Message EM_REDO
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477602"
---
# <a name="em_redo-message"></a>\_Messaggio di ripetizione em

Invia un messaggio di **\_ ripetizione em** a un controllo Rich Edit per ripetere l'azione successiva nella coda di rollforward del controllo.

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

Se l'operazione di **rollforward** ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione di **rollforward** ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Per determinare se sono presenti azioni nella coda di rollforward del controllo, inviare il messaggio [**\_ CANREDO em**](em-canredo.md) .

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

[**\_CANREDO em**](em-canredo.md)
</dt> <dt>

[**\_GETredoname em**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETundoname**](em-getundoname.md)
</dt> <dt>

[**\_Annulla**](em-undo.md)
</dt> </dl>

 

 





