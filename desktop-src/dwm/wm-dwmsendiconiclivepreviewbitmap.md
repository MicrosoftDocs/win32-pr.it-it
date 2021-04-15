---
title: Messaggio WM_DWMSENDICONICLIVEPREVIEWBITMAP (dwmapi. h)
description: Indica a una finestra di fornire una bitmap statica da utilizzare come anteprima in tempo reale (nota anche come anteprima di visualizzazione) di tale finestra.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- Messaggio WM_DWMSENDICONICLIVEPREVIEWBITMAP Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477002"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>\_Messaggio DWMSENDICONICLIVEPREVIEWBITMAP WM

Indica a una finestra di fornire una bitmap statica da utilizzare come *anteprima in tempo reale* (nota anche come *Anteprima di visualizzazione*) di tale finestra.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Un' *anteprima in tempo reale* , nota anche come *Anteprima* di una finestra, viene visualizzata quando un utente sposta il puntatore del mouse sull'anteprima della finestra nella barra delle applicazioni o assegna all'anteprima lo stato attivo nella finestra Alt + Tab. Questa vista è un'anteprima completa della finestra e può essere uno snapshot Live o una rappresentazione iconica.

Gestione finestre desktop (DWM) Invia questo messaggio a una finestra se si verificano tutte le situazioni seguenti:

-   L'anteprima in tempo reale è stata richiamata nella finestra.
-   Per DWMWA è impostato un attributo [**\_ \_ \_ bitmap iconico**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) nella finestra.
-   Una rappresentazione iconica è l'unica esistente per questa finestra.

La finestra che riceve questo messaggio deve rispondere generando una bitmap a scalabilità totale. La finestra chiama quindi la funzione [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) per impostare l'anteprima in tempo reale. Se la finestra non imposta una bitmap in un determinato periodo di tempo, DWM utilizza la propria rappresentazione iconica predefinita per la finestra.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata una risposta al messaggio **WM \_ DWMSENDICONICLIVEPREVIEWBITMAP** . L'esempio chiama la funzione [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) con un handle per una bitmap personalizzata, indipendente dal dispositivo, da usare come rappresentazione della finestra.


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



Per il codice completo, vedere l'esempio [personalizzare un'anteprima iconica e una bitmap di anteprima in tempo reale](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_DWMSENDICONICTHUMBNAIL WM**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





