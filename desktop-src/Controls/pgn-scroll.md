---
title: Codice di notifica PGN_SCROLL (COMmctrl. h)
description: Notifica alla finestra padre di un controllo pager che sta per essere eseguito lo scorrimento della finestra contenuta. Questa notifica viene inviata sotto forma di \_ messaggio di notifica WM.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- Controlli di Windows per il codice di notifica PGN_SCROLL
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119578"
---
# <a name="pgn_scroll-notification-code"></a>\_Codice di notifica di scorrimento PGN

Notifica alla finestra padre di un controllo pager che sta per essere eseguito lo scorrimento della finestra contenuta. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) che contiene e riceve informazioni sul codice di notifica. Il membro **Idir** della struttura indica la direzione dello scorrimento. I membri **iXpos** e **iYpos** contengono la posizione orizzontale e verticale della finestra contenuta prima dello scorrimento. Il membro **iScroll** contiene l'importo Delta di scorrimento predefinito. Se lo si desidera, è possibile modificare questo membro in un altro valore di scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





