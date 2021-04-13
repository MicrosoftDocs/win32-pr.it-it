---
title: Costanti EAPHost (Eaptypes. h)
description: Visualizzare un elenco di costanti EAPHost (Eaptypes. h) usate dai metodi EAPHost e vedere i requisiti per l'uso.
ms.assetid: 56338B98-06E3-4CD3-B1CA-F8F45AA39566
topic_type:
- apiref
api_name:
- EAP_INTERACTIVE_UI_DATA_VERSION
- EAP_CREDENTIAL_VERSION
- EAPHOST_PEER_API_VERSION
- CERTIFICATE_HASH_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH
- EAP_UI_INPUT_FIELD_PROPS_DEFAULT
- EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT
- EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST
- EAP_UI_INPUT_FIELD_PROPS_READ_ONLY
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84704e59ed43466c47435f4804cb4dedc9c3a92d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399708"
---
# <a name="eaphost-constants"></a>Costanti EAPHost

Costanti utilizzate dai metodi EAPHost.

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**\_ \_ \_ versione dei dati dell'interfaccia utente interattiva EAP \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Versione dei dati dell'interfaccia utente interattiva EAP.


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**\_versione credenziale EAP \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Versione delle credenziali EAP fornite dall'utente.


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**\_versione dell' \_ API \_ peer EAPHOST**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Versione dell'API peer EAPHost.


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**\_lunghezza dell'hash del certificato \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Lunghezza dell'hash SHA1 del certificato.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**lunghezza massima del \_ \_ campo di input della configurazione EAP \_ \_ \_**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



Specifica la lunghezza massima supportata di un campo di input.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**\_lunghezza del \_ \_ valore del \_ campo di input \_ \_ Max EAP config**
</dt> <dd> <dl> <dt>

1024
</dt> <dt>



Specifica la lunghezza massima supportata di un campo di input.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**Proprietà del \_ campo di input dell'interfaccia utente EAP \_ \_ \_ \_ predefinite**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Windows Vista con SP1 o versione successiva: rappresenta il valore predefinito della proprietà per le voci dei campi di input visualizzate nell'interfaccia utente.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**\_ \_ \_ \_ impostazioni predefinite del campo di input di configurazione EAP \_**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Rappresenta il valore predefinito della proprietà per le voci dei campi di input della configurazione visualizzate nell'interfaccia utente.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**Proprietà del \_ campo di input dell'interfaccia utente EAP \_ \_ \_ \_ non \_ visualizzabili**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Windows Vista con SP1 o versione successiva: specifica che le voci dei campi di input non verranno visualizzate nell'interfaccia utente (ad esempio, una password o un numero PIN).


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**proprietà \_ del \_ campo di input configurazione EAP \_ \_ \_ non \_ visualizzabili**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Specifica che le voci dei campi di input della configurazione non verranno visualizzate nell'interfaccia utente (ad esempio, una password o un numero di PIN).


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**Proprietà del \_ campo di input dell'interfaccia utente EAP \_ \_ \_ \_ non \_ permanente**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



Windows Vista con SP1 o versione successiva: indica che il metodo EAP non memorizza nella cache i dati del campo. il supplicant deve memorizzare nella cache i dati del campo per il roaming.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**Proprietà del \_ campo di input dell'interfaccia utente EAP di \_ \_ \_ \_ sola lettura \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Windows Vista con SP1 o versione successiva: indica che il campo di input è di sola lettura e non può essere modificato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows 8\]<br/> |
| Server<br/> | \[Solo app desktop Windows Server 2012\]<br/> |



 

 





