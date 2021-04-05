---
title: Messaggio HDM_GETITEMDROPDOWNRECT (COMmctrl. h)
description: Ottiene il rettangolo di delimitazione del pulsante di menu combinato per un elemento di intestazione con lo stile HDF \_ SPLITBUTTON. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetItemDropDownRect dell'intestazione.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- Controlli di Windows Message HDM_GETITEMDROPDOWNRECT
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048396"
---
# <a name="hdm_getitemdropdownrect-message"></a>\_Messaggio HDM GETITEMDROPDOWNRECT

Ottiene il rettangolo di delimitazione del pulsante di menu combinato per un elemento di intestazione con lo stile **HDF \_ SPLITBUTTON**. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetItemDropDownRect dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indice in base zero dell'elemento di controllo dell'intestazione per il quale recuperare il rettangolo di delimitazione.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**Rect**](/windows/win32/api/windef/ns-windef-rect) che riceve le informazioni sul rettangolo di delimitazione. Il mittente del messaggio è responsabile dell'allocazione della struttura. Le coordinate restituite nella struttura RECT sono espresse in relazione all'elemento padre del controllo Header.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

L'elemento dell'intestazione deve avere lo stile **HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sui controlli intestazione](header-controls.md)
</dt> </dl>

 

 





