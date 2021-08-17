---
title: RB_GETBANDINFO messaggio (Commctrl.h)
description: Recupera informazioni su una banda specificata in un controllo Rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b0ae509699c23ad24b9b97451178f4711ab52176a9c15aeef757bab85c861c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409442"
---
# <a name="rb_getbandinfo-message"></a>Messaggio RB \_ GETBANDINFO

Recupera informazioni su una banda specificata in un controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda per la quale verranno recuperate le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) che riceverà le informazioni sulla banda richieste. Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** di questa struttura sulla dimensione della struttura **REBARBANDINFO** e impostare il membro **fMask** sugli elementi da recuperare. Inoltre, è necessario impostare il membro **cch** della struttura **REBARBANDINFO** sulla dimensione del buffer **lpText** quando viene specificato RBBIM \_ TEXT.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **RB \_ GETBANDINFOW** (Unicode) e **RB \_ GETBANDINFOA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 





