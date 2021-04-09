---
title: Codice di notifica CBEN_DRAGBEGIN (COMmctrl. h)
description: Inviato quando l'utente inizia a trascinare l'immagine dell'elemento visualizzato nella parte di modifica del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- Controlli di Windows per il codice di notifica CBEN_DRAGBEGIN
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
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121155"
---
# <a name="cben_dragbegin-notification-code"></a>\_Codice di notifica DRAGBEGIN di CBEN

Inviato quando l'utente inizia a trascinare l'immagine dell'elemento visualizzato nella parte di modifica del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) che contiene informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Se l'applicazione ricevente implementa la funzionalità di trascinamento della selezione dal controllo, l'applicazione inizierà l'operazione di trascinamento della selezione in risposta a questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEN \_ DRAGBEGINW** (Unicode) e **CBEN \_ DRAGBEGINA** (ANSI)<br/>             |



 

 





