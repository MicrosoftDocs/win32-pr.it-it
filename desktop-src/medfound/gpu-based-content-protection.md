---
description: Descrive il contenuto video&\# 8211; funzionalità di protezione che possono essere fornite da un driver di grafica.
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based protezione del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc1a0f88cae199b9aab38e5ec429ea5427f44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559601"
---
# <a name="gpu-based-content-protection"></a>GPU-Based protezione del contenuto

Questo argomento descrive il contenuto video, ovvero le funzionalità di protezione che possono essere fornite da un driver di grafica.

-   [Introduzione](#introduction)
-   [Panoramica del processo di decodifica](#overview-of-the-decoding-process)
-   [Crittografia dei buffer video compressi per il decodificatore](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. eseguire una query sulle funzionalità di protezione del contenuto del driver](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. configurare il canale autenticato](#2-configure-the-authenticated-channel)
    -   [3. configurare la sessione di crittografia](#3-configure-the-cryptographic-session)
    -   [4. ottenere un handle per il dispositivo di decodificatore DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [5. associare il decodificatore DXVA alla sessione di crittografia](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [Invio di comandi del canale autenticato](#sending-authenticated-channel-commands)
-   [Invio di query sul canale autenticato](#sending-authenticated-channel-queries)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Il diagramma seguente mostra una visualizzazione semplificata del modo in cui il contenuto video protetto passa attraverso la pipeline per il rendering.

![diagramma che mostra il contenuto video protetto.](images/d3d9video01.png)

> [!Note]  
> Il [percorso multimediale protetto](protected-media-path.md) (PMP) non è illustrato in questo diagramma. Il flusso di dati visualizzato qui potrebbe verificarsi in un processo PMP o all'interno di un processo dell'applicazione.

 

Il decodificatore riceve dati video crittografati e compressi da un'origine esterna. Si presuppone inoltre che il decodificatore riceva anche una chiave crittografica per decrittografare i dati. Questo argomento non descrive lo scambio di chiave tra l'origine video e il decodificatore, ma il PMP definisce un possibile meccanismo. La GPU non è in questa fase.

Per la decodifica con accelerazione hardware, il decodificatore software passa il contenuto video compresso alla GPU. Per proteggere questo contenuto, il decodificatore esegue nuovamente la crittografia dei dati, in genere usando AES-CTR, prima di passarli all'acceleratore hardware. Viene definito un meccanismo di scambio delle chiavi tra il decodificatore e il driver di grafica.

I fotogrammi video decodificati vengono archiviati nella memoria video, generalmente in chiaro. A questo punto, i frame vengono elaborati e quindi presentati. Sono disponibili due opzioni principali per la presentazione.

-   I frame possono essere presentati usando una sovrapposizione hardware. Per ulteriori informazioni, vedere [supporto della sovrimpressione hardware](hardware-overlay-support.md).
-   I frame possono essere presentati dalla finestra desktop Manage (DWM) utilizzando una superficie condivisa.

L'ultimo passaggio consiste nel visualizzare il frame sul monitor, che può richiedere la protezione dei collegamenti tra la scheda grafica e il dispositivo di visualizzazione. Un esempio di protezione dei collegamenti è High-Bandwidth protezione del contenuto digitale (HDCP). La protezione del collegamento viene configurata tramite [Output Protection Manager](output-protection-manager.md) (OPM). Questo argomento non descrive l'OPM; Per ulteriori informazioni, vedere [utilizzo di output Protection Manager](using-output-protection-manager.md).

## <a name="overview-of-the-decoding-process"></a>Panoramica del processo di decodifica

Durante la decodifica con accelerazione hardware, il decodificatore software deve passare dati video compressi alla scheda grafica. Per il contenuto premium, questi dati in genere devono essere crittografati, usando la crittografia a chiave simmetrica, prima che vengano inviati alla GPU.

Per crittografare il video per la decodifica, il decodificatore software usa le interfacce seguenti:

-   [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder). Rappresenta il dispositivo decodificatore DXVA, detto anche acceleratore.
-   [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9). Rappresenta una sessione di crittografia che fornisce la chiave di crittografia.
-   [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9). Rappresenta un canale autenticato, che consente al decodificatore software di associare la sessione di crittografia al decodificatore DXVA.

![diagramma che mostra le interfacce di decodifica Direct3D9.](images/d3d9video02.png)

Tutte queste interfacce vengono ottenute dal dispositivo Direct3D, come indicato di seguito:



| Interfaccia                                                                | Creazione                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | Chiamare [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). Il dispositivo decodificatore DXVA è identificato da un GUID del profilo DXVA. |
| [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | Chiamare [**IDirect3DDevice9Video:: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession).                                                                         |
| [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | Chiamare [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).                                                           |



 

> [!Note]  
> Per ottenere un puntatore all'interfaccia [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) , chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su un dispositivo D3D9Ex.

 

Il canale autenticato fornisce un canale di comunicazione attendibile tra il decodificatore software e il driver. Il canale di comunicazione funziona nel modo seguente:

-   Il driver fornisce una catena di certificati X. 509 il cui certificato radice è firmato da Microsoft.
-   Il certificato contiene una chiave pubblica RSA per il driver.
-   Il decodificatore software usa la chiave pubblica per inviare al driver una chiave di sessione AES a 128 bit.
-   Il decodificatore software invia le query e i comandi al canale autenticato.
-   La chiave di sessione viene usata per calcolare i codici Mac (Message Authentication Code) per le query e i comandi. Il driver usa i computer Mac per verificare l'integrità dei dati di query/comando e il decodificatore software li usa per verificare l'integrità dei dati di risposta dal driver.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Crittografia dei buffer video compressi per il decodificatore

Ecco una panoramica di alto livello del processo di crittografia e decodifica:

1.  Il decodificatore software riceve un flusso di dati crittografati dall'origine video. Il decodificatore decrittografa il flusso.
2.  Il decodificatore software negozia una chiave di sessione con la sessione di crittografia.
3.  Il decodificatore software usa il canale autenticato per associare la sessione di crittografia al dispositivo di decodificatore DXVA.
4.  Il decodificatore software inserisce i dati compressi nei buffer DXVA ottenuti dal dispositivo di decodificatore DXVA (Accelerator). Per il contenuto protetto, il codificatore software crittografa i dati inseriti nei buffer DXVA, usando la chiave di sessione per la crittografia.
    > [!Note]  
    > Alcuni driver usano una chiave simmetrica invece della chiave della sessione per la crittografia. La chiave simmetrica può variare da un fotogramma a quello successivo.

     

5.  Il decodificatore invia i buffer compressi crittografati al tasto di scelta rapida. Per AES-CTR, il decodificatore passa anche il vettore di inizializzazione. Se viene usata una chiave simmetrica, il decodificatore passa la chiave simmetrica, crittografata usando la chiave della sessione.

Direct3D dispone del supporto standard per AES-CTR a 128 bit, ma è progettato per essere esteso ad altri tipi di crittografia.

Le cinque sezioni successive forniscono passaggi più dettagliati.

-   [1. eseguire una query sulle funzionalità di protezione del contenuto del driver](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. configurare il canale autenticato](#2-configure-the-authenticated-channel)
-   [3. configurare la sessione di crittografia](#3-configure-the-cryptographic-session)
-   [4. ottenere un handle per il dispositivo di decodificatore DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
-   [5. associare il decodificatore DXVA alla sessione di crittografia](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. eseguire una query sulle funzionalità di protezione del contenuto del driver

Prima di provare ad applicare la crittografia, ottenere le funzionalità di protezione del contenuto del driver.

1.  Ottenere un puntatore al dispositivo Direct3D 9.
2.  Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per l'interfaccia [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) .
3.  Chiamare [**IDirect3DDevice9Video:: GetContentProtectionCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps). Questo metodo compila una struttura [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) con le funzionalità di protezione del contenuto del driver.

In particolare, cercare le funzionalità seguenti:

-   Se il membro **Caps** contiene il flag **D3DCPCAPS_SOFTWARE** o **D3DCPCAPS_HARDWARE** , il driver può eseguire la crittografia.
-   Il membro **KeyExchangeType** specifica come eseguire lo scambio di chiave per la chiave della sessione.
-   Se il membro **Caps** contiene il flag di **D3DCPCAPS_CONTENTKEY** , il driver utilizza una chiave simmetrica separata per la crittografia. Questo è importante quando si genera la chiave della sessione.

Nel membro **Caps** sono indicate funzionalità aggiuntive.

### <a name="2-configure-the-authenticated-channel"></a>2. configurare il canale autenticato

Il passaggio successivo consiste nel configurare il canale autenticato.

1.  Chiamare [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) per creare il canale autenticato. Per il parametro *ChannelType* , specificare un tipo di canale corrispondente alle funzionalità del driver.
    -   Il tipo di canale **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** corrisponde a **D3DCPCAPS_SOFTWARE**.
    -   Il tipo di canale **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** corrisponde a **D3DCPCAPS_HARDWARE**.

    Il metodo **CreateAuthenticatedChannel** restituisce un puntatore all'interfaccia [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) insieme a un handle per il canale. L'handle viene utilizzato in un secondo momento per associare la sessione di crittografia al canale autenticato.
2.  Chiamare [**IDirect3DAuthenticatedChannel9:: GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) per ottenere le dimensioni del certificato X. 509 del driver. Allocare un buffer della dimensione richiesta.
3.  Chiamare [**IDirect3DAuthenticatedChannel9:: GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) per ottenere il certificato. Il metodo copia il certificato nel buffer allocato nel passaggio precedente.
4.  Verificare che il certificato del driver sia stato firmato da Microsoft e non sia stato revocato.
5.  Ottenere la chiave pubblica dal certificato.
6.  Genera una chiave di sessione RSA casuale. Questa chiave di sessione viene utilizzata per firmare i dati inviati al canale autenticato. Crittografare la chiave della sessione utilizzando la chiave pubblica del driver.
7.  Chiamare [**IDirect3DAuthenticatedChannel9:: NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) per inviare la chiave della sessione crittografata al driver.
8.  Inizializzare il canale sicuro come segue:
    1.  Compilare una struttura [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) come descritto nella documentazione.
    2.  Inviare il comando [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) chiamando [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) come descritto nella sezione invio dei [comandi del canale autenticato](#sending-authenticated-channel-commands). Questo comando contiene i numeri di sequenza iniziali per i comandi e le query inviati al canale autenticato.
9.  Verificare il tipo di canale inviando una query [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) al canale autenticato, come descritto nella sezione [invio di query sul canale autenticato](#sending-authenticated-channel-queries). Verificare che il tipo di canale corrisponda a quanto specificato nel metodo [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) .

### <a name="3-configure-the-cryptographic-session"></a>3. configurare la sessione di crittografia

Configurare quindi la sessione di crittografia e stabilire la chiave della sessione.

1.  Chiamare [**IDirect3DDevice9Video:: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) per creare la sessione di crittografia. Questo metodo restituisce un puntatore all'interfaccia [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) insieme a un handle per la sessione di crittografia.
2.  Chiamare [**IDirect3DCryptoSession9:: GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) per ottenere le dimensioni del certificato X. 509 del driver. Allocare un buffer della dimensione richiesta.
3.  Chiamare [**IDirect3DCryptoSession9:: GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) per ottenere il certificato. Il metodo copia il certificato nel buffer allocato nel passaggio precedente.
4.  Verificare che il certificato del driver sia stato firmato da Microsoft e non sia stato revocato.
5.  Ottenere la chiave pubblica dal certificato.
6.  Genera una chiave di sessione RSA casuale. Si tratta di una chiave di sessione separata dalla chiave di sessione del canale autenticato. Crittografare la chiave della sessione utilizzando la chiave pubblica del driver.
7.  Chiamare [**IDirect3DCryptoSession9:: NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) per inviare la chiave della sessione crittografata al driver.
8.  Se le funzionalità di protezione del contenuto includono **D3DCPCAPS_CONTENTKEY**, creare una chiave simmetrica casuale di RSA. Questa operazione verrà utilizzata in un secondo momento nel processo di decodifica.

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a>4. ottenere un handle per il dispositivo di decodificatore DXVA

Per il passaggio successivo, sarà necessario un handle per il dispositivo di decodificatore DXVA. Per ottenere questo handle, compilare una struttura DXVA2_DecodeExecuteParams come indicato di seguito:


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



Impostare il membro **pExtensionData** della struttura [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) sull'indirizzo di una struttura di [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) .

Nella struttura [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) impostare il membro della **funzione** su **DXVA2_DECODE_GET_DRIVER_HANDLE**. Impostare **pPrivateOutputData** sull'indirizzo di un buffer sufficientemente grande da archiviare un valore di **handle** . Nell'esempio precedente, questo buffer è la variabile *hDecodeDeviceHandle* .

Chiamare quindi [**IDirectXVideoDecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) e passare l'indirizzo della struttura [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) . L'handle per il decodificatore DXVA viene restituito in **pPrivateOutputData**.

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a>5. associare il decodificatore DXVA alla sessione di crittografia

Successivamente, associare il dispositivo DXVA decoder al dispositivo Direct3D e alla sessione di crittografia, come indicato di seguito:

1.  Ottenere un handle per il dispositivo di decodificatore DXVA, come descritto nella sezione precedente.
2.  Ottenere un handle per il dispositivo Direct3D inviando una query di [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) al canale autenticato.
3.  Compilare una struttura [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) con le seguenti informazioni:
    -   Impostare il membro **DXVA2DecodeHandle** sull'handle del dispositivo DXVA decoder.
    -   Impostare il membro **CryptoSessionHandle** sull'handle per la sessione di crittografia. Questo handle viene restituito dal metodo [**IDirect3DDevice9Video:: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) .
    -   Impostare il membro **DeviceHandle** sull'handle del dispositivo Direct3D.
4.  Chiamare [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) per inviare un comando [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) al canale autenticato.

Il diagramma seguente illustra lo scambio di handle:

![diagramma che Mostra come il decodificatore DXVA è associato alla sessione di crittografia.](images/d3d9video03.png)

Il decodificatore software ora può usare la chiave della sessione di crittografia per crittografare i buffer video compressi. Ogni buffer compresso avrà il proprio vettore di inizializzazione (IV) specificato nel membro **pvPVPState** della struttura [**DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc) .

## <a name="sending-authenticated-channel-commands"></a>Invio di comandi del canale autenticato

Viene definito un set di comandi per configurare il canale autenticato e impostare varie protezioni del contenuto. Per un elenco di comandi, vedere [protezione del contenuto comandi](content-protection-commands.md).

Per inviare un comando al canale autenticato, seguire questa procedura.

1.  Compilare la struttura dei dati di input. Questa struttura di dati è sempre una struttura di [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) seguita da campi aggiuntivi. Compilare la struttura **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** come illustrato nella tabella seguente.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Membro</th>
    <th>Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>OMAC</strong></td>
    <td>Ignorare questo campo per il momento.</td>
    </tr>
    <tr class="even">
    <td><strong>ConfigureType</strong></td>
    <td>GUID che identifica il comando. Per un elenco di comandi, vedere <a href="content-protection-commands.md">protezione del contenuto comandi</a>.</td>
    </tr>
    <tr class="odd">
    <td><strong>hChannel</strong></td>
    <td>Handle per il canale autenticato.</td>
    </tr>
    <tr class="even">
    <td><strong>SequenceNumber</strong></td>
    <td>Numero di sequenza. Il primo numero di sequenza viene specificato inviando un comando <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Ogni volta che si invia un altro comando, incrementare il numero di 1. Il numero di sequenza protegge da attacchi di riproduzione.
    <blockquote>
    [!Note]<br />
Vengono utilizzati due numeri di sequenza distinti, uno per i comandi e uno per le query.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il membro **OMAC** della struttura di input. Copiare quindi il valore del tag nel membro **OMAC** .
3.  Chiamare [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).
4.  Il driver inserisce l'output del comando nella struttura [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) .
5.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il membro **OMAC** della struttura di output. Confrontare con il valore del membro **OMAC** . Esito negativo se non corrispondono.
6.  Confrontare i valori dei membri **ConfigureType**, **hChannel** e **SequenceNumber** nella struttura di output con i valori per tali membri. Esito negativo se non corrispondono.
7.  Incrementare il numero di sequenza del comando successivo.

## <a name="sending-authenticated-channel-queries"></a>Invio di query sul canale autenticato

Viene definito un set di query per il recupero di informazioni sul canale autenticato. Per un elenco di query, vedere [protezione del contenuto query](content-protection-queries.md).

Per inviare un comando al canale autenticato, seguire questa procedura.

1.  Compilare la struttura dei dati di input. Questa struttura di dati è sempre una struttura di [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) , probabilmente seguita da campi aggiuntivi. Compilare la struttura **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** come illustrato nella tabella seguente.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Membro</th>
    <th>Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>QueryType</strong></td>
    <td>GUID che identifica la query. Per un elenco di query, vedere <a href="content-protection-queries.md">protezione del contenuto query</a>.</td>
    </tr>
    <tr class="even">
    <td><strong>hChannel</strong></td>
    <td>Handle per il canale autenticato.</td>
    </tr>
    <tr class="odd">
    <td><strong>SequenceNumber</strong></td>
    <td>Numero di sequenza. Il primo numero di sequenza viene specificato inviando un comando <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Ogni volta che si invia un'altra query, il numero viene incrementato di 1. Il numero di sequenza protegge da attacchi di riproduzione.
    <blockquote>
    [!Note]<br />
Vengono utilizzati due numeri di sequenza distinti, uno per i comandi e uno per le query.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).
3.  Il driver inserisce l'output dalla query in una struttura [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) . Questa struttura è seguita da campi aggiuntivi, a seconda del tipo di query.
4.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il membro **OMAC** della struttura di output. Confrontare con il valore del membro **OMAC** . Esito negativo se non corrispondono.
5.  Confrontare i valori dei membri **ConfigureType**, **hChannel** e **SequenceNumber** nella struttura di output con i valori per tali membri. Esito negativo se non corrispondono.
6.  Incrementa il numero di sequenza per la query successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API video Direct3D 9](direct3d-video-apis.md)
</dt> </dl>

 

 
