---
title: TB_SETSTATE messaggio (Commctrl.h)
description: Imposta lo stato per il pulsante specificato in una barra degli strumenti.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- TB_SETSTATE controlli di Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa9ee112e4bbbe9c64ceab6205d67ecd6ae9653df97be55991be38eb5d181d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167471"
---
# <a name="tb_setstate-message"></a>TB \_ SETSTATE message

Imposta lo stato per il pulsante specificato in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del comando del pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>

LoWORD [**è una combinazione**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) di valori elencati in Toolbar [Button States](toolbar-button-states.md). HiWORD [**deve**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

