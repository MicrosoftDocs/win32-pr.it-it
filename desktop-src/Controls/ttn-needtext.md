---
title: TTN_NEEDTEXT di notifica (Commctrl.h)
description: Inviato da un controllo descrizione comando per recuperare le informazioni necessarie per visualizzare una finestra della descrizione comando. Questo codice di notifica è identico a TTN \_ GETDISPINFO. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dae1ac1eb721d918acf38745f19c7e6dee4a6a296c7fa8003f516717ece6cf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967801"
---
# <a name="ttn_needtext-notification-code"></a>Codice di notifica \_ TTN NEEDTEXT

Inviato da un controllo descrizione comando per recuperare le informazioni necessarie per visualizzare una finestra della descrizione comando. Questo codice di notifica è identico a [TTN \_ GETDISPINFO](ttn-getdispinfo.md). Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_NEEDTEXT

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

Compilare i membri appropriati della struttura per restituire le informazioni richieste al controllo descrizione comando. Se il gestore di messaggi imposta il membro **uFlags** della struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) su TTF DI SETITEM, il controllo descrizione comando archivia le informazioni e non le \_ \_ richiederà di nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTN \_ NEEDTEXTW** (Unicode) e **TTN \_ NEEDTEXTA** (ANSI)<br/>                 |



 

 





