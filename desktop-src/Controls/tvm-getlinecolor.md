---
title: Messaggio TVM_GETLINECOLOR (COMmctrl. h)
description: Il \_ messaggio GETLINECOLOR TVM ottiene il colore della riga corrente.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- Controlli di Windows Message TVM_GETLINECOLOR
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048513"
---
# <a name="tvm_getlinecolor-message"></a>\_Messaggio GETLINECOLOR TVM

Il **messaggio \_ GETLINECOLOR TVM** ottiene il colore della riga corrente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore della riga corrente oppure il \_ valore predefinito CLR se non ne è stato specificato alcuno.

## <a name="remarks"></a>Commenti

Questo messaggio recupera solo i colori linea. Per recuperare i colori di "+" e "-" all'interno dei pulsanti, usare il messaggio [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETLINECOLOR TVM**](tvm-setlinecolor.md)
</dt> </dl>

 

 





