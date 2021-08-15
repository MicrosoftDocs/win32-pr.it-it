---
title: WM_ADSPROP_NOTIFY_APPLY messaggio (Adsprop.h)
description: Un'estensione della finestra delle proprietà del servizio directory Active Directory invia il messaggio WM ADSPROP NOTIFY APPLY all'oggetto notifica se il gestore PSN APPLY della pagina delle proprietà \_ \_ ha esito \_ \_ positivo.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_APPLY message Active Directory
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
ms.openlocfilehash: 6cc130a83aa77021e0be512d9b2ad27914b4c6be382c0290e082e1fbd67b8b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024299"
---
# <a name="wm_adsprop_notify_apply-message"></a>Messaggio WM \_ ADSPROP \_ NOTIFY \_ APPLY

Un'estensione della finestra delle proprietà del servizio directory Active Directory invia il messaggio **WM \_ ADSPROP \_ NOTIFY \_ APPLY** all'oggetto notifica se il gestore PSN APPLY della pagina delle proprietà \_ ha esito positivo.


```C++
WM_ADSPROP_NOTIFY_APPLY

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
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

Questo messaggio non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Quando si aggiungono pagine nello snap-in MMC di Active Directory Manager, le finestre delle proprietà mmc di Active Directory creano gli oggetti notifica tramite una chiamata alla funzione [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) e quindi passano l'handle dell'oggetto notifica a ogni pagina delle proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Messaggi in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





