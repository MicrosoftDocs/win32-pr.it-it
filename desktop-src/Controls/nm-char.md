---
title: Codice di notifica NM_CHAR (COMmctrl. h)
description: Il \_ codice di notifica del valore Nm viene inviato da un controllo quando viene elaborato un tasto carattere. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- Controlli di Windows per il codice di notifica NM_CHAR
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
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302793"
---
# <a name="nm_char-notification-code"></a>Codice di notifica di NM \_ Char

Il \_ codice di notifica del valore Nm viene inviato da un controllo quando viene elaborato un tasto carattere. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) contenente informazioni aggiuntive sul carattere che ha causato il codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dalla maggior parte dei controlli. Per ulteriori informazioni, vedere la documentazione per i singoli controlli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[NM \_ char (barra degli strumenti)](nm-char-toolbar.md)
</dt> </dl>

 

 





