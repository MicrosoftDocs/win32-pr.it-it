---
title: Codice di notifica RBN_GETOBJECT (COMmctrl. h)
description: Inviato da un controllo Rebar creato con lo \_ stile REGISTERDROP di RBS quando un oggetto viene trascinato su una banda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- Controlli di Windows per il codice di notifica RBN_GETOBJECT
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
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120502"
---
# <a name="rbn_getobject-notification-code"></a>RBN \_ codice di notifica GETobject

Inviato da un controllo Rebar creato con lo [**stile \_ REGISTERDROP di RBS**](rebar-control-styles.md) quando un oggetto viene trascinato su una banda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) contenente informazioni sulla banda su cui viene trascinato l'oggetto e riceve anche i dati forniti dall'applicazione ricevente in risposta a questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo codice di notifica deve essere zero.

## <a name="remarks"></a>Commenti

Per ricevere il \_ codice di notifica GetObject RBN, inizializzare OLE con una chiamata a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

