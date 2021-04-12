---
title: Messaggio WM_DWMCOLORIZATIONCOLORCHANGED (winuser. h)
description: Informa tutte le finestre di primo livello che il colore di colorazione è stato modificato.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- Messaggio WM_DWMCOLORIZATIONCOLORCHANGED Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119946"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a>\_Messaggio DWMCOLORIZATIONCOLORCHANGED WM

Informa tutte le finestre di primo livello che il colore di colorazione è stato modificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il nuovo colore di colorazione. Il formato del colore è 0xAARRGGBB.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica se il nuovo colore viene mescolato con l'opacità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) viene usato per determinare il valore del colore corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

