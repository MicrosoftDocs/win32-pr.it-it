---
description: Contiene informazioni sul profilo di connessione 802.1 X attualmente utilizzato per l'autenticazione 802.1 X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: Struttura ONEX_CONNECTION_PROFILE
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
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311677"
---
# <a name="onex_connection_profile-structure"></a>Struttura del profilo di \_ connessione Onex \_

La struttura del **\_ \_ profilo di connessione Onex** contiene informazioni sul profilo di connessione 802.1 x attualmente utilizzato per l'autenticazione 802.1 x.

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

Versione della struttura del **\_ \_ profilo di connessione Onex** .

</dd> <dt>

**dwTotalLen**
</dt> <dd>

Lunghezza, in byte, della struttura del **\_ \_ profilo di connessione Onex** .

</dd> <dt>

**fOneXSupplicantFlags**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwOneXSupplicantFlags** .

</dd> <dt>

**fsupplicantMode**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **supplicantMode** .

</dd> <dt>

**fauthMode**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **AuthMode** .

</dd> <dt>

**fHeldPeriod**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwHeldPeriod** .

</dd> <dt>

**fAuthPeriod**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwAuthPeriod** .

</dd> <dt>

**fStartPeriod**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwStartPeriod** .

</dd> <dt>

**fMaxStart**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwMaxStart** .

</dd> <dt>

**fMaxAuthFailures**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwMaxAuthFailures** .

</dd> <dt>

**fNetworkAuthTimeout**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwNetworkAuthTimeout** .

</dd> <dt>

**fAllowLogonDialogs**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **bAllowLogonDialogs** .

</dd> <dt>

**fNetworkAuthWithUITimeout**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwNetworkAuthWithUITimeout** .

</dd> <dt>

**fUserBasedVLan**
</dt> <dd>

Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **bUserBasedVLan** .

</dd> <dt>

**dwOneXSupplicantFlags**
</dt> <dd>

Set di flag 802.1 X che possono essere presenti nel profilo. Questi flag sono riservati per uso interno da parte del modulo di autenticazione 802.1 X.

</dd> <dt>

**supplicantMode**
</dt> <dd>

Elemento supplicantMode nello schema 802.1 X che specifica il metodo di trasmissione utilizzato per i messaggi di EAPOL-Start. Per ulteriori informazioni, vedere l' [**elemento supplicantMode (Onex)**](onexschema-supplicantmode-onex-element.md) nello schema 802.1 x.



| Valore                                                                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt> </dl> | EAPOL-Start messaggi non vengono trasmessi. Valido solo per i profili LAN cablati.<br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt> </dl>                                                         | Il client determina quando inviare pacchetti di EAPOL-Start in base alla funzionalità di rete. EAPOL-Start messaggi vengono inviati solo quando richiesto. Valido solo per i profili LAN cablati.<br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt> </dl>                                         | EAPOL-Start messaggi vengono trasmessi come specificato da 802.1 X. Valido per i profili LAN cablati e wireless.<br/>                                                             |



 

</dd> <dt>

**authMode**
</dt> <dd>

Elemento authMode nello schema 802.1 X che specifica il tipo di credenziali utilizzate per l'autenticazione 802.1 X. Per ulteriori informazioni, vedere l' [**elemento authMode (Onex)**](onexschema-authmode-onex-element.md) nello schema 802.1 x.



| Valore                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt> </dl> | Usare le credenziali del computer o dell'utente. Quando un utente è connesso, le credenziali dell'utente vengono usate per l'autenticazione. Quando nessun utente è connesso, vengono usate le credenziali del computer.<br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt> </dl>         | Usare solo le credenziali del computer.<br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt> </dl>                     | Usare solo le credenziali utente.<br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <dt>**OneXAuthModeGuest**</dt> <dt>3</dt> </dl>                                 | Utilizzare solo le credenziali Guest (vuote).<br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt> </dl>         | Non sono state specificate le credenziali da usare.<br/>                                                                                                                                   |



 

</dd> <dt>

**dwHeldPeriod**
</dt> <dd>

Elemento heldPeriod nello schema 802.1 X che specifica il periodo di tempo, in secondi, in cui un client non tenterà di nuovo l'autenticazione dopo un tentativo di autenticazione non riuscito. Per ulteriori informazioni, vedere l' [**elemento heldPeriod (Onex)**](onexschema-heldperiod-onex-element.md) nello schema 802.1 x.

</dd> <dt>

**dwAuthPeriod**
</dt> <dd>

Elemento authPeriod nello schema 802.1 X che specifica il periodo di tempo massimo, in secondi, in cui un client attende una risposta dall'autenticatore. Se non viene ricevuta una risposta entro il periodo specificato, il client presuppone che non sia presente alcun autenticatore nella rete. Per ulteriori informazioni, vedere l' [**elemento authPeriod (Onex)**](onexschema-authperiod-onex-element.md) nello schema 802.1 x.

</dd> <dt>

**dwStartPeriod**
</dt> <dd>

Elemento startPeriod nello schema 802.1 X che specifica il periodo di tempo, in secondi, di attesa prima dell'invio di un EAPOL-Start. Viene inviato un messaggio di EAPOL-Start per avviare il processo di autenticazione 802.1 X. Per ulteriori informazioni, vedere l' [**elemento startPeriod (Onex)**](onexschema-startperiod-onex-element.md) nello schema 802.1 x.

