---
title: HDN_ITEMSTATEICONCLICK messaggio (Commctrl.h)
description: Notifica alla finestra padre di un controllo intestazione che l'utente ha fatto clic sull'icona di stato di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- HDN_ITEMSTATEICONCLICK dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cba2e475ec3037ab00c379cf0c9ea371d5a336b80458c68e974a7122d9a2427a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435251"
---
# <a name="hdn_itemstateiconclick-message"></a>Messaggio \_ HDN ITEMSTATEICONCLICK

Notifica alla finestra padre di un controllo intestazione che l'utente ha fatto clic sull'icona di stato di un elemento. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni aggiuntive sull'icona di stato su cui è stato fatto clic.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





