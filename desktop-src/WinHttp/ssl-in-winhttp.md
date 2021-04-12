---
description: I servizi HTTP di Microsoft Windows (WinHTTP) supportano le transazioni Secure Sockets Layer (SSL), inclusi i certificati client. In questo argomento vengono illustrati i concetti interessati da una transazione SSL e il modo in cui vengono gestiti mediante WinHTTP.
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: SSL in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7952bb9a0227017927452502352c0354e69079c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232025"
---
# <a name="ssl-in-winhttp"></a><span data-ttu-id="704fe-104">SSL in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="704fe-104">SSL in WinHTTP</span></span>

<span data-ttu-id="704fe-105">I servizi HTTP di Microsoft Windows (WinHTTP) supportano le transazioni Secure Sockets Layer (SSL), inclusi i certificati client.</span><span class="sxs-lookup"><span data-stu-id="704fe-105">Microsoft Windows HTTP Services (WinHTTP) supports Secure Sockets Layer (SSL) transactions including client certificates.</span></span> <span data-ttu-id="704fe-106">In questo argomento vengono illustrati i concetti interessati da una transazione SSL e il modo in cui vengono gestiti mediante WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="704fe-106">This topic explains concepts involved in an SSL transaction and how they are handled using WinHTTP.</span></span>

## <a name="secure-sockets-layer"></a><span data-ttu-id="704fe-107">Secure Sockets Layer</span><span class="sxs-lookup"><span data-stu-id="704fe-107">Secure Sockets Layer</span></span>

<span data-ttu-id="704fe-108">SSL è uno standard consolidato per garantire transazioni HTTP sicure.</span><span class="sxs-lookup"><span data-stu-id="704fe-108">SSL is an established standard for ensuring secure HTTP transactions.</span></span> <span data-ttu-id="704fe-109">SSL fornisce un meccanismo per eseguire la crittografia fino a 128 bit su tutte le transazioni tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="704fe-109">SSL provides a mechanism to perform up to 128-bit encryption on all transactions between the client and server.</span></span> <span data-ttu-id="704fe-110">Consente al client di verificare che il server appartenga a un'entità attendibile tramite l'utilizzo di certificati del server.</span><span class="sxs-lookup"><span data-stu-id="704fe-110">It enables the client to verify that the server belongs to a trusted entity through the use of server certificates.</span></span> <span data-ttu-id="704fe-111">Consente inoltre al server di confermare l'identità del client con i certificati client.</span><span class="sxs-lookup"><span data-stu-id="704fe-111">It also enables the server to confirm the identity of the client with client certificates.</span></span>

<span data-ttu-id="704fe-112">Ognuno di questi problemi di crittografia, identità del server e identità client viene negoziato nell'handshake SSL che si verifica quando un client richiede prima una risorsa da un server Secure Hypertext Transfer Protocol (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="704fe-112">Each of these issues encryption, server identity, and client identity are negotiated in the SSL handshake that occurs when a client first requests a resource from a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span> <span data-ttu-id="704fe-113">In pratica, il client e il server presentano ciascuno un elenco di impostazioni obbligatorie e preferite.</span><span class="sxs-lookup"><span data-stu-id="704fe-113">Essentially, the client and server each present a list of required and preferred settings.</span></span> <span data-ttu-id="704fe-114">Se è possibile concordare e soddisfare un set comune di requisiti, viene stabilita una connessione SSL.</span><span class="sxs-lookup"><span data-stu-id="704fe-114">If a common set of requirements can be agreed upon and met, an SSL connection is established.</span></span>

