---
title: TB_MARKBUTTON messaggio (Commctrl.h)
description: Imposta lo stato di evidenziazione di un determinato pulsante in un controllo barra degli strumenti.
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- TB_MARKBUTTON di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1af7ba20ed9ce3d1b289c0c28db8fc40c476dd99f4ffb1af1af28692c44cab1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168027"
---
# <a name="tb_markbutton-message"></a>Messaggio \_ MARKBUTTON TB

Imposta lo stato di evidenziazione di un determinato pulsante in un controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di comando per un pulsante della barra degli strumenti.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD è**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **valore BOOL** che indica il nuovo stato di evidenziazione. Se **TRUE,** il pulsante è evidenziato. Se **FALSE,** il pulsante viene impostato sullo stato predefinito.

La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

