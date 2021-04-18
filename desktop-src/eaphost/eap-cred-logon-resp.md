---
title: '\_ \_ Accesso resp EAP \_ (Eaptypes. h)'
description: Archivia le credenziali di sicurezza EAP in una \_ struttura di matrice di campi di input di configurazione EAP \_ \_ \_ . | \_ \_ Accesso resp EAP \_ (Eaptypes. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321621"
---
# <a name="eap_cred_logon_resp"></a>\_ \_ accesso \_ resp EAP

La struttura di **\_ \_ accesso \_ resp EAP di EAP** archivia le credenziali di sicurezza EAP in una struttura di matrice di [**\_ campi di input di configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

**\_ \_ accesso \_ resp EAP**
</dt> <dd>

La struttura di **\_ \_ accesso \_ resp di EAP** consente di archiviare le credenziali di sicurezza EAP a cui punta il parametro *pbUiData* della struttura di [**\_ \_ \_ dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il parametro *dwDataType* del [**tipo di \_ \_ \_ dati \_ dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di richiesta di credenziale. I campi di input in questa struttura saranno uguali ai campi di input restituiti da [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **EAP \_ Il valore di \_ accesso cred \_** viene usato nella richiesta di credenziali iniziale e il valore [**EAP \_ cred \_**](eap-cred-resp.md) è usato nella richiesta di ripetizione delle credenziali durante l'autenticazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per supportare single sign-on (SSO) viene utilizzata la struttura di **\_ \_ accesso \_ resp EAP** .

La struttura di **\_ \_ accesso \_ resp di EAP creda** è identica alla struttura di [**\_ \_ \_ req di accesso di EAP cred**](eap-cred-logon-req.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[**\_matrice di \_ campi di input configurazione \_ EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**richiesta di accesso di EAP \_ cred \_ \_**](eap-cred-logon-req.md)
</dt> <dt>

[**\_ \_ dati dell'interfaccia utente interattiva EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**\_tipo di \_ dati dell'interfaccia utente interattiva EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





