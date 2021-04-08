---
title: Codice di notifica PGN_CALCSIZE (COMmctrl. h)
description: Inviato da un controllo cercapersone per ottenere le dimensioni di scorrimento della finestra contenuta.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- Controlli di Windows per il codice di notifica PGN_CALCSIZE
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741218"
---
# <a name="pgn_calcsize-notification-code"></a>\_Codice di notifica CALCSIZE di PGN

Inviato da un controllo cercapersone per ottenere le dimensioni di scorrimento della finestra contenuta. Queste dimensioni vengono utilizzate dal controllo pager per determinare la dimensione scorrevole della finestra contenuta. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) che contiene e riceve informazioni sul codice di notifica. Il membro **dwFlag** della struttura indica la dimensione da calcolare. A seconda del valore di **dwFlag**, è necessario inserire la dimensione desiderata nel membro **larghezza** o **altezza** della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





