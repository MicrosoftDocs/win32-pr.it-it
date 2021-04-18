---
title: '\_Req creda EAP \_ (Eaptypes. h)'
description: Archivia le credenziali di sicurezza EAP in una \_ struttura di matrice di campi di input di configurazione EAP \_ \_ \_ . | \_Req creda EAP \_ (Eaptypes. h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321620"
---
# <a name="eap_cred_req"></a>\_req creda EAP \_

La struttura della richiesta **EAP \_ cred \_** archivia le credenziali di sicurezza EAP in una struttura di [**matrice di campi di \_ input di configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

**\_req creda EAP \_**
</dt> <dd>

La struttura della richiesta **EAP \_ cred \_** archivia sia la vecchia che la nuova credenziale di sicurezza EAP a cui punta il parametro *pbUiData* della struttura di [**dati dell' \_ \_ interfaccia utente \_ di EAP Interactive**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il parametro *dwDataType* del tipo di [**\_ \_ \_ dati \_ dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di richiesta di credenziale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per supportare l'accesso Single Sign-on (SSO), viene utilizzata la struttura di **\_ \_ req creda EAP** .

La struttura di **\_ \_ req creda EAP** è identica alla struttura [**EAP \_ cred \_**](eap-cred-resp.md) .

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

[**\_creda \_ EAP**](eap-cred-resp.md)
</dt> <dt>

[**REQ di scadenza di EAP \_ cred \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**la \_ scadenza del credito EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**\_ \_ dati dell'interfaccia utente interattiva EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

