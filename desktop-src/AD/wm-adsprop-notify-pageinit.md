---
title: Messaggio WM_ADSPROP_NOTIFY_PAGEINIT (Adsprop. h)
description: Un'estensione della finestra delle proprietà Active Directory chiama ADsPropGetInitInfo per ottenere i dati relativi all'oggetto directory a cui viene applicata l'estensione della finestra delle proprietà.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_PAGEINIT Active Directory
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
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517601"
---
# <a name="wm_adsprop_notify_pageinit-message"></a>WM \_ ADSPROP \_ notifica \_ PAGEINIT messaggio

Un'estensione della finestra delle proprietà Active Directory chiama [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) per ottenere i dati relativi all'oggetto directory a cui viene applicata l'estensione della finestra delle proprietà. La funzione **ADsPropGetInitInfo** invia il messaggio **WM \_ ADSPROP \_ Notify \_ PAGEINIT** all'oggetto notifica per ottenere questo risultato.


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle dell'oggetto notifica. Si tratta del parametro *hNotifyObject* ottenuto da una chiamata a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*pADsPropInitParams* 
</dt> <dd>

Puntatore a una struttura [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) che riceve le informazioni sull'oggetto directory. Si tratta del parametro *pInitParams* passato a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi in Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





