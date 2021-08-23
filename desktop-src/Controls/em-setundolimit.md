---
title: EM_SETUNDOLIMIT messaggio (Richedit.h)
description: Imposta il numero massimo di azioni che possono essere archiviate nella coda di annullamento di un controllo Rich Edit.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT del messaggio Windows controlli
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771e339e38437ea0299e5da6120fa555fd26148f72ff7da4e0287ed46cc4ad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697521"
---
# <a name="em_setundolimit-message"></a>MESSAGGIO EM \_ SETUNDOLIMIT

Imposta il numero massimo di azioni che possono essere archiviate nella coda di annullamento di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il numero massimo di azioni che possono essere archiviate nella coda di annullamento.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il nuovo numero massimo di azioni di annullamento per il controllo Rich Edit. Questo valore può essere minore di *wParam* se la memoria è limitata.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il numero massimo di azioni nella coda di annullamento è 100. Se si aumenta questo numero, deve essere disponibile memoria sufficiente per contenere il nuovo numero. Per ottenere prestazioni migliori, impostare il limite sul valore più piccolo possibile.

Se si imposta il limite su zero, la funzionalità **Annulla viene disabilitata.**

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

[**EM \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ REDO**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





