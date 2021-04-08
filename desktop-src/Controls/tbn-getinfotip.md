---
title: Codice di notifica TBN_GETINFOTIP (COMmctrl. h)
description: Recupera le informazioni infotip per un elemento della barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- Controlli di Windows per il codice di notifica TBN_GETINFOTIP
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048109"
---
# <a name="tbn_getinfotip-notification-code"></a>\_Codice di notifica GETINFOTIP di TBN

Recupera le informazioni infotip per un elemento della barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) che contiene informazioni sull'elemento e riceve informazioni infotip.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dal controllo.

## <a name="remarks"></a>Commenti

Il supporto infotip sulla barra degli strumenti consente alla barra degli strumenti di visualizzare le descrizioni comandi per gli elementi con dimensioni pari a INFOTIPSIZE caratteri. Se il codice di notifica non viene elaborato, la barra degli strumenti utilizzerà il testo dell'elemento per infotip.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TBN \_ GETINFOTIPW** (Unicode) e **TBN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





