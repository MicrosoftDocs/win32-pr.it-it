---
title: TBM_SETTICFREQ messaggio (Commctrl.h)
description: Imposta la frequenza di intervallo per i segni di graduazione in un trackbar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ dei messaggi Windows
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
ms.openlocfilehash: c7c1b3e029abc8027d8708da31698f44db85ec78e427ba9461f0a71a740fb05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078015"
---
# <a name="tbm_setticfreq-message"></a>TBM \_ SETTICFREQ message

Imposta la frequenza di intervallo per i segni di graduazione in un trackbar. Ad esempio, se la frequenza è impostata su due, viene visualizzato un segno di graduazione per ogni altro incremento nell'intervallo del trackbar. L'impostazione predefinita per la frequenza è una; ciò significa che ogni incremento nell'intervallo è associato a un segno di graduazione.

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

Per usare questo messaggio, il trackbar deve avere lo stile [**TBS \_ AUTOTICKS.**](trackbar-control-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





