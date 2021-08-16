---
title: CBEN_DRAGBEGIN di notifica (Commctrl.h)
description: Inviato quando l'utente inizia a trascinare l'immagine dell'elemento visualizzato nella parte di modifica del controllo . Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 626ad4d6abbcaaeb6f647aa94657ee1a681801a3ce13a9b5539216b1b67565a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414061"
---
# <a name="cben_dragbegin-notification-code"></a>Codice di \_ notifica CBEN DRAGBEGIN

Inviato quando l'utente inizia a trascinare l'immagine dell'elemento visualizzato nella parte di modifica del controllo . Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) che contiene informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Se l'applicazione ricevente implementa la funzionalità di trascinamento della selezione dal controllo , l'applicazione inizierà l'operazione di trascinamento della selezione in risposta a questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEN \_ DRAGBEGINW** (Unicode) e **CBEN \_ DRAGBEGINA** (ANSI)<br/>             |



 

 





