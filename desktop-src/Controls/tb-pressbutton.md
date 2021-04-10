---
title: Messaggio TB_PRESSBUTTON (COMmctrl. h)
description: Preme o rilascia il pulsante specificato in una barra degli strumenti.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- Controlli di Windows Message TB_PRESSBUTTON
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
ms.openlocfilehash: 5b0e86092951b242cee7388fc0d5d1bbdbca835e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120679"
---
# <a name="tb_pressbutton-message"></a>TB \_ PRESSBUTTON messaggio

Preme o rilascia il pulsante specificato in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di comando del pulsante da premere o rilasciare.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **bool** che indica se premere o rilasciare il pulsante specificato. Se **true**, viene premuto il pulsante. Se **false**, il pulsante viene rilasciato.

Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

