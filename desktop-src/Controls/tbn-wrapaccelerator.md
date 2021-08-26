---
title: TBN_WRAPACCELERATOR di notifica (Commctrl.h)
description: Richiede l'indice del pulsante in una o più barre degli strumenti corrispondenti al carattere di scelta rapida specificato. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c5ec222f387108e2cb4d240e6dddf0fcb904d814097a96624a177425eb805ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105031"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>Codice di \_ notifica WRAPACCELERATOR TBN

Richiede l'indice del pulsante in una o più barre degli strumenti corrispondenti al carattere di scelta rapida specificato. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che contiene il carattere del tasto di scelta rapida e che riceve l'indice del pulsante corrispondente. L'indice è -1 se l'acceleratore non corrisponde a un comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TRUE** se viene restituito un indice; in caso **contrario, FALSE.**

## <a name="remarks"></a>Commenti

Le applicazioni con una o più barre degli strumenti possono ricevere questo codice di notifica.

La **struttura NMTBWRAPACCELERATOR** deve essere definita dall'applicazione come segue:

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





