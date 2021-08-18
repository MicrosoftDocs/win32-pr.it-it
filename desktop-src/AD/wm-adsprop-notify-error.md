---
title: WM_ADSPROP_NOTIFY_ERROR messaggio (Adsprop.h)
description: Il messaggio WM ADSPROP NOTIFY ERROR aggiunge un messaggio di errore a un elenco di messaggi di errore visualizzati chiamando \_ \_ la funzione \_ ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_ERROR messaggio Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52f88cd4c60dcfcceed60ca644f7c59f65bee16e344cc17664e8b4be1ee18fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024289"
---
# <a name="wm_adsprop_notify_error-message"></a>MESSAGGIO \_ DI ERRORE NOTIFY WM ADSPROP \_ \_

Il **messaggio WM \_ ADSPROP \_ NOTIFY \_ ERROR** aggiunge un messaggio di errore a un elenco di messaggi di errore visualizzati chiamando la [**funzione ADsPropShowErrorDialog.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle dell'oggetto notifica. Si tratta del *parametro hNotifyObject* ottenuto da [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) che contiene i dati del messaggio di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

La [**funzione ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) è il metodo preferito per inviare questo messaggio.

I messaggi di errore aggiunti dal messaggio **WM \_ ADSPROP \_ NOTIFY \_ ERROR** vengono accumulati fino a quando non viene [**chiamato ADsPropShowErrorDialog.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) **ADsPropShowErrorDialog** combina e visualizza i messaggi di errore accumulati. Quando la finestra di dialogo di errore viene chiusa, i messaggi di errore accumulati vengono eliminati.

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

[**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





