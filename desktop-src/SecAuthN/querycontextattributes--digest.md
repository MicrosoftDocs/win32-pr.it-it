---
description: Consente a un'applicazione di trasporto di eseguire query sul pacchetto [*di sicurezza*](../secgloss/s-gly.md) Digest per determinati attributi di un contesto [*di sicurezza.*](../secgloss/s-gly.md)
ms.assetid: d4cd2cc4-77a2-42ba-9029-f4d92706c5c2
title: Funzione QueryContextAttributes (Digest) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 11cf8cbd35242b43d3f68b6265daae02e1d5425a8c0692742cbee0a1bd93441d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920210"
---
# <a name="querycontextattributes-digest-function"></a>Funzione QueryContextAttributes (Digest)

La **funzione QueryContextAttributes (Digest)** consente a un'applicazione di trasporto di eseguire query sul [*pacchetto*](../secgloss/s-gly.md) di sicurezza Digest per determinati [*attributi*](../secgloss/a-gly.md#_security_attribute_gly) di un contesto [*di sicurezza.*](../secgloss/s-gly.md)

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

*phContext* \[ Pollici\]
</dt> <dd>

Handle per il contesto [*di sicurezza su*](../secgloss/s-gly.md) cui eseguire query.

</dd> <dt>

*ulAttribute* \[ Pollici\]
</dt> <dd>