<span data-ttu-id="704fe-115">WinHTTP fornisce un'interfaccia di alto livello per l'uso di SSL.</span><span class="sxs-lookup"><span data-stu-id="704fe-115">WinHTTP provides a high level interface for using SSL.</span></span> <span data-ttu-id="704fe-116">Sebbene i dettagli relativi all'handshake SSL e alla transazione vengano gestiti internamente, WinHTTP consente di recuperare i livelli di crittografia, specificare il protocollo di sicurezza e interagire con i certificati client e server.</span><span class="sxs-lookup"><span data-stu-id="704fe-116">While the details of the SSL handshake and transaction are handled internally, WinHTTP enables you to retrieve encryption levels, specify the security protocol, and interact with server and client certificates.</span></span> <span data-ttu-id="704fe-117">Le sezioni seguenti forniscono informazioni dettagliate sulla creazione di applicazioni basate su WinHTTP che scelgono una versione del protocollo SSL, esaminano i certificati del server e selezionano i certificati client da inviare ai server HTTPS.</span><span class="sxs-lookup"><span data-stu-id="704fe-117">The following sections provide details on creating WinHTTP based applications that elect an SSL protocol version, examine server certificates, and select client certificates to send to HTTPS servers.</span></span>

## <a name="server-certificates"></a><span data-ttu-id="704fe-118">Certificati del server</span><span class="sxs-lookup"><span data-stu-id="704fe-118">Server Certificates</span></span>

<span data-ttu-id="704fe-119">I certificati del server vengono inviati dal server al client in modo che il client possa ottenere una chiave pubblica per il server e verificare che il server sia stato verificato da un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="704fe-119">Server certificates are sent from the server to the client so that the client can obtain a public key for the server and ensure that the server has been verified by a certification authority.</span></span> <span data-ttu-id="704fe-120">I certificati possono contenere vari tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="704fe-120">Certificates can contain different types of data.</span></span> <span data-ttu-id="704fe-121">Ad esempio, un certificato X. 509 include il formato del certificato, il numero di serie del certificato, l'algoritmo usato per firmare il certificato, il nome dell'autorità di certificazione (CA) che ha emesso il certificato, il nome e la chiave pubblica dell'entità che richiede il certificato e la firma della CA.</span><span class="sxs-lookup"><span data-stu-id="704fe-121">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the certification authority (CA) that issued the certificate, the name and public key of the entity that requests the certificate, and the CA's signature.</span></span>

