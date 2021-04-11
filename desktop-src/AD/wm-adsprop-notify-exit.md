---
title: Messaggio WM_ADSPROP_NOTIFY_EXIT (Adsprop. h)
description: Un'estensione della finestra delle proprietà di Active Directory Invia il \_ \_ \_ messaggio di uscita di notifica di WM ADSPROP all'oggetto notifica quando l'oggetto notifica non è più necessario.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_EXIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964764"
---
# <a name="wm_adsprop_notify_exit-message"></a>\_Messaggio di \_ uscita notifica ADSPROP \_ WM

Un'estensione della finestra delle proprietà di Active Directory Invia il messaggio di **\_ uscita di \_ notifica \_ di WM ADSPROP** all'oggetto notifica quando l'oggetto notifica non è più necessario.


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle dell'oggetto notifica. Per ottenere questo handle, chiamare [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

L'oggetto notifica verrà eliminato in risposta a questo messaggio. Quando il messaggio è stato inviato, l'handle dell'oggetto notifica deve essere considerato non valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Messaggi in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





