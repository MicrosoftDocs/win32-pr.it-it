---
title: Messaggio TBM_SETRANGE (COMmctrl. h)
description: Imposta l'intervallo di posizioni logiche minime e massime per il dispositivo di scorrimento in un TrackBar.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- Controlli di Windows Message TBM_SETRANGE
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048115"
---
# <a name="tbm_setrange-message"></a>\_Messaggio SEtrange TBM

Imposta l'intervallo di posizioni logiche minime e massime per il dispositivo di scorrimento in un TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ridisegni flag. Se questo parametro è **true**, il TrackBar viene ridisegnato dopo l'impostazione dell'intervallo. Se questo parametro è **false**, il messaggio imposta l'intervallo senza ricreare il TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la posizione minima per il dispositivo di scorrimento e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione massima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se la posizione corrente del dispositivo di scorrimento non rientra nel nuovo intervallo, il messaggio di **\_ SetRange TBM** imposta la posizione del dispositivo di scorrimento sul nuovo valore massimo o minimo.

Poiché questo messaggio accetta valori Unsigned Integer a 2 16 bit, l'intervallo massimo che questo messaggio può specificare è compreso tra 0 e 65.535. Per specificare valori di intervallo maggiori, usare i messaggi [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md) e [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md) .

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

