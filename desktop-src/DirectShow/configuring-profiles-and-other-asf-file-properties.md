---
description: Configurazione di profili e altre proprietà dei file ASF
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Configurazione di profili e altre proprietà dei file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401263"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a>Configurazione di profili e altre proprietà dei file ASF

Gli elementi seguenti descrivono come eseguire diverse attività correlate alla creazione di file ASF. Alcune delle interfacce indicate in questo argomento sono documentate nella documentazione di Windows Media Format SDK.

Creazione di un profilo

I profili ASF sono descritti in dettaglio in Windows Media Format SDK; in sostanza, descrivono gli attributi di un file di formato Windows Media, ad esempio velocità in bit, numero e tipo di flussi e qualità di compressione. Il filtro usa il profilo per determinare il tipo di file di formato Windows Media da scrivere, il numero di pin di input che deve configurare e i tipi di supporti che possono accettare.

Per creare un profilo personalizzato, usare direttamente Windows Media Format SDK per creare un oggetto di gestione profili tramite la funzione **WMCreateProfileManager** . Successivamente, creare il profilo e passarlo al [writer ASF WM](wm-asf-writer-filter.md) usando il metodo [**IConfigASFWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) . Questo è l'unico modo per configurare il filtro con un profilo che usa i codec della serie Windows Media Audio e video 9. È possibile aggiungere i profili di sistema per le versioni precedenti di questi codec usando il metodo [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) .

È possibile reimpostare il profilo mentre i pin di input del filtro sono connessi, purché il nuovo profilo non richieda pin di input aggiuntivi. Se ad esempio si modifica il profilo da un profilo audio di input singolo a un profilo audio e video di due input, solo il pin audio verrà riconnesso e non verrà creato alcun nuovo PIN per il flusso video.

Aggiunta di metadati

Per aggiungere metadati a un file, eseguire una query sul filtro [WM ASF Writer](wm-asf-writer-filter.md) per l'interfaccia **IWMHeaderInfo** . Quando al filtro viene assegnato un profilo, utilizzare i metodi dell'interfaccia **IWMHeaderInfo** per scrivere i metadati.

Indicizzazione di un file

Per impostazione predefinita, il writer ASF WM crea file indicizzati temporaneamente. Per creare un file indicizzato con frame, usare il metodo [**IConfigAsfWriter:: SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) per disabilitare tutte le indicizzazione, quindi creare il file. Al termine, usare direttamente Windows Media Format SDK per creare un indice basato su frame per il file.

Codifica Two-Pass

La codifica a due passaggi è supportata solo nei codec Windows Media versione 8 e successive. Inserire il writer ASF WM in modalità di pre-elaborazione chiamando [**IConfigAsfWriter2:: separat**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) e specificando am \_ CONFIGASFWRITER \_ param \_ MultiPASS nel parametro *dwParam* e **true** nel parametro *dwParam1* .

Eseguire quindi il grafico del filtro. Al termine di tutti i passaggi di pre-elaborazione (in genere verrà eseguito solo un passaggio di pre-elaborazione), l'applicazione riceverà un evento di [**\_ \_ completamento della pre-elaborazione EC**](ec-preprocess-complete.md) dal filtro. Quando viene ricevuto questo evento, usare [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) per reimpostare il puntatore del flusso all'inizio ed eseguire di nuovo il grafico dei filtri. Dopo l'ultimo passaggio, in genere il secondo passaggio, l'applicazione riceverà un evento [**EC \_ complete**](ec-complete.md) per indicare che il processo di codifica è completo. Se un passaggio di pre-elaborazione viene annullato prima della ricezione dell'evento di **\_ \_ completamento della pre-elaborazione EC** , chiamare [**IConfigAsfWriter2:: ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) per reimpostare il filtro prima di tentare un'altra esecuzione di pre-elaborazione.

È necessario impostare il \_ \_ parametro CONFIGASFWRITER param \_ MultiPASS su **false** se si desidera che il filtro venga escluso completamente dalla modalità di pre-elaborazione.

> [!IMPORTANT]
> È responsabilità dell'applicazione abilitare la modalità di pre-elaborazione in base al profilo che verrà usato per la codifica. Alcuni profili richiedono la codifica a due passaggi. Se si tenta di codificare un file con un profilo di questo tipo e non si imposta AM \_ CONFIGASFWRITER \_ param \_ MultiPASS su **true**, verrà generato un errore [**EC \_ USERABORT**](ec-userabort.md) . Per ulteriori informazioni, vedere la documentazione di Windows Media Format SDK.

 

Recupero e impostazione delle proprietà del buffer in fase di esecuzione

In alcuni scenari, ad esempio se si vuole forzare l'inserimento di fotogrammi chiave durante la scrittura di un file, è possibile che un'applicazione debba ottenere o impostare informazioni su un buffer di Windows Media in fase di esecuzione. I filtri [WM ASF Reader](wm-asf-reader-filter.md) e [WM ASF Writer](wm-asf-writer-filter.md) supportano entrambi un meccanismo di callback che consente a un'applicazione di accedere all'interfaccia **INSSBuffer3** su ogni singolo buffer multimediale durante la lettura o la scrittura di file. Le applicazioni possono usare questa interfaccia per designare esempi specifici come fotogrammi chiave, impostare codici temporali SMPTE, specificare le impostazioni interlacciate o aggiungere qualsiasi tipo di dati privati a un flusso.

Usare l'interfaccia [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) per registrare i callback dal pin che sta gestendo il flusso video. Il pin chiamerà il metodo [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) per ogni buffer.

Pixel non quadrati

Il writer ASF WM si connette a un filtro upstream, ad esempio il decodificatore DV, che restituisce informazioni sulle proporzioni in pixel. Il writer ASF WM scriverà queste informazioni come estensioni dell'unità dati per ogni esempio nel file.

Quando il lettore ASF WM rileva le informazioni sulle proporzioni in pixel nell'intestazione del file o nelle estensioni dell'unità dati per gli esempi, offre un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) come prima scelta nel pin di output. I membri **dwPictAspectRatioX** e **dwPictAspectRatioY** della struttura, che descrivono le proporzioni del rettangolo video, verranno adattati correttamente per tenere conto delle proporzioni in pixel.

Gestione del formato interlacciato

Se si acquisisce video interlacciato da un televisore o una fotocamera DV, potrebbe essere necessario mantenere il video originale come campi indipendenti se si prevede che il file codificato venga riprodotto in un televisore o in un altro dispositivo di visualizzazione interlacciato. (I monitoraggi computer sono dispositivi di analisi progressiva). Se si esegue la disinterlacciamento di un video e quindi lo si riinterlaccia per la riproduzione in un televisore, si verifica una perdita di dati. In un file ASF, le informazioni di interlacciamento vengono archiviate come estensioni di unità dati che l'applicazione applica a ogni esempio utilizzando il metodo [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) descritto in precedenza. Per codificare un file che conserva le impostazioni di interlacciamento originali, attenersi alla procedura seguente:

1.  Implementare una classe che supporta **IAMWMBufferPassCallback** e scrivere una funzione Notify che imposta i flag di interlacciamento per ogni campione. Questa funzione verrà chiamata dal writer ASF WM prima di elaborare ogni campione.
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  Impostare le estensioni dell'unità dati nel profilo prima di passare il profilo al filtro.
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  Dopo aver configurato il filtro con il profilo, ottenere l'interfaccia **IWMWriterAdvanced2** dal writer ASF WM e chiamare il metodo **SetInputSettings** .

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



