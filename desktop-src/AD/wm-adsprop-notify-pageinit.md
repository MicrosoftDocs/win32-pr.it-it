---
title: WM_ADSPROP_NOTIFY_PAGEINIT messaggio (Adsprop.h)
description: Un'estensione della finestra delle proprietà di Active Directory chiama ADsPropGetInitInfo per ottenere dati relativi all'oggetto directory a cui si applica l'estensione della finestra delle proprietà.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEINIT message Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcad6ed359edf195b2355920b08d6010597f33dbc0f4e3b1e4c2438c3841ca47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024209"
---
# <a name="wm_adsprop_notify_pageinit-message"></a>MESSAGGIO WM \_ ADSPROP \_ NOTIFY \_ PAGEINIT

Un'estensione della finestra delle proprietà di Active Directory chiama [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) per ottenere dati relativi all'oggetto directory a cui si applica l'estensione della finestra delle proprietà. La **funzione ADsPropGetInitInfo** invia il messaggio **WM \_ ADSPROP \_ NOTIFY \_ PAGEINIT** all'oggetto notifica per ottenere questo risultato.


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle dell'oggetto notifica. Si tratta del *parametro hNotifyObject* ottenuto da una chiamata ad [**ADsPropCreateNotifyObj.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)

</dd> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*pADsPropInitParams* 
</dt> <dd>

Puntatore a [**una struttura ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) che riceve le informazioni sull'oggetto directory. Si tratta del *parametro pInitParams* passato [**ad ADsPropCreateNotifyObj.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non ha alcun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





