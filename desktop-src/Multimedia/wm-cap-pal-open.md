---
title: WM_CAP_PAL_OPEN messaggio (Vfw.h)
description: Il messaggio WM CAP PAL OPEN carica una nuova tavolozza da un \_ file della tavolozza e la passa a un driver di \_ \_ acquisizione.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29cb831ca0128b0562d6ee53b8e66309d2e1dbd91803dab13202dc4a6723bfa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800580"
---
# <a name="wm_cap_pal_open-message"></a>Messaggio WM \_ CAP \_ PAL \_ OPEN

Il **messaggio WM CAP PAL \_ \_ \_ OPEN** carica una nuova tavolozza da un file della tavolozza e la passa a un driver di acquisizione. I file del riquadro usano in genere l'estensione del nome file . amico. Un driver di acquisizione usa una tavolozza quando richiesto dal formato di immagine digitalizzato specificato. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capPaletteOpen.**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen)


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il nome del file del riquadro.

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

 

 





