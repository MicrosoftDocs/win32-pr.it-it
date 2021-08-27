---
title: EAP \_ CRED \_ LOGON \_ REQ (Eaptypes.h)
description: Archivia le credenziali di sicurezza EAP all'interno di una struttura EAP \_ CONFIG \_ INPUT FIELD \_ \_ ARRAY.
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719abbed6c16deb6d3bfd61811f3f24253181364fe89f5823ee682bafef001e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785624"
---
# <a name="eap_cred_logon_req"></a>EAP \_ CRED \_ LOGON \_ REQ

La **struttura EAP \_ CRED LOGON \_ \_ REQ** archivia le credenziali di sicurezza EAP all'interno di [**una struttura EAP CONFIG INPUT \_ FIELD \_ \_ \_ ARRAY.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**EAP \_ CRED \_ LOGON \_ REQ**
</dt> <dd>

La struttura **EAP \_ CRED \_ LOGON \_ REQ** archivia le credenziali di sicurezza EAP a cui punta il *parametro pbUiData* della struttura [**EAP INTERACTIVE UI \_ \_ \_ DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il *parametro dwDataType* di [**EAP INTERACTIVE UI DATA \_ \_ \_ \_ TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di richiesta di credenziali. I campi di input in questa struttura sono gli stessi dei campi di input restituiti da [**EapHostPeerQueryCredentialInputFields.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) **EAP \_ CRED \_ LOGON \_ REQ** viene usato nella richiesta di credenziali iniziale e [**EAP \_ CRED \_ REQ**](eap-cred-req.md) viene usato nella richiesta di ripetizione dei tentativi delle credenziali durante un'autenticazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura EAP \_ CRED LOGON \_ \_ REQ** viene usata per supportare l'accesso Single Sign-On (SSO).

La **struttura EAP \_ CRED LOGON \_ \_ REQ** è identica alla [**struttura EAP \_ CRED LOGON \_ \_ RESP.**](eap-cred-logon-resp.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MATRICE DI \_ CAMPI DI INPUT DI \_ \_ CONFIGURAZIONE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**EAP \_ CRED \_ REQ**](eap-cred-req.md)
</dt> <dt>

[**DATI \_ DELL'INTERFACCIA \_ UTENTE INTERATTIVA EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**TIPO DI DATI \_ \_ DELL'INTERFACCIA \_ UTENTE INTERATTIVA \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





