---
title: Messaggio WM_ADSPROP_NOTIFY_APPLY (Adsprop. h)
description: Un'estensione della finestra delle proprietà del servizio Active Directory directory invia il \_ \_ \_ messaggio di richiesta di notifica di WM ADSPROP all'oggetto notifica se la pagina delle proprietà del gestore di applicazione PSN ha \_ esito positivo.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_APPLY Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302304"
---
# <a name="wm_adsprop_notify_apply-message"></a>\_Messaggio di \_ richiesta di notifica di WM ADSPROP \_

Un'estensione della finestra delle proprietà del servizio Active Directory directory invia il messaggio di **\_ richiesta di \_ notifica \_ di WM ADSPROP** all'oggetto notifica se la pagina delle proprietà del gestore di applicazione PSN ha \_ esito positivo.


```C++
WM_ADSPROP_NOTIFY_APPLY

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

Quando si aggiungono pagine allo snap-in MMC di gestione Active Directory, Active Directory finestre delle proprietà di MMC creano gli oggetti notifica mediante una chiamata alla funzione [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) , quindi passa l'handle dell'oggetto notifica a ogni pagina delle proprietà.

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

 

 





