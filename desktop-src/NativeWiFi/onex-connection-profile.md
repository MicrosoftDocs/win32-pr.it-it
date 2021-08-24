---
description: Contiene informazioni sul profilo di connessione 802.1X attualmente usato per l'autenticazione 802.1X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: ONEX_CONNECTION_PROFILE struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500e714b6f0728104987f53ff0a8c0e7083c1af5996679a78a986b5674d54514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684891"
---
# <a name="onex_connection_profile-structure"></a>Struttura ONEX \_ CONNECTION \_ PROFILE

La **struttura ONEX \_ CONNECTION \_ PROFILE** contiene informazioni sul profilo di connessione 802.1X attualmente usato per l'autenticazione 802.1X.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Versione di questa **struttura ONEX \_ CONNECTION \_ PROFILE.**

</dd> <dt>

**dwTotalLen**
</dt> <dd>

Lunghezza, in byte, della struttura **ONEX \_ CONNECTION \_ PROFILE.**

</dd> <dt>

**fOneXSupplicantFlags**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro dwOneXSupplicantFlags.**

</dd> <dt>

**fsupplicantMode**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro supplicantMode.**

</dd> <dt>

**fauthMode**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro authMode.**

</dd> <dt>

**fHeldPeriod**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro dwHeldPeriod.**

</dd> <dt>

**fAuthPeriod**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro dwAuthPeriod.**

</dd> <dt>

**fStartPeriod**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro dwStartPeriod.**

</dd> <dt>

**fMaxStart**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro dwMaxStart.**

</dd> <dt>

**fMaxAuthFailures**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro dwMaxAuthFailures.**

</dd> <dt>

**fNetworkAuthTimeout**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro dwNetworkAuthTimeout.**

</dd> <dt>

**fAllowLogonDialogs**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro bAllowLogonDialogs.**

</dd> <dt>

**fNetworkAuthWithUITimeout**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro dwNetworkAuthWithUITimeout.**

</dd> <dt>

**fUserBasedVLan**
</dt> <dd>

Indica se la **struttura ONEX \_ CONNECTION \_ PROFILE** contiene dati validi nel **membro bUserBasedVLan.**

</dd> <dt>

**dwOneXSupplicantFlags**
</dt> <dd>

Set di flag 802.1X che possono essere presenti nel profilo. Questi flag sono riservati per l'uso interno da parte del modulo di autenticazione 802.1X.

</dd> <dt>

**supplicantMode**
</dt> <dd>

Elemento supplicantMode nello schema 802.1X che specifica il metodo di trasmissione usato per EAPOL-Start messaggi. Per altre informazioni, vedere l'elemento [**supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md) nello schema 802.1X.



| Valore                                                                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt> </dl> | EAPOL-Start messaggi non vengono trasmessi. Valido solo per i profili LAN cablati.<br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt> </dl>                                                         | Il client determina quando inviare EAPOL-Start pacchetti in base alla funzionalità di rete. EAPOL-Start messaggi vengono inviati solo quando necessario. Valido solo per i profili LAN cablati.<br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt> </dl>                                         | EAPOL-Start messaggi vengono trasmessi come specificato da 802.1X. Valido per i profili LAN cablati e wireless.<br/>                                                             |



 

</dd> <dt>

**Authmode**
</dt> <dd>

Elemento authMode nello schema 802.1X che specifica il tipo di credenziali usate per l'autenticazione 802.1X. Per altre informazioni, vedere [**l'elemento authMode (OneX)**](onexschema-authmode-onex-element.md) nello schema 802.1X.



| Valore                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt> </dl> | Usare le credenziali del computer o dell'utente. Quando un utente è connesso, le credenziali dell'utente vengono usate per l'autenticazione. Quando nessun utente è connesso, vengono usate le credenziali del computer.<br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt> </dl>         | Usare solo le credenziali del computer.<br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt> </dl>                     | Usare solo le credenziali utente.<br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <dt>**OneXAuthModeGuest**</dt> <dt>3</dt> </dl>                                 | Usare solo credenziali guest (vuote).<br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt> </dl>         | Le credenziali da utilizzare non sono specificate.<br/>                                                                                                                                   |



 

</dd> <dt>

**dwHeldPeriod**
</dt> <dd>

Elemento heldPeriod nello schema 802.1X che specifica l'intervallo di tempo, in secondi, durante il quale un client non tenterà nuovamente l'autenticazione dopo un tentativo di autenticazione non riuscito. Per altre informazioni, vedere [**l'elemento heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md) nello schema 802.1X.

</dd> <dt>

**dwAuthPeriod**
</dt> <dd>

Elemento authPeriod nello schema 802.1X che specifica la durata massima, in secondi, in cui un client attende una risposta dall'autenticatore. Se una risposta non viene ricevuta entro il periodo specificato, il client presuppone che nella rete non sia presente alcun autenticatore. Per altre informazioni, vedere [**l'elemento authPeriod (OneX)**](onexschema-authperiod-onex-element.md) nello schema 802.1X.

</dd> <dt>

**dwStartPeriod**
</dt> <dd>

Elemento startPeriod nello schema 802.1X che specifica l'intervallo di tempo, in secondi, di attesa prima dell'invio EAPOL-Start un'istanza. Viene EAPOL-Start un messaggio di errore per avviare il processo di autenticazione 802.1X. Per altre informazioni, vedere [**l'elemento startPeriod (OneX)**](onexschema-startperiod-onex-element.md) nello schema 802.1X.

</dd> <dt>

**dwMaxStart**
</dt> <dd>

