---
title: LVM_GETEMPTYTEXT messaggio (Commctrl.h)
description: Ottiene il testo destinato alla visualizzazione quando il controllo visualizzazione elenco risulta vuoto. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetEmptyText.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dd1dc1df7b0a558adda37938849b5383bbfee304d807a22a329e4f7301889b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411470"
---
# <a name="lvm_getemptytext-message"></a>Messaggio LVM \_ GETEMPTYTEXT

Ottiene il testo destinato alla visualizzazione quando il controllo visualizzazione elenco risulta vuoto. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetEmptyText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Dimensione del buffer a cui punta *lParam,* inclusa la **terminazione NULL.**

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntatore a un buffer Unicode con terminazione Null di dimensioni specificate da *wParam* per ricevere il testo. Il chiamante è responsabile dell'allocazione del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





