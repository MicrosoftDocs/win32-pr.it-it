---
title: Messaggio EM_GETEXTENDEDSTYLE (COMmctrl. h)
description: Recupera lo stile esteso per un controllo di modifica. Inviare questo messaggio in modo esplicito o usando la \_ macro Edit GetExtendedStyle.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Controlli di Windows Message EM_GETEXTENDEDSTYLE
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
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477921"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>Messaggio EM_GETEXTENDEDSTYLE (COMmctrl. h)

Recupera lo stile esteso per un controllo di visualizzazione albero. Inviare questo messaggio in modo esplicito o usando la macro [**Edit \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore dello stile esteso. Per altre informazioni sugli stili, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md).

## <a name="remarks"></a>Commenti

Gli stili estesi per un controllo di modifica non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1809 \[\]<br/>                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

