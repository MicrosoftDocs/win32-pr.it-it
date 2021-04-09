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
# <a name="sspikerberos-interoperability-with-gssapi"></a><span data-ttu-id="93e0f-103">Interoperabilità SSPI/Kerberos con GSSAPI</span><span class="sxs-lookup"><span data-stu-id="93e0f-103">SSPI/Kerberos Interoperability with GSSAPI</span></span>

<span data-ttu-id="93e0f-104">È necessario prestare attenzione quando si usa il [*Security Support Provider*](../secgloss/s-gly.md) [*Kerberos*](../secgloss/k-gly.md) (SSP) se l'interoperabilità con GSSAPI è un requisito.</span><span class="sxs-lookup"><span data-stu-id="93e0f-104">Care must be taken when using the [*Kerberos*](../secgloss/k-gly.md) [*security support provider*](../secgloss/s-gly.md) (SSP) if interoperability with GSSAPI is a requirement.</span></span> <span data-ttu-id="93e0f-105">Le convenzioni di codice seguenti consentono l'interoperabilità con le applicazioni basate su GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="93e0f-105">The following code conventions allow interoperability with GSSAPI-based applications:</span></span>

-   [<span data-ttu-id="93e0f-106">Nomi compatibili con Windows</span><span class="sxs-lookup"><span data-stu-id="93e0f-106">Windows-Compatible Names</span></span>](#windows-compatible-names)
-   [<span data-ttu-id="93e0f-107">autenticazione</span><span class="sxs-lookup"><span data-stu-id="93e0f-107">Authentication</span></span>](#authentication)
-   [<span data-ttu-id="93e0f-108">Integrità e privacy dei messaggi</span><span class="sxs-lookup"><span data-stu-id="93e0f-108">Message Integrity and Privacy</span></span>](#message-integrity-and-privacy)

<span data-ttu-id="93e0f-109">È possibile trovare il codice di esempio nel Software Development Kit (SDK) della piattaforma in esempi di \\ sicurezza \\ SSPI \\ GSS.</span><span class="sxs-lookup"><span data-stu-id="93e0f-109">You can find sample code in the Platform Software Development Kit (SDK) under Samples\\Security\\SSPI\\GSS.</span></span> <span data-ttu-id="93e0f-110">Inoltre, l'esempio UNIX equivalente viene distribuito nelle distribuzioni Kerberos MIT e Heimdal, client e server GSS.</span><span class="sxs-lookup"><span data-stu-id="93e0f-110">In addition, the equivalent UNIX sample is distributed in the MIT and Heimdal Kerberos distributions, GSS client and server.</span></span>

## <a name="windows-compatible-names"></a><span data-ttu-id="93e0f-111">Nomi Windows-Compatible</span><span class="sxs-lookup"><span data-stu-id="93e0f-111">Windows-Compatible Names</span></span>

<span data-ttu-id="93e0f-112">Le funzioni GSSAPI utilizzano un formato di nome noto \_ come \_ nome del servizio NT GSS \_ come specificato nella RFC.</span><span class="sxs-lookup"><span data-stu-id="93e0f-112">GSSAPI functions use a name format known as gss\_nt\_service\_name as specified in the RFC.</span></span> <span data-ttu-id="93e0f-113">Ad esempio, sample@host.dom.com è un nome che può essere usato in un'applicazione basata su GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="93e0f-113">For example, sample@host.dom.com is a name that can be used in a GSSAPI-based application.</span></span> <span data-ttu-id="93e0f-114">Il sistema operativo Windows non riconosce il formato del \_ nome del servizio NT GSS \_ \_ ed è necessario utilizzare il nome completo dell' [*entità servizio*](../secgloss/s-gly.md), ad esempio sample/host.dom.com@REALM .</span><span class="sxs-lookup"><span data-stu-id="93e0f-114">The Windows operating system does not recognize the gss\_nt\_service\_name format, and the full [*service principal name*](../secgloss/s-gly.md), for example sample/host.dom.com@REALM, must be used.</span></span>

## <a name="authentication"></a><span data-ttu-id="93e0f-115">Authentication</span><span class="sxs-lookup"><span data-stu-id="93e0f-115">Authentication</span></span>

<span data-ttu-id="93e0f-116">L'autenticazione viene in genere gestita quando una connessione viene configurata per la prima volta tra un client e un server.</span><span class="sxs-lookup"><span data-stu-id="93e0f-116">Authentication is usually handled when a connection is first set up between a client and a server.</span></span> <span data-ttu-id="93e0f-117">In questo esempio, il client utilizza [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) e il server utilizza GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="93e0f-117">In this sample, the client is using [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) and the server is using GSSAPI.</span></span>

<span data-ttu-id="93e0f-118">**Per impostare l'autenticazione nel client SSPI**</span><span class="sxs-lookup"><span data-stu-id="93e0f-118">**To set up authentication in the SSPI client**</span></span>

1.  <span data-ttu-id="93e0f-119">Ottenere le [*credenziali*](../secgloss/c-gly.md) in uscita usando [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span><span class="sxs-lookup"><span data-stu-id="93e0f-119">Get outbound [*credentials*](../secgloss/c-gly.md) by using [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span></span>
2.  <span data-ttu-id="93e0f-120">Creare un nome di servizio con il **\_ nome di importazione GSS \_ ()** e ottenere le credenziali in ingresso usando **GSS \_ acquire \_ cred**.</span><span class="sxs-lookup"><span data-stu-id="93e0f-120">Create a service name with **gss\_import\_name()** and get inbound credentials by using **gss\_acquire\_cred**.</span></span>
3.  <span data-ttu-id="93e0f-121">Ottenere un token di autenticazione da inviare al server utilizzando [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="93e0f-121">Get an authentication token to send to the server by using [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
4.  <span data-ttu-id="93e0f-122">Inviare il token al server.</span><span class="sxs-lookup"><span data-stu-id="93e0f-122">Send the token to the server.</span></span>

<span data-ttu-id="93e0f-123">**Per configurare l'autenticazione nel server GSSAPI**</span><span class="sxs-lookup"><span data-stu-id="93e0f-123">**To set up authentication in the GSSAPI server**</span></span>

1.  <span data-ttu-id="93e0f-124">Analizzare il messaggio dal client per estrarre il token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93e0f-124">Parse the message from the client to extract the security token.</span></span> <span data-ttu-id="93e0f-125">Utilizzare la funzione di **\_ \_ \_ contesto GSS Accept sec** , passando il token come argomento.</span><span class="sxs-lookup"><span data-stu-id="93e0f-125">Use the **gss\_accept\_sec\_context** function, passing the token as an argument.</span></span>
2.  <span data-ttu-id="93e0f-126">Analizzare il messaggio dal server per estrarre il token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93e0f-126">Parse the message from the server to extract the security token.</span></span> <span data-ttu-id="93e0f-127">Passare il token di sicurezza a [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="93e0f-127">Pass this security token to [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
3.  <span data-ttu-id="93e0f-128">Inviare un token di risposta al client.</span><span class="sxs-lookup"><span data-stu-id="93e0f-128">Send a response token to the client.</span></span>

    <span data-ttu-id="93e0f-129">La funzione di **\_ \_ \_ contesto GSS Accept sec** può restituire un token che è possibile inviare di nuovo al client.</span><span class="sxs-lookup"><span data-stu-id="93e0f-129">The **gss\_accept\_sec\_context** function can return a token that you can send back to the client.</span></span>

4.  <span data-ttu-id="93e0f-130">Se è necessario continuare, inviare un token di risposta al server. in caso contrario, l'installazione dell'autenticazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="93e0f-130">If it is necessary to continue, send a response token to the server; otherwise, the setup of authentication is complete.</span></span>
5.  <span data-ttu-id="93e0f-131">Se è necessario continuare, attendere il token successivo dal client; in caso contrario, l'installazione dell'autenticazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="93e0f-131">If it is necessary to continue, wait for the next token from the client; otherwise, the setup of authentication is complete.</span></span>

## <a name="message-integrity-and-privacy"></a><span data-ttu-id="93e0f-132">Integrità e privacy dei messaggi</span><span class="sxs-lookup"><span data-stu-id="93e0f-132">Message Integrity and Privacy</span></span>

<span data-ttu-id="93e0f-133">La maggior parte delle applicazioni basate su GSSAPI usa la funzione di **\_ wrapping GSS** per firmare un messaggio prima di inviarlo.</span><span class="sxs-lookup"><span data-stu-id="93e0f-133">Most GSSAPI-based applications use the **GSS\_Wrap** function to sign a message before sending it.</span></span> <span data-ttu-id="93e0f-134">Viceversa, la funzione di **\_ Unwrap GSS** verifica la firma.</span><span class="sxs-lookup"><span data-stu-id="93e0f-134">Conversely, the **GSS\_Unwrap** function verifies the signature.</span></span> <span data-ttu-id="93e0f-135">**GSS \_ Il wrapping** è disponibile nella versione 2,0 dell'API ed è ora ampiamente usato e specificato negli standard Internet che descrivono l'uso di GSSAPI per l'aggiunta della sicurezza ai protocolli.</span><span class="sxs-lookup"><span data-stu-id="93e0f-135">**GSS\_Wrap** is available in version 2.0 of the API and is now widely used and specified in Internet standards that describe using the GSSAPI for adding security to protocols.</span></span> <span data-ttu-id="93e0f-136">Nelle versioni precedenti le funzioni GSS **SignMessage** e **SealMessage** sono state usate per l' [*integrità*](../secgloss/i-gly.md) e la [*privacy*](../secgloss/p-gly.md)dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="93e0f-136">Earlier, the GSS **SignMessage** and **SealMessage** functions were used for message [*integrity*](../secgloss/i-gly.md) and [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="93e0f-137">**GSS \_** L' **\_ Unwrap** a capo e GSS vengono usati per l'integrità e la privacy con l'uso della privacy controllata dal valore dell'argomento "conf \_ flag".</span><span class="sxs-lookup"><span data-stu-id="93e0f-137">**GSS\_Wrap** and **GSS\_Unwrap** are used for both integrity and privacy with the use of privacy controlled by the value of the "conf\_flag" argument.</span></span>

<span data-ttu-id="93e0f-138">Se viene specificato un protocollo basato su GSSAPI per l'utilizzo delle funzioni **GSS \_ get \_ MIC** e **GSS \_ Verify \_ MIC** , le funzioni SSPI corrette saranno [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span><span class="sxs-lookup"><span data-stu-id="93e0f-138">If a GSSAPI-based protocol is specified to use the **gss\_get\_mic** and **gss\_verify\_mic** functions, the correct SSPI functions would be [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span></span> <span data-ttu-id="93e0f-139">Tenere presente che **MakeSignature** e **VerifySignature** non interagiscono con **GSS \_ Wrap** quando il \_ flag conf è impostato su zero oppure con il **\_ wrapping di GSS**.</span><span class="sxs-lookup"><span data-stu-id="93e0f-139">Be aware that **MakeSignature** and **VerifySignature** will not interoperate with **GSS\_Wrap** when conf\_flag is set to zero, or with **GSS\_Wrap**.</span></span> <span data-ttu-id="93e0f-140">Lo stesso vale per la combinazione di [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) impostata solo per la firma e **GSS \_ Verify \_ MIC**.</span><span class="sxs-lookup"><span data-stu-id="93e0f-140">The same is true for mixing [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) set for signature only and **gss\_verify\_mic**.</span></span>

> [!Note]  
> <span data-ttu-id="93e0f-141">Non utilizzare le funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) o [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) quando viene chiamato il metodo **GSS \_ Wrap** e **GSS \_ Unwrap** .</span><span class="sxs-lookup"><span data-stu-id="93e0f-141">Do not use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) or [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions when **GSS\_Wrap** and **GSS\_Unwrap** are called for.</span></span>

 

<span data-ttu-id="93e0f-142">Il valore SSPI equivalente a **GSS \_ Wrap** è [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) per l'integrità e la privacy.</span><span class="sxs-lookup"><span data-stu-id="93e0f-142">The SSPI equivalent to **GSS\_Wrap** is [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) for both integrity and privacy.</span></span>

<span data-ttu-id="93e0f-143">Nell'esempio seguente viene illustrato l'utilizzo di [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) per firmare i dati che verranno verificati da **GSS \_ Unwrap**.</span><span class="sxs-lookup"><span data-stu-id="93e0f-143">The following example shows using [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) to sign data that will be verified by **GSS\_Unwrap**.</span></span>

<span data-ttu-id="93e0f-144">Nel client SSPI:</span><span class="sxs-lookup"><span data-stu-id="93e0f-144">In the SSPI client:</span></span>


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



<span data-ttu-id="93e0f-145">Nel server GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="93e0f-145">In the GSSAPI server:</span></span>


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



<span data-ttu-id="93e0f-146">L'oggetto SSPI equivalente a **GSS \_ Unwrap** è [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="93e0f-146">The SSPI equivalent to **GSS\_Unwrap** is [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span> <span data-ttu-id="93e0f-147">Di seguito è riportato un esempio in cui viene illustrato come utilizzare **DecryptMessage (Kerberos)** per decrittografare i dati crittografati da **GSS \_ Wrap**.</span><span class="sxs-lookup"><span data-stu-id="93e0f-147">Here is an example that shows how to use **DecryptMessage (Kerberos)** to decrypt data that was encrypted by **GSS\_Wrap**.</span></span>

<span data-ttu-id="93e0f-148">Nel server GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="93e0f-148">In the GSSAPI server:</span></span>


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



<span data-ttu-id="93e0f-149">Nel client SSPI:</span><span class="sxs-lookup"><span data-stu-id="93e0f-149">In the SSPI client:</span></span>


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



 

 
