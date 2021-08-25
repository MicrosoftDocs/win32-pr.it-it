---
title: TBN_SAVE di notifica (Commctrl.h)
description: Notifica alla finestra padre di una barra degli strumenti che è in corso il salvataggio di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f9d4fb40d0e5beafcd720b4de52a8cf09d17c3e4c6f7b4dcfa8da78e00e97ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876591"
---
# <a name="tbn_save-notification-code"></a>Codice di notifica \_ TBN SAVE

Notifica alla finestra padre di una barra degli strumenti che è in corso il salvataggio di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTBSAVE.**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'applicazione riceverà questo codice di notifica una volta all'inizio del processo di salvataggio e una volta per ogni pulsante. Questo codice di notifica offre la possibilità di aggiungere le proprie informazioni a quella salvata dalla shell. Se non si desidera aggiungere informazioni, ignorare il codice di notifica. Per [una descrizione più](toolbar-controls-overview.md) dettagliata di come gestire tBN SAVE, vedere Personalizzazione della barra degli \_ strumenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[TBN \_ RESTORE](tbn-restore.md)
</dt> </dl>

 

 





