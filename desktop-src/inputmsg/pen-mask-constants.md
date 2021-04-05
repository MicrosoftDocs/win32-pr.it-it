---
title: Maschera di penna
description: Valori che possono essere visualizzati nel campo penMask della struttura POINTER_PEN_INFO.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bd181b5eafbe1cf6de56c95886deb04e5bd6d2b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120359"
---
# <a name="pen-mask"></a>Maschera di penna

Valori che possono essere visualizzati nel campo **penMask** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .

<dl> <dt>

<span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Valore predefinito. Nessuno dei campi facoltativi è valido.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



la **pressione** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) è valida.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



la **rotazione** della struttura del [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) è valida.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X** 
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



**tiltX** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) è valido.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



l' **inclinazione** della struttura del [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) è valida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





