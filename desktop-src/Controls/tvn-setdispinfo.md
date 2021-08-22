---
title: TVN_SETDISPINFO codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che deve aggiornare le informazioni mantenute su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO codice di notifica Windows controlli
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
ms.openlocfilehash: e88a9b5fed4260fa88f5f40431113456950d99985ad2f2e0e97c2e951dce96bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957770"
---
# <a name="tvn_setdispinfo-notification-code"></a>Codice di notifica \_ TVN SETDISPINFO

Notifica alla finestra padre di un controllo visualizzazione albero che deve aggiornare le informazioni mantenute su un elemento. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) che descrive l'elemento da aggiornare. Il **membro hItem** della [**struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) specifica l'elemento da aggiornare e il membro **mask** specifica gli attributi dell'elemento da aggiornare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Se il **membro pszText** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore LPSTR TEXTCALLBACK, il controllo invia questa notifica per impostare il \_ testo dell'elemento. In questo caso, il **membro mask** di *lParam* avrà il flag TVIF \_ TEXT impostato.

Se il **membro iImage** o **iSelectedImage** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore I IMAGECALLBACK, il controllo invia questa notifica per recuperare l'indice dell'immagine dell'icona \_ da visualizzare. In questo caso, il **membro mask** *di lParam* avrà il flag TVIF IMAGE o \_ TVIF \_ SELECTEDIMAGE impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ SETDISPINFOW** (Unicode) e **TVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[TVN \_ GETDISPINFO](tvn-getdispinfo.md)
</dt> </dl>

 

 





