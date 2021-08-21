---
title: WM_PSD_MARGINRECT messaggio (Commdlg.h)
description: Notifica alla procedura hook di una finestra di dialogo Imposta pagina, PagePaintHook, che la finestra di dialogo sta per disegnare il rettangolo dei margini della pagina di esempio.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- WM_PSD_MARGINRECT finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09523258d1f67cfc4f35433a43a6b5a17db0be9dedaea87511c0c6d1327f82cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985261"
---
# <a name="wm_psd_marginrect-message"></a>Messaggio \_ WM PSD \_ MARGINRECT

Notifica alla procedura hook  di una finestra di dialogo Imposta pagina, [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), che la finestra di dialogo sta per disegnare il rettangolo dei margini della pagina di esempio.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la pagina di esempio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, del rettangolo del margine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook restituisce **TRUE,** la finestra di dialogo non disegna il rettangolo del margine nella pagina di esempio.

Se la routine hook restituisce **FALSE,** la finestra di dialogo disegna il rettangolo del margine nella pagina di esempio.

## <a name="remarks"></a>Commenti

La **finestra di dialogo** Imposta pagina include un'immagine di una pagina di esempio che mostra in che modo le selezioni dell'utente influiscono sull'aspetto dell'output stampato. Quando si chiama la [**funzione PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) è possibile fornire una procedura hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio. Ogni volta che la finestra di dialogo sta per disegnare il contenuto della pagina di esempio, la finestra di dialogo invia una sequenza di messaggi alla routine hook.

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

[Libreria di finestre di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

