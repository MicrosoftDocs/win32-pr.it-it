---
title: SB_SETBKCOLOR messaggio (Commctrl.h)
description: Imposta il colore di sfondo in una barra di stato.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97893d49d475789b07c28e17e88097aa4df4336154d6b4e0f9c4fa081e52635
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637081"
---
# <a name="sb_setbkcolor-message"></a>Messaggio SB \_ SETBKCOLOR

Imposta il colore di sfondo in una barra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valore COLORREF**](/windows/desktop/gdi/colorref) che specifica il nuovo colore di sfondo. Specificare il valore CLR \_ DEFAULT per fare in modo che la barra di stato usi il colore di sfondo predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore di sfondo precedente o CLR \_ DEFAULT se il colore di sfondo è il colore predefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

