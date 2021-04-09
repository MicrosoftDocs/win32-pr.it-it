---
title: Messaggio IPM_SETRANGE (COMmctrl. h)
description: Imposta l'intervallo valido per il campo specificato nel controllo degli indirizzi IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- Controlli di Windows Message IPM_SETRANGE
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048612"
---
# <a name="ipm_setrange-message"></a>\_Messaggio SEtrange IPM

Imposta l'intervallo valido per il campo specificato nel controllo degli indirizzi IP.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice di campo in base zero a cui verrà applicato l'intervallo.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore di **parola** che contiene il limite inferiore dell'intervallo nel byte di ordine inferiore e il limite superiore nel byte di ordine superiore. Entrambi questi valori sono inclusivi. La macro [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) può essere usata anche per creare l'intervallo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Se l'utente immette un valore nel campo esterno a questo intervallo, il controllo invierà la notifica [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) con il valore immesso. Se il valore non è ancora compreso nell'intervallo dopo l'invio della notifica, il controllo tenterà di modificare il valore immesso nel limite di intervallo più vicino.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





