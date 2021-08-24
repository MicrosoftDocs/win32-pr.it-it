---
description: MSDV Driver
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: MSDV Driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5377471f61944c60f57720df6bc64482681d64515f54c853d78cfa405842ff15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748623"
---
# <a name="msdv-driver"></a>MSDV Driver

MSDV è il driver Microsoft Windows Driver Model (WDM) per i videocamere DV. Il driver viene visualizzato come DirectShow quando il dispositivo è collegato. Viene enumerata in due categorie di filtro:

-   CLSID \_ VideoInputDeviceCategory ("Origini di acquisizione video")
-   AM \_ KSCATEGORY \_ RENDER ("WDM Streaming Rendering Devices")

Il nome descrittivo del filtro è `Microsoft DV Camera and VCR` o un equivalente localizzato. In alcuni dispositivi la **proprietà Description** contiene una descrizione del modello specifico, che può essere usata al posto del nome descrittivo generico. Per altre informazioni, vedere [Selezione di un dispositivo di acquisizione.](selecting-a-capture-device.md)

MSDV ha due pin di output. Un pin fornisce fotogrammi DV contenenti dati audio e video interleaved. L'altro segnaposto fornisce fotogrammi solo video senza audio. MSDV non può trasmettere da entrambi i pin contemporaneamente, quindi è possibile collegare un solo pin di output alla volta. Per altre informazioni sull'acquisizione di video da un dispositivo DV, vedere [Capture DV to File](capture-dv-to-file.md).

![acquisizione di dati dv dal dispositivo](images/dv-filters4.png)

La maggior parte dei videocamere DV dispone di una sottounità VTR (Video Tape Recorder), in grado di trasmettere dati dal nastro al computer. Per l'applicazione, l'acquisizione da nastro funziona come l'acquisizione di video live. L'unica differenza è che l'applicazione deve controllare il trasporto del nastro esterno, ovvero avviare e arrestare il nastro, riavvolgere e così via. A questo scopo, MSDV espone [**le interfacce IAMExtDevice,**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice) [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)e [**IAMTimecodeReader.**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) Per altre informazioni sul controllo di una VTR, vedere [Controllo di un videocamere DV.](controlling-a-dv-camcorder.md)

È anche possibile trasmettere DV dal computer al camcorder. Il video può quindi essere visualizzato nello schermo di onboarded del videocamere o registrato su nastro. Per supportare questa funzionalità, MSDV dispone di un pin di input in grado di ricevere un flusso DV interleaved. Quando il pin di input è connesso, MSDV funge da filtro renderer anziché da filtro di acquisizione. MSDV non supporta la ricerca in questa modalità. Per altre informazioni sull'invio di DV al dispositivo, vedere [Trasmettere DV da file a nastro.](transmit-dv-from-file-to-tape.md)

![trasmissione di dati dv al dispositivo](images/dv-filters5.png)

Si noti che i pin di input e output non possono essere connessi contemporaneamente, perché il dispositivo non può trasmettere in entrambe le direzioni contemporaneamente.

In molti videocamere, il passaggio tra la modalità VTR e la modalità fotocamera causa lo switch del dispositivo. Di conseguenza, DirectShow potrebbe perdere il dispositivo quando l'utente passa da una modalità all'altra. Per informazioni sugli eventi di rimozione dei dispositivi, vedere [Notifica di rimozione del dispositivo.](device-removal-notification.md)

## <a name="remarks"></a>Commenti

Per informazioni sui formati DV supportati dal driver MSDV, vedere [**Sottotipi video DV.**](dv-video-subtypes.md)

Alcuni suggerimenti sulla creazione di grafi di filtro con MSDV:

-   Non è possibile usare [**IGraphBuilder::Render per**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) eseguire il rendering di un pin di output in MSDV. Il filtro Graph Manager tenta di connettere il pin di output al pin di input di MSDV, che ha esito negativo. Usare invece [**IGraphBuilder::Connessione**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) o [**ICaptureGraphBuilder2::RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
-   Quando un grafico filtro contiene MSDV, MSDV deve fornire l'orologio di riferimento per il grafico. A livello di DirectX 8.0, Filter Graph Manager sceglierà automaticamente MSDV come orologio di riferimento. Con le versioni precedenti, è necessario chiamare il [**metodo IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) in Filter Graph Manager. Per altre informazioni sugli orologi, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).
-   A seconda del dispositivo, alcuni metodi in **IAMExtDevice,** **IAMExtTransport** e **IAMTimeCodeReader** potrebbero restituire Windows di errore anziché valori **HRESULT.** I codici di errore possibili includono i seguenti.

    | Codice di errore              | Descrizione                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | TIMEOUT \_ ERRORE          | Timeout di un comando del dispositivo esterno.                                                        |
    | ERRORE \_ REQ \_ NOT \_ ACCEP  | Il dispositivo non ha accettato questo comando del dispositivo esterno.                                          |
    | ERRORE \_ NON \_ SUPPORTATO   | Il dispositivo non supporta questo comando del dispositivo esterno.                                        |
    | RICHIESTA \_ DI \_ ERRORE INTERROTTA | Un comando del dispositivo esterno è stato interrotto. È possibile che il dispositivo sia stato rimosso o che si sia verificata una reimpostazione del bus. |

    

     

### <a name="device-information"></a>Informazioni sul dispositivo

In Windows Millennium Edition e Windows XP, il moniker del dispositivo del filtro DV supporta una proprietà **Description** oltre alla **proprietà FriendlyName.** Questa proprietà restituisce una descrizione del dispositivo, tratta dal file INF, che in genere contiene il nome del marchio del dispositivo. Questa proprietà non è tuttavia supportata per tutti i modelli di dispositivo.

Per altre informazioni sui moniker dei dispositivi, vedere [Using the System Device Enumerator](using-the-system-device-enumerator.md).

### <a name="clock-times"></a>Orario di clock

Il driver MSDV usa l'orologio del bus 1394 contenuto nei pacchetti di dati 1394 per derivare l'orologio. Usa questi valori per impostare il timestamp degli esempi di supporti DV. Poiché questo clock di origine non è l'orologio del sistema del computer, gli orari alla fine si distondono dall'orologio del computer. Come indicato in precedenza, tuttavia, per impostazione predefinita Filter Graph Manager selezionerà MSDV come orologio di riferimento del grafo.

[**L'interfaccia IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) segnala la misura corrente del driver dei frame rilasciati. Questo valore potrebbe non essere perfettamente sincronizzato con il numero effettivo di frame eliminati in un determinato momento. Se i frame vengono eliminati, significa che il sistema non è bilanciato (la produzione dei dati supera il consumo di dati). Ad esempio, il disco rigido dell'utente potrebbe non essere sufficientemente veloce da supportare le frequenze di acquisizione DV.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



