---
title: Codice di notifica TBN_GETDISPINFO (COMmctrl. h)
description: Recupera le informazioni di visualizzazione per un elemento della barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- Controlli di Windows per il codice di notifica TBN_GETDISPINFO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120670"
---
# <a name="tbn_getdispinfo-notification-code"></a>\_Codice di notifica GETDISPINFO di TBN

Recupera le informazioni di visualizzazione per un elemento della barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) . Il membro **idCommand** specifica l'identificatore di comando dell'elemento, il membro **lParam** contiene i dati definiti dall'applicazione dell'elemento e il membro **dwMask** specifica quali informazioni vengono richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dal controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TBN \_ GETDISPINFOW** (Unicode) e **TBN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





