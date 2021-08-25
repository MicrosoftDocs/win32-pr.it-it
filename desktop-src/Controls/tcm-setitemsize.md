---
title: TCM_SETITEMSIZE messaggio (Commctrl.h)
description: Imposta la larghezza e l'altezza delle schede in un controllo struttura a schede a larghezza fissa o disegnato dal proprietario. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TabCtrl SetItemSize.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8845aa54cd3cca413f31ee01f4a9583e24dc875a876d1aff691f574214f6f793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876231"
---
# <a name="tcm_setitemsize-message"></a>Messaggio SETITEMSIZE di TCM \_

Imposta la larghezza e l'altezza delle schede in un controllo struttura a schede a larghezza fissa o disegnato dal proprietario. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TabCtrl SetItemSize.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**è**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **valore INT** che specifica la nuova larghezza, in pixel. HIWORD [**è**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) un **valore INT** che specifica la nuova altezza, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza e l'altezza vecchie. La larghezza è nella [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valore restituito e l'altezza è in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="remarks"></a>Commenti

Se la larghezza è impostata su un valore minore della larghezza dell'immagine impostata da [**ImageList \_ Create,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)la larghezza della scheda viene impostata sul valore più basso maggiore della larghezza dell'immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

