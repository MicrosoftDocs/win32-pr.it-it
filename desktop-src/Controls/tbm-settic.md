---
title: Messaggio TBM_SETTIC (COMmctrl. h)
description: Imposta un segno di graduazione in un TrackBar nella posizione logica specificata.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- Controlli di Windows Message TBM_SETTIC
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119327"
---
# <a name="tbm_settic-message"></a>\_Messaggio SETTIC TBM

Imposta un segno di graduazione in un TrackBar nella posizione logica specificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Posizione del segno di graduazione. Questo parametro può essere uno qualsiasi dei valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il segno di graduazione è impostato o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Un TrackBar crea il proprio primo e l'ultimo segno di graduazione. Non utilizzare questo messaggio per impostare il primo e l'ultimo segno di graduazione.

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

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**\_Getter TBM**](tbm-gettic.md)
</dt> </dl>

 

 





