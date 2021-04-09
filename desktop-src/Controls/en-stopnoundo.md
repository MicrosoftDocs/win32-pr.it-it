---
title: Codice di notifica EN_STOPNOUNDO (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che si è verificata un'azione per la quale il controllo non è in grado di allocare memoria sufficiente per mantenere lo stato di annullamento. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- Controlli di Windows per il codice di notifica EN_STOPNOUNDO
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121015"
---
# <a name="en_stopnoundo-notification-code"></a>\_Codice di notifica en STOPNOUNDO

Notifica alla finestra padre di un controllo Rich Edit che si è verificata un'azione per la quale il controllo non è in grado di allocare memoria sufficiente per mantenere lo stato di annullamento. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per continuare l'operazione di **annullamento** .

Restituisce un valore diverso da zero per arrestare l'operazione di **annullamento** .

## <a name="remarks"></a>Commenti

La finestra padre otterrà sempre un messaggio [**di \_ notifica WM**](wm-notify.md) per questo evento, ma non richiede una maschera di notifica inviata con [**em \_ SETEVENTMASK**](em-seteventmask.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[**\_notifica WM**](wm-notify.md)
</dt> </dl>

 

 





