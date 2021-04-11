---
title: Codice di notifica RBN_HEIGHTCHANGE (COMmctrl. h)
description: Inviato da un controllo Rebar quando l'altezza è cambiata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- Controlli di Windows per il codice di notifica RBN_HEIGHTCHANGE
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964158"
---
# <a name="rbn_heightchange-notification-code"></a>\_Codice di notifica HEIGHTCHANGE di RBN

Inviato da un controllo Rebar quando l'altezza è cambiata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

I controlli Rebar che usano lo stile [**CCS \_ Vert**](common-control-styles.md) inviano questo codice di notifica quando cambiano la larghezza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





