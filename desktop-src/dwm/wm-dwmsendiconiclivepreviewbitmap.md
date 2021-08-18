---
title: WM_DWMSENDICONICLIVEPREVIEWBITMAP messaggio (Dwmapi.h)
description: Indica a una finestra di fornire una bitmap statica da usare come anteprima live (nota anche come anteprima di anteprima) di tale finestra.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP messaggio Gestione finestre desktop
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
ms.openlocfilehash: a7742b70afad62a42378e50a06a6e40e503bee72309f5f233f9cf8bf62cf41d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985247"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>Messaggio WM \_ DWMSENDICONICLIVEPREVIEWBITMAP

Indica a una finestra di fornire una bitmap statica da usare come anteprima *live* (nota anche come anteprima di *anteprima)* di tale finestra.

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

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando un utente sposta il puntatore del mouse sull'anteprima della finestra nella barra delle applicazioni o assegna lo stato attivo all'anteprima nella finestra ALT+TAB, viene visualizzata un'anteprima dinamica *(nota* anche come anteprima di anteprima). Questa visualizzazione è un'anteprima a dimensione intera della finestra e può essere uno snapshot live o una rappresentazione simbolica.

Gestione finestre desktop (DWM) invia questo messaggio a una finestra se si verificano tutte le situazioni seguenti:

-   L'anteprima live è stata richiamata nella finestra.
-   L'attributo BITMAP HAS BITMAP di [**DWMWA \_ \_ \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) è impostato nella finestra.
-   Una rappresentazione simbolica è l'unica esistente per questa finestra.

La finestra che riceve questo messaggio deve rispondere generando una bitmap a scalabilità completa. La finestra chiama quindi la [**funzione DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) per impostare l'anteprima live. Se la finestra non imposta una bitmap in un determinato periodo di tempo, DWM usa la propria rappresentazione simbolica predefinita per la finestra.

## <a name="examples"></a>Esempio

L'esempio seguente illustra una risposta al **messaggio WM \_ DWMSENDICONICLIVEPREVIEWBITMAP.** L'esempio chiama [**la funzione DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) con un handle per una bitmap personalizzata e indipendente dal dispositivo da usare come rappresentazione della finestra.


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



Per il codice completo, vedere [l'esempio Customize an Preview Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) (Personalizzare un'anteprima di anteprima e una bitmap in anteprima live).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Dwmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WM \_ DWMSENDICONICTHUMBNAIL**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





