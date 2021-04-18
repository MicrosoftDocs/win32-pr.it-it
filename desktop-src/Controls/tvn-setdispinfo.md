---
title: Codice di notifica TVN_SETDISPINFO (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che deve aggiornare le informazioni che gestisce su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- Controlli di Windows per il codice di notifica TVN_SETDISPINFO
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301176"
---
# <a name="tvn_setdispinfo-notification-code"></a>\_Codice di notifica SETDISPINFO di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero che deve aggiornare le informazioni che gestisce su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**struttura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) che descrive l'elemento da aggiornare. Il membro **hitey** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) specifica l'elemento da aggiornare e il membro **mask** specifica gli attributi dell'elemento da aggiornare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Se il membro **pszText** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore TEXTCALLBACK di LPSTR \_ , il controllo Invia la notifica per impostare il testo dell'elemento. In questo caso, per il membro **mask** di *lParam* verrà impostato il \_ flag di testo TVIF.

Se il membro **IImage** o **ISelectedImage** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore i \_ IMAGECALLBACK, il controllo Invia la notifica per recuperare l'indice dell'immagine dell'icona da visualizzare. In questo caso, per il membro **mask** di *lParam* sarà impostata l' \_ immagine TVIF o il \_ flag TVIF SELECTEDIMAGE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ SETDISPINFOW** (Unicode) e **TVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[\_GETDISPINFO TVN](tvn-getdispinfo.md)
</dt> </dl>

 

 





