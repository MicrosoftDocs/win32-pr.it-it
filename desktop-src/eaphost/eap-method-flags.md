---
title: Flag del metodo EAP (Eaptypes. h)
description: I flag del metodo EAP vengono utilizzati all'interno delle funzioni di supplicant, Authenticator e peer per specificare i comportamenti di una sessione di autenticazione EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475022"
---
# <a name="eap-method-flags"></a>Flag del metodo EAP

I flag del metodo EAP vengono utilizzati all'interno delle funzioni di supplicant, Authenticator e peer per specificare i comportamenti di una sessione di autenticazione EAP.

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Flag EAP \_ Reserved1**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**\_flag EAP \_ non \_ interattivo**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Non visualizzare un'interfaccia utente (UI).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**\_accesso al flag EAP \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



I dati utente sono stati ottenuti dall'accesso di Windows.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**\_anteprima del flag EAP \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Mostra l'interfaccia utente delle credenziali prima di eseguire l'autenticazione, anche se sono presenti credenziali memorizzate nella cache.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ FLAG \_ Reserved2**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**\_ \_ autenticazione computer del flag EAP \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Usa autenticazione a livello di computer; la mancata impostazione di questo flag indica che è in uso l'autenticazione a livello di utente.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**\_ \_ accesso Guest del flag EAP \_**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



Indica una richiesta di fornire l'accesso guest.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Flag EAP \_ Reserved3**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ FLAG \_ Reserved4** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**il \_ flag EAP \_ riprende \_ dalla modalità di \_ ibernazione**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Indica che si tratta della prima chiamata dopo che l'attività del computer è stata ripresa da un periodo di ibernazione.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ FLAG \_ Reserved5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Flag EAP \_ Reserved6** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_autenticazione del flag EAP \_ completa \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Indica che i metodi tunnel devono eseguire un'autenticazione completa anziché una versione abbreviata, ad esempio la [riconnessione rapida PEAP (Protected EAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**il \_ flag EAP \_ preferisce le \_ \_ credenziali Alt**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica che le credenziali passate a [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) sono preferite per tutte le altre forme di recupero delle credenziali, anche se i dati di configurazione passati nella funzione corrente richiedono una modalità diversa di recupero delle credenziali.

> [!Note]  
> Questo flag viene utilizzato solo da [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Flag EAP \_ Reserved7**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**\_ \_ \_ \_ modifica dello stato di integrità del flag peer EAP \_**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Indica che la riautenticazione è un callback di [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP); NAP ha avviato la sessione di autenticazione perché lo stato di integrità è stato modificato. Questo flag deve essere inviato solo quando questa funzione viene chiamata da un callback [*NotificationHandler*](/previous-versions/windows/desktop/api) specifico di NAP fornito da una chiamata precedente a questa funzione.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_ \_ interfaccia utente eliminare flag EAP \_**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Continuare l'autenticazione con le informazioni disponibili. Se l'autenticazione non può continuare, non riesce.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_flag EAP \_ pre- \_ accesso**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica che EAPHost deve fornire l'accesso Single Sign-on (SSO). Per ulteriori informazioni, vedere [SSO e PLAP](understanding-sso-and-plap.md).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**\_ \_ autenticazione utente del flag EAP \_**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Indica l'autenticazione a livello di utente per i metodi legacy che non possono impostare l'autenticazione del **\_ computer del flag \_ \_ EAP**.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_flag EAP \_ config \_ ReadOnly**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Indica che la configurazione può essere visualizzata ma non aggiornata.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Flag EAP \_ Reserved8**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti EAPHost comuni](common-eap-host-error-constants.md)
</dt> </dl>

