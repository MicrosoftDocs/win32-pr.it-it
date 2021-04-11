---
title: Messaggio WM_ADSPROP_NOTIFY_PAGEHWND (Adsprop. h)
description: Un'estensione della finestra delle proprietà del servizio Active Directory directory chiama ADsPropSetHwnd per informare l'oggetto notifica dell'handle della finestra della pagina delle proprietà.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_PAGEHWND Active Directory
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
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121062"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>WM \_ ADSPROP \_ notifica \_ PAGEHWND messaggio

Un'estensione della finestra delle proprietà del servizio Active Directory directory chiama [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) per informare l'oggetto notifica dell'handle della finestra della pagina delle proprietà. La funzione **ADsPropSetHwnd** invia il messaggio di notifica **\_ \_ \_ PAGEHWND di WM ADSPROP** all'oggetto notifica, che informa l'oggetto notifica dell'handle della finestra della pagina delle proprietà.


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

Puntatore a un buffer **WCHAR** con terminazione null che contiene il titolo della pagina delle proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Un'estensione della finestra delle proprietà Active Directory in genere chiama la funzione [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) durante l'elaborazione del messaggio [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) .

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

[**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**\_INITDIALOG WM**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

