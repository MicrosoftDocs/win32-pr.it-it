---
title: Messaggio TBM_CLEARSEL (COMmctrl. h)
description: Cancella l'intervallo di selezione corrente in un TrackBar.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- Controlli di Windows Message TBM_CLEARSEL
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874666"
---
# <a name="tbm_clearsel-message"></a>\_Messaggio CLEARSEL TBM

Cancella l'intervallo di selezione corrente in un TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ridisegni flag. Se questo parametro è **true**, il TrackBar viene ridisegnato dopo la cancellazione della selezione.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un TrackBar può avere un intervallo di selezione solo se è stato specificato lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) quando è stato creato.

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

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**\_SEselend TBM**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





