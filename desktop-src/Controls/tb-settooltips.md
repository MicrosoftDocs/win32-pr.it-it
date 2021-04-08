---
title: Messaggio TB_SETTOOLTIPS (COMmctrl. h)
description: Associa un controllo ToolTip a una barra degli strumenti.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- Controlli di Windows Message TB_SETTOOLTIPS
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048118"
---
# <a name="tb_settooltips-message"></a>\_Messaggio di SEtooltips TB

Associa un controllo ToolTip a una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il controllo ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Tutti i pulsanti aggiunti a una barra degli strumenti prima di inviare il messaggio **TB \_ setooltips** non verranno registrati con il controllo ToolTip.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





