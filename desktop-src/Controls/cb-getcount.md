---
title: Messaggio CB_GETCOUNT (winuser. h)
description: Ottiene il numero di elementi nella casella di riepilogo di una casella combinata.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- Controlli di Windows Message CB_GETCOUNT
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744018"
---
# <a name="cb_getcount-message"></a>\_Messaggio GETCOUNT CB

Ottiene il numero di elementi nella casella di riepilogo di una casella combinata.

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

Il valore restituito è il numero di elementi nella casella di riepilogo. Se si verifica un errore, è CB \_ Err.

## <a name="remarks"></a>Commenti

L'indice è in base zero, quindi il conteggio restituito è maggiore di uno rispetto al valore di indice dell'ultimo elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

 