Specifica l'attributo del contesto da restituire. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_ACCESS_TOKEN"></span><span id="secpkg_attr_access_token"></span><dl> <dt>**SECPKG \_ TOKEN DI \_ \_ ACCESSO ATTR**</dt> <dt>18</dt> </dl>                                   | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ AccessToken.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken)<br/> Restituisce un handle al token di accesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_AUTHORITY"></span><span id="secpkg_attr_authority"></span><dl> <dt>**SECPKG \_ AUTORITÀ \_ ATTR**</dt> <dt>6</dt> </dl>                                              | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ Authority.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)<br/> Esegue una query sul nome dell'autorità di autenticazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></span><span id="secpkg_attr_client_specified_target"></span><dl> <dt>**SECPKG \_ DESTINAZIONE \_ SPECIFICATA \_ \_ DAL CLIENT ATTR**</dt> <dt>27</dt> </dl> | Il *parametro pBuffer* contiene un puntatore a una struttura [**SecPkgContext \_ ClientSpecifiedTarget**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget) che rappresenta il nome dell'entità servizio (SPN) della destinazione iniziale fornita dal client. <br/> Questo valore è supportato solo quando si usano associazioni di canale.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS \_ 2**</dt> <dt>0x80000086</dt> </dl>                                          | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) che specifica le credenziali client. <br/> Se le credenziali client sono nome utente e password, il buffer è una struttura [**KERB \_ INTERACTIVE LOGON \_ imballata.**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon)<br/> Se la credenziale client è il nome utente smart card PIN, il buffer è una struttura [**KERB \_ CERTIFICATE LOGON \_ imballata.**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon)<br/> Se la credenziale client è una credenziale di identità online, il buffer è una struttura [**\_ SEC WINNT \_ AUTH IDENTITY \_ \_ EX2 con**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) marshalling.<br/> Questo attributo è supportato solo nel server CredSSP.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> |
| <span id="SECPKG_ATTR_DCE_INFO"></span><span id="secpkg_attr_dce_info"></span><dl> <dt>**SECPKG \_ ATTR \_ DCE \_ INFO**</dt> <dt>3</dt> </dl>                                                | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ DceInfo.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)<br/> Query per i dati di autorizzazione usati dai servizi DCE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_FLAGS"></span><span id="secpkg_attr_flags"></span><dl> <dt>**SECPKG \_ FLAG \_ ATTR**</dt> <dt>14</dt> </dl>                                                         | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ Flags.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags)<br/> Restituisce informazioni sui flag di contesto negoziati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_KEY_INFO"></span><span id="secpkg_attr_key_info"></span><dl> <dt>**SECPKG \_ INFORMAZIONI \_ CHIAVE \_ ATTR**</dt> <dt>5</dt> </dl>                                                | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ KeyInfo.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)<br/> Esegue una query sulle chiavi utilizzate in un [*contesto di sicurezza.*](../secgloss/s-gly.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SECPKG_ATTR_LIFESPAN"></span><span id="secpkg_attr_lifespan"></span><dl> <dt>**SECPKG \_ ATTR \_ LIFESPAN**</dt> <dt>2</dt> </dl>                                                 | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ Lifespan.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)<br/> Esegue una query sull'intervallo di vita del contesto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_LOCAL_CRED"></span><span id="secpkg_attr_local_cred"></span><dl> <dt>**SECPKG \_ ATTR \_ LOCAL \_ CRED**</dt> </dl>                                                                                                 | Il *parametro pBuffer* contiene un puntatore a una **struttura SecPkgContext \_ LocalCredentialInfo.** (obsoleto)<br/> Sostituito da SECPKG \_ ATTR \_ LOCAL \_ CERT \_ CONTEXT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="SECPKG_ATTR_NAMES"></span><span id="secpkg_attr_names"></span><dl> <dt>**SECPKG \_ NOMI \_ ATTR**</dt> <dt>1</dt> </dl>                                                          | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ Names.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)<br/> Esegue una query sul nome associato al contesto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="SECPKG_ATTR_NATIVE_NAMES"></span><span id="secpkg_attr_native_names"></span><dl> <dt>**SECPKG \_ NOMI \_ NATIVI \_ ATTR**</dt> <dt>13</dt> </dl>                                   | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ NativeNames.**](https://docs.microsoft.com/windows/win32/api/sspi/ns-sspi-_secpkgcontext_nativenamesa)<br/> Restituisce il nome dell'entità (CNAME) dal ticket in uscita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_NEGOTIATION_INFO"></span><span id="secpkg_attr_negotiation_info"></span><dl> <dt>**SECPKG \_ INFORMAZIONI SULLA \_ NEGOZIAZIONE \_ ATTR**</dt> <dt>12</dt> </dl>                       | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ NegotiationInfo.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa)<br/> Restituisce informazioni sul [*pacchetto di sicurezza*](../secgloss/s-gly.md) da utilizzare con il processo di negoziazione e lo stato corrente della negoziazione per l'uso di tale pacchetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ INFORMAZIONI SUL \_ \_ PACCHETTO ATTR**</dt> <dt>10</dt> </dl>                                   | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ PackageInfo.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)<br/> Restituisce informazioni sul provider di servizi condivisi in uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_PASSWORD_EXPIRY"></span><span id="secpkg_attr_password_expiry"></span><dl> <dt>**SECPKG \_ SCADENZA \_ PASSWORD \_ ATTR**</dt> <dt>8</dt> </dl>                           | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ PasswordExpiry.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_passwordexpiry)<br/> Restituisce informazioni sulla scadenza della password.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_ROOT_STORE"></span><span id="secpkg_attr_root_store"></span><dl> <dt>**SECPKG \_ ATTR \_ ROOT \_ STORE**</dt> <dt>0x55</dt> </dl>                                       | Il *parametro pBuffer* contiene un puntatore a **HCERTCONTEXT**. Trova un contesto del certificato che contiene un certificato fornito dall'archivio radice.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_SESSION_KEY"></span><span id="secpkg_attr_session_key"></span><dl> <dt>**SECPKG \_ CHIAVE \_ DI SESSIONE \_ ATTR**</dt> <dt>9</dt> </dl>                                       | Il *parametro pBuffer* contiene un puntatore a una [**struttura \_ SessionKey secPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sessionkey)<br/> Restituisce informazioni sulle [*chiavi di*](../secgloss/s-gly.md)sessione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ DIMENSIONI \_ ATTR**</dt> <dt>0</dt> </dl>                                                          | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)<br/> Esegue una query sulle dimensioni delle strutture usate nelle funzioni per messaggio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_ATTR_STREAM_SIZES"></span><span id="secpkg_attr_stream_sizes"></span><dl> <dt>**SECPKG \_ DIMENSIONI \_ DEL \_ FLUSSO ATTR**</dt> <dt>4</dt> </dl>                                    | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ StreamSizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)<br/> Esegue query sulle dimensioni delle varie parti di un flusso usate nelle funzioni per messaggio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_TARGET_INFORMATION"></span><span id="secpkg_attr_target_information"></span><dl> <dt>**SECPKG \_ INFORMAZIONI SULLA \_ \_ DESTINAZIONE ATTR**</dt> <dt>17</dt> </dl>                 | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ TargetInformation.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_targetinformation)<br/> Restituisce informazioni sul nome del server remoto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pBuffer* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura che riceve gli attributi. Il tipo di struttura a cui punta dipende dal valore specificato nel *parametro ulAttribute.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è SEC \_ E \_ OK.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero.

## <a name="remarks"></a>Commenti

La struttura a cui punta il *parametro pBuffer* varia a seconda dell'attributo sottoposto a query. Il chiamante deve allocare la struttura *pBuffer* stessa, ma il provider di servizi condivisi alloca la memoria necessaria per contenere i membri di dimensioni variabili della *struttura pBuffer.* La memoria allocata dal provider di servizi condivisi può essere liberata chiamando la [**funzione FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Dopo aver letto il valore SECPKG \_ ATTR REMOTE CERT CONTEXT o \_ \_ \_ SECPKG \_ ATTR LOCAL CERT CONTEXT, il membro \_ \_ \_ **hCertStore** verrà impostato su un handle per un archivio certificati che contiene i certificati intermedi, se presenti. Inoltre, l'applicazione è responsabile della chiamata [**a CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) per rilasciare la memoria usata dal contesto del certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomi Unicode e ANSI<br/>   | **QueryContextAttributesW** (Unicode) e **QueryContextAttributesA** (ANSI)<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**CONTESTO \_ CERT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecPkgContext \_ Authority**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)
</dt> <dt>

[**SecPkgContext \_ ConnectionInfo**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_connectioninfo)
</dt> <dt>

[**SecPkgContext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)
</dt> <dt>

[**SecPkgContext \_ IssuerListInfoEx**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)
</dt> <dt>

[**SecPkgContext \_ KeyInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)
</dt> <dt>

[**Durata secPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)
</dt> <dt>

[**Nomi \_ secPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)
</dt> <dt>

[**Dimensioni \_ secPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> <dt>

[**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)
</dt> </dl>

 

 
