---
description: Descrive il contenuto video&\# 8211; funzionalità di protezione che possono essere fornite da un driver di grafica.
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based protezione del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e09829984273c35524fe9c8f3cd19e759e18dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465038"
---
# <a name="gpu-based-content-protection"></a>GPU-Based protezione del contenuto

Questo argomento descrive le funzionalità di protezione del contenuto video che possono essere fornite da un driver di grafica.

-   [Introduzione](#introduction)
-   [Panoramica del processo di decodifica](#overview-of-the-decoding-process)
-   [Crittografia dei buffer video compressi per il decodificatore](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. Eseguire una query protezione del contenuto funzionalità del driver](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. Configurare il canale autenticato](#2-configure-the-authenticated-channel)
    -   [3. Configurare la sessione di crittografia](#3-configure-the-cryptographic-session)
    -   [4. Ottenere un handle per il dispositivo decodificatore DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [5. Associare il decodificatore DXVA alla sessione di crittografia](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [Invio di comandi del canale autenticato](#sending-authenticated-channel-commands)
-   [Invio di query sul canale autenticato](#sending-authenticated-channel-queries)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Il diagramma seguente mostra una visualizzazione semplificata del modo in cui il contenuto video protetto passa attraverso la pipeline di cui eseguire il rendering.

![diagramma che mostra il contenuto video protetto.](images/d3d9video01.png)

> [!Note]  
> Il [percorso del supporto](protected-media-path.md) protetto (PMP) non è illustrato in questo diagramma. Il flusso di dati illustrato di seguito può verificarsi all'interno di un processo PMP o all'interno di un processo dell'applicazione.

 

Il decodificatore riceve dati video crittografati e compressi da un'origine esterna. Si presuppone anche che il decodificatore riceva anche una chiave crittografica per decrittografare i dati. Questo argomento non descrive lo scambio di chiavi tra l'origine video e il decodificatore, ma il PMP definisce un meccanismo possibile. La GPU non è coinvolta in questa fase.

Per la decodifica con accelerazione hardware, il decodificatore software passa il contenuto video compresso alla GPU. Per proteggere questo contenuto, il decodificatore crittografa nuovamente i dati, in genere usando AES-CTR, prima di passarlo all'acceleratore hardware. Viene definito un meccanismo di scambio delle chiavi tra il decodificatore e il driver di grafica.

I fotogrammi video decodificati vengono archiviati nella memoria video, in genere in chiaro. A questo punto, i frame vengono elaborati e quindi presentati. Sono disponibili due opzioni principali per la presentazione.

-   I fotogrammi possono essere presentati usando una sovrimpressione hardware. Per altre informazioni, vedere [Supporto della sovrimpressione hardware.](hardware-overlay-support.md)
-   I frame possono essere presentati da Gestione finestre desktop (DWM) usando una superficie condivisa.

L'ultimo passaggio consiste nel visualizzare il frame sul monitor, che potrebbe richiedere la protezione del collegamento tra la scheda grafica e il dispositivo di visualizzazione. Un esempio di protezione dei collegamenti è High-Bandwidth Digital protezione del contenuto (HDCP). La protezione dei collegamenti viene [configurata tramite Output Protection Manager](output-protection-manager.md) (OPM). In questo argomento non viene descritto OPM; Per altre informazioni, vedere [Uso di Output Protection Manager.](using-output-protection-manager.md)

## <a name="overview-of-the-decoding-process"></a>Panoramica del processo di decodifica

Durante la decodifica con accelerazione hardware, il decodificatore software deve passare i dati video compressi alla scheda grafica. Per il contenuto Premium, questi dati devono in genere essere crittografati, usando la crittografia a chiave simmetrica, prima di essere inviati alla GPU.

Per crittografare il video per la decodifica, il decodificatore software usa le interfacce seguenti:

-   [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder). Rappresenta il dispositivo decodificatore DXVA, chiamato anche acceleratore.
-   [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9). Rappresenta una sessione di crittografia, che fornisce la chiave di crittografia.
-   [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9). Rappresenta un canale autenticato, che consente al decodificatore software di associare la sessione di crittografia al decodificatore DXVA.

![Diagramma che mostra le interfacce di decodifica direct3d9.](images/d3d9video02.png)

Tutte queste interfacce vengono ottenute dal dispositivo Direct3D, come indicato di seguito:



| Interfaccia                                                                | Creazione                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | Chiamare [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). Il dispositivo decodificatore DXVA è identificato da un GUID del profilo DXVA. |
| [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | Chiamare [**IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession).                                                                         |
| [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | Chiamare [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).                                                           |



 

> [!Note]  
> Per ottenere un puntatore [**all'interfaccia IDirect3DDevice9Video,**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su un dispositivo D3D9Ex.

 

Il canale autenticato fornisce un canale di comunicazione attendibile tra il decodificatore software e il driver. Il canale di comunicazione funziona come segue:

-   Il driver fornisce una catena di certificati X.509 il cui certificato radice è firmato da Microsoft.
-   Il certificato contiene una chiave pubblica RSA per il driver.
-   Il decodificatore software usa la chiave pubblica per inviare al driver una chiave di sessione AES a 128 bit.
-   Il decodificatore software invia query e comandi al canale autenticato.
-   La chiave di sessione viene usata per calcolare i codici di autenticazione dei messaggi (MAC) per le query e i comandi. Il driver usa i macs per verificare l'integrità dei dati di query/comandi e il decodificatore software li usa per verificare l'integrità dei dati di risposta dal driver.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Crittografia dei buffer video compressi per il decodificatore

Ecco una panoramica generale del processo di crittografia e decodifica:

1.  Il decodificatore software riceve un flusso di dati crittografati dall'origine video. Il decodificatore decrittografa questo flusso.
2.  Il decodificatore software negozia una chiave di sessione con la sessione di crittografia.
3.  Il decodificatore software usa il canale autenticato per associare la sessione di crittografia al dispositivo decodificatore DXVA.
4.  Il decodificatore software inserisce i dati compressi nei buffer DXVA che ottiene dal dispositivo decodificatore DXVA (acceleratore). Per il contenuto protetto, il codificatore software crittografa i dati che vengono memorizzati nei buffer DXVA, usando la chiave di sessione per la crittografia.
    > [!Note]  
    > Alcuni driver usano una chiave simmetrica, anziché la chiave di sessione, per la crittografia. La chiave di contenuto può cambiare da un frame a quello successivo.

     

5.  Il decodificatore invia i buffer compressi crittografati all'acceleratore. Per AES-CTR, il decodificatore passa anche il vettore di inizializzazione. Se viene usata una chiave contenuto, il decodificatore passa la chiave content, crittografata usando la chiave di sessione.

Direct3D include il supporto standard per AES-CTR a 128 bit, ma è progettato per estendersi a tipi di crittografia aggiuntivi.

Le cinque sezioni successive forniscono passaggi più dettagliati.

-   [1. Eseguire una query protezione del contenuto funzionalità del driver](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. Configurare il canale autenticato](#2-configure-the-authenticated-channel)
-   [3. Configurare la sessione di crittografia](#3-configure-the-cryptographic-session)
-   [4. Ottenere un handle per il dispositivo decodificatore DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
-   [5. Associare il decodificatore DXVA alla sessione di crittografia](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. Eseguire una query protezione del contenuto funzionalità del driver

Prima di provare ad applicare la crittografia, ottenere le funzionalità di protezione del contenuto del driver.

1.  Ottenere un puntatore al dispositivo Direct3D 9.
2.  Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per [**l'interfaccia IDirect3DDevice9Video.**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)
3.  Chiamare [**IDirect3DDevice9Video::GetContentProtectionCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps). Questo metodo inserisce una [**struttura D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) con le funzionalità di protezione del contenuto del driver.

In particolare, cercare le funzionalità seguenti:

-   Se il **membro Caps** contiene il **flag D3DCPCAPS_SOFTWARE** o **D3DCPCAPS_HARDWARE,** il driver può eseguire la crittografia.
-   Il **membro KeyExchangeType** specifica come eseguire lo scambio di chiavi per la chiave di sessione.
-   Se il **membro Caps** contiene il flag **D3DCPCAPS_CONTENTKEY,** il driver usa una chiave simmetrica separata per la crittografia. Questo è importante quando si genera la chiave di sessione.

Le funzionalità aggiuntive sono indicate nel **membro Caps.**

### <a name="2-configure-the-authenticated-channel"></a>2. Configurare il canale autenticato

Il passaggio successivo consiste nel configurare il canale autenticato.

1.  Chiamare [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) per creare il canale autenticato. Per il *parametro ChannelType* specificare un tipo di canale corrispondente alle funzionalità del driver.
    -   Il **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** di canale corrisponde **D3DCPCAPS_SOFTWARE**.
    -   Il **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** di canale corrisponde **D3DCPCAPS_HARDWARE**.

    Il **metodo CreateAuthenticatedChannel** restituisce un puntatore all'interfaccia [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) insieme a un handle per il canale. L'handle viene usato in seguito per associare la sessione di crittografia al canale autenticato.
2.  Chiamare [**IDirect3DAuthenticatedChannel9::GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) per ottenere le dimensioni del certificato X.509 del driver. Allocare un buffer delle dimensioni richieste.
3.  Chiamare [**IDirect3DAuthenticatedChannel9::GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) per ottenere il certificato. Il metodo copia il certificato nel buffer allocato nel passaggio precedente.
4.  Verificare che il certificato del driver sia stato firmato da Microsoft e non sia stato revocato.
5.  Ottenere la chiave pubblica dal certificato.
6.  Generare una chiave di sessione RSA casuale. Questa chiave di sessione viene usata per firmare i dati inviati al canale autenticato. Crittografare la chiave di sessione usando la chiave pubblica del driver.
7.  Chiamare [**IDirect3DAuthenticatedChannel9::NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) per inviare la chiave di sessione crittografata al driver.
8.  Inizializzare il canale sicuro come indicato di seguito:
    1.  Compilare una [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) struttura come descritto nella documentazione.
    2.  Inviare [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) comando chiamando [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) come descritto nella sezione Invio di comandi [del canale autenticato](#sending-authenticated-channel-commands). Questo comando contiene i numeri di sequenza iniziale per i comandi e le query inviati al canale autenticato.
9.  Verificare il tipo di canale inviando una query [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) al canale autenticato, come descritto nella sezione [Invio di query sul canale autenticato](#sending-authenticated-channel-queries). Verificare che il tipo di canale corrisponda a quello specificato nel [**metodo CreateAuthenticatedChannel.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)

### <a name="3-configure-the-cryptographic-session"></a>3. Configurare la sessione di crittografia

Configurare quindi la sessione di crittografia e stabilire la chiave di sessione.

1.  Chiamare [**IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) per creare la sessione di crittografia. Questo metodo restituisce un puntatore [**all'interfaccia IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) e insieme a un handle per la sessione di crittografia.
2.  Chiamare [**IDirect3DCryptoSession9::GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) per ottenere le dimensioni del certificato X.509 del driver. Allocare un buffer delle dimensioni richieste.
3.  Chiamare [**IDirect3DCryptoSession9::GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) per ottenere il certificato. Il metodo copia il certificato nel buffer allocato nel passaggio precedente.
4.  Verificare che il certificato del driver sia stato firmato da Microsoft e non sia stato revocato.
5.  Ottenere la chiave pubblica dal certificato.
6.  Generare una chiave di sessione RSA casuale. Si tratta di una chiave di sessione separata dalla chiave della sessione del canale autenticata. Crittografare la chiave di sessione usando la chiave pubblica del driver.
7.  Chiamare [**IDirect3DCryptoSession9::NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) per inviare la chiave di sessione crittografata al driver.
8.  Se le funzionalità di protezione del contenuto **includono D3DCPCAPS_CONTENTKEY**, creare una chiave di contenuto RSA casuale. Verrà usato più avanti nel processo di decodifica.

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a>4. Ottenere un handle per il dispositivo decodificatore DXVA

Per il passaggio successivo sarà necessario un handle per il dispositivo decodificatore DXVA. Per ottenere questo handle, compilare una DXVA2_DecodeExecuteParams struttura come indicato di seguito:


```C++
HANDLE hDecodeDeviceHandle;

DXVA2_DecodeExecuteParams execParams = {0};
DXVA2_DecodeExtensionData ExtensionExecute = {0};
    
execParams.NumCompBuffers = 0;
execParams.pCompressedBuffers = NULL;
execParams.pExtensionData = &ExtensionExecute;

ExtensionExecute.Function = DXVA2_DECODE_GET_DRIVER_HANDLE;
ExtensionExecute.pPrivateInputData = NULL;
ExtensionExecute.PrivateInputDataSize = 0;
ExtensionExecute.pPrivateOutputData = &hDecodeDeviceHandle;
ExtensionExecute.PrivateOutputDataSize = sizeof(HANDLE);
```



Impostare il **membro pExtensionData** della [**struttura DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) sull'indirizzo di una [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) struttura .

Nella struttura [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) impostare il **membro Function** **su DXVA2_DECODE_GET_DRIVER_HANDLE**. Impostare **pPrivateOutputData sull'indirizzo** di un buffer sufficientemente grande da archiviare un **valore HANDLE.** Nell'esempio precedente questo buffer è la *variabile hDecodeDeviceHandle.*

Chiamare quindi [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) e passare l'indirizzo della [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) struttura . L'handle per il decodificatore DXVA viene restituito in **pPrivateOutputData.**

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a>5. Associare il decodificatore DXVA alla sessione di crittografia

Associare quindi il dispositivo decodificatore DXVA al dispositivo Direct3D e alla sessione di crittografia, come indicato di seguito:

1.  Ottenere un handle per il dispositivo decodificatore DXVA, come descritto nella sezione precedente.
2.  Ottenere un handle per il dispositivo Direct3D inviando una query [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) al canale autenticato.
3.  Compilare una [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) con le informazioni seguenti:
    -   Impostare il **membro DXVA2DecodeHandle sull'handle** per il dispositivo decodificatore DXVA.
    -   Impostare il **membro CryptoSessionHandle** sull'handle della sessione di crittografia. Questo handle viene restituito dal [**metodo IDirect3DDevice9Video::CreateCryptoSession.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession)
    -   Impostare il **membro DeviceHandle** sull'handle del dispositivo Direct3D.
4.  Chiamare [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) per inviare un comando [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) al canale autenticato.

Il diagramma seguente illustra lo scambio di handle:

![Diagramma che mostra come il decodificatore dxva è associato alla sessione di crittografia.](images/d3d9video03.png)

Il decodificatore software può ora usare la chiave della sessione di crittografia per crittografare i buffer video compressi. Ogni buffer compresso avrà il proprio vettore di inizializzazione (IV) specificato nel membro **pvPVPState** della [**struttura DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc) dati.

## <a name="sending-authenticated-channel-commands"></a>Invio di comandi del canale autenticato

Viene definito un set di comandi per la configurazione del canale autenticato e l'impostazione di varie protezioni del contenuto. Per un elenco di comandi, vedere protezione del contenuto [comandi](content-protection-commands.md).

Per inviare un comando al canale autenticato, seguire questa procedura.

1.  Compilare la struttura dei dati di input. Questa struttura di dati è sempre [**una D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) struttura seguita da campi aggiuntivi. Compilare la **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** struttura come illustrato nella tabella seguente.

    
| Membro | Descrizione | 
|--------|-------------|
| <strong>Omac</strong> | Ignorare questo campo per il momento. | 
| <strong>ConfigureType</strong> | GUID che identifica il comando. Per un elenco di comandi, vedere protezione del contenuto <a href="content-protection-commands.md">comandi</a>. | 
| <strong>hChannel</strong> | Handle per il canale autenticato. | 
| <strong>Sequencenumber</strong> | Numero di sequenza. Il primo numero di sequenza viene specificato inviando un <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> comando . Ogni volta che si invia un altro comando, incrementare questo numero di 1. Il numero di sequenza protegge dagli attacchi di tipo replay.    <blockquote>    [!Note]<br />    Vengono usati due numeri di sequenza separati, uno per i comandi e uno per le query.    </blockquote><br /><br /> | 


    

     

2.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il **membro omac** della struttura di input. Copiare quindi il valore del tag nel **membro omac.**
3.  Chiamare [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).
4.  Il driver inserisce l'output del comando [**nella D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) struttura .
5.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il **membro omac** della struttura di output. Confrontarlo con il valore del **membro omac.** Esito negativo se non corrispondono.
6.  Confrontare i valori dei **membri ConfigureType**, **hChannel** e **SequenceNumber** nella struttura di output con i valori per tali membri. Esito negativo se non corrispondono.
7.  Incrementare il numero di sequenza per il comando successivo.

## <a name="sending-authenticated-channel-queries"></a>Invio di query sul canale autenticato

Viene definito un set di query per il recupero di informazioni sul canale autenticato. Per un elenco di query, vedere protezione del contenuto [query](content-protection-queries.md).

Per inviare un comando al canale autenticato, seguire questa procedura.

1.  Compilare la struttura dei dati di input. Questa struttura di dati è sempre [**una D3DAUTHENTICATEDCHANNEL_QUERY_INPUT,**](d3dauthenticatedchannel-query-input.md) possibilmente seguita da campi aggiuntivi. Compilare la **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** struttura come illustrato nella tabella seguente.

    
| Membro | Descrizione | 
|--------|-------------|
| <strong>Tipo di query</strong> | GUID che identifica la query. Per un elenco di query, vedere protezione del contenuto <a href="content-protection-queries.md">query</a>. | 
| <strong>hChannel</strong> | Handle per il canale autenticato. | 
| <strong>Sequencenumber</strong> | Numero di sequenza. Il primo numero di sequenza viene specificato inviando un <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> comando. Ogni volta che si invia un'altra query, incrementare questo numero di 1. Il numero di sequenza protegge dagli attacchi di tipo replay.    <blockquote>    [!Note]<br />    Vengono usati due numeri di sequenza separati, uno per i comandi e uno per le query.    </blockquote><br /><br /> | 


    

     

2.  Chiamare [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).
3.  Il driver inserisce l'output della query in [**una D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) struttura . Questa struttura è seguita da campi aggiuntivi, a seconda del tipo di query.
4.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il **membro omac** della struttura di output. Confrontarlo con il valore del **membro omac.** Esito negativo se non corrispondono.
5.  Confrontare i valori dei **membri ConfigureType**, **hChannel** e **SequenceNumber** nella struttura di output con i valori per tali membri. Esito negativo se non corrispondono.
6.  Incrementare il numero di sequenza per la query successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API Video Direct3D 9](direct3d-video-apis.md)
</dt> </dl>

 

 
