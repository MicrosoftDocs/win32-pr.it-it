---
title: Messaggio ACM_ISPLAYING (COMmctrl. h)
description: Verifica se è in esecuzione un Audio-Video clip con interfoliazione (AVI). È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro di animazione.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- Controlli di Windows Message ACM_ISPLAYING
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048073"
---
# <a name="acm_isplaying-message"></a>\_Messaggio di riproduzione ACM

Verifica se è in esecuzione un Audio-Video clip con interfoliazione (AVI). È possibile inviare questo messaggio in modo esplicito o utilizzare la macro di [**animazione \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





