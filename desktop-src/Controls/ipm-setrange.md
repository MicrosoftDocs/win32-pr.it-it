---
title: IPM_SETRANGE messaggio (Commctrl.h)
description: Imposta l'intervallo valido per il campo specificato nel controllo indirizzo IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- IPM_SETRANGE di controllo Windows messaggio
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
ms.openlocfilehash: d599619fa9a065a27a9721b890f6d52c496bf646504009e1950b7ca1279f8a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434471"
---
# <a name="ipm_setrange-message"></a>Messaggio \_ IPM SETRANGE

Imposta l'intervallo valido per il campo specificato nel controllo indirizzo IP.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice di campo in base zero a cui verrà applicato l'intervallo.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore **WORD** che contiene il limite inferiore dell'intervallo nel byte meno significativo e il limite superiore nel byte di ordine superiore. Entrambi questi valori sono inclusivi. La macro [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) può essere usata anche per creare l'intervallo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Se l'utente immette un valore nel campo esterno a questo intervallo, il controllo invierà la notifica [ \_ FIELDCHANGED IPN](ipn-fieldchanged.md) con il valore immesso. Se il valore non è ancora compreso nell'intervallo dopo l'invio della notifica, il controllo tenterà di modificare il valore immesso al limite di intervallo più vicino.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





