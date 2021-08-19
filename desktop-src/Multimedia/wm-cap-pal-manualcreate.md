---
title: WM_CAP_PAL_MANUALCREATE messaggio (Vfw.h)
description: Il messaggio WM CAP PAL MANUALCREATE richiede al driver di acquisizione di campionare manualmente i fotogrammi \_ video e creare una nuova \_ \_ tavolozza. È possibile inviare questo messaggio in modo esplicito o usando la macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE messaggio Windows Multimediali
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
ms.openlocfilehash: c8cc313cb6eae8e757d0777642bbc0ab72fe07fcfbf5b530a6479675c8ab3c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781292"
---
# <a name="wm_cap_pal_manualcreate-message"></a>MESSAGGIO \_ WM CAP PAL \_ \_ MANUALCREATE

Il **messaggio WM CAP PAL \_ \_ \_ MANUALCREATE** richiede al driver di acquisizione di campionare manualmente i fotogrammi video e creare una nuova tavolozza. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capPaletteManual.**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual)


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*
</dt> <dd>

Flag dell'istogramma della tavolozza. Impostare questo parametro su **TRUE** per ogni frame incluso nella creazione del riquadro ottimale. Dopo aver raccolto l'ultimo frame, impostare questo parametro su **FALSE** per calcolare il riquadro ottimale e inviarlo al driver di acquisizione.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Numero di colori nella tavolozza. Il valore massimo per questo parametro è 256. Questo valore viene usato solo durante la raccolta del primo frame in una sequenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

Se si verifica un errore e viene impostata una funzione di callback degli errori usando il messaggio [**WM CAP SET CALLBACK \_ \_ \_ \_ ERROR,**](wm-cap-set-callback-error.md) viene chiamata la funzione di callback degli errori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





