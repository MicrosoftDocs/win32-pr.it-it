---
title: WM_CAP_PAL_AUTOCREATE messaggio (Vfw.h)
description: Il messaggio WM CAP PAL AUTOCREATE richiede al driver di acquisizione di campionare fotogrammi \_ video e di creare \_ \_ automaticamente una nuova tavolozza. È possibile inviare questo messaggio in modo esplicito o usando la macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE messaggio Windows Multimediali
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
ms.openlocfilehash: a18d805ef394388de2265845f4e21bebb98d94391b851a60ed38d46e9872fecc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800641"
---
# <a name="wm_cap_pal_autocreate-message"></a>Messaggio WM \_ \_ CAP PAL \_ AUTOCREATE

Il **messaggio WM CAP PAL \_ \_ \_ AUTOCREATE** richiede al driver di acquisizione di campionare fotogrammi video e di creare automaticamente una nuova tavolozza. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capPaletteAuto.**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto)


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*Iframe*
</dt> <dd>

Numero di fotogrammi da campionare.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Numero di colori nella tavolozza. Il valore massimo per questo parametro è 256.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

Se si verifica un errore e viene impostata una funzione di callback degli errori usando il messaggio [**WM CAP SET CALLBACK \_ \_ \_ \_ ERROR,**](wm-cap-set-callback-error.md) viene chiamata la funzione di callback degli errori.

## <a name="remarks"></a>Commenti

La sequenza video campionata deve includere tutti i colori desiderati nella tavolozza. Per ottenere il riquadro migliore, potrebbe essere necessario campionare l'intera sequenza anziché una parte di essa.

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

 

 





