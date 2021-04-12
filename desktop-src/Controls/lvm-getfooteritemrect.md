---
title: Messaggio LVM_GETFOOTERITEMRECT (COMmctrl. h)
description: Ottiene le coordinate di un piè di pagina per un elemento specificato in un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFooterItemRect di ListView.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- Controlli di Windows Message LVM_GETFOOTERITEMRECT
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225196"
---
# <a name="lvm_getfooteritemrect-message"></a>\_Messaggio GETFOOTERITEMRECT LVM

Ottiene le coordinate di un piè di pagina per un elemento specificato in un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFooterItemRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indice dell'elemento nel controllo visualizzazione elenco.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per ricevere le coordinate. L'applicazione chiamante è responsabile dell'allocazione di questa struttura. Le coordinate ricevute sono espresse come coordinate client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