<span data-ttu-id="704fe-122">Quando si usa il Application Programming Interface WinHTTP (API), è possibile recuperare un certificato del server chiamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e specificando il flag struct del [**certificato di \_ \_ sicurezza dell' \_ \_ opzione WinHTTP**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="704fe-122">When using the WinHTTP  application programming interface (API), you can retrieve a server certificate by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specifying the [**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**](option-flags.md) flag.</span></span> <span data-ttu-id="704fe-123">Il certificato del server viene restituito in una struttura di [**\_ \_ informazioni del certificato WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="704fe-123">The server certificate is returned in a [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="704fe-124">Se si preferisce recuperare il contesto del certificato, specificare invece il flag di contesto del certificato del [**\_ server dell'opzione \_ \_ \_ WinHTTP**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="704fe-124">If you prefer to retrieve the certificate context, specify the [**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**](option-flags.md) flag instead.</span></span>

<span data-ttu-id="704fe-125">Se un certificato del server contiene errori, è possibile ottenere informazioni dettagliate sull'errore nella funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="704fe-125">If a server certificate contains errors, details about the error can be obtained in the status callback function.</span></span> <span data-ttu-id="704fe-126">La notifica di errore [**\_ \_ \_ protetto \_ stato callback WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) indica un errore con un certificato del server.</span><span class="sxs-lookup"><span data-stu-id="704fe-126">The [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification indicates an error with a server certificate.</span></span> <span data-ttu-id="704fe-127">Il parametro *lpvStatusInformation* contiene uno o più flag di errore dettagliati.</span><span class="sxs-lookup"><span data-stu-id="704fe-127">The *lpvStatusInformation* parameter contains one or more detailed error flags.</span></span> <span data-ttu-id="704fe-128">Per ulteriori informazioni, vedere [**\_ \_ callback di stato WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="704fe-128">See [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) for more information.</span></span>

## <a name="client-certificates"></a><span data-ttu-id="704fe-129">Certificati client</span><span class="sxs-lookup"><span data-stu-id="704fe-129">Client Certificates</span></span>

<span data-ttu-id="704fe-130">Durante l'handshake SSL, il server potrebbe richiedere l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="704fe-130">During the SSL handshake, the server might require authentication.</span></span> <span data-ttu-id="704fe-131">Il client viene autenticato fornendo un certificato client valido al server.</span><span class="sxs-lookup"><span data-stu-id="704fe-131">The client is authenticated by supplying a valid client certificate to the server.</span></span> <span data-ttu-id="704fe-132">WinHTTP consente di selezionare e inviare un certificato da un [*archivio certificati*](glossary.md)locale.</span><span class="sxs-lookup"><span data-stu-id="704fe-132">WinHTTP enables you to select and send a certificate from a local [*certificate store*](glossary.md).</span></span> <span data-ttu-id="704fe-133">Le sezioni seguenti descrivono il processo che fornisce i certificati client quando si usa l'API WinHTTP o l'oggetto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="704fe-133">The following sections describe the process that provides client certificates when using either the WinHTTP API or the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

### <a name="winhttp-api"></a><span data-ttu-id="704fe-134">API WinHTTP</span><span class="sxs-lookup"><span data-stu-id="704fe-134">WinHTTP API</span></span>

<span data-ttu-id="704fe-135">Sia [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) che [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) possono non riuscire a indicare che una richiesta non è riuscita perché il server HTTPS richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="704fe-135">Both [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) and [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) can fail to indicate that a request was unsuccessful because the HTTPS server requires authentication.</span></span> <span data-ttu-id="704fe-136">In questi casi, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per restituire un errore per il \_ \_ certificato di autenticazione client WinHTTP \_ \_ \_ necessario.</span><span class="sxs-lookup"><span data-stu-id="704fe-136">In these cases, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to returns ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED.</span></span> <span data-ttu-id="704fe-137">Quando si riceve questo errore, usare le funzioni [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) appropriate per trovare un certificato appropriato.</span><span class="sxs-lookup"><span data-stu-id="704fe-137">Upon receiving this error, use the appropriate [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) functions to find an appropriate certificate.</span></span> <span data-ttu-id="704fe-138">Indica che il certificato deve essere inviato con la richiesta successiva chiamando [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con il flag [**di \_ \_ contesto del \_ certificato \_ client dell'opzione WinHTTP**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="704fe-138">Indicate that this certificate should be sent with the next request by calling [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the [**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**](option-flags.md) flag.</span></span>

<span data-ttu-id="704fe-139">Nell'esempio di codice riportato di seguito viene illustrato come aprire un [*archivio certificati*](glossary.md) e individuare un certificato in base al nome del soggetto dopo che è stato restituito l'errore relativo al certificato di \_ \_ autenticazione client WinHTTP \_ \_ \_ necessario.</span><span class="sxs-lookup"><span data-stu-id="704fe-139">The following code example shows how to open a [*certificate store*](glossary.md) and locate a certificate based on subject name after the ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED error has been returned.</span></span>


```C++
  if( !WinHttpReceiveResponse( hRequest, NULL ) )
  {
    if( GetLastError( ) == ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED )
    {
      //MY is the store the certificate is in.
      hMyStore = CertOpenSystemStore( 0, TEXT("MY") );
      if( hMyStore )
      {
        pCertContext = CertFindCertificateInStore( hMyStore,
             X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
             0,
             CERT_FIND_SUBJECT_STR,
             (LPVOID) szCertName, //Subject string in the certificate.
             NULL );
        if( pCertContext )
        {
          WinHttpSetOption( hRequest, 
                            WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                            (LPVOID) pCertContext, 
                            sizeof(CERT_CONTEXT) );
          CertFreeCertificateContext( pCertContext );
        }
        CertCloseStore( hMyStore, 0 );

        // NOTE: Application should now resend the request.
      }
    }
  }
```



<span data-ttu-id="704fe-140">Prima di inviare nuovamente una richiesta contenente un certificato client, è possibile determinare se il livello di crittografia supportato è accettabile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="704fe-140">Before resending a request that contains a client certificate, you can determine if the supported level of encryption is acceptable for your application.</span></span> <span data-ttu-id="704fe-141">Chiamare [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e specificare il flag dei [**\_ flag di \_ sicurezza \_ dell'opzione WinHTTP**](option-flags.md) per determinare il livello di crittografia usato.</span><span class="sxs-lookup"><span data-stu-id="704fe-141">Call [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specify the [**WINHTTP\_OPTION\_SECURITY\_FLAGS**](option-flags.md) flag to determine the level of encryption that is used.</span></span>

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a><span data-ttu-id="704fe-142">Recupero dell'elenco delle autorità emittenti per l'autenticazione client SSL</span><span class="sxs-lookup"><span data-stu-id="704fe-142">Issuer List Retrieval for SSL Client Authentication</span></span>

<span data-ttu-id="704fe-143">Quando l'applicazione client WinHttp invia una richiesta a un server HTTP protetto che richiede l'autenticazione del client SSL, WinHttp restituisce un errore relativo al certificato di **\_ autenticazione del \_ client WinHTTP \_ \_ \_ necessario** se l'applicazione non ha fornito un certificato client.</span><span class="sxs-lookup"><span data-stu-id="704fe-143">When the WinHttp client application sends a request to a secure HTTP server that requires SSL client authentication, WinHttp returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** if the application has not supplied a client certificate.</span></span> <span data-ttu-id="704fe-144">Per i computer che eseguono Windows Server 2008 e Windows Vista, WinHttp consente all'applicazione di recuperare l'elenco di autorità di certificazione fornito dal server nella richiesta di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="704fe-144">For computers running on Windows Server 2008 and Windows Vista, WinHttp enables the application to retrieve the certificate issuer list supplied by the server in the authentication challenge.</span></span> <span data-ttu-id="704fe-145">L'elenco di autorità emittenti specifica un elenco di autorità di certificazione (CAs) autorizzate dal server per emettere certificati client.</span><span class="sxs-lookup"><span data-stu-id="704fe-145">The Issuer List specifies a list of Certificate Authorities (CAs) that are authorized by the server to issue client certificates.</span></span> <span data-ttu-id="704fe-146">L'applicazione filtra l'elenco delle autorità emittenti per ottenere il certificato richiesto.</span><span class="sxs-lookup"><span data-stu-id="704fe-146">The application filters the issuer list to obtain the required certificate.</span></span>

<span data-ttu-id="704fe-147">L'applicazione client WinHttp recupera l'elenco di autorità emittenti quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce l' **errore \_ WinHTTP Client Authentication \_ \_ \_ CERT \_ needed**.</span><span class="sxs-lookup"><span data-stu-id="704fe-147">The WinHttp client application retrieves the issuer list when [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="704fe-148">Quando viene restituito questo errore, l'applicazione chiama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con l'opzione per l' **\_ elenco dell' \_ \_ \_ emittente \_ del certificato client dell'opzione WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="704fe-148">When this error is returned, the application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="704fe-149">Il parametro *lpBuffer* deve essere sufficientemente grande da contenere un puntatore alla struttura [ \_ IssuerListInfoEx di SecPkgContext](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) .</span><span class="sxs-lookup"><span data-stu-id="704fe-149">The *lpBuffer* parameter must be large enough to contain a pointer to the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure.</span></span> <span data-ttu-id="704fe-150">Nell'esempio di codice seguente viene illustrato come recuperare l'elenco di autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="704fe-150">The following code example shows how to retrieve the issuer list.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <schannel.h>

//...

void GetIssuerList(HINTERNET hRequest)
{
  SecPkgContext_IssuerListInfoEx* pIssuerList = NULL;
  DWORD dwBufferSize = sizeof(SecPkgContext_IssuerListInfoEx*);

  if (WinHttpQueryOption(hRequest,
           WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST,
           &pIssuerList,
           &dwBufferSize) == TRUE)
  {
    // Use the pIssuerList for cert store filtering.
    GlobalFree(pIssuerList); // Free the issuer list when done.
  }
}
```



<span data-ttu-id="704fe-151">Le informazioni contenute nella struttura [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cIssuers* e *aIssuers*, possono essere usate per cercare il certificato, come illustrato nell'esempio di codice riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="704fe-151">The information in the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure, *cIssuers* and *aIssuers*, can be used to search for the certificate as shown in the code example below.</span></span> <span data-ttu-id="704fe-152">Per ulteriori informazioni, vedere [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span><span class="sxs-lookup"><span data-stu-id="704fe-152">For more information, see [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span></span>


```C++
PCERT_CONTEXT pClientCert = NULL;
PCCERT_CHAIN_CONTEXT pClientCertChain = NULL;

CERT_CHAIN_FIND_BY_ISSUER_PARA SrchCriteria;
::ZeroMemory(&SrchCriteria, sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA));
SrchCriteria.cbSize = sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA);

SrchCriteria.cIssuer = pIssuerList->cIssuers;
SrchCriteria.rgIssuer = pIssuerList->aIssuers;

pClientCertChain = CertFindChainInStore(
            hClientCertStore,
            X509_ASN_ENCODING,
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG |
            // Do not perform wire download when building chains.
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG,
            // Do not search pCacheEntry->_ClientCertStore 
            // for issuer certs.
            CERT_CHAIN_FIND_BY_ISSUER,
            &SrchCriteria,
            NULL);

if (pClientCertChain)
{
    pClientCert = (PCERT_CONTEXT) pClientCertChain->rgpChain[0]->rgpElement[0]->pCertContext;

    CertDuplicateCertificateContext(pClientCert);

    CertFreeCertificateChain(pClientCertChain);

    pClientCertChain = NULL;
}
```



### <a name="optional-client-ssl-certificates"></a><span data-ttu-id="704fe-153">Certificati SSL client facoltativi</span><span class="sxs-lookup"><span data-stu-id="704fe-153">Optional Client SSL Certificates</span></span>

<span data-ttu-id="704fe-154">A partire da Windows Server 2008 e Windows Vista, l'API WinHttp supporta i certificati client facoltativi.</span><span class="sxs-lookup"><span data-stu-id="704fe-154">Starting in Windows Server 2008 and Windows Vista, the WinHttp API supports optional client certificates.</span></span> <span data-ttu-id="704fe-155">Quando il server richiede un certificato client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce un errore relativo al certificato di **autenticazione del \_ \_ client WinHTTP \_ \_ \_ necessario** .</span><span class="sxs-lookup"><span data-stu-id="704fe-155">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** error.</span></span> <span data-ttu-id="704fe-156">Se il server richiede il certificato ma non lo richiede, l'applicazione può specificare questa opzione per indicare che non dispone di un certificato.</span><span class="sxs-lookup"><span data-stu-id="704fe-156">If the server requests the certificate, but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="704fe-157">Il server può scegliere un altro schema di autenticazione o consentire l'accesso anonimo al server.</span><span class="sxs-lookup"><span data-stu-id="704fe-157">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="704fe-158">L'applicazione specifica la macro del **contesto del certificato del \_ \_ client WinHTTP \_ \_ Nessuna** nel parametro *lpBuffer* di [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="704fe-158">The application specifies the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

<span data-ttu-id="704fe-159">Se non è impostato **\_ alcun \_ \_ \_ contesto** del certificato client e il server richiede ancora un certificato client, può inviare un codice di stato HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="704fe-159">If the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** is set, and the server still requires a client certificate, it may send a 403 HTTP status code.</span></span> <span data-ttu-id="704fe-160">Per ulteriori informazioni, vedere l'opzione **WinHTTP opzione \_ \_ client \_ CERT \_ Issuer \_ List** .</span><span class="sxs-lookup"><span data-stu-id="704fe-160">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

### <a name="winhttprequest-object"></a><span data-ttu-id="704fe-161">Oggetto WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="704fe-161">WinHttpRequest Object</span></span>

<span data-ttu-id="704fe-162">Usare il metodo [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) dell'oggetto [**WinHttpRequest**](winhttprequest.md) per selezionare i certificati client da inviare al server con una richiesta.</span><span class="sxs-lookup"><span data-stu-id="704fe-162">Use the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method of the [**WinHttpRequest**](winhttprequest.md) object to select client certificates to send to the server with a request.</span></span> <span data-ttu-id="704fe-163">Selezionare un certificato specificando una stringa di selezione del certificato con il metodo [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="704fe-163">Select a certificate by specifying a certificate selection string with the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method.</span></span> <span data-ttu-id="704fe-164">La stringa di selezione del certificato è costituita dal percorso del certificato, dall' [*archivio certificati*](glossary.md)e dal nome soggetto delimitati da barre rovesciate.</span><span class="sxs-lookup"><span data-stu-id="704fe-164">The certificate selection string consists of the certificate location, [*certificate store*](glossary.md), and subject name delimited by backslashes.</span></span> <span data-ttu-id="704fe-165">Nella tabella seguente sono elencati i componenti per questa stringa di selezione.</span><span class="sxs-lookup"><span data-stu-id="704fe-165">The following table lists components for this selection string.</span></span>



| <span data-ttu-id="704fe-166">Componente</span><span class="sxs-lookup"><span data-stu-id="704fe-166">Component</span></span>                                                  | <span data-ttu-id="704fe-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="704fe-167">Description</span></span>                                                                                                                                                                                        | <span data-ttu-id="704fe-168">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="704fe-168">Possible values</span></span>                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="704fe-169">Location</span><span class="sxs-lookup"><span data-stu-id="704fe-169">Location</span></span>                                                   | <span data-ttu-id="704fe-170">Determina la chiave del registro di sistema in cui sono archiviati i certificati.</span><span class="sxs-lookup"><span data-stu-id="704fe-170">Determines the registry key under which the certificates are stored.</span></span>                                                                                                                               | <span data-ttu-id="704fe-171">I valori possibili sono " \_ computer locale" per indicare che l' [*archivio certificati*](glossary.md) si trova sotto il **\_ \_ computer locale HKEY**</span><span class="sxs-lookup"><span data-stu-id="704fe-171">The possible values are "LOCAL\_MACHINE" to indicate that the [*certificate store*](glossary.md) is under **HKEY\_LOCAL\_MACHINE**</span></span><br/> <span data-ttu-id="704fe-172">e " \_ utente corrente" per indicare che l' *archivio certificati* si trova sotto l'**utente corrente di hKey non rappresentato \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="704fe-172">and "CURRENT\_USER" to indicate that the *certificate store* is under the non-impersonated **HKEY\_CURRENT\_USER.**</span></span><br/> <span data-ttu-id="704fe-173">Questo componente fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="704fe-173">This component is case-sensitive.</span></span> |
| [<span data-ttu-id="704fe-174">*Archivio certificati*</span><span class="sxs-lookup"><span data-stu-id="704fe-174">*Certificate store*</span></span>](glossary.md) | <span data-ttu-id="704fe-175">Indica il nome dell' [*archivio certificati*](glossary.md) che contiene il certificato pertinente.</span><span class="sxs-lookup"><span data-stu-id="704fe-175">Indicates the name of the [*certificate store*](glossary.md) that contains the relevant certificate.</span></span>                                                                       | <span data-ttu-id="704fe-176">Gli [*archivi certificati*](glossary.md) tipici sono "My", "root" e "TrustedPeople".</span><span class="sxs-lookup"><span data-stu-id="704fe-176">Typical [*certificate stores*](glossary.md) are "MY", "Root", and "TrustedPeople".</span></span> <span data-ttu-id="704fe-177">Questo componente fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="704fe-177">This component is case-sensitive.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="704fe-178">Nome oggetto</span><span class="sxs-lookup"><span data-stu-id="704fe-178">Subject name</span></span>                                               | <span data-ttu-id="704fe-179">Identifica un certificato nell' [*archivio certificati*](glossary.md)specificato.</span><span class="sxs-lookup"><span data-stu-id="704fe-179">Identifies a certificate within the specified [*certificate store*](glossary.md).</span></span> <span data-ttu-id="704fe-180">Il primo certificato che contiene la stringa specificata per questo componente è selezionato.</span><span class="sxs-lookup"><span data-stu-id="704fe-180">The first certificate that contains the string specified for this component is selected.</span></span> | <span data-ttu-id="704fe-181">Il nome del soggetto può essere qualsiasi stringa.</span><span class="sxs-lookup"><span data-stu-id="704fe-181">The subject name can be any string.</span></span> <span data-ttu-id="704fe-182">Una stringa vuota indica che deve essere utilizzato il primo certificato nell' [*archivio certificati*](glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="704fe-182">A blank string indicates that the first certificate in the [*certificate store*](glossary.md) should be used.</span></span> <span data-ttu-id="704fe-183">Questo componente non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="704fe-183">This component is case-insensitive.</span></span>                                                                                                                         |



 

<span data-ttu-id="704fe-184">Il nome e il percorso dell' [*archivio certificati*](glossary.md) sono componenti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="704fe-184">The [*certificate store*](glossary.md) name and location are optional components.</span></span> <span data-ttu-id="704fe-185">Tuttavia, se si specifica un *archivio certificati*, è necessario specificare anche il percorso dell' *archivio certificati*.</span><span class="sxs-lookup"><span data-stu-id="704fe-185">However, if you specify a *certificate store*, you must also specify the location of that *certificate store*.</span></span> <span data-ttu-id="704fe-186">Il percorso predefinito è l' \_ utente corrente e l' *archivio certificati* predefinito è "My".</span><span class="sxs-lookup"><span data-stu-id="704fe-186">The default location is CURRENT\_USER and the default *certificate store* is "MY".</span></span>

<span data-ttu-id="704fe-187">Nell'esempio di codice seguente viene illustrato come specificare che un certificato con l'oggetto "My Middle-Tier certificate" deve essere scelto dall' [*archivio certificati*](glossary.md) "personali" nel registro di sistema in **HKEY \_ Local \_ computer**.</span><span class="sxs-lookup"><span data-stu-id="704fe-187">The following code example shows how to specify that a certificate with the subject "My Middle-Tier Certificate" should be chosen from the "Personal" [*certificate store*](glossary.md) in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> <span data-ttu-id="704fe-188">In alcuni linguaggi la barra rovesciata è un carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="704fe-188">In some languages the backslash is an escape character.</span></span> <span data-ttu-id="704fe-189">Ricordarsi di modificare la stringa di selezione del certificato per tenerne conto.</span><span class="sxs-lookup"><span data-stu-id="704fe-189">Remember to modify the certificate selection string to account for this.</span></span> <span data-ttu-id="704fe-190">In Microsoft JScript, ad esempio, usare due barre rovesciate adiacenti anziché una.</span><span class="sxs-lookup"><span data-stu-id="704fe-190">For example, in Microsoft JScript, use two adjacent backslashes instead of one.</span></span>

 

<span data-ttu-id="704fe-191">Se non si specifica un certificato e un server HTTPS richiede un certificato client, WinHTTP seleziona il primo certificato nell' [*archivio certificati*](glossary.md)predefinito.</span><span class="sxs-lookup"><span data-stu-id="704fe-191">If you do not specify a certificate and an HTTPS server requires a client certificate, WinHTTP selects the first certificate in the default [*certificate store*](glossary.md).</span></span> <span data-ttu-id="704fe-192">Se non esistono certificati, viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="704fe-192">If no certificates exist, an error is raised.</span></span> <span data-ttu-id="704fe-193">Se il certificato non viene accettato, il server restituisce un codice di stato 403 per indicare che non è possibile soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="704fe-193">If the certificate is not accepted, the server returns a 403 status code to indicate that the request cannot be fulfilled.</span></span> <span data-ttu-id="704fe-194">È quindi possibile scegliere un certificato più appropriato con [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) e inviare di nuovo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="704fe-194">You can then choose a more appropriate certificate with [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) and resend the request.</span></span>

 

