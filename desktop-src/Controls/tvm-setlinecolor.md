---
title: Messaggio TVM_SETLINECOLOR (COMmctrl. h)
description: Il \_ messaggio SETLINECOLOR TVM imposta il colore della riga corrente.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- Controlli di Windows Message TVM_SETLINECOLOR
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
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048475"
---
# <a name="tvm_setlinecolor-message"></a>\_Messaggio SETLINECOLOR TVM

Il **messaggio \_ SETLINECOLOR TVM** imposta il colore della riga corrente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuovo colore della linea. Usare il \_ valore CLR predefinito per ripristinare i colori predefiniti del sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore della riga precedente.

## <a name="remarks"></a>Commenti

Questo messaggio modifica solo i colori linea. Per modificare i colori di "+" e "-" all'interno dei pulsanti, usare il messaggio [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETLINECOLOR TVM**](tvm-getlinecolor.md)
</dt> </dl>

 

 





