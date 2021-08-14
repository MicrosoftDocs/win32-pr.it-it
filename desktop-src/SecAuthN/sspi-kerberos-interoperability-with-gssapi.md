---
description: È necessario fare attenzione quando si usa il provider di supporto per la sicurezza Kerberos se l'interoperabilità con GSSAPI è un requisito.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: Interoperabilità SSPI/Kerberos con GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5907c79fbf4ef53a40b9dc2198715f216794de5634c60c66fe3d767bfe4af026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916828"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a>Interoperabilità SSPI/Kerberos con GSSAPI

È necessario fare attenzione quando si usa il provider di [*supporto*](../secgloss/s-gly.md) per la sicurezza [*Kerberos*](../secgloss/k-gly.md) se l'interoperabilità con GSSAPI è un requisito. Le convenzioni di codice seguenti consentono l'interoperabilità con le applicazioni basate su GSSAPI:

-   [Windows nomi compatibili con gli utenti](#windows-compatible-names)
-   [autenticazione](#authentication)
-   [Integrità e privacy dei messaggi](#message-integrity-and-privacy)

Il codice di esempio è disponibile in Platform Software Development Kit (SDK) in Samples \\ Security \\ SSPI GSS (Esempi di sicurezza SSPI \\ GSS). Inoltre, l'esempio di UNIX equivalente viene distribuito nelle distribuzioni Mit e Heimdal Kerberos, nel client e nel server GSS.

## <a name="windows-compatible-names"></a>Windows-Compatible nomi

Le funzioni GSSAPI usano un formato di nome noto come gss \_ nt service name come specificato nella \_ \_ RFC. Ad esempio, sample@host.dom.com è un nome che può essere usato in un'applicazione basata su GSSAPI. Il Windows operativo non riconosce il formato del nome del servizio gss nt e deve essere usato il nome completo dell'entità servizio, ad \_ \_ \_ esempio [](../secgloss/s-gly.md) sample/host.dom.com@REALM .

## <a name="authentication"></a>Autenticazione

L'autenticazione viene in genere gestita quando si configura per la prima volta una connessione tra un client e un server. In questo esempio il client usa [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) e il server usa GSSAPI.

**Per configurare l'autenticazione nel client SSPI**

1.  Ottenere le [*credenziali in uscita*](../secgloss/c-gly.md) usando [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).
2.  Creare un nome di servizio **con gss \_ import \_ name()** e ottenere le credenziali in ingresso usando **gss \_ acquire \_ cred**.
3.  Ottenere un token di autenticazione da inviare al server tramite [**InitializeSecurityContext (Kerberos).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
4.  Inviare il token al server.

**Per configurare l'autenticazione nel server GSSAPI**

1.  Analizzare il messaggio dal client per estrarre il token di sicurezza. Usare la **funzione di contesto gss \_ accept \_ sec, \_** passando il token come argomento.
2.  Analizzare il messaggio dal server per estrarre il token di sicurezza. Passare questo token di sicurezza [**a InitializeSecurityContext (Kerberos).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
3.  Inviare un token di risposta al client.

    La **funzione di contesto gss accept \_ \_ sec \_** può restituire un token che è possibile inviare al client.

4.  Se è necessario continuare, inviare un token di risposta al server. In caso contrario, la configurazione dell'autenticazione è stata completata.
5.  Se è necessario continuare, attendere il token successivo dal client. In caso contrario, la configurazione dell'autenticazione è stata completata.

## <a name="message-integrity-and-privacy"></a>Integrità e privacy dei messaggi

La maggior parte delle applicazioni basate su GSSAPI usa la **funzione wrap \_ GSS** per firmare un messaggio prima di inviarlo. Al contrario, la **funzione GSS \_ Unwrap** verifica la firma. **GSS \_ Il** wrapping è disponibile nella versione 2.0 dell'API ed è ora ampiamente usato e specificato negli standard Internet che descrivono l'uso di GSSAPI per l'aggiunta della sicurezza ai protocolli. In precedenza, le funzioni **SignMessage** e **SealMessage** di GSS venivano usate per l'integrità [*e*](../secgloss/i-gly.md) la privacy dei [*messaggi.*](../secgloss/p-gly.md) **GSS \_ Wrap** e **GSS \_ Unwrap** vengono usati sia per l'integrità che per la privacy con l'uso della privacy controllata dal valore dell'argomento \_ "conf flag".

Se si specifica un protocollo basato su GSSAPI per usare le funzioni del microfono gss get e **gss \_ verify \_ mic,** le funzioni SSPI corrette saranno [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature). **\_ \_** Tenere presente che **MakeSignature** e **VerifySignature** non interoperabilità con **GSS \_ Wrap** quando il flag conf è impostato su zero o con \_ **GSS \_ Wrap**. Lo stesso vale per la combinazione [**di EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) impostato solo per la firma e **gss \_ verify \_ mic.**

> [!Note]  
> Non usare le [**funzioni MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) [**o VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) quando vengono chiamate le funzioni **GSS \_ Wrap** e **GSS \_ Unwrap.**

 

L'oggetto SSPI equivalente a **GSS \_ Wrap** è [**EncryptMessage (Kerberos) sia**](/windows/win32/api/sspi/nf-sspi-encryptmessage) per l'integrità che per la privacy.

L'esempio seguente illustra [**l'uso di EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) per firmare i dati che verranno verificati da **GSS \_ Unwrap**.

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



L'oggetto SSPI equivalente a **GSS \_ Unwrap** è [**DecryptMessage (Kerberos).**](/windows/win32/api/sspi/nf-sspi-decryptmessage) Di seguito è riportato un esempio che illustra come usare **DecryptMessage (Kerberos)** per decrittografare i dati crittografati da **GSS \_ Wrap**.

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



 

 
