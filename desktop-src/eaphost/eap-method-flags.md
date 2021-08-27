---
title: Flag del metodo EAP (Eaptypes.h)
description: I flag del metodo EAP vengono usati all'interno delle funzioni supplicant, authenticator e peer per specificare i comportamenti di una sessione di autenticazione EAP.
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
ms.openlocfilehash: 91acce3b3829c947bfb6e705ad7e1f07b938a986bc6f6845a4c10a54b4f1992c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094411"
---
# <a name="eap-method-flags"></a>Flag del metodo EAP

I flag del metodo EAP vengono usati all'interno delle funzioni supplicant, authenticator e peer per specificare i comportamenti di una sessione di autenticazione EAP.

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**FLAG EAP \_ \_ riservato1**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**FLAG EAP \_ \_ NON \_ INTERATTIVO**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Non visualizzare un'interfaccia utente.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**ACCESSO CON FLAG EAP \_ \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



I dati utente sono stati ottenuti da Windows accesso.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**ANTEPRIMA FLAG EAP \_ \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Mostra l'interfaccia utente delle credenziali prima dell'autenticazione, anche se sono presenti credenziali memorizzate nella cache.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ FLAG \_ Riservato2**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP \_ FLAG \_ MACHINE \_ AUTH**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Usare l'autenticazione a livello di computer; Se non si imposta questo flag, viene usata l'autenticazione a livello di utente.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**ACCESSO \_ GUEST \_ CON FLAG EAP \_**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



Indica una richiesta per fornire l'accesso guest.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**FLAG EAP \_ \_ riservato3**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ FLAG \_ Riservato4** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**RIPRESA DEL FLAG EAP \_ \_ DA \_ \_ IBERNAZIONE**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Indica che si tratta della prima chiamata dopo la ripresa dell'attività del computer da un periodo di ibernazione.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ FLAG \_ riservato5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**FLAG EAP \_ \_ riservato6** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**AUTENTICAZIONE COMPLETA DEL FLAG EAP \_ \_ \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Indica che i metodi di tunneling devono eseguire un'autenticazione completa anziché una versione abbreviata, ad esempio [PeaP (Protected EAP) Fast Reconnect](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**IL FLAG EAP \_ \_ PREFERISCE LE CREDENZIALI \_ \_ ALT**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica che le credenziali passate a [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) sono preferibili a tutte le altre forme di recupero delle credenziali, anche se i dati di configurazione passati alla funzione corrente richiede una modalità diversa di recupero delle credenziali.

> [!Note]  
> Questo flag viene usato solo da [**EapPeerBeginSession.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**FLAG EAP \_ \_ riservato7**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**MODIFICA DELLO STATO DI INTEGRITÀ \_ \_ DEL FLAG PEER \_ \_ EAP \_**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Indica che la causa della nuova autenticazione è un callback di [Protezione accesso alla](/windows/desktop/NAP/network-access-protection-start-page) rete. Protezione accesso alla rete ha avviato la sessione di autenticazione perché lo stato di integrità è cambiato. Questo flag deve essere inviato solo quando questa funzione viene chiamata da un callback [*NotificationHandler*](/previous-versions/windows/desktop/api) specifico di Protezione accesso alla rete fornito da una chiamata precedente a questa funzione.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**INTERFACCIA UTENTE DI \_ SUPRESS DEL FLAG EAP \_ \_**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Continuare l'autenticazione con le informazioni disponibili. Se l'autenticazione non può continuare, avrà esito negativo.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**PRE-ACCESSO CON FLAG EAP \_ \_ \_**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica che EAPHost deve fornire l'accesso Single Sign-On (SSO). Per altre informazioni, vedere [SSO e PLAP.](understanding-sso-and-plap.md)


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**AUTENTICAZIONE UTENTE \_ CON FLAG \_ \_ EAP**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Indica l'autenticazione a livello di utente per i metodi legacy che non possono impostare **EAP \_ FLAG MACHINE \_ \_ AUTH.**


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP \_ FLAG \_ CONFG \_ READONLY**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Indica che la configurazione può essere visualizzata ma non aggiornata.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**FLAG EAP \_ \_ riservato8**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Non usare. Riservato per utilizzi futuri.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti EAPHost comuni](common-eap-host-error-constants.md)
</dt> </dl>

