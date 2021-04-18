---
title: Codice di notifica RBN_AUTOSIZE (COMmctrl. h)
description: Inviato da un controllo Rebar creato con lo \_ stile AUTOSIZE di RBS quando il Rebar viene ridimensionato automaticamente. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- Controlli di Windows per il codice di notifica RBN_AUTOSIZE
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302641"
---
# <a name="rbn_autosize-notification-code"></a>\_Codice di notifica AUTOSIZE RBN

Inviato da un controllo Rebar creato con lo [**stile \_ AUTOSIZE di RBS**](rebar-control-styles.md) quando il Rebar viene ridimensionato automaticamente. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) che contiene informazioni sull'operazione di ridimensionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





