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
# <a name="ssl-in-winhttp"></a>SSL in WinHTTP

I servizi HTTP di Microsoft Windows (WinHTTP) supportano le transazioni Secure Sockets Layer (SSL), inclusi i certificati client. In questo argomento vengono illustrati i concetti interessati da una transazione SSL e il modo in cui vengono gestiti mediante WinHTTP.

## <a name="secure-sockets-layer"></a>Secure Sockets Layer

SSL è uno standard consolidato per garantire transazioni HTTP sicure. SSL fornisce un meccanismo per eseguire la crittografia fino a 128 bit su tutte le transazioni tra il client e il server. Consente al client di verificare che il server appartenga a un'entità attendibile tramite l'utilizzo di certificati del server. Consente inoltre al server di confermare l'identità del client con i certificati client.

Ognuno di questi problemi di crittografia, identità del server e identità client viene negoziato nell'handshake SSL che si verifica quando un client richiede prima una risorsa da un server Secure Hypertext Transfer Protocol (HTTPS). In pratica, il client e il server presentano ciascuno un elenco di impostazioni obbligatorie e preferite. Se è possibile concordare e soddisfare un set comune di requisiti, viene stabilita una connessione SSL.

WinHTTP fornisce un'interfaccia di alto livello per l'uso di SSL. Sebbene i dettagli relativi all'handshake SSL e alla transazione vengano gestiti internamente, WinHTTP consente di recuperare i livelli di crittografia, specificare il protocollo di sicurezza e interagire con i certificati client e server. Le sezioni seguenti forniscono informazioni dettagliate sulla creazione di applicazioni basate su WinHTTP che scelgono una versione del protocollo SSL, esaminano i certificati del server e selezionano i certificati client da inviare ai server HTTPS.

## <a name="server-certificates"></a>Certificati del server

I certificati del server vengono inviati dal server al client in modo che il client possa ottenere una chiave pubblica per il server e verificare che il server sia stato verificato da un'autorità di certificazione. I certificati possono contenere vari tipi di dati. Ad esempio, un certificato X. 509 include il formato del certificato, il numero di serie del certificato, l'algoritmo usato per firmare il certificato, il nome dell'autorità di certificazione (CA) che ha emesso il certificato, il nome e la chiave pubblica dell'entità che richiede il certificato e la firma della CA.

Quando si usa il Application Programming Interface WinHTTP (API), è possibile recuperare un certificato del server chiamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e specificando il flag struct del [**certificato di \_ \_ sicurezza dell' \_ \_ opzione WinHTTP**](option-flags.md) . Il certificato del server viene restituito in una struttura di [**\_ \_ informazioni del certificato WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . Se si preferisce recuperare il contesto del certificato, specificare invece il flag di contesto del certificato del [**\_ server dell'opzione \_ \_ \_ WinHTTP**](option-flags.md) .

Se un certificato del server contiene errori, è possibile ottenere informazioni dettagliate sull'errore nella funzione di callback dello stato. La notifica di errore [**\_ \_ \_ protetto \_ stato callback WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) indica un errore con un certificato del server. Il parametro *lpvStatusInformation* contiene uno o più flag di errore dettagliati. Per ulteriori informazioni, vedere [**\_ \_ callback di stato WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .

## <a name="client-certificates"></a>Certificati client

Durante l'handshake SSL, il server potrebbe richiedere l'autenticazione. Il client viene autenticato fornendo un certificato client valido al server. WinHTTP consente di selezionare e inviare un certificato da un [*archivio certificati*](glossary.md)locale. Le sezioni seguenti descrivono il processo che fornisce i certificati client quando si usa l'API WinHTTP o l'oggetto [**WinHttpRequest**](winhttprequest.md) .

### <a name="winhttp-api"></a>API WinHTTP

Sia [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) che [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) possono non riuscire a indicare che una richiesta non è riuscita perché il server HTTPS richiede l'autenticazione. In questi casi, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per restituire un errore per il \_ \_ certificato di autenticazione client WinHTTP \_ \_ \_ necessario. Quando si riceve questo errore, usare le funzioni [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) appropriate per trovare un certificato appropriato. Indica che il certificato deve essere inviato con la richiesta successiva chiamando [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con il flag [**di \_ \_ contesto del \_ certificato \_ client dell'opzione WinHTTP**](option-flags.md) .

Nell'esempio di codice riportato di seguito viene illustrato come aprire un [*archivio certificati*](glossary.md) e individuare un certificato in base al nome del soggetto dopo che è stato restituito l'errore relativo al certificato di \_ \_ autenticazione client WinHTTP \_ \_ \_ necessario.


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



Prima di inviare nuovamente una richiesta contenente un certificato client, è possibile determinare se il livello di crittografia supportato è accettabile per l'applicazione. Chiamare [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e specificare il flag dei [**\_ flag di \_ sicurezza \_ dell'opzione WinHTTP**](option-flags.md) per determinare il livello di crittografia usato.

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a>Recupero dell'elenco delle autorità emittenti per l'autenticazione client SSL

Quando l'applicazione client WinHttp invia una richiesta a un server HTTP protetto che richiede l'autenticazione del client SSL, WinHttp restituisce un errore relativo al certificato di **\_ autenticazione del \_ client WinHTTP \_ \_ \_ necessario** se l'applicazione non ha fornito un certificato client. Per i computer che eseguono Windows Server 2008 e Windows Vista, WinHttp consente all'applicazione di recuperare l'elenco di autorità di certificazione fornito dal server nella richiesta di autenticazione. L'elenco di autorità emittenti specifica un elenco di autorità di certificazione (CAs) autorizzate dal server per emettere certificati client. L'applicazione filtra l'elenco delle autorità emittenti per ottenere il certificato richiesto.

