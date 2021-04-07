---
title: Messaggio UDM_SETACCEL (COMmctrl. h)
description: Imposta l'accelerazione per un controllo di scorrimento.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- Controlli di Windows Message UDM_SETACCEL
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048761"
---
# <a name="udm_setaccel-message"></a>\_Messaggio UDM SETACCEL

Imposta l'accelerazione per un controllo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di strutture [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) specificate da *aAccels*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di strutture [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) che contengono informazioni sull'accelerazione. Gli elementi devono essere ordinati in ordine crescente in base al membro **nsec** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETACCEL UDM**](udm-getaccel.md)
</dt> </dl>

 

 





