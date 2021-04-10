---
title: Messaggio SB_SETMINHEIGHT (COMmctrl. h)
description: Imposta l'altezza minima dell'area di disegno di una finestra di stato.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- Controlli di Windows Message SB_SETMINHEIGHT
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964637"
---
# <a name="sb_setminheight-message"></a>\_Messaggio SETMINHEIGHT SB

Imposta l'altezza minima dell'area di disegno di una finestra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Altezza minima, in pixel, della finestra.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'altezza minima è la somma di *wParam* e il doppio della larghezza, in pixel, del bordo verticale della finestra di stato. Per ricreare la finestra, un'applicazione deve inviare il messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) alla finestra di stato. I parametri *wParam* e *lParam* del messaggio **\_ dimensioni WM** devono essere impostati su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

