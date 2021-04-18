---
title: Messaggio TB_SETANCHORHIGHLIGHT (COMmctrl. h)
description: Imposta l'impostazione dell'evidenziazione di ancoraggio per una barra degli strumenti.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- Controlli di Windows Message TB_SETANCHORHIGHLIGHT
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
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300974"
---
# <a name="tb_setanchorhighlight-message"></a>TB \_ SETANCHORHIGHLIGHT messaggio

Imposta l'impostazione dell'evidenziazione di ancoraggio per una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **bool** che specifica se l'evidenziazione dell'ancoraggio è abilitata o disabilitata. Se questo valore è diverso da zero, verrà abilitata l'evidenziazione dell'ancoraggio. Se questo valore è zero, l'evidenziazione dell'ancoraggio verrà disabilitata.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'impostazione di evidenziazione dell'ancoraggio precedente. Se questo valore è diverso da zero, è stata abilitata l'evidenziazione di ancoraggio. Se questo valore è zero, l'evidenziazione dell'ancoraggio è stata disabilitata.

## <a name="remarks"></a>Commenti

L'evidenziazione dell'ancoraggio in una barra degli strumenti indica che l'ultimo elemento evidenziato rimarrà evidenziato finché non viene evidenziato un altro elemento. Ciò si verifica anche se il cursore esce dal controllo Toolbar.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





