---
title: BCN_HOTITEMCHANGE di notifica (Commctrl.h)
description: Notifica al proprietario del controllo pulsante che il mouse sta per entrare o uscire dall'area client del controllo pulsante. Il controllo pulsante invia questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6966978dc1d1eee1d84a9e5caa51116ccb96e098d2c196ea143051663abbf4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921371"
---
# <a name="bcn_hotitemchange-notification-code"></a>Codice di notifica \_ BCN HOTITEMCHANGE

Notifica al proprietario del controllo pulsante che il mouse sta per entrare o uscire dall'area client del controllo pulsante. Il controllo pulsante invia questo codice di notifica sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMBCHOTITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo codice di notifica, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





