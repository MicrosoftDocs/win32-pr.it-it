---
description: Il \_ messaggio WM CTLCOLOR viene usato nelle versioni di Windows a 16 bit per modificare la combinazione di colori delle caselle di riepilogo, le caselle di riepilogo di caselle combinate, le finestre di messaggio, i controlli pulsante, i controlli di modifica, i controlli statici e le finestre di dialogo. Nota per informazioni correlate a questo messaggio e alle versioni a 32 bit di Windows, vedere la sezione Osservazioni.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: Messaggio WM_CTLCOLOR (WindowsX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328953"
---
# <a name="wm_ctlcolor-message"></a>\_Messaggio CTLCOLOR WM

Il messaggio **WM \_ CTLCOLOR** viene usato nelle versioni di Windows a 16 bit per modificare la combinazione di colori delle caselle di riepilogo, le caselle di riepilogo di caselle combinate, le finestre di messaggio, i controlli pulsante, i controlli di modifica, i controlli statici e le finestre di dialogo.

> [!Note]  
> Per informazioni correlate a questo messaggio e alle versioni a 32 bit di Windows, vedere la sezione Osservazioni.

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra di destinazione.

</dd> <dt>

*wParam* 
</dt> <dd>

Handle per un contesto di visualizzazione (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per una finestra figlio (controllo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, restituisce un handle a un pennello. Il sistema utilizza il pennello per disegnare lo sfondo del controllo.

## <a name="remarks"></a>Commenti

Il messaggio **WM \_ CTLCOLOR** di Windows a 16 bit è stato sostituito da notifiche più specifiche. Queste sostituzioni includono quanto segue:

-   [**\_CTLCOLORBTN WM**](../controls/wm-ctlcolorbtn.md)
-   [**\_CTLCOLOREDIT WM**](../controls/wm-ctlcoloredit.md)
-   [**\_CTLCOLORDLG WM**](../dlgbox/wm-ctlcolordlg.md)
-   [**\_CTLCOLORLISTBOX WM**](../controls/wm-ctlcolorlistbox.md)
-   [**\_CTLCOLORSCROLLBAR WM**](../controls/wm-ctlcolorscrollbar.md)
-   [**\_CTLCOLORSTATIC WM**](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WindowsX. h</dt> </dl> |



 

 
