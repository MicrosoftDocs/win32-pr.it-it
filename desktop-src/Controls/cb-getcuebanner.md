---
title: CB_GETCUEBANNER messaggio (Winuser.h)
description: Ottiene il testo del banner di segnale visualizzato nel controllo di modifica di una casella combinata. Inviare questo messaggio in modo esplicito o usando la \_ macro ComboBox GetCueBannerText.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- CB_GETCUEBANNER di controllo Windows messaggio
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
ms.openlocfilehash: c81ddcd8123f28317726f412255f440d47f53310aa035ab34d25190658550163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089271"
---
# <a name="cb_getcuebanner-message"></a>CB \_ GETCUEBANNER message

Ottiene il testo del banner di segnale visualizzato nel controllo di modifica di una casella combinata. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ComboBox GetCueBannerText.**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer di stringa Unicode che riceve il testo del banner di segnale. L'applicazione chiamante è responsabile dell'allocazione della memoria per il buffer. La dimensione del buffer deve essere uguale alla lunghezza della stringa del banner di segnale nei **WCHAR**, più 1 per il carattere WCHAR **NULL** **di terminazione.**

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer a cui punta *lpcwText* nei **WCHAR.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 in caso di esito positivo oppure un valore di errore in caso contrario.

Se non è presente alcun testo del banner di segnale da ottenere, il valore restituito è 0. Se l'applicazione chiamante non riesce ad allocare un buffer o impostare *lParam* prima di inviare questo messaggio, potrebbe verificarsi un comportamento non definito e il valore restituito potrebbe non essere affidabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzionalità della casella combinata](combo-box-features.md)
</dt> </dl>

 

 





