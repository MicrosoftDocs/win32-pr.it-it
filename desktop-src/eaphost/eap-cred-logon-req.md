---
title: REQ di accesso di EAP \_ cred \_ \_ (Eaptypes. h)
description: Archivia le credenziali di sicurezza EAP in una \_ struttura di matrice di campi di input di configurazione EAP \_ \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048132"
---
# <a name="eap_cred_logon_req"></a>richiesta di accesso di EAP \_ cred \_ \_

La struttura di richiesta di **accesso di EAP \_ cred \_ \_** archivia le credenziali di sicurezza EAP in una struttura di matrice di campi di [**input di \_ configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**richiesta di accesso di EAP \_ cred \_ \_**
</dt> <dd>

La struttura di **req di accesso di EAP \_ \_ \_ cred** archivia le credenziali di sicurezza EAP a cui punta il parametro *pbUiData* della struttura di [**\_ \_ \_ dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il parametro *dwDataType* del tipo di [**\_ \_ \_ dati \_ dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di richiesta di credenziale. I campi di input in questa struttura sono gli stessi dei campi di input restituiti da [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **EAP \_ La richiesta di \_ accesso cred \_** viene usata nella richiesta di credenziali iniziale e la richiesta [**EAP \_ creda \_**](eap-cred-req.md) viene usata nella richiesta di ripetizione delle credenziali durante l'autenticazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per supportare l'accesso Single Sign-on (SSO), viene usata la struttura di **\_ req di \_ accesso \_ di EAP cred** .

La struttura della richiesta di **accesso di EAP \_ cred \_ \_** è identica alla struttura di [**\_ \_ accesso \_ resp di EAP cred**](eap-cred-logon-resp.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_matrice di \_ campi di input configurazione \_ EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**\_req creda EAP \_**](eap-cred-req.md)
</dt> <dt>

[**\_ \_ dati dell'interfaccia utente interattiva EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**\_tipo di \_ dati dell'interfaccia utente interattiva EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





