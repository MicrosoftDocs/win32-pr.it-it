---
title: Messaggio WM_ADSPROP_NOTIFY_ERROR (Adsprop. h)
description: Il messaggio di errore di notifica di WM \_ ADSPROP \_ \_ aggiunge un messaggio di errore a un elenco di messaggi di errore visualizzati chiamando la funzione ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_ERROR Active Directory
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
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119846"
---
# <a name="wm_adsprop_notify_error-message"></a>\_Messaggio di \_ errore di notifica di WM ADSPROP \_

Il messaggio di **errore di notifica di WM \_ \_ \_ ADSPROP** aggiunge un messaggio di errore a un elenco di messaggi di errore visualizzati chiamando la funzione [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle dell'oggetto notifica. Si tratta del parametro *hNotifyObject* ottenuto da [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) che contiene i dati del messaggio di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

La funzione [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) è il metodo preferito per l'invio di questo messaggio.

I messaggi di errore aggiunti dal messaggio di **errore di notifica di WM \_ \_ \_ ADSPROP** vengono accumulati fino a quando non viene chiamato [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) . **ADsPropShowErrorDialog** combina e Visualizza i messaggi di errore accumulati. Quando la finestra di dialogo di errore viene rilasciata, i messaggi di errore accumulati vengono eliminati.

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

[**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





