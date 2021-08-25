---
title: TBM_GETRANGEMAX messaggio (Commctrl.h)
description: Recupera la posizione massima per il dispositivo di scorrimento in un trackbar.
ms.assetid: c0ae5f96-f4ce-46cd-84d0-9e7c473441a0
keywords:
- TBM_GETRANGEMAX controlli di Windows messaggio
topic_type:
- apiref
api_name:
- TBM_GETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14e5988802135816076bea8549df125c46708a83d3d949bbe0f90659ea2468f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046491"
---
# <a name="tbm_getrangemax-message"></a>Messaggio \_ TBM GETRANGEMAX

Recupera la posizione massima per il dispositivo di scorrimento in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit che specifica la posizione massima nell'intervallo tra le posizioni del dispositivo di scorrimento minimo e massimo del trackbar.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)
</dt> <dt>

[**TBM \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





