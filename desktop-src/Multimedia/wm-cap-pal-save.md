---
title: Messaggio di WM_CAP_PAL_SAVE (VFW. h)
description: Il \_ \_ \_ messaggio di salvataggio di WM Cap salva la tavolozza corrente in un file tavolozza. I file della tavolozza usano in genere l'estensione del nome file. Alla pubblicazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capPaletteSave.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- WM_CAP_PAL_SAVE messaggi multimediali di Windows
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
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301821"
---
# <a name="wm_cap_pal_save-message"></a>\_Messaggio di \_ salvataggio del PAL WM Cap \_

Il messaggio di **\_ \_ \_ salvataggio di WM Cap** salva la tavolozza corrente in un file tavolozza. I file della tavolozza usano in genere l'estensione del nome file. Alla pubblicazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) .


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome file della tavolozza.

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

 

 





