---
title: TB_SETPARENT messaggio (Commctrl.h)
description: Imposta la finestra a cui il controllo barra degli strumenti invia messaggi di notifica.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT di controllo Windows messaggi
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd97cdab230317feea65f2bffce74a7dec34ee336d69bb46ec4c6963ca9b3eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078145"
---
# <a name="tb_setparent-message"></a>TB \_ SETPARENT message

Imposta la finestra a cui il controllo barra degli strumenti invia messaggi di notifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle alla finestra per ricevere messaggi di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per la finestra di notifica precedente oppure **NULL** se non è presente alcuna finestra di notifica precedente.

## <a name="remarks"></a>Commenti

Il **messaggio \_ SETPARENT** tb non modifica la finestra padre specificata al momento della creazione del controllo. La chiamata [**alla funzione GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) per un controllo barra degli strumenti restituirà la finestra padre effettiva, non la finestra specificata in **\_ SETPARENT TB.** Per modificare la finestra padre del controllo, chiamare la [**funzione SetParent.**](/windows/desktop/api/winuser/nf-winuser-setparent)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

