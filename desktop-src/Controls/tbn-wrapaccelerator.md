---
title: Codice di notifica TBN_WRAPACCELERATOR (COMmctrl. h)
description: Richiede l'indice del pulsante in una o più barre degli strumenti corrispondenti al carattere dell'acceleratore specificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- Controlli di Windows per il codice di notifica TBN_WRAPACCELERATOR
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
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301177"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>\_Codice di notifica WRAPACCELERATOR di TBN

Richiede l'indice del pulsante in una o più barre degli strumenti corrispondenti al carattere dell'acceleratore specificato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che contiene il carattere del tasto di scelta rapida e che riceve l'indice del pulsante corrispondente. L'indice è-1 se il tasto di scelta rapida non corrisponde a un comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**True** se viene restituito un indice, in caso contrario **false**.

## <a name="remarks"></a>Commenti

Le applicazioni con una o più barre degli strumenti possono ricevere questo codice di notifica.

La struttura **NMTBWRAPACCELERATOR** deve essere definita dall'applicazione come segue:

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





