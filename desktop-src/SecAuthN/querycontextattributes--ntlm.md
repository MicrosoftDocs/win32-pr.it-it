---
description: Consente a un'applicazione di trasporto di eseguire una query sul [*pacchetto di sicurezza*](../secgloss/s-gly.md) NTLM per determinati attributi di un [contesto di sicurezza](../secgloss/s-gly.md).
ms.assetid: cfa545e7-c5d9-4ffd-bbba-669d2bd3df2d
title: Funzione QueryContextAttributes (NTLM) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: dba11bbfb1666a3f47b7ee2820167259319178ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128910"
---
# <a name="querycontextattributes-ntlm-function"></a>Funzione QueryContextAttributes (NTLM)

La funzione **QueryContextAttributes (NTLM)** consente a un'applicazione di trasporto di eseguire una query sul [*pacchetto di sicurezza*](../secgloss/s-gly.md) NTLM per determinati [*attributi*](../secgloss/a-gly.md#_security_attribute_gly) di un [contesto di sicurezza](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS SEC_ENTRY QueryContextAttributes(
  _In_  PCtxtHandle phContext,
  _In_  ULONG       ulAttribute,
  _Out_ PVOID       pBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phContext* \[ in\]
</dt> <dd>

Handle per il [contesto di sicurezza](../secgloss/s-gly.md) su cui eseguire una query.

</dd> <dt>

*ulAttribute* \[ in\]
</dt> <dd>

