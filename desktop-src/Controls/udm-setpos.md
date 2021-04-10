---
title: Messaggio UDM_SETPOS (COMmctrl. h)
description: Imposta la posizione corrente per un controllo di scorrimento con precisione a 16 bit.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- Controlli di Windows Message UDM_SETPOS
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120491"
---
# <a name="udm_setpos-message"></a>\_Messaggio UDM SETPOS

Imposta la posizione corrente per un controllo di scorrimento con precisione a 16 bit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuova posizione per il controllo di scorrimento. Se il parametro non è compreso nell'intervallo specificato del controllo, *lParam* verrà impostato sul valore valido più vicino.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la posizione precedente.

## <a name="remarks"></a>Commenti

Questo messaggio supporta solo posizioni a 16 bit. Se sono stati abilitati i valori a 32 bit per un controllo di scorrimento con [**UDM \_ SETRANGE32**](udm-setrange32.md), usare [**UDM \_ SETPOS32**](udm-setpos32.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**UDM \_ GETrange**](udm-getrange.md)
</dt> <dt>

[**\_GETPOS UDM**](udm-getpos.md)
</dt> </dl>

 

 





