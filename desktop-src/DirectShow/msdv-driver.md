---
description: Driver MSDV
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: Driver MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7c1bda24980abe84a11613126476ccfe35380d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401073"
---
# <a name="msdv-driver"></a>Driver MSDV

MSDV è il driver Microsoft Windows Driver Model (WDM) per le videocamere DV. Il driver viene visualizzato come filtro DirectShow quando il dispositivo è alimentato da rete elettrica. Viene enumerata in due categorie di filtro:

-   CLSID \_ VideoInputDeviceCategory ("origini acquisizione video")
-   Rendering di AM \_ KSCATEGORY \_ ("dispositivi per il rendering di flussi WDM")

Il nome descrittivo del filtro è `Microsoft DV Camera and VCR` o un equivalente localizzato. In alcuni dispositivi, la proprietà **Description** contiene una descrizione del modello specifico, che può essere usato al posto del nome descrittivo generico. Per altre informazioni, vedere [selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).

MSDV ha due pin di output. Un pin fornisce frame DV che contengono dati audio e video con interfoliazione. L'altro pin fornisce frame solo video senza audio. MSDV non è in grado di eseguire lo streaming da entrambi i pin contemporaneamente, quindi è possibile connettere un solo pin di output alla volta. Per altre informazioni sull'acquisizione di video da un dispositivo DV, vedere [Capture DV to file](capture-dv-to-file.md).

![acquisizione dei dati DV dal dispositivo](images/dv-filters4.png)

La maggior parte delle videocamere DV dispone di una sottounità VTR (video tape recorder), che può trasmettere dati dal nastro al computer. Per l'applicazione, l'acquisizione da nastro funziona come l'acquisizione di video live. L'unica differenza è che l'applicazione deve controllare il trasporto del nastro esterno, ovvero avviare e arrestare il nastro, il rewind e così via. A questo scopo, MSDV espone le interfacce [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)e [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) . Per ulteriori informazioni sul controllo di un VTR, vedere [controllo di un camcorder DV](controlling-a-dv-camcorder.md).

È anche possibile trasmettere il DV dal computer alla videocamera. Il video può quindi essere visualizzato nella schermata onboard della videocamera o registrato su nastro. Per supportare questa funzionalità, MSDV ha un pin di input che può ricevere un flusso DV con interfoliazione. Quando il pin di input è connesso, MSDV funge da filtro renderer anziché da filtro di acquisizione. MSDV non supporta la ricerca in questa modalità. Per altre informazioni sull'invio di DV al dispositivo, vedere [trasmettere DV da un file a un nastro](transmit-dv-from-file-to-tape.md).

![trasmissione di dati DV al dispositivo](images/dv-filters5.png)

Si noti che i pin di input e di output non possono essere connessi nello stesso momento, perché il dispositivo non può eseguire il flusso in entrambe le direzioni nello stesso momento.

In molti camcorder, il passaggio tra la modalità VTR e la modalità fotocamera causa la disattivazione del dispositivo. Pertanto, DirectShow potrebbe perdere il dispositivo quando l'utente passa da una modalità all'altra. Per informazioni sugli eventi di rimozione dei dispositivi, vedere [notifica di rimozione del dispositivo](device-removal-notification.md).

## <a name="remarks"></a>Commenti

Per informazioni sui formati DV supportati dal driver MSDV, vedere [**sottotipi video DV**](dv-video-subtypes.md).

Alcuni suggerimenti sulla creazione di grafici di filtro con MSDV:

-   Non è possibile usare [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) per eseguire il rendering di un pin di output in Msdv. Il gestore del grafico del filtro tenta di connettere il pin di output al pin di input di MSDV, che ha esito negativo. Usare invece [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) o [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).
-   Quando un grafico a filtro contiene MSDV, MSDV deve fornire l'orologio di riferimento per il grafico. A partire da DirectX 8,0, Filter Graph Manager sceglierà automaticamente MSDV come clock di riferimento. Con le versioni precedenti, è consigliabile chiamare il metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) in gestione grafico dei filtri. Per altre informazioni sugli orologi, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).
-   A seconda del dispositivo, alcuni metodi in **IAMExtDevice**, **IAMExtTransport** e **IAMTimeCodeReader** potrebbero restituire codici di errore Windows anziché valori **HRESULT** . I codici di errore possibili includono i seguenti.

    | Codice di errore              | Descrizione                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | \_timeout errore          | Si è verificato il timeout di un comando dispositivo esterno.                                                        |
    | ERRORE \_ req \_ non \_ definit  | Il dispositivo non ha accettato questo comando del dispositivo esterno.                                          |
    | ERRORE \_ non \_ supportato   | Il dispositivo non supporta il comando dispositivo esterno.                                        |
    | richiesta di errore \_ \_ interrotta | Un comando dispositivo esterno è stato interrotto. Probabilmente il dispositivo è stato rimosso o si è verificata una reimpostazione del bus. |

    

     

### <a name="device-information"></a>Informazioni sul dispositivo

In Windows Millennium Edition e Windows XP il moniker del dispositivo del filtro DV supporta una proprietà **Description** oltre alla proprietà **FriendlyName** . Questa proprietà restituisce una descrizione del dispositivo, tratto dal file INF, che in genere contiene il nome del marchio del dispositivo. Questa proprietà non è tuttavia supportata per tutti i modelli di dispositivo.

Per ulteriori informazioni sui moniker dei dispositivi, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).

### <a name="clock-times"></a>Ore di clock

Il driver MSDV usa il clock del bus 1394 incluso nei pacchetti di dati 1394 per derivare il clock. Usa questi valori per contrassegnare il timestamp degli esempi di supporti DV. Poiché questo orologio di origine non è il clock di sistema del computer, i tempi verranno rimossi dal clock di sistema del computer. Come indicato in precedenza, tuttavia, per impostazione predefinita, il gestore del grafo del filtro selezionerà MSDV come clock di riferimento del grafo.

L'interfaccia [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) segnala la misura corrente dei frame eliminati del driver; Questo valore potrebbe non essere perfettamente sincronizzato con il numero effettivo di frame eliminati in un determinato momento. Se i frame vengono eliminati, significa che il sistema non è bilanciato (la produzione dei dati supera l'utilizzo dei dati). Ad esempio, il disco rigido dell'utente potrebbe non essere sufficientemente veloce per supportare le velocità di acquisizione DV.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



