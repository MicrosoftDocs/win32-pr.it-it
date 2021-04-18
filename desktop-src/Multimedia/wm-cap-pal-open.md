---
title: Messaggio di WM_CAP_PAL_OPEN (VFW. h)
description: Il \_ \_ \_ messaggio di apertura di WM Cap consente di caricare una nuova tavolozza da un file tavolozza e di passarla a un driver di acquisizione.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN messaggi multimediali di Windows
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
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301073"
---
# <a name="wm_cap_pal_open-message"></a>\_ \_ \_ Messaggio aperto WM Cap

Il messaggio di **\_ \_ \_ apertura di WM Cap** consente di caricare una nuova tavolozza da un file tavolozza e di passarla a un driver di acquisizione. I file della tavolozza usano in genere l'estensione del nome file. Alla pubblicazione. Un driver di acquisizione utilizza una tavolozza quando richiesto dal formato di immagine cifrato specificato. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) .


```C++
WM_CAP_PAL_OPEN 
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

 

 





