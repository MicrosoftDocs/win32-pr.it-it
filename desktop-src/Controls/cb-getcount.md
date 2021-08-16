---
title: CB_GETCOUNT messaggio (Winuser.h)
description: Ottiene il numero di elementi nella casella di riepilogo di una casella combinata.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- CB_GETCOUNT dei messaggi Windows controlli
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
ms.openlocfilehash: 8215046ae9558fd03388b2b0637233c2f69832ea07a7f20fd24ddc0a5eb3c177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832279"
---
# <a name="cb_getcount-message"></a>Messaggio \_ GETCOUNT CB

Ottiene il numero di elementi nella casella di riepilogo di una casella combinata.

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

Il valore restituito è il numero di elementi nella casella di riepilogo. Se si verifica un errore, si tratta di CB \_ ERR.

## <a name="remarks"></a>Commenti

L'indice è in base zero, quindi il conteggio restituito è maggiore di uno rispetto al valore di indice dell'ultimo elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

 





