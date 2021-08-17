---
title: WM_DWMCOLORIZATIONCOLORCHANGED messaggio (Winuser.h)
description: Informa tutte le finestre di primo livello che il colore di colorazione è stato modificato.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- WM_DWMCOLORIZATIONCOLORCHANGED messaggio Gestione finestre desktop
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
ms.openlocfilehash: 5bdbb854821f2a25565241700d28964b2d32319bccb8226c3d7d789c0e457fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094591"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a>Messaggio WM \_ DWMCOLORIZATIONCOLORCHANGED

Informa tutte le finestre di primo livello che il colore di colorazione è stato modificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il nuovo colore di colorazione. Il formato del colore è 0xAARRGGBB.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica se il nuovo colore viene misto con l'opacità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

[**DwmGetColorizationColor viene**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) usato per determinare il valore del colore corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



 

