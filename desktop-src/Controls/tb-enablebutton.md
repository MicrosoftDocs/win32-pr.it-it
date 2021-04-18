---
title: Messaggio TB_ENABLEBUTTON (COMmctrl. h)
description: Abilita o Disabilita il pulsante specificato in una barra degli strumenti.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- Controlli di Windows Message TB_ENABLEBUTTON
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302784"
---
# <a name="tb_enablebutton-message"></a>TB \_ ENABLEBUTTON messaggio

Abilita o Disabilita il pulsante specificato in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di comando del pulsante da abilitare o disabilitare.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **bool** che indica se abilitare o disabilitare il pulsante specificato. Se **true**, il pulsante è abilitato. Se **false**, il pulsante è disabilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Quando un pulsante è stato abilitato, è possibile premerlo e selezionarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

