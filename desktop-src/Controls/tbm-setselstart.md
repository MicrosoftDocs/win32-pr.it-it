---
title: Messaggio TBM_SETSELSTART (COMmctrl. h)
description: Imposta la posizione logica iniziale dell'intervallo di selezione corrente in un TrackBar. Questo messaggio viene ignorato se il TrackBar non ha lo \_ stile ENABLESELRANGE di TBS.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- Controlli di Windows Message TBM_SETSELSTART
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047843"
---
# <a name="tbm_setselstart-message"></a>\_Messaggio SETSELSTART TBM

Imposta la posizione logica iniziale dell'intervallo di selezione corrente in un TrackBar. Questo messaggio viene ignorato se il TrackBar non ha lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ridisegni flag. Se questo parametro è **true**, il messaggio riestrae il TrackBar dopo l'impostazione dell'intervallo di selezione. Se questo parametro è **false**, il messaggio imposta l'intervallo di selezione senza ricreare il TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posizione iniziale dell'intervallo di selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

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

[**TBM \_ GETselend**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**\_SEselend TBM**](tbm-setselend.md)
</dt> </dl>

 

 





