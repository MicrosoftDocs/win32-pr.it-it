---
title: DTN_FORMATQUERY codice di notifica (Commctrl.h)
description: Inviato da un controllo di selezione data e ora (DTP) per recuperare la dimensione massima consentita della stringa che verrà visualizzata in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY codice di notifica Windows controlli
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
ms.openlocfilehash: 14bd1a9efe22251aba71f157dfb2a68e2b0a70385c30564bb7f08e420e0c0cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019989"
---
# <a name="dtn_formatquery-notification-code"></a>Codice di notifica DTN \_ FORMATQUERY

Inviato da un controllo di selezione data e ora (DTP) per recuperare la dimensione massima consentita della stringa che verrà visualizzata in un campo di callback. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) contenente informazioni sul campo di callback. La struttura contiene una sottostringa che definisce un campo di callback e riceve la dimensione massima consentita della stringa che verrà visualizzata nel campo di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il proprietario del controllo deve calcolare la larghezza massima possibile del testo che verrà visualizzato nel campo di callback, impostare il membro **szMax** della struttura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) e restituire zero.

## <a name="remarks"></a>Commenti

La gestione di questo codice di notifica prepara il controllo per la regolazione delle dimensioni massime della stringa che verrà visualizzata in un particolare campo di callback. Ciò consente al controllo di visualizzare correttamente l'output in qualsiasi momento, riducendo lo sfarfallio all'interno della visualizzazione del controllo. Per altre informazioni sui campi di callback, vedere [Campi di callback.](date-and-time-picker-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTN \_ FORMATQUERYW** (Unicode) e **DTN \_ FORMATQUERYA** (ANSI)<br/>           |



 

 





