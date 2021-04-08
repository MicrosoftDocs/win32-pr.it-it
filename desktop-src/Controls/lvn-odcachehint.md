---
title: Codice di notifica LVN_ODCACHEHINT (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco virtuale quando il contenuto dell'area di visualizzazione è stato modificato.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- Controlli di Windows per il codice di notifica LVN_ODCACHEHINT
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
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965010"
---
# <a name="lvn_odcachehint-notification-code"></a>\_Codice di notifica ODCACHEHINT di LVN

Inviato da un controllo di visualizzazione elenco virtuale quando il contenuto dell'area di visualizzazione è stato modificato. Ad esempio, un controllo di visualizzazione elenco Invia questo codice di notifica quando l'utente scorre la visualizzazione del controllo. Il \_ codice di notifica ODCACHEHINT di LVN viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) contenente informazioni sull'intervallo di elementi da memorizzare nella cache.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che riceve il codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo messaggio consente all'applicazione di aggiornare le informazioni sull'elemento contenute nella cache in modo che sia prontamente disponibile quando viene inviato un codice di notifica [ \_ GETDISPINFO LVN](lvn-getdispinfo.md) .

Si noti che questo codice di notifica non è sempre una rappresentazione esatta degli elementi che verranno richiesti da [LVN \_ GETDISPINFO](lvn-getdispinfo.md). Se pertanto l'elemento richiesto non viene memorizzato nella cache durante la gestione \_ di LVN GETDISPINFO, l'applicazione deve essere preparata a fornire le informazioni richieste da un'origine esterna alla cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





