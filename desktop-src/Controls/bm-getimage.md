---
title: BM_GETIMAGE messaggio (Winuser.h)
description: Recupera un handle per l'immagine (icona o bitmap) associata al pulsante.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE di controllo Windows messaggio
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
ms.openlocfilehash: 4b98ede304499aa97d9129957aa69a0991dee98565ff7827cdad4d0c1a82f19b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921261"
---
# <a name="bm_getimage-message"></a>Messaggio \_ GETIMAGE BM

Recupera un handle per l'immagine (icona o bitmap) associata al pulsante.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di immagine da associare al pulsante. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                      | Significato              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**BITMAP \_ IMMAGINE**</dt> </dl> | Bitmap.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ICONA \_ IMMAGINE**</dt> </dl>       | Un'icona.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per l'immagine, se presente; in caso contrario, è **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**BM \_ SETIMAGE**](bm-setimage.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Pulsanti](buttons.md)
</dt> </dl>

 

 





