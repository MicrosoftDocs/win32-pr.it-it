---
title: Messaggio STM_GETIMAGE (winuser. h)
description: Un'applicazione invia un \_ messaggio STM GetImage per recuperare un handle per l'immagine (icona o bitmap) associata a un controllo statico.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- Controlli di Windows Message STM_GETIMAGE
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047917"
---
# <a name="stm_getimage-message"></a>\_Messaggio GETIMAGE STM

Un'applicazione invia un messaggio **STM \_ GetImage** per recuperare un handle per l'immagine (icona o bitmap) associata a un controllo statico.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il tipo di immagine da recuperare. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                                     | Significato                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**\_bitmap immagine**</dt> </dl>                | Bitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**\_cursore immagine**</dt> </dl>                | Cursore.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**\_ENHMETAFILE immagine**</dt> </dl> | Enhanced Metafile.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**\_icona immagine**</dt> </dl>                      | Icona.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per l'immagine, se disponibile. in caso contrario, è **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Immagine STM**](stm-setimage.md)
</dt> </dl>

 

 





