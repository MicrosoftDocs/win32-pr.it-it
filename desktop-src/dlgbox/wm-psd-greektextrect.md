---
title: WM_PSD_GREEKTEXTRECT messaggio (Commdlg.h)
description: Notifica alla procedura hook di una finestra di dialogo Imposta pagina, PagePaintHook, che la finestra di dialogo sta per disegnare testo greco all'interno del rettangolo dei margini della pagina di esempio.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- WM_PSD_GREEKTEXTRECT finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30e4873255a59a86da91b3145d0675f6940ce35081273696ce6c68b70a1560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726051"
---
# <a name="wm_psd_greektextrect-message"></a>Messaggio WM \_ PSD \_ GREEKTEXTRECT

Notifica alla routine hook  di una finestra di dialogo Imposta pagina, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), che la finestra di dialogo sta per disegnare testo greco all'interno del rettangolo dei margini della pagina di esempio.


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la pagina di esempio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, del rettangolo di testo greco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook restituisce **TRUE,** la finestra di dialogo non disegna la parte di testo in greco della pagina di esempio.

Se la routine hook restituisce **FALSE,** la finestra di dialogo disegna la parte di testo greco della pagina di esempio.

## <a name="remarks"></a>Commenti

La **finestra di dialogo** Imposta pagina include un'immagine di una pagina di esempio che mostra come le selezioni dell'utente influiscono sull'aspetto dell'output stampato. Quando si chiama la [**funzione PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) è possibile fornire una routine hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio. Ogni volta che la finestra di dialogo sta per disegnare il contenuto della pagina di esempio, la finestra di dialogo invia una sequenza di messaggi alla procedura hook.

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

[**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comuni](common-dialog-box-library.md)
</dt> </dl>

 

