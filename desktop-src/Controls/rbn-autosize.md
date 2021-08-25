---
title: RBN_AUTOSIZE codice di notifica (Commctrl.h)
description: Inviato da un controllo rebar creato con lo stile \_ RBS AUTOSIZE quando l'oggetto rebar viene ridimensionato automaticamente. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE codice di notifica Windows controlli
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
ms.openlocfilehash: 32c0ef601562c6887e05c78c06a66cf61e330843769eb3bb66105eb941e09339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985371"
---
# <a name="rbn_autosize-notification-code"></a>Codice di notifica RBN \_ AUTOSIZE

Inviato da un controllo rebar creato con lo [**stile \_ RBS AUTOSIZE**](rebar-control-styles.md) quando l'oggetto rebar viene ridimensionato automaticamente. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) che contiene informazioni sull'operazione di ridimensionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





