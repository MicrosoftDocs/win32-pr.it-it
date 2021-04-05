---
title: Messaggio CB_GETCUEBANNER (winuser. h)
description: Ottiene il testo del banner cue visualizzato nel controllo di modifica di una casella combinata. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro ComboBox GetCueBannerText.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- Controlli di Windows Message CB_GETCUEBANNER
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874050"
---
# <a name="cb_getcuebanner-message"></a>\_Messaggio GETCUEBANNER CB

Ottiene il testo del banner cue visualizzato nel controllo di modifica di una casella combinata. Inviare questo messaggio in modo esplicito o utilizzando la macro [**ComboBox \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Puntatore a un buffer di stringa Unicode che riceve il testo del banner cue. L'applicazione chiamante è responsabile dell'allocazione della memoria per il buffer. La dimensione del buffer deve essere uguale alla lunghezza della stringa del banner cue in **WCHAR**, più 1 per il **valore null** di terminazione **WCHAR**.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Dimensioni del buffer a cui punta *lpcwText* in **WCHAR**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 se l'operazione ha esito positivo o un valore di errore in caso contrario.

Se non è presente un testo del banner cue da ottenere, il valore restituito è 0. Se l'applicazione chiamante non riesce ad allocare un buffer o impostare *lParam* prima di inviare questo messaggio, può verificarsi un comportamento non definito e il valore restituito potrebbe non essere affidabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzionalità della casella combinata](combo-box-features.md)
</dt> </dl>

 

 





