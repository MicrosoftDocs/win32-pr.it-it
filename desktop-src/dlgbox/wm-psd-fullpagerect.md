---
title: Messaggio WM_PSD_FULLPAGERECT (COMMDLG. h)
description: Notifica a una procedura di hook PagePaintHook le coordinate del rettangolo della pagina di esempio nella finestra di dialogo Imposta pagina. La finestra di dialogo Invia questo messaggio quando sta per essere disegnato il contenuto della pagina di esempio.
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- Finestre di dialogo WM_PSD_FULLPAGERECT messaggio
topic_type:
- apiref
api_name:
- WM_PSD_FULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5265144822ba1f46c470b71169e0b27f2e1c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964595"
---
# <a name="wm_psd_fullpagerect-message"></a>\_ \_ Messaggio FULLPAGERECT di WM PSD

Notifica a una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) le coordinate del rettangolo della pagina di esempio nella finestra di dialogo **Imposta pagina** . La finestra di dialogo Invia questo messaggio quando sta per essere disegnato il contenuto della pagina di esempio.


```C++
#define WM_USER                  0x0400
#define WM_PSD_FULLPAGERECT     (WM_USER+1)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la pagina di esempio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, della pagina di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la procedura di hook restituisce **true**, la finestra di dialogo non invia più messaggi e non viene disegnato nella pagina di esempio fino alla successiva necessità di ricreare la pagina di esempio dal sistema.

Se la routine hook restituisce **false**, la finestra di dialogo Invia i messaggi rimanenti della sequenza di disegno.

## <a name="remarks"></a>Commenti

Nella finestra di dialogo **Imposta pagina** è inclusa un'immagine di una pagina di esempio in cui viene illustrato il modo in cui le selezioni dell'utente influiscono sull'aspetto dell'output stampato. Quando si chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , è possibile fornire una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio. Ogni volta che la finestra di dialogo sta per creare il contenuto della pagina di esempio, la finestra di dialogo Invia una sequenza di messaggi alla routine hook.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**\_PAGESETUPDLG PSD \_ WM**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

