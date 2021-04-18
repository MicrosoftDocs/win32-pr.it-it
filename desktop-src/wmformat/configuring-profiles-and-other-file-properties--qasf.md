---
title: Configurazione di profili e altre proprietà di file (QASF)
description: Configurazione di profili e altre proprietà di file (QASF)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows Media Format SDK, configurazione di profili (QASF)
- Windows Media Format SDK, configurazione delle proprietà dei file (QASF)
- Windows Media Format SDK, metadati (QASF)
- ASF (Advanced Systems Format), configurazione dei profili (QASF)
- ASF (formato avanzato dei sistemi), configurazione di profili (QASF)
- ASF (Advanced Systems Format), configurazione delle proprietà dei file (QASF)
- ASF (formato avanzato dei sistemi), configurazione delle proprietà dei file (QASF)
- ASF (Advanced Systems Format), metadati (QASF)
- ASF (formato avanzato dei sistemi), metadati (QASF)
- Windows Media Format SDK, QASF
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- metadati, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473739"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a>Configurazione di profili e altre proprietà di file (QASF)

Gli elementi seguenti descrivono come eseguire diverse attività correlate alla creazione di file ASF.

## <a name="creating-a-profile-qasf"></a>Creazione di un profilo (QASF)

Per creare un profilo personalizzato, usare direttamente Windows Media Format SDK per creare un oggetto di gestione profili tramite la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) . Successivamente, creare il profilo e passarlo al [writer ASF WM](wm-asf-writer-filter.md) usando il metodo [**IConfigASFWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) . Questo è l'unico modo per configurare il filtro con un profilo che usa i codec della serie Windows Media Audio e video 9. È possibile aggiungere i profili di sistema per le versioni precedenti di questi codec usando il metodo [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) .

## <a name="adding-metadata-qasf"></a>Aggiunta di metadati (QASF)

Per aggiungere metadati a un file, chiamare **QueryInterface** dall'interfaccia **IBASEFILTER** sul [writer ASF WM](wm-asf-writer-filter.md) per recuperare l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) . Quando al filtro viene assegnato un profilo, utilizzare i metodi dell'interfaccia **IWMHeaderInfo** per scrivere i metadati.

## <a name="indexing-a-file-qasf"></a>Indicizzazione di un file (QASF)

Per impostazione predefinita, il writer ASF WM crea file indicizzati temporaneamente. Per creare un file indicizzato con frame, usare il metodo [**IConfigAsfWriter:: SetIndexMode**](iconfigasfwriter-setindexmode.md) per disabilitare tutte le indicizzazione, quindi creare il file. Al termine, usare direttamente Windows Media Format SDK per creare un indice basato su frame per il file.

## <a name="performing-two-pass-encoding-qasf"></a>Esecuzione della codifica Two-Pass (QASF)

La codifica a due passaggi è supportata solo nei codec Windows Media versione 8 e successive. Inserire il writer ASF WM in modalità di pre-elaborazione chiamando [**IConfigAsfWriter2:: separat**](iconfigasfwriter2-setparam.md) e specificando am \_ CONFIGASFWRITER \_ param \_ MultiPASS nel parametro *dwParam* e **true** nel parametro *dwParam1* .

Eseguire quindi il grafico del filtro. Al termine di tutti i passaggi di pre-elaborazione (in genere verrà eseguito solo un passaggio di pre-elaborazione), l'applicazione riceverà un evento di **\_ \_ completamento della pre-elaborazione EC** dal filtro. Quando viene ricevuto questo evento, usare **IMediaSeeking:: Sepositions** per reimpostare il puntatore del flusso all'inizio ed eseguire di nuovo il grafico dei filtri. Dopo l'ultimo passaggio, in genere il secondo passaggio, l'applicazione riceverà un evento **EC \_ complete** per indicare che il processo di codifica è completo. Se un passaggio di pre-elaborazione viene annullato prima della ricezione dell'evento di **\_ \_ completamento della pre-elaborazione EC** , chiamare [**IConfigAsfWriter2:: ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) per reimpostare il filtro prima di tentare un'altra esecuzione di pre-elaborazione.

È necessario chiamare **IConfigAsfWriter:: separat**(AM \_ CONFIGASFWRITER \_ param \_ MultiPASS, **false**) se si desidera che il filtro venga escluso completamente dalla modalità di pre-elaborazione.

