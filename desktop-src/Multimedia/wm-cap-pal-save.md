---
title: WM_CAP_PAL_SAVE messaggio (Vfw.h)
description: Il messaggio WM \_ CAP PAL SAVE salva il riquadro corrente in un file del \_ \_ riquadro. I file di tavolozza usano in genere l'estensione del nome file . amico. È possibile inviare questo messaggio in modo esplicito o usando la macro capPaletteSave.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- WM_CAP_PAL_SAVE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff8703eafcc3c612fbde5bac7d15433758aa3d6ee44ab47697ffb25f9324dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891881"
---
# <a name="wm_cap_pal_save-message"></a>Messaggio DI SALVATAGGIO DI WM \_ \_ CAP PAL \_

Il **messaggio WM CAP PAL \_ \_ \_ SAVE** salva il riquadro corrente in un file del riquadro. I file di tavolozza usano in genere l'estensione del nome file . amico. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capPaletteSave.**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave)


```C++
WM_CAP_PAL_SAVE 
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

 

 





