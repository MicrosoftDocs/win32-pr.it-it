---
title: WM_PSD_YAFULLPAGERECT messaggio (Commdlg.h)
description: Notifica alla procedura hook di una finestra di dialogo Imposta pagina, PagePaintHook, che la finestra di dialogo sta per disegnare la parte relativa all'indirizzo del mittente di una pagina di esempio della busta.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- WM_PSD_YAFULLPAGERECT finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62cfbd187cb3db5a27579b428c352be1da1a4bdf91f3336ed41511fe59d75d23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787361"
---
# <a name="wm_psd_yafullpagerect-message"></a>Messaggio \_ YAFULLPAGERECT di WM PSD \_

Notifica alla procedura hook  di una finestra di dialogo Imposta pagina, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), che la finestra di dialogo sta per disegnare la parte relativa all'indirizzo del mittente di una pagina di esempio della busta.


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la pagina di esempio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, della pagina di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook restituisce **TRUE,** la finestra di dialogo non disegna la parte relativa all'indirizzo del mittente di una pagina di esempio della busta.

Se la routine hook restituisce **FALSE,** la finestra di dialogo disegna la parte relativa all'indirizzo del mittente di una pagina di esempio della busta.

Se il tipo di carta non è una busta, il valore restituito non ha alcun effetto.

## <a name="remarks"></a>Commenti

La **finestra di dialogo** Imposta pagina include un'immagine di una pagina di esempio che mostra in che modo le selezioni dell'utente influiscono sull'aspetto dell'output stampato. Quando si chiama la [**funzione PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) è possibile fornire una procedura hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio. Ogni volta che la finestra di dialogo sta per disegnare il contenuto della pagina di esempio, la finestra di dialogo invia una sequenza di messaggi alla procedura hook.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**PAGINA \_ DI WM \_ PSDSETUPDLG**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

