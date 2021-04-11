---
title: Messaggio STM_SETIMAGE (winuser. h)
description: Un'applicazione invia un \_ messaggio di immagine STM per associare una nuova immagine a un controllo statico.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- Controlli di Windows Message STM_SETIMAGE
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963889"
---
# <a name="stm_setimage-message"></a>\_Messaggio immagine STM

Un'applicazione invia un messaggio di **\_ Immagine STM** per associare una nuova immagine a un controllo statico.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il tipo di immagine da associare al controllo statico. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                                     | Significato                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**\_bitmap immagine**</dt> </dl>                | Bitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**\_cursore immagine**</dt> </dl>                | Cursore.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**\_ENHMETAFILE immagine**</dt> </dl> | Enhanced Metafile.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**\_icona immagine**</dt> </dl>                      | Icona.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'immagine da associare al controllo statico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per l'immagine associata in precedenza al controllo statico, se disponibile. in caso contrario, è **null**.

## <a name="remarks"></a>Commenti

Per associare un'immagine a un controllo statico, il controllo deve avere lo stile appropriato. La tabella seguente illustra lo stile necessario per ogni tipo di immagine.



| Tipo di immagine         | Stile del controllo statico |
|--------------------|----------------------|
| \_bitmap immagine      | \_bitmap SS           |
| \_cursore immagine      | \_icona SS             |
| \_ENHMETAFILE immagine | \_ENHMETAFILE SS      |
| \_icona immagine        | \_icona SS             |



 

> [!IMPORTANT]
>
> Nella versione 6 dei controlli Microsoft Win32, una bitmap passata a un controllo statico che utilizza il messaggio di **\_ Immagine STM** è la stessa bitmap restituita da un successivo messaggio di **\_ Immagine STM** . Il client è responsabile dell'eliminazione di tutte le bitmap inviate a un controllo statico.
>
> Con Windows XP, se la bitmap passata nel messaggio **di \_ Immagine STM** contiene pixel con un valore alfa diverso da zero, il controllo statico acquisisce una copia della bitmap. Questa bitmap copiata viene restituita dal successivo messaggio dell' **\_ Immagine STM** . Il codice client può rilevare in modo indipendente le bitmap passate al controllo statico, ma se non controlla e rilascia le bitmap restituite da messaggi di **\_ Immagine STM** , le bitmap vengono perse.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetImage STM \_**](stm-getimage.md)
</dt> </dl>

 

 





