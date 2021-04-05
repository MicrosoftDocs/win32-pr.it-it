---
title: Codice di notifica TBN_DUPACCELERATOR (COMmctrl. h)
description: Verifica se un tasto di scelta rapida può essere utilizzato su due o più barre degli strumenti attive. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- Controlli di Windows per il codice di notifica TBN_DUPACCELERATOR
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048593"
---
# <a name="tbn_dupaccelerator-notification-code"></a>\_Codice di notifica DUPACCELERATOR di TBN

Verifica se un tasto di scelta rapida può essere utilizzato su due o più barre degli strumenti attive. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che fornisce un tasto di scelta rapida e che riceve un valore che specifica se più barre degli strumenti rispondono allo stesso carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se ha esito positivo; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

L'applicazione deve dichiarare la struttura **NMTBDUPACCELERATOR** come segue:

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





