---
description: Consente a un'applicazione di trasporto di eseguire una query sul pacchetto di sicurezza CredSSP (Credential Security Support Provider) per determinati attributi di un contesto di sicurezza.
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
title: Funzione QueryContextAttributes (CredSSP) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b8ff421a2173f2ce2c5521e0706b53c3f6c326038179345d139acd0a157c7d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920230"
---
# <a name="querycontextattributes-credssp-function"></a>Funzione QueryContextAttributes (CredSSP)

La **funzione QueryContextAttributes (CredSSP)** consente a un'applicazione di trasporto di eseguire [](../secgloss/a-gly.md#_security_attribute_gly) una query sul pacchetto di sicurezza CredSSP (Credential Security Support Provider) per determinati attributi di un contesto di sicurezza.

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

Handle per il contesto di sicurezza su cui eseguire query.

</dd> <dt>

*ulAttribute* \[ Pollici\]
</dt> <dd>

Attributo del contesto da restituire. Questo parametro può avere uno dei valori seguenti. Se non diversamente specificato, gli attributi sono applicabili sia al client che al server.



| Valore                                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_C_ACCESS_TOKEN"></span><span id="secpkg_attr_c_access_token"></span><dl> <dt>**SECPKG \_ Token di \_ \_ ACCESSO \_ ATTR C**</dt> <dt>0x80000012</dt> </dl>                                 | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) che specifica il token di accesso per il contesto di sicurezza corrente.<br/> Questo attributo è supportato solo nel server.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></span><span id="secpkg_attr_c_full_access_token"></span><dl> <dt>**SECPKG \_ Token DI ACCESSO COMPLETO ATTR \_ \_ \_ \_ C**</dt> <dt>0x80000082</dt> </dl>                 | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) che specifica il token di accesso per il contesto di sicurezza corrente.<br/> Questo attributo è supportato solo nel server.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_CERT_TRUST_STATUS"></span><span id="secpkg_attr_cert_trust_status"></span><dl> <dt>**SECPKG \_ ATTR \_ CERT \_ TRUST STATUS \_ 0x80000084**</dt> <dt></dt> </dl>                        | Il *parametro pBuffer* contiene un puntatore a una [**struttura CERT TRUST \_ \_ STATUS**](/windows/win32/api/wincrypt/ns-wincrypt-cert_trust_status) che specifica le informazioni di attendibilità sul certificato.<br/> Questo attributo è supportato solo nel client.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_CREDS"></span><span id="secpkg_attr_creds"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS**</dt> <dt>0x80000080</dt> </dl>                                                              | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) che specifica le credenziali client.<br/> Le credenziali client possono essere nome utente e password o nome utente e smart card PIN.<br/> Questo attributo è supportato solo nel server.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS \_ 2**</dt> <dt>0x80000086</dt> </dl>                                                       | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) che specifica le credenziali client. <br/> Se le credenziali client sono nome utente e password, il buffer è una struttura [**KERB \_ INTERACTIVE LOGON \_ imballata.**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon)<br/> Se la credenziale client è il nome utente smart card PIN, il buffer è una struttura [**KERB \_ CERTIFICATE LOGON \_ imballata.**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon)<br/> Se la credenziale client è una credenziale di identità online, il buffer è una struttura [**\_ SEC WINNT \_ AUTH IDENTITY \_ \_ EX2 con**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) marshalling.<br/> Questo attributo è supportato solo nel server CredSSP.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> |
| <span id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></span><span id="secpkg_attr_negotiation_package"></span><dl> <dt>**SECPKG \_ PACCHETTO DI \_ \_ NEGOZIAZIONE ATTR**</dt> <dt>0x80000081</dt> </dl>                   | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) che specifica il nome del pacchetto di autenticazione negoziato dal provider [Microsoft Negotiate.](microsoft-negotiate.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ INFORMAZIONI SUL \_ \_ PACCHETTO ATTR**</dt> <dt>10</dt> </dl>                                                | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ PackageInfo.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)<br/> Restituisce informazioni sul provider di servizi condivisi in uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></span><span id="secpkg_attr_server_auth_flags"></span><dl> <dt>**SECPKG \_ FLAG DI \_ AUTENTICAZIONE DEL SERVER \_ ATTR \_**</dt> <dt>0x80000083</dt> </dl>                        | Il *parametro pBuffer* contiene un puntatore a [**una struttura SecPkgContext \_ Flags**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) che specifica informazioni sui flag nel contesto di sicurezza corrente.<br/> Questo attributo è supportato solo nel client.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ Dimensioni \_ ATTR**</dt> <dt>0x0</dt> </dl>                                                                     | Il *parametro pBuffer* contiene un puntatore a una [**struttura SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)<br/> Esegue query sulle dimensioni delle strutture usate nelle funzioni per messaggio e negli scambi di autenticazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></span><span id="secpkg_attr_subject_security_attributes"></span><dl> <dt>**SECPKG \_ ATTR \_ SUBJECT \_ SECURITY \_ ATTRIBUTES**</dt> <dt>124</dt> </dl> | Il *parametro pBuffer* contiene un puntatore a una [**struttura \_ SubjectAttributes SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_subjectattributes)<br/> Questo valore restituisce informazioni sugli attributi di sicurezza per la connessione.<br/> Questo valore è supportato solo nel server CredSSP.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pBuffer* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura che riceve gli attributi. Il tipo di struttura dipende dal valore del *parametro ulAttribute.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, può restituire i codici di errore seguenti.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ HANDLE \_ NON**</dt> VALIDO <dt>0x80100003</dt> </dl>       | La funzione non è riuscita. Il *parametro phContext* specifica un handle per un contesto incompleto.<br/> |
| <dl> <dt>**SEC \_ E \_ FUNZIONE NON SUPPORTATA \_ 0x80090302**</dt> <dt></dt> </dl> | La funzione non è riuscita. Il valore del *parametro ulAttribute* non è valido.<br/>                 |



 

## <a name="remarks"></a>Commenti

La struttura a cui punta il *parametro pBuffer* varia a seconda dell'attributo sottoposto a query.

Mentre il chiamante deve allocare la struttura *pBuffer* stessa, il provider di servizi condivisi alloca la memoria necessaria per contenere membri di dimensioni variabili della *struttura pBuffer.* La memoria allocata dal provider di servizi condivisi deve essere liberata chiamando la [**funzione FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                   |
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

[**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)
</dt> <dt>

[**Dimensioni \_ secPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> </dl>

 

 
