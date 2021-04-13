---
title: SChannel
description: Il pacchetto di sicurezza del canale sicuro (Schannel), il cui identificatore del servizio di autenticazione è RPC \_ C \_ AuthN \_ GSS \_ Schannel, supporta i seguenti protocolli a chiave pubblica SSL (Secure Sockets Layer) versioni 2,0 e 3,0, Transport Layer Security (TLS) 1,0 e private Communication Technology (PCT) 1,0. TLS 1,0 è una versione standardizzata, leggermente modificata di SSL 3,0, rilasciata da Internet Engineering Task Force (IETF) nel gennaio 1999, nel documento RFC 2246. Poiché TLS è stato standardizzato, gli sviluppatori sono invitati a usare TLS anziché SSL. PCT è incluso solo per la compatibilità con le versioni precedenti e non deve essere usato per il nuovo sviluppo. Quando si utilizza il pacchetto di sicurezza Schannel, DCOM negozia automaticamente il protocollo migliore, a seconda delle funzionalità client e server.
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc9f82a05d1542e7585426128f10cdf452d31d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339390"
---
# <a name="schannel"></a>SChannel

Il pacchetto di sicurezza del canale sicuro (Schannel), il cui identificatore del servizio di autenticazione è RPC \_ C \_ AuthN \_ GSS \_ Schannel, supporta i protocolli basati su chiave pubblica seguenti: SSL (Secure Sockets Layer) versioni 2,0 e 3,0, Transport Layer Security (TLS) 1,0 e private Communication Technology (PCT) 1,0. TLS 1,0 è una versione standardizzata, leggermente modificata di SSL 3,0, rilasciata da Internet Engineering Task Force (IETF) nel gennaio 1999, nel documento [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt). Poiché TLS è stato standardizzato, gli sviluppatori sono invitati a usare TLS anziché SSL. PCT è incluso solo per la compatibilità con le versioni precedenti e non deve essere usato per il nuovo sviluppo. Quando si utilizza il pacchetto di sicurezza Schannel, DCOM negozia automaticamente il protocollo migliore, a seconda delle funzionalità client e server.

Gli argomenti seguenti descrivono brevemente il protocollo TLS e il relativo funzionamento con DCOM.

