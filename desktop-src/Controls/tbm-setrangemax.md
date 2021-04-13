---
title: Messaggio TBM_SETRANGEMAX (COMmctrl. h)
description: Imposta la posizione logica massima per il dispositivo di scorrimento in un TrackBar.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- Controlli di Windows Message TBM_SETRANGEMAX
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475136"
---
# <a name="tbm_setrangemax-message"></a>\_Messaggio SETRANGEMAX TBM

Imposta la posizione logica massima per il dispositivo di scorrimento in un TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ridisegni flag. Se questo parametro è **true**, il TrackBar viene ridisegnato dopo l'impostazione dell'intervallo. Se questo parametro è **false**, il messaggio imposta l'intervallo senza ricreare il TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posizione massima del dispositivo di scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se la posizione corrente del dispositivo di scorrimento è maggiore del nuovo valore massimo, il messaggio **TBM \_ SETRANGEMAX** imposta la posizione del dispositivo di scorrimento sul nuovo valore massimo.

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

[**\_SEtrange TBM**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

 





