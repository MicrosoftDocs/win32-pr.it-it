---
description: Il messaggio WM CTLCOLOR viene usato nelle versioni a 16 bit di Windows per modificare la combinazione di colori delle caselle di riepilogo, le caselle di riepilogo delle caselle combinate, le caselle di messaggio, i controlli pulsante, i controlli di modifica, i controlli statici e le finestre \_ di dialogo. Nota Per informazioni relative a questo messaggio e alle versioni a 32 bit Windows, vedere la sezione Osservazioni.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: WM_CTLCOLOR messaggio (WindowsX.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c53f18bc42737e44a2137e0c9763dfc41de44f65661ca4754915f7a21317641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343291"
---
# <a name="wm_ctlcolor-message"></a>Messaggio \_ WM CTLCOLOR

Il messaggio **WM \_ CTLCOLOR** viene usato nelle versioni a 16 bit di Windows per modificare la combinazione di colori delle caselle di riepilogo, le caselle di riepilogo delle caselle combinate, le caselle di messaggio, i controlli pulsante, i controlli di modifica, i controlli statici e le finestre di dialogo.

> [!Note]  
> Per informazioni relative a questo messaggio e alle versioni a 32 bit Windows, vedere la sezione Osservazioni.

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra di destinazione.

</dd> <dt>

*wParam* 
</dt> <dd>

Handle per un contesto di visualizzazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per una finestra figlio (controllo ).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, restituisce un handle a un pennello. Il sistema usa il pennello per disegnare lo sfondo del controllo.

## <a name="remarks"></a>Commenti

Il **messaggio \_ WM CTLCOLOR** da un Windows a 16 bit è stato sostituito da notifiche più specifiche. Queste sostituzioni includono quanto segue:

-   [**WM \_ CTLCOLORBTN**](../controls/wm-ctlcolorbtn.md)
-   [**WM \_ CTLCOLOREDIT**](../controls/wm-ctlcoloredit.md)
-   [**WM \_ CTLCOLORDLG**](../dlgbox/wm-ctlcolordlg.md)
-   [**WM \_ CTLCOLORLISTBOX**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ CTLCOLORSCROLLBAR**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ CTLCOLORSTATIC**](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WindowsX.h</dt> </dl> |



 

 
