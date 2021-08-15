---
title: EAP \_ CRED \_ RESP (Eaptypes.h)
description: Archivia le credenziali di sicurezza EAP all'interno di una struttura EAP \_ CONFIG \_ INPUT FIELD \_ \_ ARRAY. | EAP \_ CRED \_ RESP (Eaptypes.h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b9bda55ed1b4aee9a9847740b25d46418c6ec3544dfdd6ba71b2c282042b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904638"
---
# <a name="eap_cred_resp"></a>EAP \_ CRED \_ RESP

La **struttura EAP \_ CRED \_ RESP** archivia le credenziali di sicurezza EAP all'interno di [**una struttura EAP CONFIG INPUT \_ FIELD \_ \_ \_ ARRAY.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

**EAP \_ CRED \_ RESP**
</dt> <dd>

La struttura **EAP \_ CRED \_ RESP** archivia sia le credenziali di sicurezza EAP nuove che le credenziali di sicurezza nuove a cui punta il *parametro pbUiData* della struttura [**EAP \_ INTERACTIVE UI \_ \_ DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il *parametro dwDataType* di [**EAP INTERACTIVE UI DATA \_ \_ \_ \_ TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di risposta delle credenziali.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura EAP \_ CRED \_ RESP** viene usata per supportare l'accesso Single Sign-On (SSO).

La **struttura \_ EAP CRED \_ RESP** è identica alla [**struttura \_ \_ REQ CRED EAP.**](eap-cred-req.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture supplicant EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**EAP \_ CRED \_ REQ**](eap-cred-req.md)
</dt> <dt>

[**EAP \_ CRED \_ EXPIRY \_ REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**DATI \_ DELL'INTERFACCIA \_ UTENTE INTERATTIVA EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

