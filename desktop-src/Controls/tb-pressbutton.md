---
title: TB_PRESSBUTTON messaggio (Commctrl.h)
description: Preme o rilascia il pulsante specificato in una barra degli strumenti.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- TB_PRESSBUTTON dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c72bd3e58b06510463fcfb872060d7fcbb529ce3e5a96376ae8cb25e142d9e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168011"
---
# <a name="tb_pressbutton-message"></a>MESSAGGIO \_ PRESSBUTTON TB

Preme o rilascia il pulsante specificato in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di comando del pulsante da premere o rilasciare.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD è**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **valore BOOL** che indica se premere o rilasciare il pulsante specificato. Se **TRUE,** il pulsante viene premuto. Se **FALSE,** il pulsante viene rilasciato.

La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

