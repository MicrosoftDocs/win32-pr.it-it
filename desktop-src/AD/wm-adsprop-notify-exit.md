---
title: WM_ADSPROP_NOTIFY_EXIT messaggio (Adsprop.h)
description: Un'estensione della finestra delle proprietà di Active Directory invia il messaggio WM ADSPROP NOTIFY EXIT all'oggetto notifica quando \_ l'oggetto notifica non è più \_ \_ necessario.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_EXIT message Active Directory
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
ms.openlocfilehash: 6e144bb0b24112cabe1a806d4c746aac07708443665c0f457df8756be36d80b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181965"
---
# <a name="wm_adsprop_notify_exit-message"></a>MESSAGGIO DI USCITA DI WM \_ ADSPROP \_ NOTIFY \_

Un'estensione della finestra delle proprietà di Active Directory invia il messaggio **WM \_ ADSPROP \_ NOTIFY \_ EXIT** all'oggetto notifica quando l'oggetto notifica non è più necessario.


```C++
WM_ADSPROP_NOTIFY_EXIT

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

L'oggetto notifica verrà eliminato automaticamente in risposta a questo messaggio. Dopo l'invio di questo messaggio, l'handle dell'oggetto di notifica deve essere considerato non valido.

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

 

 





