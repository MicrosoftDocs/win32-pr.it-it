---
title: Metodo IMsTscAxEvents OnDisconnected
description: Chiamato quando il controllo client è stato disconnesso dal server Desktop remoto host sessione Desktop remoto.
ms.assetid: f01086e7-61d1-41df-ba0a-4eecfa57d492
ms.tgt_platform: multiple
keywords:
- Metodo OnDisconnected Servizi Desktop remoto
- Metodo OnDisconnected Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnDisconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bc7351d1cc0fafa46aab1f93feed4cafc184dc33090d4d2c7947a285fbb234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125131"
---
# <a name="imstscaxeventsondisconnected-method"></a>Metodo IMsTscAxEvents::OnDisconnected

Chiamato quando il controllo client è stato disconnesso dal server Desktop remoto host sessione Desktop remoto.

## <a name="syntax"></a>Sintassi


```C++
void OnDisconnected(
  [in] long discReason
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*discReason* \[ Pollici\]
</dt> <dd>

Specifica il motivo della disconnessione. Di seguito è riportato un elenco di codici di errore. Alcuni di questi codici di errore sono definiti in Wincred.h.

<dt>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))


</dt> <dd>

Socket chiuso.

</dd> <dt>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))


</dt> <dd>

Disconnessione remota in base al server. Non si tratta di un codice di errore.

</dd> <dt>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))


</dt> <dd>

Errore di decompressione.

</dd> <dt>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))


</dt> <dd>

Timeout della connessione.

</dd> <dt>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))


</dt> <dd>

Errore di decrittografia.

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))


</dt> <dd>

Errore di ricerca dei nomi DNS.

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))


</dt> <dd>

Ricerca DNS non riuscita.

</dd> <dt>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))


</dt> <dd>

Errore di crittografia.

</dd> <dt>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))


</dt> <dd>

Windows Chiamata [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) del socket non riuscita.

</dd> <dt>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))


</dt> <dd>

Errore host non trovato.

</dd> <dt>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))


</dt> <dd>

Errore interno.

</dd> <dt>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))


</dt> <dd>

Errore di sicurezza interno.

</dd> <dt>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))


</dt> <dd>

Errore di sicurezza interno.

</dd> <dt>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))


</dt> <dd>

Il metodo di crittografia specificato non è valido.

</dd> <dt>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))


</dt> <dd>

Indirizzo IP non valido specificato.

</dd> <dt>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))


</dt> <dd>

I dati di sicurezza del server non sono validi.

</dd> <dt>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))


</dt> <dd>

I dati di sicurezza non sono validi.

</dd> <dt>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))


</dt> <dd>

L'indirizzo IP specificato non è valido.

</dd> <dt>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))


</dt> <dd>

Negoziazione della licenza non riuscita.

</dd> <dt>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))


</dt> <dd>

Timeout delle licenze.

</dd> <dt>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))


</dt> <dd>

Disconnessione locale. Non si tratta di un codice di errore.

</dd> <dt>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))


</dt> <dd>

Nessuna informazione disponibile.

</dd> <dt>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))


</dt> <dd>

Memoria insufficiente.

</dd> <dt>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))


</dt> <dd>

Memoria insufficiente.

</dd> <dt>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))


</dt> <dd>

Memoria insufficiente.

</dd> <dt>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0x2))


</dt> <dd>

Disconnessione remota in base all'utente. Non si tratta di un codice di errore.

</dd> <dt>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))


</dt> <dd>

Impossibile decomprimere il certificato server.

</dd> <dt>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))


</dt> <dd>

Windows Connessione socket [**non**](/windows/desktop/api/winsock2/nf-winsock2-connect) riuscita.

</dd> <dt>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))


</dt> <dd>

Windows Chiamata [**recv dei**](/windows/desktop/api/winsock/nf-winsock-recv) socket non riuscita.

</dd> <dt>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))


</dt> <dd>

Si è verificato il timeout.

</dd> <dt>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))


</dt> <dd>

Errore interno del timer.

</dd> <dt>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))


</dt> <dd>

Windows Chiamata di [**invio socket**](/windows/desktop/api/winsock2/nf-winsock2-send) non riuscita.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL \_ ACCOUNT ERR \_ \_ DISABILITATO** (2823 (0xB07))


</dt> <dd>

L'account è disabilitato.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL \_ ACCOUNT ERR \_ \_ SCADUTO** (3591 (0xE07))


</dt> <dd>

L'account è scaduto.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL \_ ACCOUNT \_ ERR \_ BLOCCATO \_** (3335 (0xD07))


</dt> <dd>

L'account è bloccato.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL \_ RESTRIZIONE \_ \_ DELL'ACCOUNT ERR** (3079 (0xC07))


</dt> <dd>

L'account è limitato.

</dd> <dt>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL \_ ERR \_ CERT \_ EXPIRED** (6919 (0x1B07))


</dt> <dd>

Il certificato ricevuto è scaduto.

</dd> <dt>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL \_ CRITERI DI \_ DELEGA \_ ERR** (5639 (0x1607))


</dt> <dd>

I criteri non supportano la delega delle credenziali al server di destinazione.

</dd> <dt>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL \_ ERR \_ FRESH \_ CRED RICHIESTO DAL \_ \_ \_ SERVER** (8455 (0x2107))


</dt> <dd>

I criteri di autenticazione del server non consentono richieste di connessione che usano credenziali salvate. L'utente deve immettere nuove credenziali.

</dd> <dt>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL \_ ERRORE DI \_ ACCESSO \_ ERR** (2055 (0x807))


</dt> <dd>

Accesso non riuscito.

</dd> <dt>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL \_ ERR \_ NO \_ AUTHENTICATING \_ AUTHORITY** (6151 (0x1807))


</dt> <dd>

Non è stato possibile contattare alcuna autorità per l'autenticazione. Il nome di dominio dell'entità autenticante potrebbe non essere corretto, il dominio potrebbe non essere raggiungibile o potrebbe esserci stato un errore di relazione di trust.

</dd> <dt>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL \_ ERR \_ NO \_ SUCH \_ USER** (2567 (0xA07))


</dt> <dd>

L'utente specificato non dispone di alcun account.

</dd> <dt>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL \_ PASSWORD ERR \_ \_ SCADUTA** (3847 (0xF07))


</dt> <dd>

La password è scaduta.

</dd> <dt>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL \_ LA PASSWORD DI ERR \_ \_ DEVE \_ CAMBIARE** (4615 (0x1207))


</dt> <dd>

La password utente deve essere modificata prima di accedere per la prima volta.

</dd> <dt>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL \_ ERR \_ POLICY \_ NTLM \_ ONLY** (5895 (0x1707))


</dt> <dd>

La delega delle credenziali al server di destinazione non è consentita a meno che non sia stata ottenuta l'autenticazione reciproca.

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL \_ SCHEDA \_ SMART CARD ERR \_ \_ BLOCCATA** (8711 (0x2207))


</dt> <dd>

Il smart card è bloccato.

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL \_ \_ \_ \_ PIN ERRATO DELLA SMART CARD ERR** (7175 (0x1C07))


</dt> <dd>

È stato presentato un PIN non corretto al smart card.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per recuperare una descrizione dell'errore di disconnessione, chiamare il metodo [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) e passarlo al parametro *discReason* e alla proprietà [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) dell'interfaccia [**IMsRdpClient.**](imsrdpclient-interface.md)

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

