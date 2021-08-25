---
title: RB_INSERTBAND messaggio (Commctrl.h)
description: Inserisce una nuova banda in un controllo Rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- RB_INSERTBAND dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e21020302e4dcbfeb75f4a57d37be4b5c5703668231e8ec8e9dd9bd9577cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770161"
---
# <a name="rb_insertband-message"></a>Messaggio \_ INSERTBAND RB

Inserisce una nuova banda in un controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della posizione in cui verrà inserita la banda. Se si imposta questo parametro su -1, il controllo aggiungerà la nuova banda nell'ultima posizione.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) che definisce la banda da inserire. È necessario impostare il **membro cbSize** di questa struttura su **sizeof**(REBARBANDINFO) prima di inviare questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **RB \_ INSERTBANDW** (Unicode) e **RB \_ INSERTBANDA** (ANSI)<br/>               |



 

 





