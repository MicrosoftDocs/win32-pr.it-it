---
title: Codice di notifica NM_RELEASEDCAPTURE (barra degli strumenti) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo della barra degli strumenti che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8d9b637c-710e-4337-9466-8616a93d1c44
keywords:
- Codice di notifica di NM_RELEASEDCAPTURE (barra degli strumenti) controlli Windows
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d915b3af073ba0c6b5c74a7b13317f7b2d4ab8a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119923"
---
# <a name="nm_releasedcapture-toolbar-notification-code"></a>\_Codice di notifica RELEASEDCAPTURE di Nm (barra degli strumenti)

Notifica alla finestra padre di un controllo della barra degli strumenti che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il controllo Ignora il valore restituito da questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





