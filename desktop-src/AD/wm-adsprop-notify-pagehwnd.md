---
title: WM_ADSPROP_NOTIFY_PAGEHWND messaggio (Adsprop.h)
description: Un'estensione della finestra delle proprietà del servizio directory Active Directory chiama ADsPropSetHwnd per informare l'oggetto notifica dell'handle della finestra della pagina delle proprietà.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEHWND message Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2835b4e0ff878b4c747f8c34b983beb3d66c550008a82ecadb2e5a23667abc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181732"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>Messaggio WM \_ ADSPROP \_ NOTIFY \_ PAGEHWND

Un'estensione della finestra delle proprietà del servizio directory Active Directory chiama [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) per informare l'oggetto notifica dell'handle della finestra della pagina delle proprietà. La **funzione ADsPropSetHwnd** invia il messaggio **WM \_ ADSPROP \_ NOTIFY \_ PAGEHWND** all'oggetto notifica, che informa l'oggetto notifica dell'handle della finestra della pagina delle proprietà.


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hNotifyObj* 
</dt> <dd>

Handle dell'oggetto notifica. Per ottenere questo handle, chiamare [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*hPage* 
</dt> <dd>

Handle di finestra della pagina delle proprietà.

</dd> <dt>

*ptzTitle* 
</dt> <dd>

Puntatore a un buffer **WCHAR** con terminazione NULL che contiene il titolo della pagina delle proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Un'estensione della finestra delle proprietà di Active Directory chiama in genere la [**funzione ADsPropSetHwnd durante**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) l'elaborazione [**del messaggio WM \_ INITDIALOG.**](../dlgbox/wm-initdialog.md)

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

[**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

