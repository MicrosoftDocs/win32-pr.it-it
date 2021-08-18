---
title: SB_SETMINHEIGHT messaggio (Commctrl.h)
description: Imposta l'altezza minima dell'area di disegno di una finestra di stato.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT dei messaggi Windows controlli
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
ms.openlocfilehash: 1b644067e48312b265d132f7d06d53343c4612b879c3a09b638ebd0a98a7c88a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293731"
---
# <a name="sb_setminheight-message"></a>Messaggio SB \_ SETMINHEIGHT

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

L'altezza minima è la somma di *wParam* e il doppio della larghezza, in pixel, del bordo verticale della finestra di stato. Un'applicazione deve inviare [**il messaggio WM \_ SIZE**](/windows/desktop/winmsg/wm-size) alla finestra di stato per ridisegnare la finestra. I *parametri wParam* *e lParam* del **messaggio WM \_ SIZE** devono essere impostati su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