L'applicazione client WinHttp recupera l'elenco di autorità emittenti quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce l' **errore \_ WinHTTP Client Authentication \_ \_ \_ CERT \_ needed**. Quando viene restituito questo errore, l'applicazione chiama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con l'opzione per l' **\_ elenco dell' \_ \_ \_ emittente \_ del certificato client dell'opzione WinHTTP** . Il parametro *lpBuffer* deve essere sufficientemente grande da contenere un puntatore alla struttura [ \_ IssuerListInfoEx di SecPkgContext](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) . Nell'esempio di codice seguente viene illustrato come recuperare l'elenco di autorità di certificazione.


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



Le informazioni contenute nella struttura [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cIssuers* e *aIssuers*, possono essere usate per cercare il certificato, come illustrato nell'esempio di codice riportato di seguito. Per ulteriori informazioni, vedere [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).


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



### <a name="optional-client-ssl-certificates"></a>Certificati SSL client facoltativi

A partire da Windows Server 2008 e Windows Vista, l'API WinHttp supporta i certificati client facoltativi. Quando il server richiede un certificato client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce un errore relativo al certificato di **autenticazione del \_ \_ client WinHTTP \_ \_ \_ necessario** . Se il server richiede il certificato ma non lo richiede, l'applicazione può specificare questa opzione per indicare che non dispone di un certificato. Il server può scegliere un altro schema di autenticazione o consentire l'accesso anonimo al server. L'applicazione specifica la macro del **contesto del certificato del \_ \_ client WinHTTP \_ \_ Nessuna** nel parametro *lpBuffer* di [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , come illustrato nell'esempio di codice seguente.

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

Se non è impostato **\_ alcun \_ \_ \_ contesto** del certificato client e il server richiede ancora un certificato client, può inviare un codice di stato HTTP 403. Per ulteriori informazioni, vedere l'opzione **WinHTTP opzione \_ \_ client \_ CERT \_ Issuer \_ List** .

### <a name="winhttprequest-object"></a>Oggetto WinHttpRequest

Usare il metodo [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) dell'oggetto [**WinHttpRequest**](winhttprequest.md) per selezionare i certificati client da inviare al server con una richiesta. Selezionare un certificato specificando una stringa di selezione del certificato con il metodo [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) . La stringa di selezione del certificato è costituita dal percorso del certificato, dall' [*archivio certificati*](glossary.md)e dal nome soggetto delimitati da barre rovesciate. Nella tabella seguente sono elencati i componenti per questa stringa di selezione.



| Componente                                                  | Descrizione                                                                                                                                                                                        | Valori possibili                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Location                                                   | Determina la chiave del registro di sistema in cui sono archiviati i certificati.                                                                                                                               | I valori possibili sono " \_ computer locale" per indicare che l' [*archivio certificati*](glossary.md) si trova sotto il **\_ \_ computer locale HKEY**<br/> e " \_ utente corrente" per indicare che l' *archivio certificati* si trova sotto l'**utente corrente di hKey non rappresentato \_ \_ .**<br/> Questo componente fa distinzione tra maiuscole e minuscole. |
| [*Archivio certificati*](glossary.md) | Indica il nome dell' [*archivio certificati*](glossary.md) che contiene il certificato pertinente.                                                                       | Gli [*archivi certificati*](glossary.md) tipici sono "My", "root" e "TrustedPeople". Questo componente fa distinzione tra maiuscole e minuscole.                                                                                                                                                                                          |
| Nome oggetto                                               | Identifica un certificato nell' [*archivio certificati*](glossary.md)specificato. Il primo certificato che contiene la stringa specificata per questo componente è selezionato. | Il nome del soggetto può essere qualsiasi stringa. Una stringa vuota indica che deve essere utilizzato il primo certificato nell' [*archivio certificati*](glossary.md) . Questo componente non fa distinzione tra maiuscole e minuscole.                                                                                                                         |



 

Il nome e il percorso dell' [*archivio certificati*](glossary.md) sono componenti facoltativi. Tuttavia, se si specifica un *archivio certificati*, è necessario specificare anche il percorso dell' *archivio certificati*. Il percorso predefinito è l' \_ utente corrente e l' *archivio certificati* predefinito è "My".

Nell'esempio di codice seguente viene illustrato come specificare che un certificato con l'oggetto "My Middle-Tier certificate" deve essere scelto dall' [*archivio certificati*](glossary.md) "personali" nel registro di sistema in **HKEY \_ Local \_ computer**.

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> In alcuni linguaggi la barra rovesciata è un carattere di escape. Ricordarsi di modificare la stringa di selezione del certificato per tenerne conto. In Microsoft JScript, ad esempio, usare due barre rovesciate adiacenti anziché una.

 

Se non si specifica un certificato e un server HTTPS richiede un certificato client, WinHTTP seleziona il primo certificato nell' [*archivio certificati*](glossary.md)predefinito. Se non esistono certificati, viene generato un errore. Se il certificato non viene accettato, il server restituisce un codice di stato 403 per indicare che non è possibile soddisfare la richiesta. È quindi possibile scegliere un certificato più appropriato con [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) e inviare di nuovo la richiesta.

 

