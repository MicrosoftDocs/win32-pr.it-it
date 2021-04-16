---
title: Messaggio WM_PSD_MARGINRECT (COMMDLG. h)
description: Notifica alla procedura di hook di una finestra di dialogo di impostazione della pagina, PagePaintHook, che la finestra di dialogo sta per creare il rettangolo dei margini della pagina di esempio.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- Finestre di dialogo WM_PSD_MARGINRECT messaggio
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
ms.openlocfilehash: 4718cfbe16db53378544d9fca0ab44ade23ffb3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477968"
---
# <a name="wm_psd_marginrect-message"></a>\_ \_ Messaggio MARGINRECT di WM PSD

Notifica alla procedura di hook di una finestra di dialogo di **impostazione della pagina** , [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), che la finestra di dialogo sta per creare il rettangolo dei margini della pagina di esempio.


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

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, del rettangolo del margine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la procedura di hook restituisce **true**, nella finestra di dialogo non viene disegnato il rettangolo dei margini nella pagina di esempio.

Se la routine hook restituisce **false**, nella finestra di dialogo viene disegnato il rettangolo dei margini nella pagina di esempio.

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

 

