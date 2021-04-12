---
title: Codice di notifica TVN_GETDISPINFO (COMmctrl. h)
description: Richiede che la finestra padre di un controllo di visualizzazione albero fornisca le informazioni necessarie per visualizzare o ordinare un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- Controlli di Windows per il codice di notifica TVN_GETDISPINFO
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517829"
---
# <a name="tvn_getdispinfo-notification-code"></a>\_Codice di notifica GETDISPINFO di TVN

Richiede che la finestra padre di un controllo di visualizzazione albero fornisca le informazioni necessarie per visualizzare o ordinare un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**struttura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . Il membro dell' **elemento** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) i cui membri **mask**, **hitet**, **state** e **lParam** specificano il tipo di informazioni richieste. È necessario compilare i membri della struttura con le informazioni appropriate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato nelle circostanze seguenti:

-   Se il membro **pszText** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore TEXTCALLBACK di LPSTR \_ , il controllo Invia questo codice di notifica per recuperare il testo dell'elemento. In questo caso, per il membro **mask** di *lParam* verrà impostato il \_ flag di testo TVIF.
-   Se il membro **IImage** o **ISelectedImage** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore i \_ IMAGECALLBACK, il controllo Invia questo codice di notifica per recuperare l'indice delle icone di un elemento nell'elenco immagini del controllo. In questo caso, se l'elemento è selezionato, il membro **mask** di *lParam* avrà il flag TVIF \_ SELECTEDIMAGE impostato. Se l'elemento non è selezionato, per il membro **mask** di *lParam* verrà impostato il \_ flag immagine TVIF.
-   Se il membro **cfigli** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore i \_ CHILDRENCALLBACK, il controllo Invia questo codice di notifica per recuperare un valore che indica se l'elemento contiene elementi figlio. In questo caso, per il membro **mask** di *lParam* verrà impostato il \_ flag TVIF Children.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ GETDISPINFOW** (Unicode) e **TVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_SETDISPINFO TVN](tvn-setdispinfo.md)
</dt> </dl>

 

 





