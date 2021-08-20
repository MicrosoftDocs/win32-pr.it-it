---
title: TB_MAPACCELERATOR messaggio (Commctrl.h)
description: Determina l'ID del pulsante che corrisponde al carattere del tasto di scelta rapida specificato.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f905ccf5ea01e3c06cb87a160a44598c2c4a7790c972f4ee83b245e3ed5c0111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168085"
---
# <a name="tb_mapaccelerator-message"></a>MESSAGGIO \_ MAPACCELERATOR TB

Determina l'ID del pulsante che corrisponde al carattere del tasto di scelta rapida specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Carattere del tasto di scelta rapida.

</dd> <dt>

*lParam* \[ Cambio\]
</dt> <dd>

Puntatore a **un OGGETTO UINT.** In caso di esito positivo, in caso di esito positivo, questo parametro conterà l'ID del pulsante con *wParam* come carattere di tasti di scelta rapida.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se uno dei pulsanti ha *wParam* come carattere di scelta rapida oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ MAPACCELERATORW** (Unicode) e **TB \_ MAPACCELERATORA** (ANSI)<br/>       |



 

 





