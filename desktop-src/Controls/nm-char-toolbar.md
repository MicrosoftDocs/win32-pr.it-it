---
title: Codice di notifica NM_CHAR (barra degli strumenti) (COMmctrl. h)
description: Inviato da una barra degli strumenti quando riceve un \_ messaggio WM Char. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- Codice di notifica di NM_CHAR (barra degli strumenti) controlli Windows
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874697"
---
# <a name="nm_char-toolbar-notification-code"></a>Codice di notifica di NM \_ char (barra degli strumenti)

Inviato da una barra degli strumenti quando riceve un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) contenente informazioni aggiuntive sul carattere che ha causato il codice di notifica. Il membro **dwItemPrev** della struttura contiene l'identificatore di comando dell'elemento attualmente attivo o-1 se nessun elemento è attualmente attivo. Il membro **dwItemNext** di questa struttura contiene l'identificatore di comando dell'elemento che diventerà attivo o-1 se la chiave non corrisponde al tasto di scelta rapida di un elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per indicare che la barra degli strumenti non deve elaborare il carattere e **false** per fare in modo che la barra degli strumenti elabori il carattere.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

