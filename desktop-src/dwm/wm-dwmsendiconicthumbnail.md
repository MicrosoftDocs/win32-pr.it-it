---
title: Messaggio WM_DWMSENDICONICTHUMBNAIL (dwmapi. h)
description: Indica a una finestra di fornire una bitmap statica da utilizzare come rappresentazione di anteprima di tale finestra.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- Messaggio WM_DWMSENDICONICTHUMBNAIL Gestione finestre desktop
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
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478766"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>\_Messaggio DWMSENDICONICTHUMBNAIL WM

Indica a una finestra di fornire una bitmap statica da utilizzare come rappresentazione di anteprima di tale finestra.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) di questo valore è la coordinata x massima dell'anteprima. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è la coordinata y massima. Se un'anteprima ha una dimensione che supera uno o entrambi questi valori, DWM non accetta l'anteprima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

DWM Invia questo messaggio a una finestra se si verificano tutte le situazioni seguenti:

-   DWM Visualizza una rappresentazione iconica della finestra.
-   Per DWMWA è impostato un attributo [**\_ \_ \_ bitmap iconico**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) nella finestra.
-   Nella finestra non è stata impostata una bitmap memorizzata nella cache.
-   Nella cache è presente spazio per un'altra bitmap.

La finestra che riceve questo messaggio deve rispondere generando una bitmap che non è più grande della dimensione richiesta nei parametri del messaggio. La finestra chiama quindi la funzione [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) per eseguire l'override dell'anteprima predefinita. Se la finestra non fornisce una bitmap in un determinato periodo di tempo, DWM usa la propria rappresentazione iconica predefinita per la finestra.

La finestra deve appartenere al processo chiamante.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come rispondere al messaggio **WM \_ DWMSENDICONICTHUMBNAIL** . Nell'esempio viene chiamato [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail)con un handle per una bitmap personalizzata indipendente dal dispositivo da utilizzare come rappresentazione di Windows.


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



Per l'esempio completo, vedere l'esempio [personalizzare un'anteprima iconica e una bitmap di anteprima in tempo reale](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**\_DWMSENDICONICLIVEPREVIEWBITMAP WM**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

