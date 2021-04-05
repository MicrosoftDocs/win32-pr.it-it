---
title: Messaggio TB_SETPARENT (COMmctrl. h)
description: Imposta la finestra a cui il controllo Toolbar invia messaggi di notifica.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- Controlli di Windows Message TB_SETPARENT
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
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874422"
---
# <a name="tb_setparent-message"></a>TB \_ messaggio padre

Imposta la finestra a cui il controllo Toolbar invia messaggi di notifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra per la ricezione di messaggi di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per la finestra di notifica precedente oppure **null** se non è presente una finestra di notifica precedente.

## <a name="remarks"></a>Commenti

Il **messaggio \_ padre TB** non modifica la finestra padre specificata al momento della creazione del controllo. Chiamando la funzione [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) per un controllo Toolbar, viene restituita la finestra padre effettiva, non la finestra specificata in **TB \_ padre**. Per modificare la finestra padre del controllo, chiamare la funzione [**padre**](/windows/desktop/api/winuser/nf-winuser-setparent) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

