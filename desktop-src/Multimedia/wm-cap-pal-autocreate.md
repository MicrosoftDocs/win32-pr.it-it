---
title: Messaggio di WM_CAP_PAL_AUTOCREATE (VFW. h)
description: Il \_ messaggio WM Cap \_ PAL \_ creazione automatica richiede che il driver di acquisizione fotogrammi video di esempio e crei automaticamente una nuova tavolozza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301371"
---
# <a name="wm_cap_pal_autocreate-message"></a>\_Messaggio di \_ \_ creazione autocreata di WM Cap PAL

Il messaggio **WM \_ Cap \_ PAL \_ creazione** automatica richiede che il driver di acquisizione fotogrammi video di esempio e crei automaticamente una nuova tavolozza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Numero di frame da campionare.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Numero di colori nella tavolozza. Il valore massimo per questo parametro è 256.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.

## <a name="remarks"></a>Commenti

La sequenza video campionata deve includere tutti i colori desiderati nella tavolozza. Per ottenere la tavolozza migliore, potrebbe essere necessario campionare l'intera sequenza anziché una parte di esso.

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

 

 