</dd> <dt>

**dwMaxStart**
</dt> <dd>

Elemento maxStart nello schema 802.1 X che specifica il numero massimo di messaggi di EAPOL-Start inviati. Una volta inviato il numero massimo di EAPOL-Start messaggi, il client presuppone che non sia presente alcun autenticatore nella rete. Per ulteriori informazioni, vedere l' [**elemento maxStart (Onex)**](onexschema-maxstart-onex-element.md) nello schema 802.1 x.

</dd> <dt>

**dwMaxAuthFailures**
</dt> <dd>

Elemento maxAuthFailures nello schema 802.1 X che specifica il numero massimo di errori di autenticazione consentiti per un set di credenziali. Per ulteriori informazioni, vedere l'elemento [**maxAuthFailures (Onex)**](onexschema-maxauthfailures-onex-element.md) nello schema 802.1 x.

</dd> <dt>

**dwNetworkAuthTimeout**
</dt> <dd>

Tempo di attesa, in secondi, per il completamento dell'autenticazione 802.1 X prima di procedere con l'accesso normale. Questo valore viene utilizzato in scenari Single Sign-on (SSO). Il valore predefinito è 10 secondi in un profilo 802.1 X. Per ulteriori informazioni, vedere l' [**elemento maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md) nello schema 802.1 x.

</dd> <dt>

**dwNetworkAuthWithUITimeout**
</dt> <dd>

Tempo massimo di attesa, in secondi, per la connessione, nel caso in cui venga visualizzata una finestra di dialogo dell'interfaccia utente che richiede l'input dell'utente durante l'accesso SSO per accesso.

In Windows Vista con SP1 e versioni successive questo valore è hardcoded a 10 minuti e non è configurabile. In Windows Vista Release to Manufacturing, questo valore viene impostato su 60 secondi in un profilo 802.1 X e controllato dall'elemento **maxDelayWithAdditionalDialogs** nello schema.

In Windows Vista con SP1 e versioni successive, l'elemento **maxDelayWithAdditionalDialogs** nello schema 802.1 x viene ignorato e deprecato.

</dd> <dt>

**bAllowLogonDialogs**
</dt> <dd>

Valore che specifica se consentire la visualizzazione di finestre di dialogo EAP quando si utilizza SSO di pre-accesso. Per ulteriori informazioni, vedere l'elemento **allowAdditionalDialogs** nello schema 802.1 x.

</dd> <dt>

**bUserBasedVLan**
</dt> <dd>

Elemento userBasedVirtualLan nello schema 802.1 X che specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente. Alcuni dispositivi NAS (Network Access Server) modificano la VLAN dopo l'autenticazione dell'utente. Quando userBasedVirtualLan è TRUE, il NAS può modificare la VLAN di un dispositivo dopo l'autenticazione dell'utente. Per ulteriori informazioni, vedere l' [**elemento userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) nello schema 802.1 x.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura del **\_ \_ profilo di connessione Onex** viene utilizzata dal modulo 802.1 x, un nuovo componente di configurazione wireless supportato in Windows Vista e versioni successive.

I [**\_ dati dell' \_ aggiornamento \_ dei risultati di Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contengono informazioni su una modifica dello stato dell'autenticazione 802.1 x. La **struttura \_ \_ \_ dei dati di aggiornamento dei risultati di Onex** viene restituita quando il membro **NotificationSource** della struttura dei [**\_ \_ dati di notifica**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) WLAN è l'origine di **\_ notifica WLAN \_ \_ Onex** e il membro **NotificationCode** della struttura **\_ \_ dei dati di notifica WLAN** per la notifica ricevuta è **OneXNotificationTypeResultUpdate**. Per questa notifica, il membro **pData** della struttura **di \_ \_ dati di notifica WLAN** punta a una struttura di dati di **\_ \_ aggiornamento \_ dei risultati di Onex** che contiene informazioni sulla modifica dello stato di autenticazione 802.1 x.

Se il membro **fOneXAuthParams** nella struttura [**\_ \_ \_ dei dati di aggiornamento dei risultati di Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) è impostato, il membro **authParams** della struttura **\_ \_ \_ dei dati di aggiornamento dei risultati Onex** contiene una struttura di [**\_ \_ BLOB di variabili Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) con una struttura di [**\_ \_ parametri auth Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) incorporata a partire dal membro **dwOffset** del **\_ \_ BLOB della variabile Onex**. Il membro **oneXConnProfile** della struttura **Onex \_ auth \_ params** contiene una struttura **\_ \_ BLOB della variabile Onex** con una struttura del **\_ \_ profilo di connessione Onex** incorporata a partire dal membro **dwOffset** del **\_ \_ BLOB della variabile Onex**.

La struttura del **\_ \_ profilo di connessione Onex** non è definita in un file di intestazione pubblico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sull'architettura di ACM](about-the-acm-architecture.md)
</dt> <dt>

[Schema OneX](onexschema-schema.md)
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

[**\_parametri di autenticazione Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[**\_tipo di notifica Onex \_**](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[**\_ \_ dati aggiornamento risultati \_ Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[**Elemento dello schema OneX**](onexschema-onex-element.md)
</dt> <dt>

[**\_BLOB variabile \_ Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

[**\_dati di notifica WLAN \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))
</dt> <dt>

[**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
