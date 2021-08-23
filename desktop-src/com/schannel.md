---
title: SChannel
description: Il pacchetto di sicurezza Schannel (Secure Channel), il cui identificatore del servizio di autenticazione è RPC C AUTHN GSS SCHANNEL, supporta i protocolli basati su chiave pubblica \_ \_ SEGUENTI SSL \_ \_ (Secure Sockets Layer) versioni 2.0 e 3.0, Transport Layer Security (TLS) 1.0 e PCT (Private Communication Technology) 1.0. TLS 1.0 è una versione standardizzata e leggermente modificata di SSL 3.0 rilasciata dalla Internet Engineering Task Force (IETF) nel gennaio 1999, nel documento RFC 2246. Poiché TLS è stato standardizzato, gli sviluppatori sono invitati a usare TLS anziché SSL. PCT è incluso solo per la compatibilità con le versioni precedenti e non deve essere usato per il nuovo sviluppo. Quando viene usato il pacchetto di sicurezza Schannel, DCOM negozia automaticamente il protocollo migliore, a seconda delle funzionalità client e server.
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ab40ed9d87013f646137e23ccc755dfdf9ab6b8f2ded367940b4ae630d7b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047849"
---
# <a name="schannel"></a>SChannel

Il pacchetto di sicurezza Schannel (Secure Channel), il cui identificatore del servizio di autenticazione è RPC C AUTHN GSS SCHANNEL, supporta i protocolli basati su chiave pubblica \_ \_ \_ \_ seguenti: SSL (Secure Sockets Layer) versioni 2.0 e 3.0, Transport Layer Security (TLS) 1.0 e PCT (Private Communication Technology) 1.0. TLS 1.0 è una versione standardizzata e leggermente modificata di SSL 3.0 rilasciata dalla Internet Engineering Task Force (IETF) nel gennaio 1999, nel documento [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt). Poiché TLS è stato standardizzato, gli sviluppatori sono invitati a usare TLS anziché SSL. PCT è incluso solo per la compatibilità con le versioni precedenti e non deve essere usato per il nuovo sviluppo. Quando viene usato il pacchetto di sicurezza Schannel, DCOM negozia automaticamente il protocollo migliore, a seconda delle funzionalità client e server.

Gli argomenti seguenti descrivono brevemente il protocollo TLS e il suo funzionamento con DCOM.