Specifica l'attributo del contesto da restituire. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_ACCESS_TOKEN"></span><span id="secpkg_attr_access_token"></span><dl> <dt>**SECPKG \_ ATTR \_ Access \_ token**</dt> <dt>18</dt> </dl>                                       | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ AccessToken di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) .<br/> Restituisce un handle per il token di accesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_AUTHORITY"></span><span id="secpkg_attr_authority"></span><dl> <dt>**SECPKG \_ ATTR \_ Authority**</dt> <dt>6</dt> </dl>                                                  | Il parametro *pbuffer* contiene un puntatore a una struttura dell' [**\_ autorità SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya) .<br/> Esegue una query sul nome dell'autorità di autenticazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></span><span id="secpkg_attr_client_specified_target"></span><dl> <dt>**SECPKG \_ Il \_ client attr ha \_ specificato la \_ destinazione**</dt> <dt>27</dt> </dl>     | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ ClientSpecifiedTarget di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget) che rappresenta il nome dell'entità servizio (SPN) della destinazione iniziale fornita dal client. <br/> Questo valore è supportato solo quando si utilizzano le associazioni di canale.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ credenziali \_ 2**</dt> <dt>0x80000086</dt> </dl>                                              | Il parametro *pbuffer* contiene un puntatore a una struttura [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) che specifica le credenziali client. <br/> Se la credenziale client è il nome utente e la password, il buffer è una struttura di [**\_ \_ accesso interattivo per marciapiede**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) compresso.<br/> Se la credenziale client corrisponde al nome utente e al PIN della smart card, il buffer è una struttura di [**\_ \_ accesso al certificato a cordolo**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) compresso.<br/> Se la credenziale client è una credenziale di identità online, il buffer è una struttura [**\_ \_ \_ \_ EX2 dell'identità auth**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) del marshalling al secondo.<br/> Questo attributo è supportato solo nel server CredSSP.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.<br/> |
| <span id="SECPKG_ATTR_DCE_INFO"></span><span id="secpkg_attr_dce_info"></span><dl> <dt>**SECPKG \_ ATTR \_ DCE \_ info**</dt> <dt>3</dt> </dl>                                                    | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ DceInfo di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo) .<br/> Esegue una query per i dati di autorizzazione usati dai servizi DCE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_FLAGS"></span><span id="secpkg_attr_flags"></span><dl> <dt>**SECPKG \_ \_Flag attr**</dt> <dt>14</dt> </dl>                                                             | Il parametro *pbuffer* contiene un puntatore a una struttura di [**\_ flag SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) .<br/> Restituisce informazioni sui flag di contesto negoziato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_KEY_INFO"></span><span id="secpkg_attr_key_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informazioni chiave attr**</dt> <dt>5</dt> </dl>                                                    | Il parametro *pbuffer* contiene un puntatore a una struttura di [**\_ informazioni di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa) .<br/> Esegue una query delle informazioni sulle chiavi utilizzate in un [contesto di sicurezza](../secgloss/s-gly.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS"></span><span id="secpkg_attr_last_client_token_status"></span><dl> <dt>**SECPKG \_ \_Stato ultimo \_ \_ token client \_ di attr**</dt> <dt>30</dt> </dl> | Il parametro *pbuffer* contiene un puntatore a una struttura [**SecPkgContext \_ LastClientTokenStatus**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lastclienttokenstatus) che specifica se il token della chiamata più recente alla funzione [**InitializeSecurityContext**](initializesecuritycontext--general.md) è l'ultimo token del client.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_ATTR_LIFESPAN"></span><span id="secpkg_attr_lifespan"></span><dl> <dt>**SECPKG \_ ATTR \_ durata**</dt> <dt>2</dt> </dl>                                                     | Il parametro *pbuffer* contiene un puntatore a una struttura di [**\_ durata SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan) .<br/> Esegue una query sull'intervallo di vita del contesto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_LOCAL_CRED"></span><span id="secpkg_attr_local_cred"></span><dl> <dt>**SECPKG \_ attr \_ Local \_ cred**</dt> </dl>                                                                                                     | Il parametro *pbuffer* contiene un puntatore a una **struttura \_ LocalCredentialInfo di SecPkgContext** . (obsoleto)<br/> Sostituito dal \_ \_ contesto del certificato locale SECPKG attr \_ \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="SECPKG_ATTR_NAMES"></span><span id="secpkg_attr_names"></span><dl> <dt>**SECPKG \_ \_Nomi attr**</dt> <dt>1</dt> </dl>                                                              | Il parametro *pbuffer* contiene un puntatore a una struttura [**SecPkgContext \_ names**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa) .<br/> Esegue una query sul nome associato al contesto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="SECPKG_ATTR_NATIVE_NAMES"></span><span id="secpkg_attr_native_names"></span><dl> <dt>**SECPKG \_ ATTR \_ \_ nomi nativi**</dt> <dt>13</dt> </dl>                                       | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ NativeNames di SecPkgContext**](https://docs.microsoft.com/windows/win32/api/sspi/ns-sspi-_secpkgcontext_nativenamesa) .<br/> Restituisce il nome dell'entità (CNAME) dal ticket in uscita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_NEGOTIATION_INFO"></span><span id="secpkg_attr_negotiation_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informazioni sulle negoziazioni attr**</dt> <dt>12</dt> </dl>                           | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ NegotiationInfo di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa) .<br/> Restituisce informazioni sul [*pacchetto di sicurezza*](../secgloss/s-gly.md) da utilizzare con il processo di negoziazione e lo stato corrente della negoziazione per l'utilizzo del pacchetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informazioni sul pacchetto attr**</dt> <dt>10</dt> </dl>                                       | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ PackageInfo di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .<br/> Restituisce informazioni sul provider di servizi condivisi in uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_PASSWORD_EXPIRY"></span><span id="secpkg_attr_password_expiry"></span><dl> <dt>**SECPKG \_ ATTR \_ password \_ scadenza**</dt> <dt>8</dt> </dl>                               | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ PasswordExpiry di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_passwordexpiry) .<br/> Restituisce le informazioni relative alla scadenza della password.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_ROOT_STORE"></span><span id="secpkg_attr_root_store"></span><dl> <dt>**SECPKG \_ 0x55 \_ \_ archivio radice attr**</dt> <dt></dt> </dl>                                           | Il parametro *pbuffer* contiene un puntatore a un **HCERTCONTEXT**. <br/> Trova un contesto del certificato che contiene un certificato fornito dall'archivio radice.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_SESSION_KEY"></span><span id="secpkg_attr_session_key"></span><dl> <dt>**SECPKG \_ \_ \_ Chiave di sessione attr**</dt> <dt>9</dt> </dl>                                           | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ SessionKey di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sessionkey) .<br/> Restituisce informazioni sulle [*chiavi della sessione*](../secgloss/s-gly.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ ATTR \_ dimensioni**</dt> <dt>0</dt> </dl>                                                              | Il parametro *pbuffer* contiene un puntatore a una struttura di [**\_ dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .<br/> Esegue una query sulle dimensioni delle strutture utilizzate nelle funzioni per messaggio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_ATTR_TARGET_INFORMATION"></span><span id="secpkg_attr_target_information"></span><dl> <dt>**SECPKG \_ \_ \_ Informazioni sulla destinazione attr**</dt> <dt>17</dt> </dl>                     | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ TargetInformation di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_targetinformation) .<br/> Restituisce informazioni sul nome del server remoto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pbuffer* \[ out\]
</dt> <dd>

Puntatore a una struttura che riceve gli attributi. Il tipo di struttura a cui punta dipende dal valore specificato nel parametro *ulAttribute* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è SEC \_ E \_ OK.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero.

## <a name="remarks"></a>Commenti

La struttura a cui punta il parametro *pbuffer* varia a seconda dell'attributo sottoposto a query. Il chiamante deve allocare la struttura *pbuffer* stessa, ma il provider di servizi condivisi alloca qualsiasi memoria necessaria per mantenere i membri di dimensioni variabili della struttura *pbuffer* . La memoria allocata dal provider di servizi condivisi può essere liberata chiamando la funzione [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Dopo che \_ \_ \_ \_ è stato letto il valore di contesto SECPKG attr Remote certificate o SECPKG \_ attr \_ Local \_ Certificate \_ , il membro **hCertStore** verrà impostato su un handle per un archivio certificati che contiene i certificati intermedi, se presenti. Inoltre, l'applicazione è responsabile della chiamata a [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) per rilasciare la memoria utilizzata dal contesto del certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomi Unicode e ANSI<br/>   | **QueryContextAttributesW** (Unicode) e **QueryContextAttributesA** (ANSI)<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**contesto del certificato \_**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**\_Autorità SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)
</dt> <dt>

[**SecPkgContext \_ ConnectionInfo**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_connectioninfo)
</dt> <dt>

[**\_DceInfo SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)
</dt> <dt>

[**\_IssuerListInfoEx SecPkgContext**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)
</dt> <dt>

[**Informazioni di SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)
</dt> <dt>

[**\_Durata SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)
</dt> <dt>

[**\_Nomi SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)
</dt> <dt>

[**\_Dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> <dt>

[**\_StreamSizes SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)
</dt> </dl>

 

 
