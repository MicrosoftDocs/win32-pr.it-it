---
description: Questo argomento descrive come scrivere una trasformazione Media Foundation (MFT) che funge da proxy per un codificatore hardware, un decodificatore o un processore di segnale digitale (DSP).
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: MFT hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532fef959e2c2b5946d5a27ad98106a2e25cc77f8426c0a871e821c7298a69f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724935"
---
# <a name="hardware-mfts"></a>MFT hardware

> [!Note]  
> Questo argomento si applica a Windows 7 o versioni successive.

 

Questo argomento descrive come scrivere una trasformazione Media Foundation (MFT) che funge da proxy per un codificatore hardware, un decodificatore o un processore di segnale digitale (DSP).

> [!IMPORTANT]
> Se un codec hardware usa il driver della classe multimediale AVStream, non richiede un MFT personalizzato. Media Foundation fornisce un proxy AVStream a questo scopo. Le informazioni contenute in questo argomento si applicano solo nel caso speciale in cui il codec hardware non usa AVStream. Per altre informazioni, vedere [Supporto dei codec hardware in AVStream.](https://msdn.microsoft.com/library/dd568169.aspx)

 

In questo argomento sono incluse le sezioni seguenti:

-   [Introduzione](#introduction)
-   [Attributi MFT hardware](#hardware-mft-attributes)
-   [Sequenza di handshake hardware](#hardware-handshake-sequence)
-   [Elaborazione dati](#data-processing)
-   [Decodificatore/codificatore associato](#paired-decoderencoder)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Qualsiasi codec hardware non basato su AVStream deve fornire il proprio MFT per fungere da proxy per il driver. Un codec hardware potrebbe incorporare diversi blocchi funzionali distinti:

-   Codificatore
-   Decodificatore
-   Ridimensionamento dei frame/conversione del formato

Ognuna di queste funzioni deve essere gestita da un MFT separato. Un MFT hardware non deve mai fungere da "transcodificatore" multiuso. Inserire invece le funzioni di codifica in un codificatore MFT e le funzioni di decodifica in un decodificatore MFT. Se l'hardware offre la scalabilità dei fotogrammi e le conversioni di formato, posizionare tali funzioni in un processore video separato, registrato nella **categoria MFT \_ CATEGORIA \_ PROCESSORE VIDEO. \_** Se l'hardware non supporta la scalabilità dei fotogrammi o la conversione del formato, Media Foundation fornisce un processore video software.

I MFT hardware hanno i requisiti generali seguenti:

-   I MFT hardware devono usare il nuovo modello di elaborazione asincrona, come descritto in [MFT asincroni.](asynchronous-mfts.md)
-   I file MFT hardware devono supportare le modifiche al formato dinamico, come descritto in [Dynamic Format Changes](basic-mft-processing-model.md).

## <a name="hardware-mft-attributes"></a>Attributi MFT hardware

Un MFT hardware deve implementare i metodi seguenti correlati agli attributi:

-   [**IMFTransform::GetAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)restituisce un archivio di attributi per gli attributi MFT globali.
-   [**IMFTransform::GetInputStreamAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)restituisce un archivio di attributi per un flusso di input.
-   [**IMFTransform::GetOutputStreamAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)restituisce un archivio di attributi per un flusso di output.

Quando viene creato per la prima volta, l'MFT deve impostare gli attributi seguenti nel proprio archivio attributi globale, ovvero l'archivio attributi restituito da [**GetAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)



| Attributo                                                                                    | Descrizione                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md)                                               | Deve essere impostato su **TRUE.** Indica che MFT esegue l'elaborazione asincrona.                                                                                                      |
| [Attributo URL \_ HARDWARE MFT ENUM \_ \_ \_](mft-enum-hardware-url-attribute.md)                   | Contiene il collegamento simbolico per il dispositivo hardware.<br/> Il caricatore della topologia utilizza la presenza di questo attributo per verificare se un MFT rappresenta un dispositivo hardware.<br/> |
| [**MODIFICA DEL FORMATO \_ DINAMICO \_ DEL SUPPORTO \_ \_ MFT**](mft-support-dynamic-format-change-attribute.md) | Deve essere impostato su **TRUE.** Indica che MFT supporta le modifiche di formato dinamico.                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>Sequenza di handshake hardware

Se due MFT rappresentano lo stesso dispositivo fisico, possono scambiare dati all'interno dell'hardware, ad esempio tramite un bus hardware. Non è necessario copiare i dati nella memoria di sistema e quindi nel dispositivo.

Nel diagramma seguente i MFT etichettati "A" e "B" rappresentano blocchi funzionali all'interno dello stesso hardware. In uno scenario di transcoding, ad esempio, "A" potrebbe rappresentare un decodificatore hardware e "B" potrebbe rappresentare un codificatore hardware. Il flusso di dati tra "A" e "B" si verifica all'interno dell'hardware. MFT con etichetta "C" è un software MFT. Il flusso di dati da "B" a "C" usa la memoria di sistema.

![diagramma che mostra le caselle etichettate da a a c e un codec hardware: a punta a b e il codec, il codec punta a b e b punta a c](images/proxy-mft.png)

Per stabilire una connessione hardware, i due MFT hardware devono usare un canale di comunicazione privato. Questa connessione viene stabilita durante la negoziazione del formato, prima che i tipi di supporti siano impostati e prima della prima chiamata a [**ProcessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) Il processo di connessione funziona come segue:

1.  Il caricatore della topologia verifica la presenza dell'attributo [MFT \_ ENUM \_ HARDWARE URL \_ \_ Attribute](mft-enum-hardware-url-attribute.md) in entrambi i MFT. Si noti che non esamina il valore di questo attributo.
2.  Se [l'attributo \_ URL hardware MFT ENUM \_ \_ \_ ](mft-enum-hardware-url-attribute.md) è presente in entrambi i MFT, il caricatore della topologia esegue le operazioni seguenti:
    1.  Il caricatore della topologia chiama [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) sul MFT upstream (A). Questo metodo restituisce un [**puntatore IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Lasciare che questo puntatore sia *denotato come pUpstream.*
    2.  Il caricatore della topologia chiama [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) sul MFT downstream (B). Questa chiamata restituisce anche un [**puntatore IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Lasciare che questo puntatore sia *denotato pDownstream.*
    3.  Il caricatore della topologia imposta [l'attributo MFT \_ CONNECTED STREAM \_ \_ ATTRIBUTE](mft-connected-stream-attribute.md) su *pDownstream* chiamando [**IMFAttributes::SetUnknown.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) Il valore dell'attributo è il *puntatore pUpstream.*
    4.  Il caricatore della topologia imposta [l'attributo MFT \_ CONNECTED \_ TO \_ HW \_ STREAM](mft-connected-to-hw-stream.md) su **TRUE** sia in *pDownstream* che *in pUpstream.*
3.  A questo punto, l'MFT downstream ha un puntatore all'archivio attributi di MFT upstream, come illustrato nel diagramma seguente.

    ![diagramma con ogni mft che punta al relativo flusso, ogni flusso che punta al relativo archivio e l'archivio di input con una linea tratteggiata all'archivio di output](images/proxy-mft2.png)

    > [!Note]  
    > Per maggiore chiarezza, questo diagramma mostra i flussi e gli archivi di attributi come oggetti distinti, ma questo non è necessario per l'implementazione.

     

4.  Il MFT downstream usa il [**puntatore IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per stabilire un canale di comunicazione privato con il MFT upstream. Poiché il canale è privato, il meccanismo esatto viene definito dall'implementazione di . Ad esempio, MFT potrebbe eseguire una query per un'interfaccia COM privata.

Durante il passaggio 4, il MFT downstream deve verificare se i due MFT condividono lo stesso dispositivo fisico. In caso contrario, è necessario eseguire il fall back all'uso della memoria di sistema per il trasporto dei dati. In questo modo MFT può funzionare correttamente con MFT software e altri dispositivi hardware.

Se l'handshake ha esito positivo e i due MFT condividono un canale dati privato, non usano il modello di elaborazione dati standard (descritto nella sezione successiva) nel punto di connessione. In particolare, il MFT downstream non invia [eventi METransformNeedInput.](metransformneedinput.md) Per altri dettagli, vedere la sezione successiva di questo argomento.

## <a name="data-processing"></a>Elaborazione dei dati

Quando un MFT hardware usa la memoria di sistema per il trasporto dei dati, il processo funziona come segue:

1.  Per richiedere più input, MFT invia un [evento METransformNeedInput.](metransformneedinput.md)
2.  [L'evento METransformNeedInput](metransformneedinput.md) fa in modo che la pipeline [**chiami IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
3.  Quando il MFT ha dati di output, il MFT invia un [evento METransformHaveOutput.](metransformhaveoutput.md)
4.  [L'evento METransformHaveOutput](metransformhaveoutput.md) fa in modo che la pipeline [**chiami IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Per informazioni dettagliate, vedere [MFT asincroni.](asynchronous-mfts.md)

Se tuttavia il MFT usa un canale hardware, non invia questi eventi al punto di connessione hardware, perché tutto il trasferimento dei dati avviene internamente all'interno dell'hardware. Pertanto, la pipeline non chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) o [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) nel punto di connessione.

Si consideri ad esempio il primo diagramma di questo argomento. Data questa configurazione, l'elaborazione dei dati si verificherà come segue:

1.  "A" invia [METransformNeedInput ai](metransformneedinput.md) dati della richiesta.
2.  La pipeline chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) su "A".
3.  "A" e "B" elaborano i dati nell'hardware.
4.  Al termine dell'elaborazione, "B" invia un [evento METransformHaveOutput.](metransformhaveoutput.md)
5.  La pipeline chiama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) su "B".

## <a name="paired-decoderencoder"></a>Decodificatore/codificatore associato

Se un decodificatore e un codificatore si trovano nello stesso chip hardware, può essere preferibile usarli insieme durante la transcoding. In altre parole, se ne seleziona uno, l'altro deve essere selezionato nella pipeline di transcoduttura. Per assicurarsi che i codec hardware corrispondenti siano scelti, entrambi i codec MFT devono offrire un tipo di supporto personalizzato. Per creare un tipo di supporto personalizzato:

-   Impostare [**l'attributo \_ MF MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) su **MFMediaType \_ Audio** o **MFMediaType \_ Video,** in base alle esigenze.
-   Impostare [**l'attributo \_ MF MT \_ SUBTYPE**](mf-mt-subtype-attribute.md) su un valore GUID personalizzato.

Altri attributi di tipo sono facoltativi. Il decodificatore restituisce il tipo personalizzato dal relativo [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)e il codificatore restituisce il tipo personalizzato dal metodo [**IMFTransform::GetInputAvailableType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) In entrambi i casi, il tipo personalizzato deve essere la prima voce nell'elenco (*dwTypeIndex* = 0).

Per usare i codec software, il codec deve restituire anche almeno un formato standard, ad esempio NV12 per il video. I formati standard devono essere visualizzati dopo il tipo personalizzato (*dwTypeIndex* > 0). Se i due codec devono essere sempre associati e non possono interagire con i codec software, i codec MFT devono restituire solo il formato personalizzato e non restituire alcun formato standard.

> [!Note]  
> Se un decodificatore non restituisce alcun formato standard, non può essere usato per la riproduzione con [il renderer video avanzato.](enhanced-video-renderer.md) In tal caso, deve essere registrato come decodificatore solo transcodifica. Vedere [Decodificatori solo transcodifica.](implementing-a-codec-mft.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> <dt>

[Implementazione di un codec MFT](implementing-a-codec-mft.md)
</dt> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 