-   [Quando usare TLS](#when-to-use-tls)
-   [Breve panoramica del funzionamento di TLS](#brief-overview-of-how-tls-works)
-   [Certificati X. 509](#x509-certificates)
    -   [Certificati client](#client-certificates)
-   [Uso di TLS in COM](#using-tls-in-com)
    -   [Modalità di impostazione della copertura di sicurezza da parte di un server](#how-a-server-sets-the-security-blanket)
    -   [Modalità di impostazione della copertura di sicurezza da parte di un client](#how-a-client-sets-the-security-blanket)
    -   [Modalità di modifica della copertura di sicurezza da parte di un client](#how-a-client-changes-the-security-blanket)
    -   [Esempio: il client modifica la copertura di sicurezza](#example-client-changes-the-security-blanket)
-   [Argomenti correlati](#related-topics)

> [!Note]  
> Tutte le informazioni sul protocollo TLS in queste sezioni sono valide anche per i protocolli SSL e PCT.

 

## <a name="when-to-use-tls"></a>Quando usare TLS

TLS è l'unica opzione di sicurezza disponibile quando i server devono dimostrare la propria identità ai client anonimi. Questo è particolarmente importante per i siti Web che vogliono partecipare all'e-commerce perché contribuisce a proteggere la trasmissione di informazioni riservate, ad esempio i numeri di carta di credito. TLS garantisce che i clienti di e-commerce possano essere certi di chi sta facendo affari perché ricevono la prova dell'identità del server. Fornisce inoltre al server di e-commerce l'efficienza di non doversi preoccupare di autenticare l'identità di ogni cliente.

TLS richiede che tutti i server dimostrino la propria identità ai client. TLS offre inoltre la possibilità per i client di dimostrare la propria identità ai server. Questa autenticazione reciproca può essere utile per limitare l'accesso di determinate pagine Web in una rete Intranet aziendale di grandi dimensioni.

TLS supporta i livelli di autenticazione più avanzati e offre un'architettura aperta che consente di aumentare la complessità della crittografia nel tempo per restare al passo con l'innovazione tecnologica. TLS è la scelta migliore per gli ambienti in cui è necessario il massimo livello di sicurezza per i dati in transito.

## <a name="brief-overview-of-how-tls-works"></a>Breve panoramica del funzionamento di TLS

TLS si basa su un'infrastruttura a chiave pubblica (PKI), che usa coppie di chiavi pubbliche/private per abilitare la crittografia dei dati e stabilire l'integrità dei dati e USA certificati X. 509 per l'autenticazione.

Molti protocolli di sicurezza, ad esempio il protocollo Kerberos V5, dipendono da un'unica chiave per crittografare e decrittografare i dati. Tali protocolli dipendono quindi dallo scambio protetto delle chiavi di crittografia. nel protocollo Kerberos questa operazione viene eseguita tramite i ticket ottenuti dal Centro distribuzione chiavi (KDC). Questa operazione richiede che tutti gli utenti che usano il protocollo Kerberos siano registrati con il KDC, che rappresenterebbe una limitazione non pratica per un server Web di e-commerce destinato a attirare milioni di clienti in tutto il mondo. TLS si basa quindi su un'infrastruttura PKI, che usa due chiavi per i dati encryptionâ, quando una chiave della coppia crittografa i dati, ma solo l'altra chiave della coppia può decrittografarla. Il vantaggio principale di questa progettazione è che la crittografia può essere eseguita senza richiedere lo scambio sicuro delle chiavi di crittografia.

Un'infrastruttura a chiave pubblica utilizza una tecnica in cui una delle chiavi viene mantenuta privata ed è disponibile solo per l'entità a cui è stata registrata, mentre l'altra chiave viene resa pubblica per chiunque possa accedere a. Se un utente desidera inviare un messaggio privato al proprietario di una coppia di chiavi, il messaggio può essere crittografato con la chiave pubblica ed è possibile utilizzare solo la chiave privata per decrittografare il messaggio.

Le coppie di chiavi vengono usate anche per verificare l'integrità dei dati inviati. A tale scopo, il proprietario della coppia di chiavi può associare una firma digitale ai dati prima di inviarli. La creazione di una firma digitale comporta il calcolo di un hash dei dati e la crittografia dell'hash con la chiave privata. Chiunque usi la chiave pubblica per decrittografare la firma digitale è certo che la firma digitale deve avere solo la persona che possiede la chiave privata. Il destinatario può inoltre calcolare un hash dei dati utilizzando lo stesso algoritmo del mittente e, se l'hash calcolato corrisponde a quello inviato nella firma digitale, il destinatario può essere certo che i dati non siano stati modificati dopo la firma digitale.

Uno svantaggio dell'uso di un'infrastruttura a chiave pubblica per la crittografia dei dati con volumi elevati è il livello di prestazioni relativamente rallentato. Grazie alla matematica complessa, la crittografia e la decrittografia dei dati tramite una crittografia asimmetrica che dipende da una coppia di chiavi possono essere fino a 1.000 volte più lente rispetto alla crittografia e alla decrittografia con una crittografia simmetrica che dipende solo da una singola chiave. TLS usa quindi un'infrastruttura a chiave pubblica solo per la generazione di firme digitali e per negoziare la chiave singola specifica della sessione che verrà usata sia dal client che dal server per la crittografia e la decrittografia dei dati in blocco. TLS supporta un'ampia gamma di crittografie simmetriche a chiave singola e altre crittografie potrebbero essere aggiunte in futuro.

Per ulteriori informazioni sul protocollo di handshake TLS, vedere il [protocollo di handshake TLS](/windows/desktop/SecAuthN/tls-handshake-protocol).

Per altri dettagli sulla crittografia dietro il protocollo TLS, vedere [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).

## <a name="x509-certificates"></a>Certificati X.509

Un problema cruciale che deve essere gestito da un'infrastruttura PKI è la possibilità di considerare attendibile l'autenticità della chiave pubblica usata. Quando si utilizza una chiave pubblica rilasciata a una società con cui si desidera eseguire l'attività, è necessario essere certi che la chiave appartenga effettivamente all'azienda invece che a un ladro che desidera individuare il numero di carta di credito.

Per garantire l'identità di un'entità che contiene una coppia di chiavi, viene emesso un certificato X. 509 da un'autorità di certificazione (CA). Questo certificato contiene informazioni che identificano l'entità, contiene la chiave pubblica dell'entità ed è firmata digitalmente dalla CA. Questa firma digitale indica che la CA ritiene che la chiave pubblica contenuta nel certificato appartenga effettivamente all'entità identificata dal certificato.

E in che modo si considera attendibile la CA? Poiché la CA contiene un certificato X. 509 che è stato firmato da una CA di livello superiore. Questa catena di firme del certificato continua fino a quando non raggiunge una CA radice, ovvero un'autorità di certificazione che firma i propri certificati. Se si considera attendibile l'integrità della CA radice di un certificato, sarà possibile considerare attendibile l'autenticità del certificato stesso. Quindi, la selezione delle CA radice che si è disposti a considerare attendibile è un compito importante per un amministratore di sistema.

### <a name="client-certificates"></a>Certificati client

Quando sono emersi prima i protocolli a livello di trasporto di sicurezza, lo scopo principale era garantire che un client si connettesse a un server autentico e protegga la privacy dei dati in transito. Tuttavia, SSL 3,0 e TLS 1,0 includono anche il supporto per la trasmissione di un certificato del client durante l'handshake del protocollo. Questa funzionalità facoltativa Abilita l'autenticazione reciproca del client e del server.

La decisione di utilizzare o meno un certificato client deve essere eseguita nel contesto dell'applicazione. I certificati client non sono necessari se il requisito principale è l'autenticazione del server. Tuttavia, se l'autenticazione client è essenziale, è possibile usare un certificato del client anziché basarsi sull'autenticazione personalizzata all'interno dell'applicazione. L'uso di certificati client è preferibile rispetto all'autenticazione personalizzata, perché fornisce agli utenti uno scenario Single Sign-On.

## <a name="using-tls-in-com"></a>Uso di TLS in COM

TLS supporta solo il livello di rappresentazione (rappresentazione \_ \_ \_ a livello di RPC C Imp \_ ). Se COM negozia TLS come servizio di autenticazione in un proxy, COM imposterà il livello di rappresentazione da rappresentare indipendentemente dall'impostazione predefinita del processo. Per il corretto funzionamento della rappresentazione in TLS, il client deve fornire un certificato X. 509 al server e il server deve disporre di tale certificato mappato a un determinato account utente sul server. Per ulteriori informazioni, vedere la [Guida dettagliata al mapping dei certificati agli account utente](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates).

TLS non supporta il [mascheramento](cloaking.md). Se vengono specificati un flag di mascheramento e TLS in una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**IClientSecurity:: seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) , \_ viene restituito E INVALIDARG.

TLS non funziona con il livello di autenticazione impostato su nessuno. L'handshake tra il client e il server esamina il livello di autenticazione impostato da ciascuno e sceglie l'impostazione di sicurezza più elevata per la connessione.

È possibile impostare i parametri di sicurezza per TLS chiamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket). Le sezioni seguenti descrivono le sfumature necessarie per eseguire tali chiamate.

### <a name="how-a-server-sets-the-security-blanket"></a>Modalità di impostazione della copertura di sicurezza da parte di un server

Se un server vuole usare TLS, deve specificare Schannel (RPC \_ C \_ AuthN \_ GSS \_ Schannel) come servizio di autenticazione nel parametro *asAuthSvc* di [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Per evitare che i client si connettano al server utilizzando un servizio di autenticazione meno sicuro, il server deve specificare solo Schannel come servizio di autenticazione quando chiama **CoInitializeSecurity**. Il server non è in grado di modificare la copertura della sicurezza dopo aver chiamato **CoInitializeSecurity**.

Per usare TLS, è necessario specificare i parametri seguenti quando un server chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *PVOID* deve essere un puntatore a un oggetto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) o un puntatore a un [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor). Non deve essere **null** o un puntatore a un AppID.
-   *cAuthSvc* non può essere 0 o-1. I server COM non scelgono mai Schannel quando *cAuthSvc* è-1.
-   *asAuthSvc* deve specificare Schannel come servizio di autenticazione possibile. Questa operazione viene eseguita impostando i seguenti parametri [**esclusivi del \_ \_ servizio di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) per il membro Schannel dell' [**unico \_ \_ elenco di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list):
    -   *dwAuthnSvc* deve essere un linguaggio RPC di autenticazione del linguaggio \_ C \_ \_ \_ .
    -   *dwAuthzSvc* deve essere RPC \_ C \_ AUTHZ \_ None. Attualmente viene ignorato.
    -   *pPrincipalName* deve essere un puntatore a un [**\_ contesto del certificato**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), eseguito il cast come puntatore a OLECHAR, che rappresenta il certificato X. 509 del server.
-   *dwAuthnLevel* indica il livello di autenticazione minimo che verrà accettato dai client per una connessione corretta. Non può essere il \_ livello auth C di RPC \_ \_ \_ .
-   *dwCapabilities* non deve avere il \_ flag AppID EOAC impostato. Il \_ \_ flag di controllo di accesso di EOAC deve essere impostato se *PVOID* punta a un oggetto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) . non deve essere impostato se *PVOID* punta a un \_ descrittore di sicurezza. Per altri flag che possono essere impostati, vedere [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Per altre informazioni sull'uso di [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), vedere [impostazione della sicurezza Processwide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-sets-the-security-blanket"></a>Modalità di impostazione della copertura di sicurezza da parte di un client

Se un client desidera usare TLS, deve specificare Schannel (RPC \_ C \_ AuthN \_ GSS \_ Schannel) nell'elenco dei servizi di autenticazione nel parametro *pAuthList* di [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Se Schannel non è specificato come servizio di autenticazione possibile quando viene chiamato **CoInitializeSecurity** , una chiamata successiva a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (o [**IClientSecurity:: seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)) avrà esito negativo se tenta di specificare Schannel come servizio di autenticazione.

Quando un client chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), è necessario specificare i parametri seguenti:

-   *dwAuthnLevel* specifica il livello di autenticazione predefinito che il client desidera utilizzare. Non può essere il \_ livello auth C di RPC \_ \_ \_ .
-   *dwImpLevel* deve essere una \_ rappresentazione a livello di RPC C \_ Imp \_ \_ .
-   *pAuthList* deve avere i seguenti parametri di [**\_ \_ informazioni di autenticazione esclusivi**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) come membro dell'elenco:
    -   *dwAuthnSvc* deve essere un linguaggio RPC di autenticazione del linguaggio \_ C \_ \_ \_ .
    -   *dwAuthzSvc* deve essere RPC \_ C \_ AUTHZ \_ None.
    -   *pAuthInfo* è un puntatore a un [**\_ contesto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)del certificato, di cui viene eseguito il cast come puntatore a void, che rappresenta il certificato X. 509 del client. Se il client non dispone di un certificato o non desidera presentare il certificato al server, *pAuthInfo* deve essere **null** e verrà eseguito un tentativo di connessione anonima con il server.
-   *dwCapabilities* è un set di flag che indicano funzionalità client aggiuntive. Per informazioni sui flag da impostare, vedere [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .

Per altre informazioni sull'uso di [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), vedere [impostazione della sicurezza Processwide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-changes-the-security-blanket"></a>Modalità di modifica della copertura di sicurezza da parte di un client

Se un client desidera usare TLS ma modificare la copertura della sicurezza dopo aver chiamato [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), deve chiamare [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) o [**IClientSecurity:: seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) con parametri simili a quelli usati nella chiamata a **CoInitializeSecurity**, con le differenze seguenti:

-   *pServerPrincName* indica il nome dell'entità del server, nel formato msstd o fullsic. Per informazioni su questi formati, vedere [nomi principali](/windows/desktop/Rpc/principal-names). Se il client dispone del certificato X. 509 del server, può trovare il nome dell'entità chiamando [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname).
-   *pAuthInfo* è un puntatore a un [**\_ contesto del certificato**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), di cui viene eseguito il cast come puntatore all' \_ handle di identità di autenticazione RPC \_ \_ , che rappresenta il certificato X. 509 del client. Se il client non dispone di un certificato o non desidera presentare il certificato al server, *pAuthInfo* deve essere **null** e verrà eseguito un tentativo di connessione anonima con il server.
-   *dwCapabilities* è costituito da flag che indicano funzionalità client aggiuntive. È possibile usare solo quattro flag per modificare le impostazioni della copertura della sicurezza: EOAC \_ default, EOAC \_ reciproal \_ AUTH, EOAC \_ Any \_ Authority (questo flag è deprecato) e EOAC \_ make \_ FULLSIC. Per ulteriori informazioni, vedere [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

Per altre informazioni sull'uso di [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), vedere [impostazione della sicurezza a livello di proxy di interfaccia](setting-security-at-the-interface-proxy-level.md).

### <a name="example-client-changes-the-security-blanket"></a>Esempio: il client modifica la copertura di sicurezza

Nell'esempio seguente viene illustrato come un client può modificare la copertura di sicurezza in modo da consentire a una richiesta del server per il client di fornire il certificato X. 509. Il codice di gestione degli errori viene omesso per brevità.


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

[Pacchetti COM e di sicurezza](com-and-security-packages.md)
</dt> </dl>

 

 