---
description: È necessario prestare attenzione quando si usa il Security Support Provider Kerberos (SSP) se l'interoperabilità con GSSAPI è un requisito.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: Interoperabilità SSPI/Kerberos con GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9efaae6b2433d76dff290d57e27e893885692a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749599"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a>Interoperabilità SSPI/Kerberos con GSSAPI

È necessario prestare attenzione quando si usa il [*Security Support Provider*](../secgloss/s-gly.md) [*Kerberos*](../secgloss/k-gly.md) (SSP) se l'interoperabilità con GSSAPI è un requisito. Le convenzioni di codice seguenti consentono l'interoperabilità con le applicazioni basate su GSSAPI:

-   [Nomi compatibili con Windows](#windows-compatible-names)
-   [autenticazione](#authentication)
-   [Integrità e privacy dei messaggi](#message-integrity-and-privacy)

È possibile trovare il codice di esempio nel Software Development Kit (SDK) della piattaforma in esempi di \\ sicurezza \\ SSPI \\ GSS. Inoltre, l'esempio UNIX equivalente viene distribuito nelle distribuzioni Kerberos MIT e Heimdal, client e server GSS.

## <a name="windows-compatible-names"></a>Nomi Windows-Compatible

Le funzioni GSSAPI utilizzano un formato di nome noto \_ come \_ nome del servizio NT GSS \_ come specificato nella RFC. Ad esempio, sample@host.dom.com è un nome che può essere usato in un'applicazione basata su GSSAPI. Il sistema operativo Windows non riconosce il formato del \_ nome del servizio NT GSS \_ \_ ed è necessario utilizzare il nome completo dell' [*entità servizio*](../secgloss/s-gly.md), ad esempio sample/host.dom.com@REALM .

## <a name="authentication"></a>Authentication

L'autenticazione viene in genere gestita quando una connessione viene configurata per la prima volta tra un client e un server. In questo esempio, il client utilizza [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) e il server utilizza GSSAPI.

**Per impostare l'autenticazione nel client SSPI**

1.  Ottenere le [*credenziali*](../secgloss/c-gly.md) in uscita usando [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).
2.  Creare un nome di servizio con il **\_ nome di importazione GSS \_ ()** e ottenere le credenziali in ingresso usando **GSS \_ acquire \_ cred**.
3.  Ottenere un token di autenticazione da inviare al server utilizzando [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
4.  Inviare il token al server.

**Per configurare l'autenticazione nel server GSSAPI**

1.  Analizzare il messaggio dal client per estrarre il token di sicurezza. Utilizzare la funzione di **\_ \_ \_ contesto GSS Accept sec** , passando il token come argomento.
2.  Analizzare il messaggio dal server per estrarre il token di sicurezza. Passare il token di sicurezza a [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
3.  Inviare un token di risposta al client.

    La funzione di **\_ \_ \_ contesto GSS Accept sec** può restituire un token che è possibile inviare di nuovo al client.

4.  Se è necessario continuare, inviare un token di risposta al server. in caso contrario, l'installazione dell'autenticazione è stata completata.
5.  Se è necessario continuare, attendere il token successivo dal client; in caso contrario, l'installazione dell'autenticazione è stata completata.

## <a name="message-integrity-and-privacy"></a>Integrità e privacy dei messaggi

La maggior parte delle applicazioni basate su GSSAPI usa la funzione di **\_ wrapping GSS** per firmare un messaggio prima di inviarlo. Viceversa, la funzione di **\_ Unwrap GSS** verifica la firma. **GSS \_ Il wrapping** è disponibile nella versione 2,0 dell'API ed è ora ampiamente usato e specificato negli standard Internet che descrivono l'uso di GSSAPI per l'aggiunta della sicurezza ai protocolli. Nelle versioni precedenti le funzioni GSS **SignMessage** e **SealMessage** sono state usate per l' [*integrità*](../secgloss/i-gly.md) e la [*privacy*](../secgloss/p-gly.md)dei messaggi. **GSS \_** L' **\_ Unwrap** a capo e GSS vengono usati per l'integrità e la privacy con l'uso della privacy controllata dal valore dell'argomento "conf \_ flag".

Se viene specificato un protocollo basato su GSSAPI per l'utilizzo delle funzioni **GSS \_ get \_ MIC** e **GSS \_ Verify \_ MIC** , le funzioni SSPI corrette saranno [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature). Tenere presente che **MakeSignature** e **VerifySignature** non interagiscono con **GSS \_ Wrap** quando il \_ flag conf è impostato su zero oppure con il **\_ wrapping di GSS**. Lo stesso vale per la combinazione di [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) impostata solo per la firma e **GSS \_ Verify \_ MIC**.

> [!Note]  
> Non utilizzare le funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) o [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) quando viene chiamato il metodo **GSS \_ Wrap** e **GSS \_ Unwrap** .

 

Il valore SSPI equivalente a **GSS \_ Wrap** è [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) per l'integrità e la privacy.

Nell'esempio seguente viene illustrato l'utilizzo di [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) per firmare i dati che verranno verificati da **GSS \_ Unwrap**.

Nel client SSPI:


```C++
// Need three descriptors, two for the SSP and
// one to hold the application data. 
in_buf_desc.cBuffers = 3;
in_buf_desc.pBuffers = wrap_bufs;
in_buf_desc.ulVersion = SECBUFFER_VERSION;
wrap_bufs[0].cbBuffer = sizes.cbSecurityTrailer;
wrap_bufs[0].BufferType = SECBUFFER_TOKEN;
wrap_bufs[0].pvBuffer = malloc(sizes.cbSecurityTrailer);

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = in_buf.cbBuffer;
wrap_bufs[1].pvBuffer = malloc(wrap_bufs[1].cbBuffer);
memcpy(wrap_bufs[1].pvBuffer, in_buf.pvBuffer, in_buf.cbBuffer);
wrap_bufs[2].BufferType = SECBUFFER_PADDING;
wrap_bufs[2].cbBuffer = sizes.cbBlockSize;
wrap_bufs[2].pvBuffer = malloc(wrap_bufs[2].cbBuffer);
maj_stat = EncryptMessage(&context,
SignOnly ? KERB_WRAP_NO_ENCRYPT : 0,
&in_buf_desc, 0);

// Send a message to the server.
```



Nel server GSSAPI:


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



L'oggetto SSPI equivalente a **GSS \_ Unwrap** è [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage). Di seguito è riportato un esempio in cui viene illustrato come utilizzare **DecryptMessage (Kerberos)** per decrittografare i dati crittografati da **GSS \_ Wrap**.

Nel server GSSAPI:


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



Nel client SSPI:


```C++
wrap_buf_desc.cBuffers = 2;
wrap_buf_desc.pBuffers = wrap_bufs;
wrap_buf_desc.ulVersion = SECBUFFER_VERSION; 

// This buffer is for SSPI.
wrap_bufs[0].BufferType = SECBUFFER_STREAM;
wrap_bufs[0].pvBuffer = xmit_buf.pvBuffer;
wrap_bufs[0].cbBuffer = xmit_buf.cbBuffer;

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = 0;
wrap_bufs[1].pvBuffer = NULL;
maj_stat = DecryptMessage(
&context,
&wrap_buf_desc,
0, // no sequence number
&qop
);

// This is where the data is.
msg_buf = wrap_bufs[1];

// Check QOP of received message.
// If QOP is KERB_WRAP_NO_ENCRYPT, the message is signed only; 
// otherwise, it is encrypted.
```



 

 
