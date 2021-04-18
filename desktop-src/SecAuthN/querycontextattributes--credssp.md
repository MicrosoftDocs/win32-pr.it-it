---
description: Consente a un'applicazione di trasporto di eseguire una query sul pacchetto di sicurezza Credential Security Support Provider (CredSSP) per determinati attributi di un contesto di sicurezza.
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
title: Funzione QueryContextAttributes (CredSSP) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 191c3c8d3b2b5bd829aaf8eb45bacadbbd2bbade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313725"
---
# <a name="querycontextattributes-credssp-function"></a>Funzione QueryContextAttributes (CredSSP)

La funzione **QueryContextAttributes (CredSSP)** consente a un'applicazione di trasporto di eseguire una query sul pacchetto di sicurezza Credential Security Support Provider (CredSSP) per determinati [*attributi*](../secgloss/a-gly.md#_security_attribute_gly) di un contesto di sicurezza.

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

Handle per il contesto di sicurezza su cui eseguire una query.

</dd> <dt>

*ulAttribute* \[ in\]
</dt> <dd>

Attributo del contesto da restituire. Questo parametro può avere uno dei valori seguenti. Se non diversamente specificato, gli attributi sono applicabili sia al client che al server.



| Valore                                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_C_ACCESS_TOKEN"></span><span id="secpkg_attr_c_access_token"></span><dl> <dt>**SECPKG \_ 0x80000012 \_ \_ \_ token di accesso attr C**</dt> <dt></dt> </dl>                                 | Il parametro *pbuffer* contiene un puntatore a una struttura [**SecPkgContext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) che specifica il token di accesso per il contesto di sicurezza corrente.<br/> Questo attributo è supportato solo nel server.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></span><span id="secpkg_attr_c_full_access_token"></span><dl> <dt>**SECPKG \_ 0x80000082 \_ \_ token di \_ accesso \_ completo attr C**</dt> <dt></dt> </dl>                 | Il parametro *pbuffer* contiene un puntatore a una struttura [**SecPkgContext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) che specifica il token di accesso per il contesto di sicurezza corrente.<br/> Questo attributo è supportato solo nel server.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_CERT_TRUST_STATUS"></span><span id="secpkg_attr_cert_trust_status"></span><dl> <dt>**SECPKG \_ ATTR \_ CERT \_ trust \_ status**</dt> <dt>0x80000084</dt> </dl>                        | Il parametro *pbuffer* contiene un puntatore a una struttura di [**\_ \_ stato di attendibilità CERT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_trust_status) che specifica le informazioni sull'attendibilità del certificato.<br/> Questo attributo è supportato solo nel client.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_CREDS"></span><span id="secpkg_attr_creds"></span><dl> <dt>**SECPKG \_ ATTR \_ credenziali**</dt> <dt>0x80000080</dt> </dl>                                                              | Il parametro *pbuffer* contiene un puntatore a una struttura [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) che specifica le credenziali client.<br/> Le credenziali client possono essere nome utente e password oppure il nome utente e il PIN della smart card.<br/> Questo attributo è supportato solo nel server.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ credenziali \_ 2**</dt> <dt>0x80000086</dt> </dl>                                                       | Il parametro *pbuffer* contiene un puntatore a una struttura [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) che specifica le credenziali client. <br/> Se la credenziale client è il nome utente e la password, il buffer è una struttura di [**\_ \_ accesso interattivo per marciapiede**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) compresso.<br/> Se la credenziale client corrisponde al nome utente e al PIN della smart card, il buffer è una struttura di [**\_ \_ accesso al certificato a cordolo**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) compresso.<br/> Se la credenziale client è una credenziale di identità online, il buffer è una struttura [**\_ \_ \_ \_ EX2 dell'identità auth**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) del marshalling al secondo.<br/> Questo attributo è supportato solo nel server CredSSP.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.<br/> |
| <span id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></span><span id="secpkg_attr_negotiation_package"></span><dl> <dt>**SECPKG \_ 0x80000081 \_ \_ pacchetto di negoziazione attr**</dt> <dt></dt> </dl>                   | Il parametro *pbuffer* contiene un puntatore a una struttura [**SecPkgContext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) che specifica il nome del pacchetto di autenticazione negoziato dal provider [Microsoft Negotiate](microsoft-negotiate.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informazioni sul pacchetto attr**</dt> <dt>10</dt> </dl>                                                | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ PackageInfo di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkginfoa).<br/> Restituisce informazioni sul provider di servizi condivisi in uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></span><span id="secpkg_attr_server_auth_flags"></span><dl> <dt>**SECPKG \_ \_Flag di \_ autenticazione \_ Server attr**</dt> <dt>0x80000083</dt> </dl>                        | Il parametro *pbuffer* contiene un puntatore a una struttura di [**\_ flag SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) che specifica informazioni sui flag nel contesto di sicurezza corrente.<br/> Questo attributo è supportato solo nel client.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ ATTR \_ dimensioni**</dt> <dt>0x0</dt> </dl>                                                                     | Il parametro *pbuffer* contiene un puntatore a una struttura di [**\_ dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .<br/> Esegue una query sulle dimensioni delle strutture utilizzate nelle funzioni per messaggio e negli scambi di autenticazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></span><span id="secpkg_attr_subject_security_attributes"></span><dl> <dt>**SECPKG \_ \_Attributi di \_ sicurezza \_ dell'oggetto attr**</dt> <dt>124</dt> </dl> | Il parametro *pbuffer* contiene un puntatore a una [**struttura \_ SubjectAttributes di SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_subjectattributes) .<br/> Questo valore restituisce informazioni sugli attributi di sicurezza per la connessione.<br/> Questo valore è supportato solo nel server CredSSP.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pbuffer* \[ out\]
</dt> <dd>

Puntatore a una struttura che riceve gli attributi. Il tipo di struttura dipende dal valore del parametro *ulAttribute* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, può restituire i codici di errore seguenti.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Sec \_ 0x80100003 \_ \_ handle non valido**</dt> <dt></dt> </dl>       | La funzione non è riuscita. Il parametro *phContext* specifica un handle per un contesto incompleto.<br/> |
| <dl> <dt>**Sec \_ E \_ \_ funzione non supportata**</dt> <dt>0X80090302</dt> </dl> | La funzione non è riuscita. Il valore del parametro *ulAttribute* non è valido.<br/>                 |



 

## <a name="remarks"></a>Commenti

La struttura a cui punta il parametro *pbuffer* varia a seconda dell'attributo sottoposto a query.

Mentre il chiamante deve allocare la struttura *pbuffer* stessa, il provider di servizi condivisi alloca qualsiasi memoria necessaria per mantenere i membri di dimensioni variabili della struttura *pbuffer* . La memoria allocata dal provider di servizi condivisi deve essere liberata chiamando la funzione [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                   |
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

[**\_ClientCreds SecPkgContext**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)
</dt> <dt>

[**\_Dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> </dl>

 

 
