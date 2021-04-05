---
description: Oggetto che incapsula diversi DSP correlati all'acquisizione vocale.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: DSP di acquisizione vocale (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48c3b3194873008f45ef80ef3a21dad416158b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755226"
---
# <a name="voice-capture-dsp"></a>DSP di acquisizione vocale

Oggetto che incapsula diversi DSP correlati all'acquisizione vocale.

## <a name="clsid"></a>CLSID

\_CWMAUDIOAEC CLSID

## <a name="interfaces"></a>Interfacce

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **IPropertyStore**

## <a name="properties"></a>Proprietà



| Proprietà                                                                                     | Descrizione                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [indici del \_ dispositivo WMAAECMA di MFPKEY \_ \_](mfpkey-wmaaecma-device-indexesproperty.md)              | Specifica i dispositivi audio usati da DMO per l'acquisizione e il rendering dell'audio.                     |
| [\_ \_ GUID DEVICEPAIR WMAAECMA \_ MFPKEY](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Identifica la combinazione di dispositivi audio attualmente in uso nell'applicazione.              |
| [\_ \_ \_ modalità origine MFPKEY WMAAECMA \_ DMO](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | Specifica se DMO utilizza la modalità di origine o filtro.                                        |
| [MFPKEY \_ WMAAECMA \_ featr \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | Specifica il numero di volte in cui DMO esegue l'eliminazione dell'eco acustico (AES) sul segnale residuo. |
| [MFPKEY \_ WMAAECMA \_ featr \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)                        | Specifica se DMO esegue il controllo di guadagno automatico.                                        |
| [\_clip MFPKEY WMAAECMA \_ featr \_ Center \_](mfpkey-wmaaecma-featr-center-clipproperty.md)       | Specifica se DMO esegue il ritaglio al centro.                                               |
| [\_lunghezza Echo MFPKEY WMAAECMA \_ featr \_ \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Specifica la durata di ECHO che l'algoritmo AEC (Acoustic Echo Cancel) può gestire.    |
| [\_dimensioni frame MFPKEY WMAAECMA \_ Feater \_ \_](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Specifica la dimensione del frame audio.                                                                   |
| [MFPKEY \_ WMAAECMA \_ Feater \_ MICARR \_ Beam](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | Specifica il fascio utilizzato da DMO per l'elaborazione di matrici di microfoni.                                |
| [\_modalità MFPKEY WMAAECMA \_ featr \_ MICARR \_](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | Specifica il modo in cui DMO esegue l'elaborazione di matrici di microfoni.                                       |
| [MFPKEY \_ WMAAECMA \_ featr \_ MICARR \_ Preproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | Specifica se DMO esegue la pre-elaborazione della matrice di microfoni.                                |
| [\_riempimento rumore MFPKEY WMAAECMA \_ featr \_ \_](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | Specifica se DMO esegue il riempimento del rumore.                                                 |
| [\_NS MFPKEY WMAAECMA \_ featr \_](mfpkey-wmaaecma-featr-nsproperty.md)                          | Specifica se DMO esegue l'eliminazione del rumore.                                             |
| [\_VAD MFPKEY WMAAECMA \_ featr \_](mfpkey-wmaaecma-featr-vadproperty.md)                        | Specifica il tipo di rilevamento di attività vocali eseguito da DMO.                             |
| [\_ \_ modalità funzionalità WMAAECMA \_ MFPKEY](mfpkey-wmaaecma-feature-modeproperty.md)                  | Consente all'applicazione di eseguire l'override delle impostazioni predefinite di diverse proprietà.                   |
| [\_ \_ \_ limite guadagno MFPKEY WMAAECMA \_ MIC](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | Specifica se DMO applica la delimitazione del guadagno del microfono.                                       |
| [MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Specifica la geometria della matrice di microfoni.                                                          |
| [\_metrica della \_ qualità \_ WMAAECMA di MFPKEY](mfpkey-wmaaecma-quality-metricsproperty.md)            | Recupera le metriche di qualità per AEC.                                                                |
| [MFPKEY \_ WMAAECMA \_ recuperare le \_ statistiche di Servizi terminal \_](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | Specifica se DMO archivia le statistiche relative al timestamp nel registro di sistema.                           |
| [\_modalità di \_ sistema \_ WMAAECMA di MFPKEY](mfpkey-wmaaecma-system-modeproperty.md)                    | Imposta la modalità di elaborazione.                                                                         |



 

## <a name="remarks"></a>Commenti

Diversamente dagli altri DSP, l'oggetto di acquisizione vocale incapsula più DSP in un singolo oggetto e l'oggetto è solo un oggetto DMO (non implementa [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)). Il DMO di acquisizione voce include i componenti DSP seguenti:

-   Annullamento Echo acustico (AEC)
-   Elaborazione di matrici di microfoni
-   Eliminazione del rumore
-   Controllo di guadagno automatico
-   Rilevamento di attività vocali

Le applicazioni possono attivare e disattivare ogni componente singolarmente.

Il servizio di acquisizione voce DMO supporta due modalità operative, modalità *filtro* e modalità *origine* . In modalità filtro, l'applicazione invia esempi di audio dal microfono e dalla linea di altoparlanti a DMO e DMO produce l'output.

In modalità origine, l'applicazione non deve recapitare campioni a DMO. Al contrario, DMO gestisce tutte le operazioni sui dispositivi audio, tra cui l'inizializzazione dei dispositivi, l'acquisizione e la sincronizzazione dei flussi audio, il calcolo dei timestamp e il recupero della geometria della matrice microfonica. Utilizzando la modalità origine, l'applicazione configura semplicemente DMO e l'output di DMO è un segnale del microfono pulito ed elaborato. La modalità di origine è molto più semplice da utilizzare rispetto alla modalità filtro ed è consigliata per la maggior parte delle applicazioni.

Attualmente la funzionalità di acquisizione voce DMO supporta solo l'annullamento dell'eco acustico a canale singolo (AEC), quindi l'output della linea del parlante deve essere a canale singolo. Se l'elaborazione della matrice microfonica è disabilitata, l'input multicanale viene ripiegato verso il basso su un canale per l'elaborazione AEC. Se sono abilitate sia l'elaborazione dell'array di microfoni che l'elaborazione AEC, l'AEC viene eseguito su ogni elemento Microphone prima dell'elaborazione della matrice del microfono.

### <a name="microphone-array-processing"></a>Elaborazione di matrici di microfoni

Una matrice di microfoni è un set di microfoni molto posizionati. Gli array di microfoni raggiungono una maggiore direzionalità rispetto a un singolo microfono, perché le onde acustiche arrivano a ogni microfono in un momento leggermente diverso. Per ulteriori informazioni sugli array di microfoni, vedere l'articolo relativo al [supporto di matrici di microfoni in Windows Vista](/windows-hardware/design/component-guidelines/audio) e [come creare e utilizzare matrici di microfoni per Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

### <a name="using-the-voice-capture-dsp"></a>Uso del DSP di acquisizione vocale

Per usare il DSP di acquisizione vocale, seguire questa procedura.

### <a name="1-initialize-the-dmo"></a>1. inizializzare DMO

Creare il DMO di acquisizione vocale chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID CLSID **\_ CWMAudioAEC**. Il DSDP di acquisizione vocale espone solo le interfacce [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) e [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , quindi può essere usato solo come DMO.

Il valore predefinito di DMO è la modalità di origine. Per selezionare la modalità di filtro, impostare la proprietà [MFPKEY \_ WMAAECMA \_ DMO \_ source \_ mode](mfpkey-wmaaecma-dmo-source-modeproperty.md) su **Variant \_ false**.

Configurare quindi le proprietà interne di DMO usando l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . L'unica proprietà che un'applicazione deve impostare è la proprietà della [ \_ modalità di \_ sistema \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md) . Questa proprietà configura la pipeline di elaborazione all'interno di DMO. Le altre proprietà sono facoltative.

### <a name="2-set-the-input-and-output-formats"></a>2. impostare i formati di input e di output

Se si utilizza DMO in modalità filtro, impostare il formato di input chiamando [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype). Il formato di input può essere quasi qualsiasi tipo di audio a virgola mobile o PCM non compresso valido. Se il formato di input non corrisponde al formato di output, DMO esegue automaticamente la conversione della frequenza di campionamento.

Se si utilizza DMO in modalità origine, non impostare il formato di input. DMO configura automaticamente il formato di input in base ai dispositivi audio.

In entrambe le modalità impostare il formato di output chiamando [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). Il DMO può accettare i formati di output seguenti:

-   Sottotipo: **MEDIASUBTYPE \_ PCM** o **MEDIASUBTYPE \_ IEEE \_ float**
-   Blocco di formato: [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))
-   Campioni al secondo: 8.000; 11.025; 16.000; o 22.050
-   Canali: 1 per la modalità solo AEC, 2 o 4 per l'elaborazione di matrici di microfoni
-   BITS per campione: 16

Il codice seguente imposta il tipo di output su audio PCM a canale singolo a 16 bit:


```
DMO_MEDIA_TYPE mt;  // Media type.
mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.lSampleSize = 0;
mt.bFixedSizeSamples = TRUE;
mt.bTemporalCompression = FALSE;
mt.formattype = FORMAT_WaveFormatEx;

// Allocate the format block to hold the WAVEFORMATEX structure.
hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    WAVEFORMATEX *pwav = (WAVEFORMATEX*)mt.pbFormat;
    pwav->wFormatTag = WAVE_FORMAT_PCM;
    pwav->nChannels = 1;
    pwav->nSamplesPerSec = 16000;
    pwav->nAvgBytesPerSec = 32000;
    pwav->nBlockAlign = 2;
    pwav->wBitsPerSample = 16;
    pwav->cbSize = 0;

    // Set the output type.
    if (SUCCEEDED(hr))
    {
        hr = pDMO->SetOutputType(0, &mt, 0); 
    }
    // Free the format block.
    MoFreeMediaType(&mt);
}
```



### <a name="3-process-data"></a>3. elaborare i dati

Prima di elaborare i dati, è consigliabile chiamare [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources). Questo metodo alloca le risorse utilizzate internamente da DMO. Chiamare **AllocateStreamingResources** dopo i passaggi elencati in precedenza, non prima. Se non si chiama questo metodo, DMO alloca automaticamente le risorse all'avvio dell'elaborazione dei dati.

Se si utilizza DMO in modalità filtro, è necessario passare i dati di input a DMO chiamando [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput). I dati audio dal microfono passano al flusso 0 e i dati audio dalla linea di altoparlanti passano al flusso 1. Se si usa DMO in modalità origine, non è necessario chiamare **ProcessInput**.

Per ottenere i dati di output dal DSP, seguire questa procedura:

1.  Creare un oggetto buffer per memorizzare i dati di output. L'oggetto buffer deve implementare l'interfaccia [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . Le dimensioni del buffer dipendono dai requisiti dell'applicazione. L'allocazione di un buffer più grande può ridurre le probabilità che si verifichino problemi.
2.  Dichiarare una struttura del [**\_ \_ \_ buffer dei dati di output DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) e impostare il membro **pbuffer** in modo che punti all'oggetto buffer.
3.  Passare la struttura del [**\_ \_ \_ buffer dei dati di output DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) al metodo [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) .
4.  Continuare a chiamare questo metodo per il periodo di tempo in cui DMO contiene dati di output. Il DSP segnala che è presente un maggior output impostando il flag di **\_ output DMO \_ data \_ BUFFERF \_ incomplete** nel membro **dwStatus** della struttura del [**\_ \_ \_ buffer dei dati di output DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
