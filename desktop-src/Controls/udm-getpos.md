---
title: Messaggio UDM_GETPOS (COMmctrl. h)
description: Recupera la posizione corrente di un controllo di scorrimento con precisione a 16 bit.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- Controlli di Windows Message UDM_GETPOS
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301174"
---
# <a name="udm_getpos-message"></a>\_Messaggio UDM GETPOS

Recupera la posizione corrente di un controllo di scorrimento con precisione a 16 bit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è impostato su zero e [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è impostato sulla posizione corrente del controllo. Se si verifica un errore, **HIWORD** viene impostato su un valore diverso da zero.

## <a name="remarks"></a>Commenti

Durante l'elaborazione di questo messaggio, il controllo di scorrimento aggiorna la posizione corrente in base alla didascalia della finestra di Buddy. Il controllo di scorrimento restituisce un errore se non è presente alcuna finestra di Buddy o se la didascalia specifica un valore non valido o non compreso nell'intervallo. Inoltre, un flag di errore viene impostato nel HIWORD della restituzione se il controllo viene creato senza lo [**stile \_ SETBUDDYINT di UDS**](up-down-control-styles.md) , anche se restituisce un valore di posizione valido nel LOWORD della restituzione.

Se sono stati abilitati i valori a 32 bit per un controllo di scorrimento con [**UDM \_ SETRANGE32**](udm-setrange32.md), questo messaggio restituisce solo i 16 bit inferiori della posizione. Per recuperare la posizione completa a 32 bit, usare [**UDM \_ GETPOS32**](udm-getpos32.md).

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

[**\_GETRANGE32 UDM**](udm-getrange32.md)
</dt> <dt>

[**\_SETPOS UDM**](udm-setpos.md)
</dt> <dt>

[**\_SETRANGE32 UDM**](udm-setrange32.md)
</dt> </dl>

 

