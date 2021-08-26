---
title: TVN_GETDISPINFO codice di notifica (Commctrl.h)
description: Richiede che la finestra padre di un controllo visualizzazione albero fornica le informazioni necessarie per visualizzare o ordinare un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO codice di notifica Windows controlli
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
ms.openlocfilehash: 59728c816ee3fe7dac46c12d7e62da6c18cfdad8387f03d3861e63792d9c8f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059911"
---
# <a name="tvn_getdispinfo-notification-code"></a>Codice di notifica \_ TVN GETDISPINFO

Richiede che la finestra padre di un controllo visualizzazione albero fornica le informazioni necessarie per visualizzare o ordinare un elemento. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) Il **membro** dell'elemento è una [**struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) i cui membri **mask**, **hItem**, **state** e **lParam** specificano il tipo di informazioni necessarie. È necessario compilare i membri della struttura con le informazioni appropriate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato nelle circostanze seguenti:

-   Se il **membro pszText** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore LPSTR TEXTCALLBACK, il controllo invia questo codice di notifica per recuperare il \_ testo dell'elemento. In questo caso, il **membro mask** di *lParam* avrà il flag TVIF \_ TEXT impostato.
-   Se il membro **iImage** o **iSelectedImage** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore I IMAGECALLBACK, il controllo invia questo codice di notifica per recuperare l'indice delle icone di un elemento nell'elenco di immagini del \_ controllo. In questo caso, se l'elemento è selezionato, il **membro mask** di *lParam* avrà il flag TVIF \_ SELECTEDIMAGE impostato. Se l'elemento non è selezionato, il **membro mask** di *lParam* avrà il flag TVIF \_ IMAGE impostato.
-   Se il **membro cChildren** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore I CHILDRENCALLBACK, il controllo invia questo codice di notifica per recuperare un valore che indica se l'elemento dispone di \_ elementi figlio. In questo caso, il **membro mask** *di lParam* avrà il flag TVIF \_ CHILDREN impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ GETDISPINFOW** (Unicode) e **TVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[TVN \_ SETDISPINFO](tvn-setdispinfo.md)
</dt> </dl>

 

 





