---
title: Codice di notifica TBN_RESTORE (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che è in corso il ripristino di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- Controlli di Windows per il codice di notifica TBN_RESTORE
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478083"
---
# <a name="tbn_restore-notification-code"></a>\_Codice di notifica del ripristino TBN

Notifica alla finestra padre di una barra degli strumenti che è in corso il ripristino di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione deve restituire zero in risposta al primo codice di notifica del **\_ ripristino di TBN** ricevuto all'inizio del processo di ripristino per continuare a ripristinare le informazioni sul pulsante. Se l'applicazione restituisce un valore diverso da zero, il processo di ripristino viene annullato.

## <a name="remarks"></a>Commenti

L'applicazione riceverà il codice di notifica una volta all'inizio del processo di ripristino e una volta per ogni pulsante. Questo codice di notifica consente di estrarre le informazioni dal flusso di dati salvato in precedenza. Se non sono state salvate informazioni, ignorare il codice di notifica. Per una descrizione più dettagliata di come gestire il **\_ ripristino di TBN**, vedere [personalizzazione della barra degli strumenti](toolbar-controls-overview.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





