---
title: TVN_KEYDOWN di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che l'utente ha premuto un tasto e che il controllo visualizzazione albero ha lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dadd3386e83e541288249b83028119111a42855a111f7ecb398571a1d46ab356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002471"
---
# <a name="tvn_keydown-notification-code"></a>Codice di notifica \_ TVN KEYDOWN

Notifica alla finestra padre di un controllo visualizzazione albero che l'utente ha premuto un tasto e che il controllo visualizzazione albero ha lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTVKEYDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) Il **membro wVKey** specifica il codice della chiave virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il **membro wVKey** di *lParam* è un codice chiave carattere, il carattere verrà usato come parte di una ricerca incrementale. Restituisce un valore diverso da zero per escludere il carattere dalla ricerca incrementale oppure zero per includere il carattere nella ricerca. Per tutte le altre chiavi, il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