> [!IMPORTANT]
> È responsabilità dell'applicazione abilitare la modalità di pre-elaborazione in base al profilo che verrà usato per la codifica. Alcuni profili richiedono la codifica a due passaggi. Se si tenta di codificare un file con un profilo di questo tipo e non si imposta AM \_ CONFIGASFWRITER \_ param \_ MultiPASS su **true**, \_ verrà generato un errore EC USERABORT. Per ulteriori informazioni su come determinare se un determinato profilo richiede una codifica a due passaggi, vedere [utilizzo Two-Pass codifica](using-two-pass-encoding.md) o [scrittura di flussi di velocità in bit variabili](writing-variable-bit-rate-streams.md).

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a>Recupero e impostazione delle proprietà del buffer in fase di esecuzione (QASF)

In alcuni scenari, ad esempio se si vuole forzare l'inserimento di fotogrammi chiave durante la scrittura di un file, è possibile che un'applicazione debba ottenere o impostare informazioni su un buffer di Windows Media in fase di esecuzione. I filtri [WM ASF Reader](wm-asf-reader-filter.md) e [WM ASF Writer](wm-asf-writer-filter.md) supportano entrambi un meccanismo di callback che consente a un'applicazione di accedere all'interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) su ogni singolo buffer multimediale durante la lettura o la scrittura di file. Le applicazioni possono usare questa interfaccia per designare esempi specifici come fotogrammi chiave, o [*cleanpoints*](wmformat-glossary.md), per impostare codici temporali SMPTE, per specificare le impostazioni interlacciate o per aggiungere qualsiasi tipo di dati privati a un flusso.

Usare l'interfaccia [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) per registrare i callback dal pin che sta gestendo il flusso video. Quando il pin chiama il metodo [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) , esaminare gli indicatori temporali sul buffer e, se necessario, chiamare [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) per impostare la proprietà **\_ SampleExtensionGUID \_ OutputCleanPoint di WM** sul buffer su **true**.

## <a name="non-square-pixel-support-qasf"></a>Supporto di pixel non quadrati (QASF)

Il writer ASF WM si connette a un filtro upstream, ad esempio il decodificatore DV, che restituisce informazioni sulle proporzioni in pixel. Il writer ASF WM scriverà queste informazioni come estensioni dell'unità dati per ogni esempio nel file.

Quando il lettore ASF WM rileva le informazioni sulle proporzioni in pixel nell'intestazione del file o nelle estensioni dell'unità dati per gli esempi, offre un tipo di supporto **VIDEOINFOHEADER2** come prima scelta nel pin di output. I membri **dwPictAspectRatioX** e **dwPictAspectRatioY** della struttura, che descrivono le proporzioni del rettangolo video, verranno adattati correttamente per tenere conto delle proporzioni in pixel.

## <a name="maintaining-interlaced-format"></a>Gestione del formato interlacciato

Se si acquisisce video interlacciato da un televisore o una fotocamera DV, potrebbe essere necessario mantenere il video originale come campi indipendenti se si prevede che il file codificato venga riprodotto in un televisore o in un altro dispositivo di visualizzazione interlacciato. (I monitoraggi computer sono dispositivi di analisi progressiva). Se si esegue la disinterlacciamento di un video e quindi lo si riinterlaccia per la riproduzione in un televisore, si verifica una perdita di dati. In un file ASF, le informazioni di interlacciamento vengono archiviate come estensioni di unità dati che l'applicazione applica a ogni esempio utilizzando il metodo **IAMWMBufferPassCallback** descritto in precedenza. Per codificare un file che conserva le impostazioni di interlacciamento originali, attenersi alla procedura seguente:

-   Implementare una classe che supporta **IAMWMBufferPassCallback** e scrivere una funzione Notify che imposta i flag di interlacciamento per ogni campione. Questa funzione verrà chiamata dal writer ASF WM prima di elaborare ogni campione.


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   Impostare le estensioni dell'unità dati nel profilo prima di passare il profilo al filtro.


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   Dopo aver configurato il filtro con il profilo, ottenere l'interfaccia **IWMWriterAdvanced2** dal writer ASF WM e chiamare il metodo **SetInputSettings** .

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 