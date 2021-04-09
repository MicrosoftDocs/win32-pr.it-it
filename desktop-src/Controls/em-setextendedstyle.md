---
title: Messaggio EM_SETEXTENDEDSTYLE (COMmctrl. h)
description: Informa il controllo di modifica per impostare gli stili estesi. Inviare questo messaggio o usare la macro Edit \_ SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- Controlli di Windows Message EM_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121031"
---
# <a name="em_setextendedstyle-message"></a>\_Messaggio SETEXTENDEDSTYLE em

Informa il controllo di modifica per impostare gli stili estesi. Inviare questo messaggio o usare la macro [**Edit \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Maschera utilizzata per selezionare gli stili da impostare.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che indica lo stile esteso. Per altre informazioni sugli stili, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Gli stili estesi per un controllo di modifica non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1809 \[\]<br/>                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

