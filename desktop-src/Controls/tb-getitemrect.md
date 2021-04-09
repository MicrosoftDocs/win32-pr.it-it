---
title: Messaggio TB_GETITEMRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione di un pulsante in una barra degli strumenti.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- Controlli di Windows Message TB_GETITEMRECT
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874218"
---
# <a name="tb_getitemrect-message"></a>TB \_ GETITEMRECT messaggio

Recupera il rettangolo di delimitazione di un pulsante in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero del pulsante per il quale recuperare le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve le coordinate client del rettangolo di delimitazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio non recupera il rettangolo di delimitazione per i pulsanti il cui stato è impostato sul valore [**\_ nascosto TBSTATE**](toolbar-button-states.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

