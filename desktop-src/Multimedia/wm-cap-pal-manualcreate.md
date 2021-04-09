---
title: Messaggio di WM_CAP_PAL_MANUALCREATE (VFW. h)
description: Il \_ messaggio MANUALCREATE di WM Cap \_ \_ richiede che il driver di acquisizione campiona manualmente i fotogrammi video e crei una nuova tavolozza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740959"
---
# <a name="wm_cap_pal_manualcreate-message"></a>\_Messaggio MANUALCREATE di WM Cap \_ PAL \_

Il **messaggio \_ \_ \_ MANUALCREATE di WM Cap** richiede che il driver di acquisizione campiona manualmente i fotogrammi video e crei una nuova tavolozza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*
</dt> <dd>

Flag istogramma tavolozza. Impostare questo parametro su **true** per ogni frame incluso nella creazione della tavolozza ottimale. Dopo che l'ultimo frame è stato raccolto, impostare questo parametro su **false** per calcolare la tavolozza ottimale e inviarla al driver di acquisizione.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Numero di colori nella tavolozza. Il valore massimo per questo parametro è 256. Questo valore viene usato solo durante la raccolta del primo frame in una sequenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





