---
title: WM_PSD_ENVSTAMPRECT messaggio (Commdlg.h)
description: Notifica alla procedura hook di una finestra di dialogo Imposta pagina, PagePaintHook, che la finestra di dialogo sta per disegnare il rettangolo di stampa della pagina di esempio.
ms.assetid: f193baa0-a084-416e-90c9-9c838758a3d3
keywords:
- WM_PSD_ENVSTAMPRECT finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- WM_PSD_ENVSTAMPRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf846779f2fba5c2b2ac85d806c794d3e88aa6dcac0ce906ad82332e2ca2bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720708"
---
# <a name="wm_psd_envstamprect-message"></a>Messaggio \_ WM PSD \_ ENVSTAMPRECT

Notifica alla procedura hook  di una finestra di dialogo Imposta pagina, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), che la finestra di dialogo sta per disegnare il rettangolo di stampa della pagina di esempio.


```C++
#define WM_USER                  0x0400
#define WM_PSD_ENVSTAMPRECT     (WM_USER+5)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la pagina di esempio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, del rettangolo del timbro della busta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook restituisce **TRUE,** la finestra di dialogo non disegna la parte envelope-stamp della pagina di esempio.

Se la routine hook restituisce **FALSE,** la finestra di dialogo disegna la parte della busta della pagina di esempio.

## <a name="remarks"></a>Commenti

La **finestra di dialogo** Imposta pagina include un'immagine di una pagina di esempio che mostra come le selezioni dell'utente influiscono sull'aspetto dell'output stampato. Quando si chiama la [**funzione PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) è possibile fornire una routine hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio. Ogni volta che la finestra di dialogo sta per disegnare il contenuto della pagina di esempio, la finestra di dialogo invia una sequenza di messaggi alla procedura hook.

Una procedura hook riceve questo messaggio solo se il tipo di carta selezionato è una busta.

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

 

