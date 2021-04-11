---
title: Codice di notifica TBN_GETOBJECT (COMmctrl. h)
description: Inviato da un controllo Toolbar che usa lo \_ stile REGISTERDROP TBSTYLE per richiedere un oggetto destinazione di rilascio quando il puntatore passa su uno dei pulsanti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- Controlli di Windows per il codice di notifica TBN_GETOBJECT
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118966"
---
# <a name="tbn_getobject-notification-code"></a>TBN \_ codice di notifica GETobject

Inviato da un controllo Toolbar che usa lo [**stile \_ REGISTERDROP TBSTYLE**](toolbar-control-and-button-styles.md) per richiedere un oggetto destinazione di rilascio quando il puntatore passa su uno dei pulsanti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) contenente informazioni sul pulsante passato dal puntatore e che riceve i dati forniti dall'applicazione in risposta a questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'elaborazione dell'applicazione del codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

Per fornire un oggetto, un'applicazione deve impostare i valori in alcuni membri della struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) in *lParam*. Il membro **pObject** deve essere impostato su un puntatore a un oggetto valido e il membro **HRESULT** deve essere impostato su un flag Success. Per rispettare gli standard Component Object Model (COM), incrementare sempre il conteggio dei riferimenti dell'oggetto quando viene fornito un puntatore a un oggetto.

Se un'applicazione non fornisce un oggetto, deve impostare **pObject** su **null** e **HRESULT** su un flag di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





