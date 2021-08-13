---
title: EM_SETEXTENDEDSTYLE messaggio (Commctrl.h)
description: Indica al controllo di modifica di impostare gli stili estesi. Inviare questo messaggio o usare la macro \_ Edit SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE del messaggio Windows controlli
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
ms.openlocfilehash: 710ad6535bd7891f322a4bf02a5fed0f766dd97c2569fa5ec9b961478bf6a457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673077"
---
# <a name="em_setextendedstyle-message"></a>Messaggio EM \_ SETEXTENDEDSTYLE

Indica al controllo di modifica di impostare gli stili estesi. Inviare questo messaggio o usare la macro [**\_ Edit SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Maschera usata per selezionare gli stili da impostare.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che indica lo stile esteso. Per altre informazioni sugli stili, vedere [Modifica degli stili estesi del controllo.](edit-control-window-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Gli stili estesi per un controllo di modifica non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la [**funzione SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10, versione 1809 solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2019 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

