---
title: Codice di notifica TBN_SAVE (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che è in corso il salvataggio di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- Controlli di Windows per il codice di notifica TBN_SAVE
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
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743802"
---
# <a name="tbn_save-notification-code"></a>TBN \_ salvare il codice di notifica

Notifica alla finestra padre di una barra degli strumenti che è in corso il salvataggio di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'applicazione riceverà il codice di notifica una volta all'inizio del processo di salvataggio e una volta per ogni pulsante. Questo codice di notifica consente di aggiungere le proprie informazioni a salvate dalla Shell. Se non si desidera aggiungere informazioni, ignorare il codice di notifica. Per una descrizione più dettagliata di come gestire TBN Salva, vedere [personalizzazione della barra degli strumenti](toolbar-controls-overview.md) \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_ripristino TBN](tbn-restore.md)
</dt> </dl>

 

 





