---
title: WM_DWMSENDICONICTHUMBNAIL messaggio (Dwmapi.h)
description: Indica a una finestra di fornire una bitmap statica da usare come rappresentazione di anteprima di tale finestra.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL messaggio Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3263f34cd59ba68ee895e5d5c77e297144cbadd6c8d8bbaa49ca6272248c2024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842651"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>Messaggio \_ WM DWMSENDICONICTHUMBNAIL

Indica a una finestra di fornire una bitmap statica da usare come rappresentazione di anteprima di tale finestra.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) di questo valore è la coordinata x massima dell'anteprima. LOWORD [**è**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la coordinata y massima. Se un'anteprima ha una dimensione che supera uno o entrambi questi valori, DWM non accetta l'anteprima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

DWM invia questo messaggio a una finestra se tutte le situazioni seguenti sono vere:

-   DWM visualizza una rappresentazione simbolica della finestra.
-   L'attributo BITMAP HAS BITMAP di [**DWMWA \_ \_ \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) è impostato nella finestra.
-   La finestra non ha impostato una bitmap memorizzata nella cache.
-   C'è spazio nella cache per un'altra bitmap.

La finestra che riceve questo messaggio deve rispondere generando una bitmap non superiore alla dimensione richiesta nei parametri del messaggio. La finestra chiama quindi la [**funzione DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) per eseguire l'override dell'anteprima predefinita. Se la finestra non fornisce una bitmap in un determinato periodo di tempo, DWM usa la propria rappresentazione simbolica predefinita per la finestra.

La finestra deve appartenere al processo chiamante.

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra come rispondere al messaggio **WM \_ DWMSENDICONICTHUMBNAIL.** L'esempio [**chiama DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), con un handle per una bitmap personalizzata e indipendente dal dispositivo da usare come rappresentazione delle finestre.


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



Per l'esempio completo, vedere [l'esempio Customize an Preview Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) (Personalizzare un'anteprima di anteprima e una bitmap in anteprima live).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Dwmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

