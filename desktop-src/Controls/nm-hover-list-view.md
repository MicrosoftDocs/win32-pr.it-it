---
title: Codice di notifica NM_HOVER (visualizzazione elenco) (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando il mouse viene spostato su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- Codice di notifica NM_HOVER (visualizzazione elenco) controlli Windows
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873305"
---
# <a name="nm_hover-list-view-notification-code"></a>Codice di notifica del passaggio del mouse su NM \_ (visualizzazione elenco)

Inviato da un controllo di visualizzazione elenco quando il mouse viene spostato su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire alla visualizzazione elenco di elaborare normalmente il passaggio del mouse o un valore diverso da zero per impedire l'elaborazione del passaggio del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





