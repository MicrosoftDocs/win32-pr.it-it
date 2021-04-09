---
description: Come i decodificatori usano IAMVideoAccelerator
ms.assetid: 0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d
title: Come i decodificatori usano IAMVideoAccelerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436768b3561a999f6708ef4f6438b816e0ad303b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965467"
---
# <a name="how-decoders-use-iamvideoaccelerator"></a>Come i decodificatori usano IAMVideoAccelerator

L'interfaccia [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) consente operazioni di accelerazione video generiche, inclusa l'accelerazione video DirectX (va). Per l'accelerazione non DirectX VA, il decodificatore e il driver video devono entrambi rispettare un protocollo comune.

In questa sezione viene descritto l'ordine generale delle operazioni che qualsiasi decodificatore deve seguire quando si utilizza questa interfaccia. Altre informazioni specifiche per i decodificatori basati su DirectX VA sono disponibili in [mapping dell'accelerazione video DirectX a IAMVideoAccelerator](mapping-directx-video-acceleration-to-iamvideoaccelerator.md).

> [!Note]  
> Questa interfaccia è disponibile in Windows 2000 e versioni successive.

 

L'interfaccia [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) viene esposta sul pin di input del [mixer overlay](overlay-mixer-filter.md) o del renderer di mixaggio video (VMR). L'interfaccia [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) viene esposta sul pin di output del decodificatore. La sequenza di eventi per la connessione dei pin del filtro è la seguente:

1.  Il gestore del grafo dei filtri chiama [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) sul pin di output del filtro decodificatore. Un [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) è un parametro facoltativo.
    -   [**Am \_ MEDIA \_ Type**](/windows/win32/api/strmif/ns-strmif-am_media_type) è una struttura di dati che descrive un tipo di supporto. Contiene un GUID di majortype (che in questo caso deve essere MEDIATYPE \_ video), un GUID del sottotipo (che in questo caso deve essere un GUID del tasto di scelta rapida video) e una serie di altri elementi. Uno di questi elementi è un GUID di tipo formato che contiene informazioni sui supporti, inclusi in questo caso la larghezza e l'altezza di un'immagine video non compressa, molto probabilmente in una struttura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
    -   La struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , se presente, indica al decodificatore di funzionare usando il tipo di supporto specificato, che può essere "completo" o "parzialmente specificato". Se "completamente specificato", il decodificatore normalmente tenterà semplicemente di operare con tale tipo di supporto. Se il valore è "parzialmente specificato", verrà tentata la ricerca di una modalità di funzionamento compatibile con "completo", che può essere usata per connettersi in modo coerente con il tipo di supporto "parzialmente specificato".
    -   Il modo comune per tentare di trovare un tipo di supporto "completo" da usare per una connessione consiste semplicemente nell'eseguire un elenco di tutti i tipi di supporto "completo" supportati dal pin di output, che è compatibile con il tipo di supporto "parzialmente specificato" e tenta di connettersi a ognuno di essi fino a quando non riesce. Il processo sarebbe normalmente simile se nessun \_ \_ tipo di supporto AM è contenuto nella chiamata [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , ma con il pin di output è necessario controllare tutti i relativi tipi di supporto.
