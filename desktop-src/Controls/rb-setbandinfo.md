---
title: RB_SETBANDINFO messaggio (Commctrl.h)
description: Imposta le caratteristiche di una banda esistente in un controllo rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee89d91bc65556179d14c7e86a69a9e6399223f38bb1bcc44f746d7cd8f8a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798471"
---
# <a name="rb_setbandinfo-message"></a>Messaggio RB \_ SETBANDINFO

Imposta le caratteristiche di una banda esistente in un controllo rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda per ricevere le nuove impostazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) che definisce la banda da modificare e le nuove impostazioni. Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** di questa struttura sulla struttura **sizeof**(REBARBANDINFO). Inoltre, è necessario impostare il membro **cch** della struttura **REBARBANDINFO** sulla dimensione del buffer **lpText** quando viene specificato RBBIM \_ TEXT.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **RB \_ SETBANDINFOW** (Unicode) e **RB \_ SETBANDINFOA** (ANSI)<br/>             |



 

 





