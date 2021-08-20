---
title: LVN_ODCACHEHINT di notifica (Commctrl.h)
description: Inviato da un controllo visualizzazione elenco virtuale quando il contenuto della relativa area di visualizzazione viene modificato.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3693291eeaef0879bdf861f392b89a1d0f2d5ec52f8a9c0d092b5495eb4565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170178"
---
# <a name="lvn_odcachehint-notification-code"></a>Codice di notifica \_ LVN ODCACHEHINT

Inviato da un controllo visualizzazione elenco virtuale quando il contenuto della relativa area di visualizzazione viene modificato. Ad esempio, un controllo visualizzazione elenco invia questo codice di notifica quando l'utente scorre la visualizzazione del controllo. Il codice di notifica \_ LVN ODCACHEHINT viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) contenente informazioni sull'intervallo di elementi da memorizzare nella cache.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che riceve questo codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo messaggio consente all'applicazione di aggiornare le informazioni sull'elemento contenute nella cache in modo che siano immediatamente disponibili quando viene inviato un codice di notifica [ \_ LVN GETDISPINFO.](lvn-getdispinfo.md)

Si noti che questo codice di notifica non è sempre una rappresentazione esatta degli elementi che verranno richiesti da [LVN \_ GETDISPINFO](lvn-getdispinfo.md). Pertanto, se l'elemento richiesto non viene memorizzato nella cache durante la gestione dell'LVN GETDISPINFO, l'applicazione deve essere preparata a fornire le informazioni richieste da un'origine esterna \_ alla cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





