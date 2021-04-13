---
title: Messaggio BM_GETIMAGE (winuser. h)
description: Recupera un handle per l'immagine (icona o bitmap) associata al pulsante.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- Controlli di Windows Message BM_GETIMAGE
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340972"
---
# <a name="bm_getimage-message"></a>\_Messaggio BM GETimage

Recupera un handle per l'immagine (icona o bitmap) associata al pulsante.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di immagine da associare al pulsante. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                      | Significato              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**\_bitmap immagine**</dt> </dl> | Bitmap.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**\_icona immagine**</dt> </dl>       | Un'icona.<br/>  |



 

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

**Riferimento**
</dt> <dt>

[**\_immagine BM**](bm-setimage.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Pulsanti](buttons.md)
</dt> </dl>

 

 





