---
title: Messaggio TBM_SETSELEND (COMmctrl. h)
description: Imposta la posizione logica finale dell'intervallo di selezione corrente in un TrackBar. Questo messaggio viene ignorato se il TrackBar non ha lo \_ stile ENABLESELRANGE di TBS.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- Controlli di Windows Message TBM_SETSELEND
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146446df4daf8e8ac7c0f3499149ba0f46940880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118967"
---
# <a name="tbm_setselend-message"></a>\_Messaggio SEselend TBM

Imposta la posizione logica finale dell'intervallo di selezione corrente in un TrackBar. Questo messaggio viene ignorato se il TrackBar non ha lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ridisegni flag. Se questo parametro è **true**, il messaggio riestrae il TrackBar dopo l'impostazione dell'intervallo di selezione. Se questo parametro è **false**, il messaggio imposta l'intervallo di selezione senza ricreare il TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Fine della posizione logica dell'intervallo di selezione.

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

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





