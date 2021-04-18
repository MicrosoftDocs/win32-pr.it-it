---
title: '\_Creda EAP \_ (Eaptypes. h)'
description: Archivia le credenziali di sicurezza EAP in una \_ struttura di matrice di campi di input di configurazione EAP \_ \_ \_ . | \_Creda EAP \_ (Eaptypes. h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c2176377dbde0f7c02d2a7d8083ad1bcff9e71
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321200"
---
# <a name="eap_cred_resp"></a>\_creda \_ EAP

La struttura **EAP cred. consente \_ \_** di archiviare le credenziali di sicurezza EAP in una struttura di [**matrice di campi di \_ input di configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

**\_creda \_ EAP**
</dt> <dd>

Nella struttura **EAP \_ creda \_** è possibile archiviare sia la vecchia che la nuova credenziale di sicurezza EAP a cui punta il parametro *pbUiData* della struttura di [**\_ \_ \_ dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il parametro *dwDataType* del [**tipo di dati di EAP \_ Interactive \_ UI \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di risposta delle credenziali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per supportare single sign-on (SSO), viene usata la struttura **EAP \_ cred \_** .

La struttura di **EAP \_ creda \_** è identica alla struttura della richiesta [**EAP \_ cred \_**](eap-cred-req.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture supplicant EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**\_req creda EAP \_**](eap-cred-req.md)
</dt> <dt>

[**REQ di scadenza di EAP \_ cred \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**la \_ scadenza del credito EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**\_ \_ dati dell'interfaccia utente interattiva EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

