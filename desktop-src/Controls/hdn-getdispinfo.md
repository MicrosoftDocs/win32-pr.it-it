---
title: HDN_GETDISPINFO di notifica (Commctrl.h)
description: Inviato al proprietario di un controllo intestazione quando il controllo necessita di informazioni su un elemento di intestazione di callback. Questo codice di notifica viene inviato come messaggio WM \_ NOTIFY.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6e6cbc9559cda3312ecdca341aa7c7ad2b44dc5cc29e50690ddf10b2729a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435451"
---
# <a name="hdn_getdispinfo-notification-code"></a>Codice di notifica \_ GETDISPINFO HDN

Inviato al proprietario di un controllo intestazione quando il controllo necessita di informazioni su un elemento di intestazione di callback. Questo codice di notifica viene inviato come [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHDDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) Nell'input, i campi della struttura specificano le informazioni necessarie e l'elemento di interesse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un LRESULT.

## <a name="remarks"></a>Commenti

Compilare i membri appropriati della struttura per restituire le informazioni richieste al controllo intestazione. Se il gestore di messaggi imposta il membro **mask** della struttura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) su HDI DI SETITEM, il controllo intestazione archivia le informazioni e non \_ le \_ richiederà di nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ GETDISPINFOW** (Unicode) e **HDN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





