---
title: TVM_SETLINECOLOR messaggio (Commctrl.h)
description: Il messaggio TVM \_ SETLINECOLOR imposta il colore della linea corrente.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR di Windows messaggi
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af66e7a711611ff5e59ec0d68b58a24fb39399245437b0e5d81840c1c38b2d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669521"
---
# <a name="tvm_setlinecolor-message"></a>Messaggio \_ TVM SETLINECOLOR

Il **messaggio TVM \_ SETLINECOLOR** imposta il colore della linea corrente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Colore nuova linea. Usare il valore \_ CLR DEFAULT per ripristinare i colori predefiniti del sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore della linea precedente.

## <a name="remarks"></a>Commenti

Questo messaggio modifica solo i colori delle linee. Per modificare i colori di '+' e '-' all'interno dei pulsanti, usare il messaggio [**\_ TVM SETTEXTCOLOR.**](tvm-settextcolor.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 





