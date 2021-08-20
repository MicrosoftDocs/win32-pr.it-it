---
title: TB_SETANCHORHIGHLIGHT messaggio (Commctrl.h)
description: Imposta l'impostazione di evidenziazione dell'ancoraggio per una barra degli strumenti.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a66193aebee80a2ffde97b7e802b5bab750f0a9e2f1773b32d872211d52150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167984"
---
# <a name="tb_setanchorhighlight-message"></a>TB \_ SETANCHORHIGHLIGHT message

Imposta l'impostazione di evidenziazione dell'ancoraggio per una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Valore BOOL** che specifica se l'evidenziazione dell'ancoraggio è abilitata o disabilitata. Se questo valore è diverso da zero, verrà abilitata l'evidenziazione dell'ancoraggio. Se questo valore è zero, l'evidenziazione dell'ancoraggio verrà disabilitata.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'impostazione di evidenziazione dell'ancoraggio precedente. Se questo valore è diverso da zero, è stata abilitata l'evidenziazione dell'ancoraggio. Se questo valore è zero, l'evidenziazione dell'ancoraggio è stata disabilitata.

## <a name="remarks"></a>Commenti

L'evidenziazione dell'ancoraggio in una barra degli strumenti significa che l'ultimo elemento evidenziato rimarrà evidenziato fino a quando non viene evidenziato un altro elemento. Ciò si verifica anche se il cursore lascia il controllo barra degli strumenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





