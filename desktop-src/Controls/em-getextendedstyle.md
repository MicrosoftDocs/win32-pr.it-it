---
title: EM_GETEXTENDEDSTYLE messaggio (Commctrl.h)
description: Recupera lo stile esteso per un controllo di modifica. Inviare questo messaggio in modo esplicito o usando la \_ macro Edit GetExtendedStyle.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE del messaggio Windows controlli
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 77aa5827cc256c040d34ca24574dfa0b12816accaff9e5c0e92b4400195cae2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019669"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>EM_GETEXTENDEDSTYLE messaggio (Commctrl.h)

Recupera lo stile esteso per un controllo di visualizzazione albero. Inviare questo messaggio in modo esplicito o usando la macro [**\_ Edit GetExtendedStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore dello stile esteso. Per altre informazioni sugli stili, vedere [Modifica degli stili estesi del controllo.](edit-control-window-extended-styles.md)

## <a name="remarks"></a>Commenti

Gli stili estesi per un controllo di modifica non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la [**funzione SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10, versione 1809 solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2019 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

