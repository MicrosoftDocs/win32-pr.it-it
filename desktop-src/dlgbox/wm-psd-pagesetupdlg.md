---
title: Messaggio WM_PSD_PAGESETUPDLG (COMMDLG. h)
description: Notifica a una procedura PagePaintHook hook che la finestra di dialogo Imposta pagina sta per creare il contenuto della pagina di esempio. La procedura hook può utilizzare questo messaggio per eseguire attività di inizializzazione correlate alla creazione del contenuto della pagina di esempio.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- Finestre di dialogo WM_PSD_PAGESETUPDLG messaggio
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400900"
---
# <a name="wm_psd_pagesetupdlg-message"></a>\_ \_ Messaggio PAGESETUPDLG di WM PSD

Notifica a una procedura [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook che la finestra di dialogo **Imposta pagina** sta per creare il contenuto della pagina di esempio. La procedura hook può utilizzare questo messaggio per eseguire attività di inizializzazione correlate alla creazione del contenuto della pagina di esempio.


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore specifica un valore che indica il formato della carta. Questo valore può essere uno dei valori **DMPAPER \_** elencati nella descrizione della struttura. La parola più significativa specifica l'orientamento della carta o della busta e indica se la stampante è una matrice di punti o un dispositivo HPPCL (Hewlett Packard Printer Control Language). Questo parametro può avere uno dei valori seguenti.



| Valore                                                                             | Significato                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>0x0001</dt> </dl> | Carta in modalità orizzontale (matrice di punti)<br/>    |
| <dl> <dt>0x0003</dt> </dl> | Carta in modalità orizzontale (HPPCL)<br/>         |
| <dl> <dt>0x0005</dt> </dl> | Carta in modalità verticale (matrice a punti)<br/>     |
| <dl> <dt>0x0007</dt> </dl> | Carta in modalità verticale (HPPCL)<br/>          |
| <dl> <dt>0x000b</dt> </dl> | Busta in modalità orizzontale (HPPCL)<br/>      |
| <dl> <dt>0x000d</dt> </dl> | Busta in modalità verticale (matrice di punti)<br/>  |
| <dl> <dt>0x0019</dt> </dl> | Busta in modalità orizzontale (matrice di punti)<br/> |
| <dl> <dt>0x001F</dt> </dl> | Busta in modalità verticale (HPPCL)<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) contenente le informazioni utilizzate per inizializzare la finestra di dialogo **Imposta pagina** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la procedura di hook restituisce **true**, la finestra di dialogo non invia più messaggi e non viene disegnato nella pagina di esempio fino alla successiva necessità di ricreare la pagina di esempio dal sistema.

Se la routine hook restituisce **false**, la finestra di dialogo Invia i messaggi rimanenti della sequenza di disegno.

## <a name="remarks"></a>Commenti

Nella finestra di dialogo **Imposta pagina** è inclusa un'immagine di una pagina di esempio in cui viene illustrato il modo in cui le selezioni dell'utente influiscono sull'aspetto dell'output stampato. Quando si chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , è possibile fornire una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio. Ogni volta che la finestra di dialogo sta per creare il contenuto della pagina di esempio, la finestra di dialogo Invia una sequenza di messaggi alla routine hook.

I primi tre messaggi di una sequenza di disegno (**WM \_ PSD \_ PAGESETUPDLG**, [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)o [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) forniscono informazioni che la procedura hook può utilizzare per disegnare il contenuto della pagina di esempio. I messaggi rimanenti [**(WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md), [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notificano alla procedura hook che la finestra di dialogo sta per creare una parte specifica della pagina di esempio. Questo consente alla routine hook di creare selettivamente parti della pagina di esempio.

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

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**\_ENVSTAMPRECT PSD \_ WM**](wm-psd-envstamprect.md)
</dt> <dt>

[**\_FULLPAGERECT PSD \_ WM**](wm-psd-fullpagerect.md)
</dt> <dt>

[**\_GREEKTEXTRECT PSD \_ WM**](wm-psd-greektextrect.md)
</dt> <dt>

[**\_MARGINRECT PSD \_ WM**](wm-psd-marginrect.md)
</dt> <dt>

[**\_MINMARGINRECT PSD \_ WM**](wm-psd-minmarginrect.md)
</dt> <dt>

[**\_YAFULLPAGERECT PSD \_ WM**](wm-psd-yafullpagerect.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

