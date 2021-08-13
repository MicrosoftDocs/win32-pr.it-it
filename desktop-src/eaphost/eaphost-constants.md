---
title: Costanti EAPHost (Eaptypes.h)
description: Visualizzare un elenco di costanti EAPHost (Eaptypes.h) usate dai metodi EAPHost e vedere i requisiti per l'uso.
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
ms.openlocfilehash: ab336b147557722f1bec72bfe662b12599a64ee1622b31bdad6a92a05af6d92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119483011"
---
# <a name="eaphost-constants"></a>Costanti EAPHost

Costanti utilizzate dai metodi EAPHost.

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**VERSIONE DEI DATI \_ \_ DELL'INTERFACCIA \_ UTENTE INTERATTIVA \_ EAP**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Versione dei dati dell'interfaccia utente interattiva EAP.


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**VERSIONE CREDENZIALI EAP \_ \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Versione delle credenziali EAP fornite dall'utente.


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**VERSIONE \_ API PEER EAPHOST \_ \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Versione dell'API peer EAPHost.


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**LUNGHEZZA \_ HASH \_ CERTIFICATO**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Lunghezza dell'hash SHA1 del certificato.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**LUNGHEZZA \_ MASSIMA DEL CAMPO DI INPUT DI \_ \_ \_ CONFIGURAZIONE \_ EAP**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



Specifica la lunghezza massima supportata di un campo di input.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**MAX \_ EAP \_ CONFIG \_ INPUT \_ FIELD \_ VALUE \_ LENGTH**
</dt> <dd> <dl> <dt>

1024
</dt> <dt>



Specifica la lunghezza massima supportata di un campo di input.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**PROPRIETÀ DEI CAMPI \_ \_ DI INPUT \_ DELL'INTERFACCIA \_ UTENTE \_ EAP PREDEFINITE**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Windows Vista con SP1 o versione successiva: rappresenta il valore predefinito della proprietà per le voci dei campi di input visualizzate nell'interfaccia utente.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**PROPRIETÀ DEL CAMPO DI INPUT DI CONFIGURAZIONE EAP \_ \_ \_ \_ \_ PREDEFINITE**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Rappresenta il valore predefinito della proprietà per le voci dei campi di input di configurazione visualizzate nell'interfaccia utente.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**PROPRIETÀ DEI CAMPI \_ \_ DI INPUT \_ \_ DELL'INTERFACCIA UTENTE EAP \_ NON \_ VISUALIZZABILI**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Windows Vista con SP1 o versione successiva: specifica che le voci dei campi di input non verranno visualizzate nell'interfaccia utente,ad esempio una password o un numero PIN.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**PROPRIETÀ DEL CAMPO DI INPUT DI CONFIGURAZIONE EAP \_ \_ NON \_ \_ \_ \_ VISUALIZZABILI**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Specifica che le voci dei campi di input di configurazione non verranno visualizzate nell'interfaccia utente, ad esempio una password o un numero PIN.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**PROPRIETÀ DEI CAMPI \_ \_ DI INPUT \_ \_ DELL'INTERFACCIA UTENTE EAP \_ NON \_ PERSISTENTI**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



Windows Vista con SP1 o versione successiva: indica che il metodo EAP non memorizza nella cache i dati del campo. il supplicant deve memorizzare nella cache i dati dei campi per il roaming.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**PROPRIETÀ DI CAMPO \_ \_ DI INPUT \_ \_ DELL'INTERFACCIA UTENTE \_ \_ EAP DI SOLA LETTURA**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Windows Vista con SP1 o versione successiva: indica che il campo di input è di sola lettura e non può essere modificato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | \[Windows 8 solo app desktop\]<br/> |
| Server<br/> | \[Windows Server 2012 solo app desktop\]<br/> |



 

 