2.  Se il decodificatore vuole verificare se un [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) specifico (incluso un GUID del tasto di scelta rapida) è supportato dal pin di input downstream, può chiamare il [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) (con il GUID del tasto di scelta rapida video come sottotipo del **\_ \_ tipo di supporto am**) o semplicemente tentare di connettersi al pin, come descritto nell'articolo 5 seguente.
3.  Se il decodificatore non è in grado di stabilire quali GUID del tasto di scelta rapida sono supportati dal pin di input downstream e non si desidera proporre solo un determinato GUID dell'acceleratore video candidato chiamando il [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)del PIN di input downstream, il decodificatore può chiamare [**IAMVideoAccelerator:: GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) per ottenere un elenco dei GUID del tasto di scelta rapida supportati dal pin.
4.  Per alcuni GUID del tasto di scelta rapida video, il decodificatore può chiamare il pin di input downstream [**IAMVideoAccelerator:: GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) per ottenere un elenco dei formati pixel **DDPIXELFORMAT** che possono essere usati per eseguire il rendering di un GUID acceleratore video specifico. L'elenco restituito deve essere considerato in ordine di preferenza decrescente (ovvero con il formato preferito elencato per primo).
5.  Il decodificatore chiama il [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)del PIN di input downstream, passandogli un [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) con il GUID del tasto di scelta rapida del video appropriato come sottotipo del tipo di supporto. In questo modo viene configurata la connessione per l'operazione, inclusa la creazione delle superfici di output non compresse (allocate usando la larghezza e l'altezza trovate nel **\_ \_ tipo di supporto am** e il numero di superfici da allocare trovate da una chiamata descritta di seguito e tutte le altre informazioni disponibili per l'acceleratore video, ad esempio il GUID dell'acceleratore video). Se il pin di input downstream rifiuta il GUID dell'acceleratore video o un altro aspetto della connessione, questo può causare un errore di **Ipin:: ReceiveConnection** . Se **Ipin:: ReceiveConnection** ha esito negativo, viene indicato in un **HRESULT** restituito e il decodificatore può tentare di eseguire di nuovo la chiamata, ad esempio, con un nuovo GUID acceleratore video nella struttura del **\_ \_ tipo di supporto am** .
    -   [!Note]  
        > Si tratta di un altro modo (e il modo più definitivo) per il decodificatore di determinare ciò che è supportato dal pin di input downstream, ovvero semplicemente chiamando [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e tentando di connettersi, quindi controllando se il tentativo di connessione ha avuto esito positivo.

         

    -   Durante [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection), il renderer chiama [**IAMVideoAcceleratorNotify:: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo)del decodificatore, passandogli il GUID dell'acceleratore video e una struttura [**AMVAUncompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompbufferinfo) per determinare il numero di superfici non compresse da allocare. Il decodificatore compila e restituisce la struttura che contiene il numero minimo e massimo di superfici da allocare del tipo specifico e una struttura **DDPIXELFORMAT** che descrive il formato pixel delle superfici da allocare.
    -   [!Note]  
        > Nessun elemento viene effettivamente passato al decodificatore nella chiamata a [**IAMVideoAcceleratorNotify:: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo) diverso dal GUID del tasto di scelta rapida del video.

         

6.  Il renderer chiama il [**IAMVideoAcceleratorNotify:: SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)del decodificatore, passando al decodificatore il numero effettivo di superfici non compresse allocate.
7.  Il renderer chiama il [**IAMVideoAcceleratorNotify:: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) del decodificatore per ottenere tutti i dati necessari per inizializzare il video Accelerator.
8.  Il decodificatore chiama [**IAMVideoAccelerator:: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo), passandogli un GUID dell'acceleratore video, una struttura [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) e il numero di tipi di buffer compressi, da ottenere in restituire un set di strutture di dati [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) , una corrispondente a ogni tipo di buffer di dati compresso usato dal GUID del tasto di scelta rapida del video.
    -   La struttura [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) contiene la larghezza e l'altezza dei dati non compressi decodificati (in pixel) e il DDPIXELFORMAT dell'immagine non compressa.
    -   Le strutture di dati [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) restituite ogni contengono:
        -   Numero di buffer compressi necessari per il tipo specifico.
        -   Larghezza e altezza della superficie da creare, ovvero campi che possono o meno avere un significato effettivo.
            > [!Note]  
            > L'operazione di allocazione della superficie di DirectDraw per i buffer compressi attualmente non prevede che la larghezza o l'altezza di queste superfici sia maggiore o uguale a 2 ^ 15, sebbene la chiamata di allocazione della superficie non abbia esito positivo se questo limite viene violato. Il driver potrebbe pertanto strutturare le richieste di memoria buffer compresso per evitare tali dimensioni estreme. Ad esempio, anziché richiedere un buffer con Width = "1" e Height = "65536", il driver deve richiedere un buffer di Width = "1024" e Height = "64".

             

        -   Numero totale di byte che devono essere utilizzati dalla superficie.
        -   Struttura di tipo **DDSCAPS2** che definisce un oggetto DirectDrawSurface, che descrive le funzionalità per creare superfici per archiviare i dati compressi.
        -   DDPIXELFORMAT, che descrive il formato pixel usato per creare le superfici per archiviare i dati compressi (un campo che può avere o meno un significato effettivo).

> [!Note]  
> Le chiamate del renderer ad alcuni dei metodi dell'interfaccia [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) del decodificatore possono (e normalmente) essere eseguite all'interno della chiamata del decodificatore al [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)del renderer. In particolare, si applica a quanto segue:
>
> -   [**IAMVideoAcceleratorNotify:: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo),
> -   [**IAMVideoAcceleratorNotify:: SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)e
> -   [**IAMVideoAcceleratorNotify:: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata).

 

> [!Note]  
> Per supportare le modifiche del formato dinamico, il decodificatore può anche chiamare [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e altri metodi per le versioni precedenti, mentre i filtri sono connessi e in esecuzione. Questa funzionalità viene fornita per supportare le modifiche del formato dinamico (anche se non è presente nel file H. 263, allegato P, Sense, perché tutti i set di dati vengono riavviati da zero e le informazioni sull'immagine di riferimento vengono pertanto perse).

 

Di seguito è riportata una descrizione dell'uso di [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) durante l'operazione dopo l'inizializzazione:

1.  Per ogni superficie non compressa, il decodificatore chiama [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) per iniziare l'elaborazione per creare l'immagine di output. Quando esegue questa operazione, il decodificatore invia una struttura [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) .
    -   La struttura [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) contiene un indice per un buffer di destinazione, un puntatore a alcuni dati da inviare a valle e un puntatore a una posizione in cui l'acceleratore può inserire alcuni dati per la lettura del decodificatore.
    -   Nota 1: il tasto di scelta rapida non riceve effettivamente l'indice del buffer di destinazione perché viene convertito dal renderer prima di andare a valle.
    -   Nota 2: [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) può essere chiamato più di una volta tra le chiamate a [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe).
    -   Nota 3: non esiste alcun presupposto nell'operazione di interfaccia che [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) e [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) devono essere chiamati per l'elaborazione di ogni singola immagine nel bitstream.

        Il risultato di [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) , per quanto riguarda l'interfaccia, consiste nel creare un'associazione all'interno del renderer tra un indice e una superficie non compressa. Fornisce inoltre un metodo per chiamare una funzione specifica in un driver di dispositivo (con supporto di un mezzo per passare dati arbitrari tra il decodificatore e il driver di dispositivo).

        (Tuttavia, nell'operazione DirectX VA viene descritto il requisito seguente che [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) e [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) devono essere chiamati per l'elaborazione di ogni singola immagine nel bitstream).

2.  Per l'invio di dati non compressi al tasto di scelta rapida, il decodificatore chiama:
    -   [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) per determinare se un buffer è sicuro per la lettura o la scrittura in.
    -   [**IAMVideoAccelerator:: GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) per bloccare e ottenere l'accesso a un buffer specificato (se non è stato precedentemente chiamato per ottenere tale accesso). **GetBuffer** può essere utilizzato anche per ottenere una copia del contenuto dell'ultima immagine di output non compressa per cui è stato chiamato [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) , fornendo [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) non è stato chiamato per l'indice del buffer di destinazione. Se l'interfaccia DDI restituisce uno stato di rendering di DDERR \_ WASSTILLDRAWING per il buffer richiesto, un ciclo di sospensione verrà gestito all'interno di **GetBuffer** finché questa condizione non verrà cancellata. Per chiamare **GetBuffer**, il decodificatore richiederà alcune informazioni da una struttura di dati [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) ottenuta chiamando [**IAMVideoAccelerator:: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo).
    -   [**IAMVideoAccelerator:: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) per indicare che devono essere elaborati i dati in un set di buffer compressi come indicato in una matrice di strutture di dati [**AMVABUFFERINFO**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabufferinfo) . Un codice di funzione dwFunction viene passato al driver in questa chiamata. Un puntatore lpPrivateInputData viene inoltre passato ad alcuni dati per l'invio a valle e un puntatore lpPrivateOutputData viene passato a una posizione in cui il processo downstream può inserire alcuni dati per la lettura del decodificatore.
    -   [**IAMVideoAccelerator:: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) per indicare che il decodificatore ha completato l'uso di un buffer specificato per il momento e non è più necessario bloccare l'accesso al buffer. Se il decodificatore vuole continuare a usare il buffer, può semplicemente non chiamare **IAMVideoAccelerator:: ReleaseBuffer** per il momento, evitando di dover chiamare [**IAMVideoAccelerator:: GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) fino a quando non si intende effettivamente utilizzare il buffer. Il decodificatore non deve scrivere nel buffer dopo la chiamata di [**Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) fino a quando [**QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) non indica che il buffer è sicuro per la scrittura.
3.  Per completare l'elaborazione dell'output per un buffer di destinazione, il decodificatore chiama [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe). Può passare dati arbitrari a valle con questa chiamata e questo è essenzialmente tutto ciò che accade in seguito a questa chiamata. Non invia un indice del buffer di destinazione in questa chiamata, pertanto non può indicare all'acceleratore esattamente quale buffer di destinazione viene completato a meno che questa indicazione non sia contenuta nei dati arbitrari passati.
4.  Per visualizzare un frame, il decodificatore chiama [**IAMVideoAccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) con l'indice del frame da visualizzare e una struttura [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) che contiene i timestamp di inizio e di fine e i flag pertinenti, ad esempio **dwTypeSpecificFlags** , nella struttura delle [**\_ \_ Proprietà am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) e **dwInterlaceFlags** nella struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Il decodificatore deve verificare che tutte le operazioni di decompressione che influiscono sul contenuto del frame siano state completate prima di chiamare **DisplayFrame**.
5.  Infine, il decodificatore deve, al completamento di tutte le operazioni di elaborazione, indicare il completamento di tutti i frame di output restanti avviati chiamando [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) e rilasciare tutti i buffer bloccati chiamando [**IAMVideoAccelerator:: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) per ogni buffer non rilasciato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifiche e interfacce del decodificatore](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



