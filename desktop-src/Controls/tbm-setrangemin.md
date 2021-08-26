---
title: TBM_SETRANGEMIN messaggio (Commctrl.h)
description: Imposta la posizione logica minima per il dispositivo di scorrimento in un trackbar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35cbb162b42636d886cb5e41eb9ba6de1a2101a8327ff8ddffbc71c57fa6735
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046071"
---
# <a name="tbm_setrangemin-message"></a>Messaggio \_ TBM SETRANGEMIN

Imposta la posizione logica minima per il dispositivo di scorrimento in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di ridisegno. Se questo parametro è **TRUE,** il messaggio ridisegna il trackbar dopo l'impostazione dell'intervallo. Se questo parametro è **FALSE,** il messaggio imposta l'intervallo ma non ridisegna il trackbar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posizione minima per il dispositivo di scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se la posizione corrente del dispositivo di scorrimento è minore del nuovo valore minimo, il messaggio **\_ TBM SETRANGEMIN** imposta la posizione del dispositivo di scorrimento sul nuovo valore minimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TBM \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





