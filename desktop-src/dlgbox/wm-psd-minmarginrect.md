---
title: Messaggio WM_PSD_MINMARGINRECT (COMMDLG. h)
description: Notifica a una procedura di hook PagePaintHook le coordinate del rettangolo dei margini nella pagina di esempio. La finestra di dialogo Imposta pagina Invia questo messaggio quando sta per essere disegnato il contenuto della pagina di esempio.
ms.assetid: 14977b52-7a6f-4c55-956a-716398a71613
keywords:
- Finestre di dialogo WM_PSD_MINMARGINRECT messaggio
topic_type:
- apiref
api_name:
- WM_PSD_MINMARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ec7271026ba7557fcbe3fe17cd890d62eadbca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518339"
---
# <a name="wm_psd_minmarginrect-message"></a>\_ \_ Messaggio MINMARGINRECT di WM PSD

Notifica a una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) le coordinate del rettangolo dei margini nella pagina di esempio. La finestra di dialogo **Imposta pagina** Invia questo messaggio quando sta per essere disegnato il contenuto della pagina di esempio.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MINMARGINRECT    (WM_USER+2)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la pagina di esempio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, del rettangolo del margine minimo.

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

 