-   [Quando usare TLS](#when-to-use-tls)
-   [Breve panoramica del funzionamento di TLS](#brief-overview-of-how-tls-works)
-   [Certificati X.509](#x509-certificates)
    -   [Certificati client](#client-certificates)
-   [Uso di TLS in COM](#using-tls-in-com)
    -   [Modalità di impostazione della protezione da parte di un server](#how-a-server-sets-the-security-blanket)
    -   [Modalità di impostazione della protezione da parte di un client](#how-a-client-sets-the-security-blanket)
    -   [Modalità di modifica della protezione da parte di un client](#how-a-client-changes-the-security-blanket)
    -   [Esempio: Il client modifica la protezione generale](#example-client-changes-the-security-blanket)
-   [Argomenti correlati](#related-topics)

> [!Note]  
> Tutte le informazioni sul protocollo TLS in queste sezioni si applicano anche ai protocolli SSL e PCT.

 

## <a name="when-to-use-tls"></a>Quando usare TLS

TLS è l'unica opzione di sicurezza disponibile quando i server devono dimostrare la propria identità ai client anonimi. Ciò è particolarmente importante per i siti Web che vogliono partecipare all'e-commerce perché consentono di proteggere la trasmissione di informazioni riservate, ad esempio i numeri di carta di credito. TLS garantisce che i clienti dell'e-commerce possano essere certi di chi stanno facendo affari perché gli viene data la prova dell'identità del server. Offre inoltre al server di e-commerce l'efficienza di non doversi preoccupare di autenticare l'identità di ogni cliente.

TLS richiede che tutti i server dimostrino la propria identità ai client. TLS offre anche la possibilità di fare in modo che i client dimostrino la propria identità ai server. Questa autenticazione reciproca può essere utile per limitare l'accesso di determinate pagine Web in una intranet aziendale di grandi dimensioni.

TLS supporta i livelli di autenticazione più elevati e offre un'architettura aperta che consente un aumento della complessità della crittografia nel tempo per tenere il passo con l'innovazione tecnologica. TLS è la scelta migliore per gli ambienti in cui si desidera il massimo livello di sicurezza per i dati in transito.

## <a name="brief-overview-of-how-tls-works"></a>Breve panoramica del funzionamento di TLS

TLS si basa su un'infrastruttura a chiave pubblica (PKI), che usa coppie di chiavi pubbliche/private per abilitare la crittografia dei dati e stabilire l'integrità dei dati e usa certificati X.509 per l'autenticazione.

Molti protocolli di sicurezza, ad esempio il protocollo Kerberos v5, dipendono da una singola chiave per crittografare e decrittografare i dati. Tali protocolli dipendono quindi dal sicuro scambio di chiavi di crittografia. nel protocollo Kerberos, questa operazione viene eseguita tramite ticket ottenuti dal Centro distribuzione chiavi (KDC). Ciò richiede che tutti gli utenti che usano il protocollo Kerberos siano registrati con il KDC, che sarebbe una limitazione poco pratica per un server Web di e-commerce destinato ad attirare milioni di clienti da tutto il mondo. TLS si basa quindi su un'infrastruttura a chiave pubblica, che usa due chiavi per la crittografia dei dati" quando una chiave della coppia crittografa i dati, solo l'altra chiave della coppia può decrittografarla. Il vantaggio principale di questa progettazione è che la crittografia può essere eseguita senza richiedere lo scambio sicuro di chiavi di crittografia.

Un'infrastruttura a chiave pubblica usa una tecnica in cui una delle chiavi viene mantenuta privata ed è disponibile solo per l'entità a cui è registrata, mentre l'altra chiave viene resa pubblica per chiunque possa accedere. Se un utente vuole inviare un messaggio privato al proprietario di una coppia di chiavi, il messaggio può essere crittografato con la chiave pubblica e solo la chiave privata può essere usata per decrittografare il messaggio.

Le coppie di chiavi vengono usate anche per verificare l'integrità dei dati inviati. A tale scopo, il proprietario della coppia di chiavi può allegare una firma digitale ai dati prima di inviarla. La creazione di una firma digitale comporta il calcolo di un hash dei dati e la crittografia dell'hash con la chiave privata. Chiunque usi la chiave pubblica per decrittografare la firma digitale è certo che la firma digitale deve essere stata firmata solo dalla persona proprietaria della chiave privata. Inoltre, il destinatario può calcolare un hash dei dati usando lo stesso algoritmo del mittente e, se l'hash calcolato corrisponde a quello inviato nella firma digitale, il destinatario può essere certo che i dati non sono stati modificati dopo la firma digitale.

Uno svantaggio dell'uso di un'infrastruttura a chiave pubblica per la crittografia dei dati con volumi elevati è la relativa lentezza delle prestazioni. A causa della matematica intensiva, la crittografia e la decrittografia dei dati usando una crittografia asimmetrica che dipende da una coppia di chiavi può essere fino a 1.000 volte più lenta rispetto alla crittografia e alla decrittografia usando una crittografia simmetrica che dipende solo da una singola chiave. TLS usa quindi un'infrastruttura a chiave pubblica solo per la generazione di firme digitali e per negoziare la chiave singola specifica della sessione che verrà usata sia dal client che dal server per la crittografia e la decrittografia bulk dei dati. TLS supporta un'ampia gamma di crittografie simmetriche a chiave singola e potrebbero essere aggiunte crittografie aggiuntive in futuro.

Per altre informazioni sul protocollo handshake TLS, vedere [Protocollo handshake TLS](/windows/desktop/SecAuthN/tls-handshake-protocol).

Per altre informazioni sulla crittografia alla base del protocollo TLS, vedere [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).

## <a name="x509-certificates"></a>Certificati X.509

Un problema critico che deve essere gestito da un'infrastruttura a chiave pubblica è la possibilità di considerare attendibile l'autenticità della chiave pubblica in uso. Quando si usa una chiave pubblica rilasciata a un'azienda con cui si vuole fare affari, si vuole essere certi che la chiave appartenga effettivamente all'azienda anziché a un furto che vuole scoprire il numero della carta di credito.

Per garantire l'identità di un'entità che contiene una coppia di chiavi, l'entità viene emessa da un'autorità di certificazione (CA) un certificato X.509. Questo certificato contiene informazioni che identificano l'entità, contengono la chiave pubblica dell'entità e sono firmate digitalmente dalla CA. Questa firma digitale indica che la CA ritiene che la chiave pubblica contenuta nel certificato appartenga effettivamente all'entità identificata dal certificato.

E come si considera attendibile la CA? Poiché la CA stessa contiene un certificato X.509 firmato da una CA di livello superiore. Questa catena di firme di certificato continua fino a raggiungere una CA radice, ovvero una CA che firma i propri certificati. Se si considera attendibile l'integrità della CA radice di un certificato, sarà possibile considerare attendibile l'autenticità del certificato stesso. Pertanto, la selezione delle CA radice di cui si è disposti a considerare attendibili è un compito importante per un amministratore di sistema.

### <a name="client-certificates"></a>Certificati client

Quando sono emersi per la prima volta protocolli a livello di trasporto di sicurezza, lo scopo principale era garantire che un client si connetteva a un server autentico e contribuire a proteggere la privacy dei dati durante il transito. TUTTAVIA, SSL 3.0 e TLS 1.0 includono anche il supporto per la trasmissione del certificato di un client durante l'handshake del protocollo. Questa funzionalità facoltativa consente l'autenticazione reciproca del client e del server.

La decisione di usare un certificato client deve essere presa nel contesto dell'applicazione. I certificati client non sono necessari se il requisito principale è l'autenticazione del server. Tuttavia, se l'autenticazione client è essenziale, è possibile usare il certificato di un client anziché basarsi sull'autenticazione personalizzata all'interno dell'applicazione. L'uso dei certificati client è preferibile rispetto all'autenticazione personalizzata perché offre agli utenti uno scenario di Single Sign-On.

## <a name="using-tls-in-com"></a>Uso di TLS in COM

TLS supporta solo il livello di rappresentazione (RPC \_ C \_ IMP LEVEL \_ \_ IMPERSONATE). Se COM negozia TLS come servizio di autenticazione in un proxy, COM imposta il livello di rappresentazione per rappresentare indipendentemente dall'impostazione predefinita del processo. Per il corretto funzionamento della rappresentazione in TLS, il client deve fornire un certificato X.509 al server e tale certificato deve essere mappato a un determinato account utente nel server. Per altre informazioni, vedere la Guida dettagliata al mapping dei [certificati agli account utente.](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates)

TLS non supporta la [clonazione di](cloaking.md). Se un flag di cloaking e TLS vengono specificati in una chiamata [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**IClientSecurity::SetBlanket,**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) verrà restituito E \_ INVALIDARG.

TLS non funziona con il livello di autenticazione impostato su Nessuno. L'handshake tra il client e il server esamina il livello di autenticazione impostato da ognuno e sceglie l'impostazione di sicurezza più elevata per la connessione.

I parametri di sicurezza per TLS possono essere impostati chiamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket). Le sezioni seguenti descrivono le sfumature coinvolte nell'esecuzione di tali chiamate.

### <a name="how-a-server-sets-the-security-blanket"></a>Modalità di impostazione della protezione da parte di un server

Se un server vuole usare TLS, deve specificare Schannel (RPC \_ C AUTHN GSS SCHANNEL) come servizio di autenticazione nel parametro \_ \_ \_ *asAuthSvc* di [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Per impedire ai client di connettersi al server usando un servizio di autenticazione meno sicuro, il server deve specificare solo Schannel come servizio di autenticazione quando chiama **CoInitializeSecurity**. Il server non può modificare la protezione dopo aver chiamato **CoInitializeSecurity**.

Per usare TLS, è necessario che i parametri seguenti siano specificati quando un server chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *pVoid* deve essere un puntatore a un [**oggetto IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) o un puntatore a [**UN \_ DESCRIPTOR DI SICUREZZA.**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) Non deve essere **NULL o** un puntatore a un AppID.
-   *cAuthSvc* non può essere 0 o -1. I server COM non scelgono mai Schannel quando *cAuthSvc* è -1.
-   *asAuthSvc deve* specificare Schannel come possibile servizio di autenticazione. Questa operazione viene eseguita impostando i parametri [**SOLE \_ AUTHENTICATION \_ SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) seguenti per il membro Schannel di [**SOLE AUTHENTICATION \_ \_ LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list):
    -   *dwAuthnSvc* deve essere RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL.
    -   *dwAuthzSvc* deve essere RPC \_ C \_ AUTHZ \_ NONE. Attualmente, viene ignorato.
    -   *pPrincipalName* deve essere un puntatore a [**un CERT \_ CONTEXT,**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)di cui viene eseguito il cast come puntatore a OLECHAR, che rappresenta il certificato X.509 del server.
-   *dwAuthnLevel* indica il livello di autenticazione minimo che verrà accettato dai client per una connessione riuscita. Non può essere RPC \_ C \_ AUTHN \_ LEVEL \_ NONE.
-   *dwCapabilities* non deve avere il flag APPID EOAC \_ impostato. Il flag EOAC ACCESS CONTROL deve essere impostato se pVoid punta a un \_ \_ oggetto [**IAccessControl.**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol)  Non deve essere impostato se *pVoid* punta a un DESCRITTORE DI \_ SICUREZZA. Per altri flag che possono essere impostati, vedere [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Per altre informazioni sull'uso di [**CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)vedere Impostazione della sicurezza a livello di [processo con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-sets-the-security-blanket"></a>Modalità di impostazione della protezione da parte di un client

Se un client vuole usare TLS, deve specificare Schannel (RPC \_ C \_ AUTHN GSS SCHANNEL) nell'elenco dei servizi di autenticazione nel \_ \_ parametro *pAuthList* di [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Se Schannel non viene specificato come possibile servizio di autenticazione quando viene chiamato **CoInitializeSecurity,** una chiamata successiva a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (o [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)) avrà esito negativo se tenta di specificare Schannel come servizio di autenticazione.

I parametri seguenti devono essere specificati quando un client chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *dwAuthnLevel* specifica il livello di autenticazione predefinito che il client vuole usare. Non può essere RPC \_ C \_ AUTHN \_ LEVEL \_ NONE.
-   *dwImpLevel* deve essere RPC \_ C IMP LEVEL \_ \_ \_ IMPERSONATE.
-   *pAuthList* deve avere i parametri [**SOLE \_ AUTHENTICATION \_ INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) seguenti come membro dell'elenco:
    -   *dwAuthnSvc* deve essere RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL.
    -   *dwAuthzSvc* deve essere RPC \_ C \_ AUTHZ \_ NONE.
    -   *pAuthInfo* è un puntatore a [**un CERT \_ CONTEXT,**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)di cui viene eseguito il cast come puntatore a void, che rappresenta il certificato X.509 del client. Se il client non dispone di un certificato o non vuole presentare il certificato al server, *pAuthInfo* deve essere **NULL** e verrà tentata una connessione anonima con il server.
-   *dwCapabilities* è un set di flag che indicano funzionalità client aggiuntive. Per informazioni sui flag da impostare, vedere [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

Per altre informazioni sull'uso di [**CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)vedere Impostazione della sicurezza a livello di [processo con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-changes-the-security-blanket"></a>Modalità di modifica della protezione da parte di un client

Se un client vuole usare TLS ma modificare la protezione dopo aver chiamato [**CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)deve chiamare [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) o [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) con parametri simili a quelli usati nella chiamata a **CoInitializeSecurity**, con le differenze seguenti:

-   *pServerPrincName* indica il nome principale del server, in formato msstd o fullsic. Per informazioni su questi formati, vedere [Nomi delle entità](/windows/desktop/Rpc/principal-names). Se il client ha il certificato X.509 del server, può trovare il nome dell'entità chiamando [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname).
-   *pAuthInfo* è un puntatore a [**un CERT \_ CONTEXT,**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)di cui viene eseguito il cast come puntatore a RPC AUTH IDENTITY HANDLE, che rappresenta il certificato \_ \_ \_ X.509 del client. Se il client non dispone di un certificato o non vuole presentare il certificato al server, *pAuthInfo* deve essere **NULL** e verrà tentata una connessione anonima con il server.
-   *dwCapabilities* è costituito da flag che indicano funzionalità client aggiuntive. È possibile usare solo quattro flag per modificare le impostazioni di sicurezza generale: \_ EOAC DEFAULT, EOAC \_ MUTUAL \_ AUTH, EOAC ANY AUTHORITY (questo flag è \_ deprecato) e \_ EOAC \_ MAKE \_ FULLSIC. Per altre informazioni, vedere [**CoSetProxyBlanket.**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)

Per altre informazioni sull'uso [**di CoSetProxyBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)vedere [Impostazione della sicurezza a livello di proxy di interfaccia](setting-security-at-the-interface-proxy-level.md).

### <a name="example-client-changes-the-security-blanket"></a>Esempio: Il client modifica la protezione generale

Nell'esempio seguente viene illustrato come un client può modificare la copertura di sicurezza per soddisfare una richiesta dal server per il client di fornire il certificato X.509. Il codice di gestione degli errori viene omesso per brevità.


```C++
void ClientChangesSecurity ()
{
  HCRYPTPROV                   provider           = 0;
  HCERTSTORE                   cert_store         = NULL;
  PCCERT_CONTEXT               client_cert        = NULL;
  PCCERT_CONTEXT               server_cert        = NULL;
  WCHAR                        *server_princ_name = NULL;
  ISecret                      *pSecret           = NULL;
  MULTI_QI                     server_instance;
  COSERVERINFO                 server_machine;
  SOLE_AUTHENTICATION_LIST     auth_list;
  SOLE_AUTHENTICATION_INFO     auth_info[1];



  // Specify all the authentication info. 
  // The client is willing to connect using SChannel,
  //   with no client certificate.
  auth_list.cAuthInfo     = 1;
  auth_list.aAuthInfo     = auth_info;
  auth_info[0].dwAuthnSvc = RPC_C_AUTHN_GSS_SCHANNEL;
  auth_info[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
  auth_info[0].pAuthInfo  = NULL;  // No certificate

  // Initialize client security with no client certificate.
  CoInitializeSecurity( NULL, -1, NULL, NULL,
                        RPC_C_AUTHN_LEVEL_PKT,
                        RPC_C_IMP_LEVEL_IMPERSONATE, &auth_list,
                        EOAC_NONE, NULL );
  
  // Specify info for the proxy.
  server_instance = {&IID_ISecret, NULL, S_OK};
  server_machine  = {0, L"ServerMachineName", NULL, 0};
  
  // Create a proxy.
  CoCreateInstanceEx( CLSID_Secret, NULL, CLSCTX_REMOTE_SERVER, 
                      &server_machine, 1, &server_instance);
  pSecret = (ISecret *) server_instance.pItf;

  //** The client obtained the server's certificate during the handshake.
  //** The server requests a certificate from the client.

  // Get the default certificate provider.
  CryptAcquireContext( &provider, NULL, NULL, PROV_RSA_SCHANNEL, 0 );

  // Open the certificate store.
  cert_store = CertOpenSystemStore( provider, L"my" );

  // Find the client's certificate.
  client_cert = 
    CertFindCertificateInStore( cert_store,
                                X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
                                0,
                                CERT_FIND_SUBJECT_STR,
                                L"ClientName",  // Use the principal name
                                NULL );

  // Find the fullsic principal name of the server.
  RpcCertGeneratePrincipalName( server_cert, RPC_C_FULL_CERT_CHAIN, 
                                &server_princ_name );

  // Change the client's security: 
  // Increase the authentication level and attach a certificate.
  CoSetProxyBlanket( pSecret, RPC_C_AUTHN_GSS_SCHANNEL,
                     RPC_C_AUTHZ_NONE,
                     server_princ_name, RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
                     RPC_C_IMP_LEVEL_IMPERSONATE, 
                     (RPC_AUTH_IDENTITY_HANDLE *) client_cert,
                     EOAC_NONE );

  cleanup:
  if (server_princ_name != NULL)
    RpcStringFree( &server_princ_name );
  if (client_cert != NULL)
    CertFreeCertificateContext(client_cert);
  if (server_cert != NULL)
    CertFreeCertificateContext(server_cert);
  if (cert_store != NULL)
    CertCloseStore( cert_store, CERT_CLOSE_STORE_CHECK_FLAG );
  if (provider != 0 )
    CryptReleaseContext( provider, 0 );
  if (pSecret != NULL)
    pSecret->Release();
  CoUninitialize();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Com e pacchetti di sicurezza](com-and-security-packages.md)
</dt> </dl>

 

 