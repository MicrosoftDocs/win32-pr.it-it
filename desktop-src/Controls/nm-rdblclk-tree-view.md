---
title: Codice di notifica di NM_RDBLCLK (visualizzazione albero) (COMmctrl. h)
description: Notifica all'elemento padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questa notifica viene inviata sotto forma di \_ messaggio di notifica WM.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- NM_RDBLCLK (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5b4f1dbaf1031c995028028cc0b44e544f5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120839"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a>\_Codice di notifica di RDBLCLK Nm (visualizzazione albero)

Notifica all'elemento padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





