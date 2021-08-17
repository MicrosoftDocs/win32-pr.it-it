---
title: EM_REDO messaggio (Richedit.h)
description: Invia un messaggio EM REDO a un controllo Rich Edit per ripetere l'azione successiva nella coda \_ di redo del controllo.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO dei messaggi Windows controlli
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
ms.openlocfilehash: d39b679e8bf7e78cf7ce028d0bb440438770d0d0123516313fb418b2136ebc11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437861"
---
# <a name="em_redo-message"></a>Messaggio \_ EM REDO

Invia un **messaggio \_ EM REDO** a un controllo Rich Edit per ripetere l'azione successiva nella coda di redo del controllo.

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

Se **l'operazione di ripristino** ha esito positivo, il valore restituito è un valore diverso da zero.

Se **l'operazione di ripristino** non riesce, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Per determinare se sono presenti azioni nella coda di redo del controllo, inviare il [**messaggio EM \_ CANREDO.**](em-canredo.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





