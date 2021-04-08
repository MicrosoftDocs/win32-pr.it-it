---
title: Messaggio SBM_SETRANGEREDRAW (winuser. h)
description: Un'applicazione invia il \_ messaggio SETRANGEREDRAW SBM a un controllo barra di scorrimento per impostare i valori minimo e massimo della posizione e per ricreare il controllo.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- Controlli di Windows Message SBM_SETRANGEREDRAW
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047846"
---
# <a name="sbm_setrangeredraw-message"></a>\_Messaggio SETRANGEREDRAW SBM

Un'applicazione invia il **messaggio \_ SETRANGEREDRAW SBM** a un controllo barra di scorrimento per impostare i valori minimo e massimo della posizione e per ricreare il controllo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica la posizione di scorrimento minima.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica la posizione di scorrimento massima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**ComCtl32.dll versione 5,0**: se la posizione della casella di scorrimento è cambiata, il valore restituito è la posizione precedente della casella di scorrimento; in caso contrario, è zero.

**ComCtl32.dll versione 6,0**: la posizione corrente della casella di scorrimento, indipendentemente dal fatto che sia stata modificata.

## <a name="remarks"></a>Commenti

I valori di posizione minima e massima predefiniti sono pari a zero. La differenza tra i valori specificati dai parametri *wParam* e *lParam* non deve essere maggiore di MAXLONG.

Se i valori di posizione minima e massima sono uguali, il controllo barra di scorrimento è nascosto e, in effetti, disabilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETPOS SBM**](sbm-getpos.md)
</dt> <dt>

[**GetRange di SBM \_**](sbm-getrange.md)
</dt> <dt>

[**\_SETPOS SBM**](sbm-setpos.md)
</dt> <dt>

[**\_SEtrange SBM**](sbm-setrange.md)
</dt> </dl>

 

 





