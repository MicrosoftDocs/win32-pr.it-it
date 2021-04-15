---
title: Messaggio UDM_GETACCEL (COMmctrl. h)
description: Recupera le informazioni di accelerazione per un controllo di scorrimento.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- Controlli di Windows Message UDM_GETACCEL
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475736"
---
# <a name="udm_getaccel-message"></a>\_Messaggio UDM GETACCEL

Recupera le informazioni di accelerazione per un controllo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi nella matrice specificata da *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di strutture [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) che ricevono informazioni di accelerazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di acceleratori attualmente impostati per il controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETACCEL UDM**](udm-setaccel.md)
</dt> </dl>

 

 





