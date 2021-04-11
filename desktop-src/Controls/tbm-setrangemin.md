---
title: Messaggio TBM_SETRANGEMIN (COMmctrl. h)
description: Imposta la posizione logica minima per il dispositivo di scorrimento in un TrackBar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- Controlli di Windows Message TBM_SETRANGEMIN
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
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963753"
---
# <a name="tbm_setrangemin-message"></a>\_Messaggio SETRANGEMIN TBM

Imposta la posizione logica minima per il dispositivo di scorrimento in un TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ridisegni flag. Se questo parametro è **true**, il messaggio riestrae il TrackBar dopo l'impostazione dell'intervallo. Se questo parametro è **false**, il messaggio imposta l'intervallo senza ricreare il TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posizione minima del dispositivo di scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se la posizione corrente del dispositivo di scorrimento è inferiore al nuovo valore minimo, il messaggio **TBM \_ SETRANGEMIN** imposta la posizione del dispositivo di scorrimento sul nuovo valore minimo.

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





