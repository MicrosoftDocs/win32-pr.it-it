---
description: Questo argomento descrive il contenuto video&\# 8211; funzionalità di protezione che un driver di grafica può fornire.
ms.assetid: 3FDB4908-C75D-4AE0-B32E-93F840E4F30A
title: GPU-Based protezione del contenuto con D3D11 Video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24af51187c400c11afa2ea273e7718c2d38ce429
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481737"
---
# <a name="gpu-based-content-protection-with-d3d11-video"></a>GPU-Based protezione del contenuto con D3D11 Video

Questo argomento descrive le funzionalità di protezione dei contenuti video che un driver di grafica può offrire.

-   [Introduzione](#introduction)
-   [Panoramica del processo di decodifica](#overview-of-the-decoding-process)
-   [Crittografia dei buffer video compressi per il decodificatore](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. Eseguire una query protezione del contenuto funzionalità del driver](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. Configurare il canale autenticato](#2-configure-the-authenticated-channel)
    -   [3. Configurare la sessione di crittografia](#3-configure-the-cryptographic-session)
    -   [4. Associare il decodificatore alla sessione di crittografia](#4-associate-the-decoder-with-the-cryptographic-session)
-   [Invio di comandi del canale autenticato](#sending-authenticated-channel-commands)
-   [Invio di query sul canale autenticato](#sending-authenticated-channel-queries)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Il diagramma seguente mostra una visualizzazione semplificata del modo in cui il contenuto video protetto attraversa la pipeline di cui eseguire il rendering.

![diagramma che mostra il contenuto video protetto.](images/d3d9video01.png)

> [!Note]
>
> Il [percorso del supporto](protected-media-path.md) protetto (PMP) non è illustrato in questo diagramma. Il flusso di dati illustrato qui può verificarsi all'interno di un processo PMP o all'interno di un processo dell'applicazione.

 

Il decodificatore riceve dati video crittografati e compressi da un'origine esterna. Si presuppone anche che il decodificatore riceva anche una chiave crittografica per decrittografare questi dati. Questo argomento non descrive lo scambio di chiavi tra l'origine video e il decodificatore, ma il PMP definisce un possibile meccanismo. La GPU non è coinvolta in questa fase.

Per la decodifica con accelerazione hardware, il decodificatore software passa il contenuto video compresso alla GPU. Per proteggere questo contenuto, il decodificatore crittografa nuovamente i dati, in genere usando AES-CTR, prima di passarlo all'acceleratore hardware. Viene definito un meccanismo di scambio di chiavi tra il decodificatore e il driver di grafica.

I fotogrammi video decodificati vengono archiviati nella memoria video, in genere in chiaro. A questo punto, i frame vengono elaborati e quindi presentati. Sono disponibili due opzioni principali per la presentazione.

-   Quando si usa l'API D3D9, i frame possono essere presentati usando una sovrapposizione hardware. L'hardware non è supportato in D3D11. Per altre informazioni, vedere [Supporto della sovrimpressione hardware](hardware-overlay-support.md).
-   I frame possono essere presentati da Desktop Window Manage (DWM) usando una superficie condivisa.

L'ultimo passaggio consiste nel visualizzare il frame sul monitor, che potrebbe richiedere la protezione del collegamento tra la scheda grafica e il dispositivo di visualizzazione. Un esempio di protezione dei collegamenti è High-Bandwidth Digital protezione del contenuto (HDCP). La protezione dei collegamenti viene [configurata tramite Output Protection Manager](output-protection-manager.md) (OPM). In questo argomento non viene descritto OPM. Per altre informazioni, vedere [Uso di Output Protection Manager.](using-output-protection-manager.md)

## <a name="overview-of-the-decoding-process"></a>Panoramica del processo di decodifica

Durante la decodifica con accelerazione hardware, il decodificatore software deve passare i dati video compressi alla scheda grafica. Per il contenuto Premium, questi dati devono in genere essere crittografati, usando la crittografia a chiave simmetrica, prima di essere inviati alla GPU.

Per crittografare il video per la decodifica, il decodificatore software usa le interfacce seguenti:

-   [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder). Rappresenta il dispositivo decodificatore, denominato anche acceleratore.
-   [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession). Rappresenta una sessione di crittografia, che fornisce la chiave di crittografia.
-   [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel). Rappresenta un canale autenticato, che consente al decodificatore software di associare la sessione di crittografia al decodificatore.

![diagramma che mostra le interfacce di decodifica direct3d9.](images/d3d9video02.png)

Tutte queste interfacce vengono ottenute dal dispositivo Direct3D11, come indicato di seguito:



| Interfaccia                                                        | Creazione                                                                                                                                                |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)                 | Chiamare [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview). Il tipo di decodificatore è identificato da un GUID del profilo. |
| [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)               | Chiamare [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession).                                                           |
| [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) | Chiamare [**ID3D11VideoDevice::CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel).                                             |



 

> [!Note]  
> Per ottenere un puntatore [**all'interfaccia ID3D11VideoDevice,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'interfaccia [**ID3D11Device.**](/windows/win32/api/d3d11/nn-d3d11-id3d11device)

 

Il canale autenticato fornisce un canale di comunicazione attendibile tra il decodificatore software e il driver. Il canale di comunicazione funziona come segue:

-   Il driver fornisce una catena di certificati X.509 il cui certificato radice è firmato da Microsoft.
-   Il certificato contiene una chiave pubblica RSA per il driver.
-   Il decodificatore software usa la chiave pubblica per inviare al driver una chiave di sessione AES a 128 bit.
-   Il decodificatore software invia query e comandi al canale autenticato.
-   La chiave di sessione viene usata per calcolare i codici di autenticazione dei messaggi (MAC) per le query e i comandi. Il driver usa i macs per verificare l'integrità dei dati di query/comando e il decodificatore software li usa per verificare l'integrità dei dati di risposta dal driver.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Crittografia dei buffer video compressi per il decodificatore

Ecco una panoramica generale del processo di crittografia e decodifica:

1.  Il decodificatore software riceve un flusso di dati crittografati dall'origine video. Il decodificatore decrittografa questo flusso.
2.  Il decodificatore software negozia una chiave di sessione con la sessione di crittografia.
3.  Il decodificatore software usa il canale autenticato per associare la sessione di crittografia al dispositivo decodificatore.
4.  Il decodificatore software inserisce i dati compressi in buffer che ottiene dal dispositivo decodificatore (acceleratore). Per il contenuto protetto, il codificatore software crittografa i dati che vengono memorizzati nei buffer usando la chiave di sessione per la crittografia.
    > [!Note]  
    > Alcuni driver usano una chiave simmetrica, anziché la chiave di sessione, per la crittografia. La chiave di contenuto può cambiare da un frame a quello successivo.

     

5.  Il decodificatore invia i buffer compressi crittografati all'acceleratore. Per AES-CTR, il decodificatore passa anche il vettore di inizializzazione. Se viene usata una chiave di contenuto, il decodificatore passa la chiave di contenuto, crittografata usando la chiave di sessione.

Direct3D11 include il supporto standard per AES-CTR a 128 bit, ma è progettato per estendersi a tipi di crittografia aggiuntivi.

Le cinque sezioni successive forniscono passaggi più dettagliati.

-   [1. Eseguire una query protezione del contenuto funzionalità del driver](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. Configurare il canale autenticato](#2-configure-the-authenticated-channel)
-   [3. Configurare la sessione di crittografia](#3-configure-the-cryptographic-session)
-   [4. Associare il decodificatore alla sessione di crittografia](#4-associate-the-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. Eseguire una query protezione del contenuto funzionalità del driver

Prima di tentare di applicare la crittografia, ottenere le funzionalità di protezione del contenuto del driver.

1.  Ottenere un puntatore all'interfaccia ID3D11Device.
2.  Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per [**l'interfaccia ID3D11VideoDevice.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice)
3.  Chiamare [**ID3D11VideoDevice::GetContentProtectionCaps**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps). Questo metodo compila una struttura [**D3D11_VIDEO_CONTENT_PROTECTION_CAPS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps) con le funzionalità di protezione del contenuto del driver.

In particolare, cercare le funzionalità seguenti:

-   Se il **membro Caps** contiene **il** flag D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE o **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE,** il driver può eseguire la crittografia.
-   Se il **membro Caps** contiene il flag **D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY,** il driver usa una chiave simmetrica separata per la decrittografia.
-   Chiamare [**ID3D11VideoDevice::CheckCryptoKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) per determinare i tipi di scambio di chiavi supportati dal driver per la generazione della chiave di sessione.

Le funzionalità aggiuntive sono indicate nel **membro Caps.**

### <a name="2-configure-the-authenticated-channel"></a>2. Configurare il canale autenticato

Il passaggio successivo consiste nel configurare il canale autenticato.

1.  Chiamare [**ID3D11VideoDevice::CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) per creare il canale autenticato. Per il *parametro ChannelType* specificare un tipo di canale che corrisponda alle funzionalità del driver.
    -   Il **D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE** di canale corrisponde a **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE**.
    -   Il **D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE** di canale corrisponde a **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE**.

    Il **metodo CreateAuthenticatedChannel** restituisce un puntatore all'interfaccia [**ID3D11AuthenticatedChannel.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel)
2.  Chiamare [**ID3D11AuthenticatedChannel::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize) per ottenere le dimensioni del certificato X.509 del driver. Allocare un buffer delle dimensioni richieste.
3.  Chiamare [**ID3D11AuthenticatedChannel::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate) per ottenere il certificato. Il metodo copia il certificato nel buffer allocato nel passaggio precedente.
4.  Verificare che il certificato del driver sia stato firmato da Microsoft e non sia stato revocato.
5.  Ottenere la chiave pubblica dal certificato.
6.  Generare una chiave di sessione RSA casuale. Questa chiave di sessione viene usata per firmare i dati inviati al canale autenticato. Crittografare la chiave di sessione usando la chiave pubblica del driver.
7.  Chiamare [**ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) per inviare la chiave di sessione crittografata al driver.
8.  Inizializzare il canale protetto come indicato di seguito:
    1.  Compilare una [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) struttura come descritto nella documentazione.
    2.  Inviare [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) comando chiamando [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) come descritto nella sezione Invio [di comandi del canale autenticato](#sending-authenticated-channel-commands). Questo comando contiene i numeri di sequenza iniziale per i comandi e le query inviati al canale autenticato.
9.  Verificare il tipo di canale inviando [**D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output) query al canale autenticato, come descritto nella sezione [Invio di query sul canale autenticato](#sending-authenticated-channel-queries). Verificare che il tipo di canale corrisponda a quello specificato nel [**metodo CreateAuthenticatedChannel.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)

### <a name="3-configure-the-cryptographic-session"></a>3. Configurare la sessione di crittografia

Configurare quindi la sessione di crittografia e stabilire la chiave di sessione.

1.  Chiamare [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) per creare la sessione di crittografia. Questo metodo restituisce un puntatore [**all'interfaccia ID3D11CryptoSession.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)
2.  Chiamare [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize) per ottenere le dimensioni del certificato X.509 del driver. Allocare un buffer delle dimensioni richieste.
3.  Chiamare [**ID3D11CryptoSession::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate) per ottenere il certificato. Il metodo copia il certificato nel buffer allocato nel passaggio precedente.
4.  Verificare che il certificato del driver sia stato firmato da Microsoft e non sia stato revocato.
5.  Ottenere la chiave pubblica dal certificato.
6.  Generare una chiave di sessione RSA casuale. Si tratta di una chiave di sessione separata dalla chiave di sessione del canale autenticato. Crittografare la chiave di sessione usando la chiave pubblica del driver.
7.  Chiamare [**ID3D11VideoContext::NegotiateCryptoSessionKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) per inviare la chiave di sessione crittografata al driver.
8.  Se le funzionalità di protezione del **contenuto includono 3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY**, creare una chiave di contenuto RSA casuale. Verrà usato più avanti nel processo di decodifica.

### <a name="4-associate-the-decoder-with-the-cryptographic-session"></a>4. Associare il decodificatore alla sessione di crittografia

Associare quindi il dispositivo decodificatore al dispositivo Direct3D11 e alla sessione di crittografia, come indicato di seguito:

1.  Ottenere un handle per il dispositivo Direct3D11 inviando una [**D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output) query al canale autenticato.
2.  Compilare una [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) con le informazioni seguenti:
    -   Impostare il **membro DecodeHandle** sull'handle restituito da [**ID3D11VideoDecoder::GetDriverHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle).
    -   Impostare il **membro CryptoSessionHandle** sull'handle restituito da [**ID3D11CryptoSession::GetCryptoSessionHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle).
    -   Impostare il **membro DeviceHandle** sull'handle del dispositivo Direct3D11.
3.  Chiamare [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) per [](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) inviare un D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION comando al canale autenticato.

Il diagramma seguente illustra lo scambio di handle:

![diagramma che illustra come il decodificatore dxva è associato alla sessione di crittografia.](images/d3d9video03.png)

Il decodificatore software può ora usare la chiave di sessione crittografica per crittografare i buffer video compressi. Ogni buffer compresso avrà il proprio vettore di inizializzazione (IV) specificato nel **membro pIV** della [**D3D11_VIDEO_DECODER_BUFFER_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc) struttura.

## <a name="sending-authenticated-channel-commands"></a>Invio di comandi del canale autenticato

Viene definito un set di comandi per la configurazione del canale autenticato e l'impostazione di varie protezioni del contenuto. Per un elenco di comandi, vedere protezione del contenuto [comandi](content-protection-commands.md).

Per inviare un comando al canale autenticato, seguire questa procedura.

1.  Compilare la struttura dei dati di input. Questa struttura di dati è sempre una [**D3D11_AUTHENTICATED_CONFIGURE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input) struttura seguita da campi aggiuntivi. Compilare la **D3D11_AUTHENTICATED_CONFIGURE_INPUT** struttura come illustrato nella tabella seguente.

    
| Membro | Descrizione | 
|--------|-------------|
| <strong>Omac</strong> | Ignorare questo campo per il momento. | 
| <strong>ConfigureType</strong> | GUID che identifica il comando. Per un elenco di comandi, vedere protezione del contenuto <a href="content-protection-commands.md">comandi</a>. | 
| <strong>hChannel</strong> | Handle per il canale autenticato. | 
| <strong>Sequencenumber</strong> | Numero di sequenza. Il primo numero di sequenza viene specificato inviando un <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> comando. Ogni volta che si invia un altro comando, incrementare questo numero di 1. Il numero di sequenza protegge dagli attacchi di riproduzione.    <blockquote>    [!Note]<br />    Vengono usati due numeri di sequenza separati, uno per i comandi e uno per le query.    </blockquote><br /><br /> | 


    

     

2.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il **membro omac** della struttura di input. Copiare quindi il valore del tag nel **membro omac.**
3.  Chiamare [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel).
4.  Il driver inserisce l'output del comando [**nella struttura D3D11_AUTHENTICATED_CONFIGURE_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output) comando.
5.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il membro **omac** della struttura di output. Confrontarlo con il valore del **membro omac.** Ha esito negativo se non corrispondono.
6.  Confrontare i valori dei **membri ConfigureType**, **hChannel** e **SequenceNumber** nella struttura di output con i valori per tali membri. Ha esito negativo se non corrispondono.
7.  Incrementare il numero di sequenza per il comando successivo.

## <a name="sending-authenticated-channel-queries"></a>Invio di query sul canale autenticato

Viene definito un set di query per il recupero di informazioni sul canale autenticato. Per un elenco di query, vedere protezione del contenuto [query](content-protection-queries.md).

Per inviare un comando al canale autenticato, seguire questa procedura.

1.  Compilare la struttura dei dati di input. Questa struttura di dati è sempre una [**D3D11_AUTHENTICATED_QUERY_INPUT,**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input) possibilmente seguita da campi aggiuntivi. Compilare la **D3D11_AUTHENTICATED_QUERY_INPUT** struttura come illustrato nella tabella seguente.

    
| Membro | Descrizione | 
|--------|-------------|
| <strong>QueryType</strong> | GUID che identifica la query. Per un elenco di query, vedere protezione del contenuto <a href="content-protection-queries.md">query</a>. | 
| <strong>hChannel</strong> | Handle per il canale autenticato. | 
| <strong>Sequencenumber</strong> | Numero di sequenza. Il primo numero di sequenza viene specificato inviando un <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> comando. Ogni volta che si invia un'altra query, incrementare questo numero di 1. Il numero di sequenza protegge dagli attacchi di riproduzione.    <blockquote>    [!Note]<br />    Vengono usati due numeri di sequenza separati, uno per i comandi e uno per le query.    </blockquote><br /><br /> | 


    

     

2.  Chiamare [**ID3D11VideoContext::QueryAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel).
3.  Il driver inserisce l'output della query in [**una D3D11_AUTHENTICATED_QUERY_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output) struttura . Questa struttura è seguita da campi aggiuntivi, a seconda del tipo di query.
4.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il **membro omac** della struttura di output. Confrontarlo con il valore del **membro omac.** Esito negativo se non corrispondono.
5.  Confrontare i valori dei **membri ConfigureType**, **hChannel** e **SequenceNumber** nella struttura di output con i valori per tali membri. Esito negativo se non corrispondono.
6.  Incrementare il numero di sequenza per la query successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API Video Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 
