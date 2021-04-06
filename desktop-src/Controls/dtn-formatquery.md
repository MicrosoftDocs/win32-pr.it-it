---
title: Codice di notifica DTN_FORMATQUERY (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) per recuperare la dimensione massima consentita della stringa che verrà visualizzata in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- Controlli di Windows per il codice di notifica DTN_FORMATQUERY
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963808"
---
# <a name="dtn_formatquery-notification-code"></a>\_Codice di notifica FORMATQUERY di DTN

Inviato da un controllo di selezione data e ora (DTP) per recuperare la dimensione massima consentita della stringa che verrà visualizzata in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) contenente informazioni sul campo di callback. La struttura contiene una sottostringa che definisce un campo di callback e riceve la dimensione massima consentita della stringa che verrà visualizzata nel campo callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il proprietario del controllo deve calcolare la larghezza massima possibile del testo che verrà visualizzato nel campo callback, impostare il membro **szMax** della struttura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) e restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica prepara il controllo per la regolazione della dimensione massima della stringa che verrà visualizzata in un particolare campo di callback. Ciò consente al controllo di visualizzare correttamente l'output in qualsiasi momento, riducendo lo sfarfallio all'interno della visualizzazione del controllo. Per ulteriori informazioni sui campi di callback, vedere [campi callback](date-and-time-picker-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTN \_ FORMATQUERYW** (Unicode) e **DTN \_ FORMATQUERYA** (ANSI)<br/>           |



 

 





