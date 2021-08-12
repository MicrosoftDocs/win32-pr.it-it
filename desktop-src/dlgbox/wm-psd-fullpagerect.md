---
title: WM_PSD_FULLPAGERECT messaggio (Commdlg.h)
description: Notifica a una routine hook PagePaintHook le coordinate del rettangolo della pagina di esempio nella finestra di dialogo Imposta pagina. La finestra di dialogo invia questo messaggio quando sta per disegnare il contenuto della pagina di esempio.
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- WM_PSD_FULLPAGERECT finestre di dialogo del messaggio
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
ms.openlocfilehash: a0b3d49ca34775657fbb626823fe68632ad963abc29a99ff5aa99dce69753e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280371"
---
# <a name="wm_psd_fullpagerect-message"></a>Messaggio \_ WM PSD \_ FULLPAGERECT

Notifica a una [*routine hook PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) le coordinate del rettangolo della pagina di esempio nella **finestra di dialogo Imposta** pagina. La finestra di dialogo invia questo messaggio quando sta per disegnare il contenuto della pagina di esempio.


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

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, della pagina di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook restituisce **TRUE,** la finestra di dialogo non invia altri messaggi e non disegna nella pagina di esempio fino al successivo ridisegno della pagina di esempio da parte del sistema.

Se la routine hook restituisce **FALSE,** la finestra di dialogo invia i messaggi rimanenti della sequenza di disegno.

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

 

