---
title: Messaggio SB_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo di una barra di stato.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- Controlli di Windows Message SB_SETBKCOLOR
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400827"
---
# <a name="sb_setbkcolor-message"></a>\_Messaggio SETBKCOLOR SB

Imposta il colore di sfondo di una barra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore [**COLORREF**](/windows/desktop/gdi/colorref) che specifica il nuovo colore di sfondo. Specificare il \_ valore predefinito CLR per fare in modo che la barra di stato usi il colore di sfondo predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore di sfondo precedente oppure il \_ valore predefinito CLR se il colore di sfondo è il colore predefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

