---
title: Codice di notifica DL_CANCELDRAG (COMmctrl. h)
description: Segnala che l'utente ha annullato un'operazione di trascinamento facendo clic con il pulsante destro del mouse o premendo il tasto ESC.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- Controlli di Windows per il codice di notifica DL_CANCELDRAG
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121778"
---
# <a name="dl_canceldrag-notification-code"></a>\_Codice di notifica CANCELDRAG DL

Segnala che l'utente ha annullato un'operazione di trascinamento facendo clic con il pulsante destro del mouse o premendo il tasto ESC. Una casella di riepilogo di trascinamento Invia questo codice di notifica alla finestra padre sotto forma di messaggio elenco di trascinamento. Per ulteriori informazioni, vedere [trascinare i messaggi della casella di riepilogo](about-list-boxes.md).


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il \_ codice di notifica CANCELDRAG DL, l'handle per la casella di riepilogo di trascinamento e la posizione del cursore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Elaborando il \_ codice di notifica CANCELDRAG di DL, un'applicazione può reimpostare lo stato interno per indicare che il trascinamento non è attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