Elemento maxStart nello schema 802.1X che specifica il numero massimo di EAPOL-Start inviati. Dopo l'invio EAPOL-Start numero massimo di messaggi, il client presuppone che nella rete non sia presente alcun autenticatore. Per altre informazioni, vedere [**l'elemento maxStart (OneX)**](onexschema-maxstart-onex-element.md) nello schema 802.1X.

</dd> <dt>

**dwMaxAuthFailures**
</dt> <dd>

Elemento maxAuthFailures nello schema 802.1X che specifica il numero massimo di errori di autenticazione consentiti per un set di credenziali. Per altre informazioni, vedere [**l'elemento maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) nello schema 802.1X.

</dd> <dt>

**dwNetworkAuthTimeout**
</dt> <dd>

Tempo di attesa, in secondi, per il completamento dell'autenticazione 802.1X prima che l'accesso normale proceda. Questo valore viene usato in scenari single sign-on (SSO). Il valore predefinito è 10 secondi in un profilo 802.1X. Per altre informazioni, vedere [**l'elemento maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md) nello schema 802.1X.

</dd> <dt>

**dwNetworkAuthWithUITimeout**
</dt> <dd>

Durata massima, in secondi, di attesa di una connessione nel caso in cui una finestra di dialogo dell'interfaccia utente che richiede l'input dell'utente sia visualizzata durante l'accesso SSO per accesso.

In Windows Vista con SP1 e versioni successive, questo valore è hardcoded a 10 minuti e non è configurabile. In Windows Vista Release to Manufacturing questo valore predefinito è 60 secondi in un profilo 802.1X ed è stato controllato dall'elemento **maxDelayWithAdditionalDialogs** nello schema.

In Windows Vista con SP1 e versioni successive, l'elemento **maxDelayWithAdditionalDialogs** nello schema 802.1X viene ignorato e deprecato.

</dd> <dt>

**bAllowLogonDialogs**
</dt> <dd>

Valore che specifica se consentire la visualizzazione delle finestre di dialogo EAP quando si usa l'accesso SSO pre-accesso. Per altre informazioni, vedere **l'elemento allowAdditionalDialogs** nello schema 802.1X.

</dd> <dt>

**bUserBasedVLan**
</dt> <dd>

Elemento userBasedVirtualLan nello schema 802.1X che specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente. Alcuni dispositivi NAS (Network Access Server) modificano la VLAN dopo l'autenticazione di un utente. Quando userBasedVirtualLan è TRUE, il nas può modificare la VLAN di un dispositivo dopo l'autenticazione di un utente. Per altre informazioni, vedere [**l'elemento userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) nello schema 802.1X.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura ONEX \_ CONNECTION \_ PROFILE** viene usata dal modulo 802.1X, un nuovo componente di configurazione wireless supportato in Windows Vista e versioni successive.

[**ONEX \_ RESULT UPDATE DATA \_ \_ contiene**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) informazioni su una modifica dello stato all'autenticazione 802.1X. La struttura **ONEX \_ RESULT UPDATE \_ \_ DATA** viene restituita quando il membro **NotificationSource** della struttura [**WLAN NOTIFICATION \_ \_ DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) è **WLAN \_ NOTIFICATION SOURCE \_ \_ ONEX** e il membro **NotificationCode** della struttura **WLAN NOTIFICATION \_ \_ DATA** per la notifica ricevuta è **OneXNotificationTypeResultUpdate.** Per questa notifica, il membro **pData** della struttura **WLAN \_ NOTIFICATION \_ DATA** punta a una struttura **ONEX \_ RESULT UPDATE \_ \_ DATA** contenente informazioni sulla modifica dello stato di autenticazione 802.1X.

Se il membro **fOneXAuthParams** nella struttura [**ONEX \_ RESULT UPDATE \_ \_ DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) è impostato, il membro **authParams** della struttura **ONEX RESULT UPDATE \_ \_ \_ DATA** contiene una struttura [**ONEX VARIABLE \_ \_ BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) con una struttura [**ONEX \_ AUTH \_ PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) incorporata a partire dal membro **dwOffset** del **BLOB ONEX \_ VARIABLE. \_** Il **membro oneXConnProfile** della struttura **ONEX \_ AUTH \_ PARAMS** contiene una struttura **ONEX VARIABLE \_ \_ BLOB** con una struttura **ONEX CONNECTION \_ \_ PROFILE** incorporata a partire dal membro **dwOffset** di **ONEX VARIABLE \_ \_ BLOB.**

La **struttura ONEX \_ CONNECTION \_ PROFILE** non è definita in un file di intestazione pubblico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sull'architettura di ACM](about-the-acm-architecture.md)
</dt> <dt>

[OneX Schema](onexschema-schema.md)
</dt> <dt>

[**Elemento authMode (OneX)**](onexschema-authmode-onex-element.md)
</dt> <dt>

[**Elemento authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
</dt> <dt>

[**Elemento heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[**Elemento maxStart (OneX)**](onexschema-maxstart-onex-element.md)
</dt> <dt>

[**Elemento startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
</dt> <dt>

[**Elemento supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[**Elemento userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[**ONEX \_ AUTH \_ PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[**TIPO DI \_ NOTIFICA \_ ONEX**](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[**DATI DI AGGIORNAMENTO DEI RISULTATI ONEX \_ \_ \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[**Elemento dello schema OneX**](onexschema-onex-element.md)
</dt> <dt>

[**BLOB DI VARIABILI ONEX \_ \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

[**DATI DI NOTIFICA WLAN \_ \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))
</dt> <dt>

[**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
