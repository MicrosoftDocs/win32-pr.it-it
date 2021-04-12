---
title: Messaggio LVM_GETEMPTYTEXT (COMmctrl. h)
description: Ottiene il testo destinato a essere visualizzato quando il controllo elenco-visualizzazione appare vuoto. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetEmptyText di ListView.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- Controlli di Windows Message LVM_GETEMPTYTEXT
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
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475167"
---
# <a name="lvm_getemptytext-message"></a>\_Messaggio GETEMPTYTEXT LVM

Ottiene il testo destinato a essere visualizzato quando il controllo elenco-visualizzazione appare vuoto. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetEmptyText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Dimensioni del buffer a cui punta *lParam*, inclusa la terminazione **null**.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a un buffer Unicode con terminazione null di dimensioni specificate da *wParam* per ricevere il testo. Il chiamante è responsabile dell'allocazione del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





