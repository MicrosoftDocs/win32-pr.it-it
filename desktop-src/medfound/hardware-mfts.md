---
description: Questo argomento descrive come scrivere una trasformazione Media Foundation (MFT) che funge da proxy per un codificatore hardware, un decodificatore o un processore di segnale digitale (DSP).
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: MFTs hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5ce05b4fdad6040b51f66f543c1737fc3918d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226460"
---
# <a name="hardware-mfts"></a>MFTs hardware

> [!Note]  
> Questo argomento si applica a Windows 7 o versione successiva.

 

Questo argomento descrive come scrivere una trasformazione Media Foundation (MFT) che funge da proxy per un codificatore hardware, un decodificatore o un processore di segnale digitale (DSP).

> [!IMPORTANT]
> Se un codec hardware usa il driver della classe multimediale AVStream, non richiede un MFT personalizzato. Media Foundation fornisce un proxy AVStream a questo scopo. Le informazioni contenute in questo argomento si applicano solo nel caso speciale in cui il codec hardware non utilizza AVStream. Per ulteriori informazioni, vedere [supporto dei codec hardware in AVStream](https://msdn.microsoft.com/library/dd568169.aspx).

 

In questo argomento sono incluse le sezioni seguenti:

-   [Introduzione](#introduction)
-   [Attributi hardware MFT](#hardware-mft-attributes)
-   [Sequenza di handshake hardware](#hardware-handshake-sequence)
-   [Elaborazione dati](#data-processing)
-   [Codificatore/codificatore abbinato](#paired-decoderencoder)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Qualsiasi codec hardware non basato su AVStream deve fornire il proprio MFT per fungere da proxy per il driver. Un codec hardware può incorporare diversi blocchi funzionali distinti:

-   Codificatore
-   Decodificatore
-   Ridimensionamento del frame/conversione del formato

Ognuna di queste funzioni deve essere gestita da un MFT separato. Una MFT hardware non deve mai fungere da "transcodificatore multifunzione". Al contrario, inserire le funzioni di codifica in un codificatore MFT e decodifica le funzioni in un decodificatore MFT. Se l'hardware offre la scalabilità dei frame e le conversioni di formato, inserire le funzioni in un processore video separato, registrato nella categoria del **\_ \_ \_ processore video della categoria MFT** . Se l'hardware non supporta il ridimensionamento dei frame o la conversione del formato, Media Foundation fornisce un processore video software.

I requisiti generali per MFTs hardware sono i seguenti:

-   MFTs hardware deve usare il nuovo modello di elaborazione asincrona, come descritto in [MFTS asincrono](asynchronous-mfts.md).
-   MFTs hardware deve supportare le modifiche del formato dinamico, come descritto in [modifiche al formato dinamico](basic-mft-processing-model.md).

## <a name="hardware-mft-attributes"></a>Attributi hardware MFT

Una MFT hardware deve implementare i metodi seguenti correlati agli attributi:

-   [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes): restituisce un archivio di attributi per gli attributi MFT globali.
-   [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes): restituisce un archivio di attributi per un flusso di input.
-   [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes): restituisce un archivio di attributi per un flusso di output.

Quando il file MFT viene creato per la prima volta, deve impostare gli attributi seguenti nel relativo archivio attributi globale (ovvero l'archivio di attributi restituito da [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)):



| Attributo                                                                                    | Descrizione                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ trasforma \_ asincrono](mf-transform-async.md)                                               | Deve essere impostato su **true**. Indica che il MFT esegue l'elaborazione asincrona.                                                                                                      |
| [\_ \_ \_ Attributo URL hardware dell'enumerazione MFT \_](mft-enum-hardware-url-attribute.md)                   | Contiene il collegamento simbolico per il dispositivo hardware.<br/> Il caricatore della topologia usa la presenza di questo attributo per verificare se una MFT rappresenta un dispositivo hardware.<br/> |
| [**la \_ \_ modifica del \_ formato \_ dinamico del supporto MFT**](mft-support-dynamic-format-change-attribute.md) | Deve essere impostato su **true**. Indica che il MFT supporta le modifiche del formato dinamico.                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>Sequenza di handshake hardware

Se due MFTs rappresentano lo stesso dispositivo fisico, possono scambiare dati all'interno dell'hardware, ad esempio tramite un bus hardware. Non è necessario copiare i dati nella memoria di sistema e quindi tornare al dispositivo.

Nel diagramma seguente i MFTs con etichetta "A" e "B" rappresentano i blocchi funzionali all'interno dello stesso hardware. In uno scenario di transcodifica, ad esempio, è possibile che "A" rappresenti un decodificatore hardware e che "B" rappresenti un codificatore hardware. Il flusso di dati tra "A" e "B" si verifica all'interno dell'hardware. Il MFT denominato "C" è un software MFT. Il flusso di dati da "B" a "C" utilizza la memoria di sistema.

![diagramma che mostra le caselle con etichetta da a a c e un codec hardware: un punta a b e il codec, il codec punta a b e b punta a c](images/proxy-mft.png)

Per stabilire una connessione hardware, i due MFTs hardware devono usare un canale di comunicazione privato. Questa connessione viene stabilita durante la negoziazione del formato, prima che vengano impostati i tipi di supporto e prima della prima chiamata a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). Il processo di connessione funziona nel modo seguente:

1.  Il caricatore della topologia verifica sia MFTs per la presenza dell'attributo dell' [ \_ \_ \_ \_ attributo dell'URL dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) . Si noti che non viene esaminato il valore di questo attributo.
2.  Se [l' \_ \_ attributo dell' \_ URL \_ hardware dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) è presente in entrambi MFTS, il caricatore della topologia esegue le operazioni seguenti:
    1.  Il caricatore della topologia chiama [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) sulla MFT upstream (A). Questo metodo restituisce un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Lasciare che il puntatore venga indicato come *pUpstream*.
    2.  Il caricatore della topologia chiama [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) nella MFT downstream (B). Questa chiamata restituisce anche un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Lasciare che il puntatore venga indicato come *pDownstream*.
    3.  Il caricatore della topologia imposta l'attributo dell' [ \_ \_ \_ attributo del flusso connesso a MFT](mft-connected-stream-attribute.md) in *PDownstream* chiamando [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). Il valore dell'attributo è il puntatore *pUpstream* .
    4.  Il caricatore della topologia imposta il [MFT \_ connesso all'attributo del \_ \_ \_ flusso HW](mft-connected-to-hw-stream.md) su **true** sia in *pDownstream* che in *pUpstream*.
3.  A questo punto, la MFT downstream presenta un puntatore all'archivio attributi dell'oggetto MFT upstream, come illustrato nel diagramma seguente.

    ![diagramma con ogni MFTS che punta al relativo flusso, ogni flusso che punta al relativo archivio e l'archivio di input con una linea tratteggiata nell'archivio di output](images/proxy-mft2.png)

    > [!Note]  
    > Per maggiore chiarezza, questo diagramma mostra i flussi e gli archivi di attributi come oggetti distinti, ma ciò non è necessario per l'implementazione.

     

4.  La MFT downstream usa il puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per stabilire un canale di comunicazione privato con la MFT upstream. Poiché il canale è privato, il meccanismo esatto viene definito dall'implementazione di. Ad esempio, il MFT potrebbe eseguire una query per un'interfaccia COM privata.

Durante il passaggio 4, l'MFT downstream deve verificare se le due MFTs condividono lo stesso dispositivo fisico. In caso contrario, devono usare la memoria di sistema per il trasporto dei dati. In questo modo, le MFT funzionano correttamente con MFTs software e altri dispositivi hardware.

Se l'handshake ha esito positivo e le due MFTs condividono un canale dati privato, non usano il modello di elaborazione dati standard (descritto nella sezione successiva) nel punto di connessione. In particolare, l'MFT downstream non invia eventi [METransformNeedInput](metransformneedinput.md) ; Per ulteriori informazioni, vedere la sezione successiva in questo argomento.

## <a name="data-processing"></a>Elaborazione dei dati

Quando una MFT hardware usa la memoria di sistema per il trasporto dei dati, il processo funziona nel modo seguente:

1.  Per richiedere più input, il MFT Invia un evento [METransformNeedInput](metransformneedinput.md) .
2.  L'evento [METransformNeedInput](metransformneedinput.md) fa sì che la pipeline chiami [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
3.  Quando il MFT contiene dati di output, il MFT Invia un evento [METransformHaveOutput](metransformhaveoutput.md) .
4.  L'evento [METransformHaveOutput](metransformhaveoutput.md) fa sì che la pipeline chiami [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Per informazioni dettagliate, vedere [MFTS asincrono](asynchronous-mfts.md).

Se la MFT utilizza un canale hardware, tuttavia, questi eventi non vengono inviati al punto di connessione hardware perché tutto il trasferimento dei dati avviene internamente nell'hardware. Pertanto, la pipeline non chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) o [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in corrispondenza del punto di connessione.

Si consideri, ad esempio, il primo diagramma di questo argomento. Data questa configurazione, l'elaborazione dei dati verrebbe eseguita nel modo seguente:

1.  "A" Invia [METransformNeedInput](metransformneedinput.md) ai dati della richiesta.
2.  La pipeline chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) su "A".
3.  "A" e "B" elaborano i dati nell'hardware.
4.  Al termine dell'elaborazione, "B" Invia un evento [METransformHaveOutput](metransformhaveoutput.md) .
5.  La pipeline chiama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) su "B".

## <a name="paired-decoderencoder"></a>Codificatore/codificatore abbinato

Se un codificatore e un codificatore si trovano nello stesso chip hardware, può essere preferibile utilizzarli insieme durante la transcodifica. In altre termini, la selezione di uno deve causare la selezione dell'altra nella pipeline di transcodifica. Per assicurarsi che vengano scelti i codec hardware corrispondenti, sia il codec MFTs dovrebbe offrire un tipo di supporto personalizzato. Per creare un tipo di supporto personalizzato:

-   Impostare l'attributo di [**\_ \_ \_ tipo principale MF mt**](mf-mt-major-type-attribute.md) su **MFMediaType \_ audio** o **MFMediaType \_ video**, in base alle esigenze.
-   Impostare l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) su un valore GUID personalizzato.

Altri attributi di tipo sono facoltativi. Il decodificatore restituisce il tipo personalizzato dal relativo [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)e il codificatore restituisce il tipo personalizzato dal metodo [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) . In entrambi i casi, il tipo personalizzato deve essere la prima voce dell'elenco (*dwTypeIndex* = 0).

Per lavorare con i codec software, il codec deve anche restituire almeno un formato standard, ad esempio NV12 per il video. I formati standard devono essere visualizzati dopo il tipo personalizzato (*dwTypeIndex* > 0). Se i due codec devono essere sempre abbinati e non possono interagire con i codec software, MFTs deve restituire solo il formato personalizzato e non restituire alcun formato standard.

> [!Note]  
> Se un decodificatore non restituisce formati standard, non può essere usato per la riproduzione con il [renderer video migliorato](enhanced-video-renderer.md). In tal caso, deve essere registrato come decodificatore solo transcodifica. Vedere [decodificatori solo transcodificati](implementing-a-codec-mft.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> <dt>

[Implementazione di un codec MFT](implementing-a-codec-mft.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




