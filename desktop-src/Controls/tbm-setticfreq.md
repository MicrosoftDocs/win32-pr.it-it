---
title: Messaggio TBM_SETTICFREQ (COMmctrl. h)
description: Imposta la frequenza di intervallo per i segni di graduazione in un TrackBar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- Controlli di Windows Message TBM_SETTICFREQ
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048114"
---
# <a name="tbm_setticfreq-message"></a>\_Messaggio SETTICFREQ TBM

Imposta la frequenza di intervallo per i segni di graduazione in un TrackBar. Se, ad esempio, la frequenza è impostata su due, viene visualizzato un segno di graduazione per ogni altro incremento nell'intervallo del TrackBar. L'impostazione predefinita per la frequenza è uno; ovvero ogni incremento nell'intervallo è associato a un segno di graduazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Frequenza dei segni di graduazione.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Per usare questo messaggio, il TrackBar deve avere lo stile per i segni di [**\_ scandili TBS**](trackbar-control-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





