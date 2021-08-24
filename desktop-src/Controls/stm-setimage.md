---
title: STM_SETIMAGE messaggio (Winuser.h)
description: Un'applicazione invia un messaggio SETIMAGE STM \_ per associare una nuova immagine a un controllo statico.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE dei controlli Windows messaggio
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
ms.openlocfilehash: d48cc8aeb5e28ac67a6bbe25636be1a2f6f9b89f225568be02e517e1ad04dc55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078455"
---
# <a name="stm_setimage-message"></a>Messaggio \_ SETIMAGE STM

Un'applicazione invia un **messaggio \_ SETIMAGE STM** per associare una nuova immagine a un controllo statico.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il tipo di immagine da associare al controllo statico. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                                     | Significato                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**BITMAP \_ IMMAGINE**</dt> </dl>                | Bitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**IMAGE \_ CURSOR**</dt> </dl>                | Cursore.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**IMAGE \_ ENHMETAFILE**</dt> </dl> | Metafile avanzato.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ICONA \_ IMMAGINE**</dt> </dl>                      | Icona.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'immagine da associare al controllo statico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle all'immagine precedentemente associata al controllo statico, se presente; in caso contrario, è **NULL.**

## <a name="remarks"></a>Commenti

Per associare un'immagine a un controllo statico, il controllo deve avere lo stile corretto. La tabella seguente illustra lo stile necessario per ogni tipo di immagine.



| Tipo di immagine         | Stile del controllo statico |
|--------------------|----------------------|
| BITMAP \_ IMMAGINE      | SS \_ BITMAP           |
| IMAGE \_ CURSOR      | ICONA \_ SS             |
| IMAGE \_ ENHMETAFILE | SS \_ ENHMETAFILE      |
| ICONA \_ IMMAGINE        | ICONA \_ SS             |



 

> [!IMPORTANT]
>
> Nella versione 6 dei controlli Microsoft Win32, una bitmap passata a un controllo statico usando il messaggio **\_ SETIMAGE STM** era la stessa bitmap restituita da un messaggio **\_ SETIMAGE STM** successivo. Il client è responsabile dell'eliminazione di qualsiasi bitmap inviata a un controllo statico.
>
> Con Windows XP, se la bitmap passata nel messaggio **\_ SETIMAGE STM** contiene pixel con alfa diverso da zero, il controllo statico accetta una copia della bitmap. Questa bitmap copiata viene restituita dal messaggio **\_ SETIMAGE STM** successivo. Il codice client può tenere traccia in modo indipendente delle bitmap passate al controllo statico, ma se non controlla e rilascia le bitmap restituite dai messaggi **\_ SETIMAGE STM,** le bitmap vengono persi.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**STM \_ GETIMAGE**](stm-getimage.md)
</dt> </dl>

 

 





