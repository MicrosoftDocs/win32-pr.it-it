---
title: WM_CAP_PAL_PASTE messaggio (Vfw.h)
description: Il messaggio WM CAP PAL PASTE copia il riquadro dagli \_ Appunti e lo passa a un driver di \_ \_ acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro capPalettePaste.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- WM_CAP_PAL_PASTE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bedb760a444abe9b0667592855d701dc24a02b8ee57ea15ab30912a5e216d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686831"
---
# <a name="wm_cap_pal_paste-message"></a>Messaggio \_ WM CAP PAL \_ \_ PASTE

Il **messaggio WM CAP PAL \_ \_ \_ PASTE** copia il riquadro dagli Appunti e lo passa a un driver di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capPalettePaste.**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste)


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

Se si verifica un errore e viene impostata una funzione di callback degli errori usando il messaggio [**WM CAP SET CALLBACK \_ \_ \_ \_ ERROR,**](wm-cap-set-callback-error.md) viene chiamata la funzione di callback degli errori.

## <a name="remarks"></a>Commenti

Un driver di acquisizione usa una tavolozza quando richiesto dal formato video digitalizzato specificato.

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

 

 





