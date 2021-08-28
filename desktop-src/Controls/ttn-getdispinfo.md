---
title: TTN_GETDISPINFO codice di notifica (Commctrl.h)
description: Inviato da un controllo descrizione comando per recuperare le informazioni necessarie per visualizzare una finestra della descrizione comando. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- TTN_GETDISPINFO codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29df1da7643384233b25af6a6efd99930d5b49d0b47b5ffead335b2307bd3de3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967811"
---
# <a name="ttn_getdispinfo-notification-code"></a>Codice di notifica GETDISPINFO TTN \_

Inviato da un controllo descrizione comando per recuperare le informazioni necessarie per visualizzare una finestra della descrizione comando. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) che identifica lo strumento che richiede testo e riceve le informazioni richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene usato.

## <a name="remarks"></a>Commenti

Compilare i membri appropriati della struttura per restituire le informazioni richieste al controllo descrizione comando. Se il gestore di messaggi imposta il membro **uFlags** della struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) su TTF DI SETITEM, il controllo della descrizione comando archivia le informazioni e non le \_ \_ richiederà di nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTN \_ GETDISPINFOW** (Unicode) e **TTN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





