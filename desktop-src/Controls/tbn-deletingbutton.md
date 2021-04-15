---
title: Messaggio TBN_DELETINGBUTTON (COMmctrl. h)
description: Inviato da un controllo Toolbar quando un pulsante sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- Controlli di Windows Message TBN_DELETINGBUTTON
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517511"
---
# <a name="tbn_deletingbutton-message"></a>\_Messaggio TBN DELETINGBUTTON

Inviato da un controllo Toolbar quando un pulsante sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) contenente informazioni sul pulsante da eliminare. Per questo codice di notifica, sono validi solo i membri **HDR** e **iItem** di questa struttura. Il membro **iItem** della struttura contiene l'identificatore di comando del pulsante da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





