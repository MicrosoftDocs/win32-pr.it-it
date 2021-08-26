---
title: RBN_GETOBJECT codice di notifica (Commctrl.h)
description: Inviato da un controllo rebar creato con lo stile RBS REGISTERDROP quando un oggetto viene trascinato \_ su una banda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9709313a16d068e44b847f5e0862adf1e133b9f0ea92136a12e9aae24ffb14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985041"
---
# <a name="rbn_getobject-notification-code"></a>Codice di \_ notifica RBN GETOBJECT

Inviato da un controllo rebar creato con [**lo stile \_ RBS REGISTERDROP**](rebar-control-styles.md) quando un oggetto viene trascinato su una banda nel controllo. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) che contiene informazioni sulla banda su cui è trascinato l'oggetto e riceve anche i dati forniti dall'applicazione ricevente in risposta a questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo codice di notifica deve essere zero.

## <a name="remarks"></a>Commenti

Per ricevere il codice di notifica RBN \_ GETOBJECT, inizializzare OLE con una chiamata a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

