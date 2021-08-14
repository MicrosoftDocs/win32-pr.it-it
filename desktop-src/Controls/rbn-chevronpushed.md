---
title: RBN_CHEVRONPUSHED di notifica (Commctrl.h)
description: Inviato da un controllo Rebar quando viene premuto un elemento chevron. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f5f8d52558251524e9d978c52ae703565a9641febdd53190925cfb8b127160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985321"
---
# <a name="rbn_chevronpushed-notification-code"></a>Codice di \_ notifica RBN CHEVRONPUSHED

Inviato da un controllo Rebar quando viene premuto un elemento chevron. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore alla struttura [**NMREBARCHEVRON della**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

Quando un'applicazione riceve questo codice di notifica, è responsabile della visualizzazione di un menu popup con voci per ogni strumento nascosto. Usare il **membro rc** della struttura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) per trovare la posizione corretta per il menu di scelta rapida.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





