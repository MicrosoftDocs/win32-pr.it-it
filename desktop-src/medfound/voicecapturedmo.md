---
description: Oggetto che incapsula diversi DSP correlati all'acquisizione vocale.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: Voice Capture DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d05eb6d3f97f748d5c82d8fa566ee25a3a01ce225ab76e84d73f0a86b132afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972550"
---
# <a name="voice-capture-dsp"></a>Voice Capture DSP

Oggetto che incapsula diversi DSP correlati all'acquisizione vocale.

## <a name="clsid"></a>CLSID

CLSID \_ CWMAudioAEC

## <a name="interfaces"></a>Interfacce

-   [**Oggetto IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **Ipropertystore**

## <a name="properties"></a>Proprietà



| Proprietà                                                                                     | Descrizione                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [INDICI DEI DISPOSITIVI MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-device-indexesproperty.md)              | Specifica quali dispositivi audio vengono DMO per l'acquisizione e il rendering dell'audio.                     |
| [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Identifica la combinazione di dispositivi audio attualmente in uso nell'applicazione.              |
| [MFPKEY \_ WMAAECMA \_ DMO \_ SOURCE \_ MODE](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | Specifica se l'DMO utilizza la modalità di origine o la modalità filtro.                                        |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | Specifica quante volte il DMO esegue l'eliminazione dell'eco acustica (AES) sul segnale residuo. |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)                        | Specifica se l'DMO esegue il controllo automatico del guadagno.                                        |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ CENTER \_ CLIP](mfpkey-wmaaecma-featr-center-clipproperty.md)       | Specifica se l'DMO esegue il ritaglio al centro.                                               |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Specifica la durata dell'eco che l'algoritmo di annullamento dell'eco acustica (AEC) può gestire.    |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ FRAME \_ SIZE](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Specifica le dimensioni del fotogramma audio.                                                                   |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ TRASFPKEY](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | Specifica quale trazione viene DMO per l'elaborazione della matrice del microfono.                                |
| [MODALITÀ MFPKEY \_ WMAAECMA \_ FEATR \_ \_ MICARR](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | Specifica il modo in cui il DMO l'elaborazione della matrice del microfono.                                       |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | Specifica se l'DMO esegue la pre-elaborazione dell'array di microfoni.                                |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ NOISE \_ FILL](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | Specifica se l'DMO esegue il riempimento del rumore.                                                 |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)                          | Specifica se l'DMO esegue l'eliminazione del rumore.                                             |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)                        | Specifica il tipo di rilevamento dell'attività vocale eseguita DMO chiamata.                             |
| [MODALITÀ DI FUNZIONALITÀ MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-feature-modeproperty.md)                  | Consente all'applicazione di eseguire l'override delle impostazioni predefinite in varie proprietà.                   |
| [MFPKEY \_ WMAAECMA \_ MIC \_ GAIN \_ BOUNDER](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | Specifica se l'DMO applica il delimitazione del guadagno del microfono.                                       |
| [MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Specifica la geometria della matrice del microfono.                                                          |
| [MFPKEY \_ WMAAECMA \_ QUALITY \_ METRICS](mfpkey-wmaaecma-quality-metricsproperty.md)            | Recupera le metriche di qualità per AEC.                                                                |
| [MFPKEY \_ WMAAECMA \_ RETRIEVE \_ TS \_ STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | Specifica se il DMO le statistiche timestamp nel Registro di sistema.                           |
| [MODALITÀ DI SISTEMA MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-system-modeproperty.md)                    | Imposta la modalità di elaborazione.                                                                         |



 

## <a name="remarks"></a>Commenti

A differenza degli altri DSP, l'oggetto acquisizione voce incapsula più DSP in un singolo oggetto e l'oggetto è solo un oggetto DMO (non implementa [**IMFTransform).**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) L'acquisizione DMO include i componenti DSP seguenti:

-   Annullamento dell'eco acustica (AEC)
-   Elaborazione di matrici di microfoni
-   Eliminazione del rumore
-   Controllo automatico del guadagno
-   Rilevamento delle attività vocali

Le applicazioni possono attivare e disattivare ogni componente singolarmente.

L'acquisizione DMO supporta due modalità di funzionamento, la *modalità filtro* e la *modalità di* origine. In modalità filtro, l'applicazione invia campioni audio dal microfono e dalla linea dell'altoparlante al DMO e il DMO produce output.

In modalità di origine, l'applicazione non deve recapitare esempi al DMO. Al contrario, il DMO gestisce tutte le operazioni sui dispositivi audio, tra cui l'inizializzazione dei dispositivi, l'acquisizione e la sincronizzazione dei flussi audio, il calcolo dei timestamp e il recupero della geometria della matrice del microfono. Usando la modalità di origine, l'applicazione configura semplicemente il DMO e l'output del DMO è un segnale del microfono pulito ed elaborato. La modalità di origine è notevolmente più semplice da usare rispetto alla modalità filtro ed è consigliata per la maggior parte delle applicazioni.

Attualmente l'acquisizione DMO supporta solo l'annullamento dell'eco acustico a canale singolo, quindi l'output della linea del parlante deve essere a canale singolo. Se l'elaborazione della matrice del microfono è disabilitata, l'input multicanale viene ridimensionato a un canale per l'elaborazione AEC. Se sono abilitate sia l'elaborazione dell'array di microfoni che l'elaborazione AEC, il controllo di accesso viene eseguito su ogni elemento del microfono prima dell'elaborazione della matrice del microfono.

### <a name="microphone-array-processing"></a>Elaborazione di matrici di microfoni

Un array di microfoni è un set di microfoni molto posizionati. Gli array di microfoni hanno una direzionalità migliore rispetto a un singolo microfono, perché le onde acustiche arrivano a ogni microfono in un momento leggermente diverso. Per altre informazioni sulle matrici di microfoni, vedere gli articoli Web Supporto dell'array microfono [in Windows Vista](/windows-hardware/design/component-guidelines/audio) e How to Build and Use Microphone [Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

### <a name="using-the-voice-capture-dsp"></a>Uso di Voice Capture DSP

Per usare il DSP di acquisizione vocale, seguire questa procedura.

### <a name="1-initialize-the-dmo"></a>1. Inizializzare il DMO

Creare l'acquisizione DMO chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con il **CLSID CLSID \_ CWMAudioAEC.** Il DSDP di acquisizione vocale espone solo le interfacce [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) e [**IPropertyStore,**](/windows/win32/api/propsys/nn-propsys-ipropertystore) quindi può essere usato solo come DMO.

L DMO predefinita è la modalità di origine. Per selezionare la modalità filtro, impostare la proprietà [MFPKEY \_ WMAAECMA \_ DMO SOURCE \_ \_ MODE](mfpkey-wmaaecma-dmo-source-modeproperty.md) su **VARIANT \_ FALSE.**

Configurare quindi le proprietà interne del DMO usando [**l'interfaccia IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) L'unica proprietà che un'applicazione deve impostare è [la proprietà MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE.](mfpkey-wmaaecma-system-modeproperty.md) Questa proprietà configura la pipeline di elaborazione all'interno del DMO. Le altre proprietà sono facoltative.

### <a name="2-set-the-input-and-output-formats"></a>2. Impostare i formati di input e output

Se si usa il DMO in modalità filtro, impostare il formato di input chiamando [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype). Il formato di input può essere quasi qualsiasi tipo di audio a virgola mobile PCM o IEEE non compresso valido. Se il formato di input non corrisponde al formato di output, il DMO automaticamente la conversione della frequenza di campionamento.

Se si usa il DMO in modalità di origine, non impostare il formato di input. Il DMO configura automaticamente il formato di input in base ai dispositivi audio.

In entrambe le modalità impostare il formato di output chiamando [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). Il DMO può accettare i formati di output seguenti:

-   Sottotipo: **MEDIASUBTYPE \_ PCM** o **MEDIASUBTYPE \_ IEEE \_ FLOAT**
-   Blocco di formato: [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))
-   Esempi al secondo: 8.000; 11,025; 16,000; o 22.050
-   Canali: 1 per la modalità solo AEC, 2 o 4 per l'elaborazione dell'array di microfoni
-   Bit per campione: 16

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



### <a name="3-process-data"></a>3. Elaborare i dati

Prima di elaborare i dati, è consigliabile chiamare [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources). Questo metodo alloca le risorse usate internamente dal DMO. Chiamare **AllocateStreamingResources dopo** i passaggi elencati in precedenza, non prima. Se non si chiama questo metodo, il DMO alloca automaticamente le risorse all'avvio dell'elaborazione dati.

Se si usa il DMO in modalità filtro, è necessario passare i dati di input al DMO chiamando [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput). I dati audio dal microfono passano al flusso 0 e i dati audio dalla linea del parlante passano al flusso 1. Se si usa il DMO in modalità di origine, non è necessario chiamare **ProcessInput**.

Per ottenere i dati di output dal provider di servizi condivisi, seguire questa procedura:

1.  Creare un oggetto buffer per contenere i dati di output. L'oggetto buffer deve implementare [**l'interfaccia IMediaBuffer.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) Le dimensioni del buffer dipendono dai requisiti dell'applicazione. L'allocazione di un buffer più grande può ridurre le probabilità che si verifichino errori.
2.  Dichiarare una [**DMO \_ OUTPUT DATA \_ \_ BUFFER**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) e impostare il **membro pBuffer** in modo che punti all'oggetto buffer.
3.  Passare la [**DMO \_ OUTPUT DATA \_ \_ BUFFER**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) al metodo [**IMediaObject::P rocessOutput.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)
4.  Continuare a chiamare questo metodo per tutto il tempo in cui DMO dati di output. Il DSP segnala che ha più output impostando il flag **DMO \_ OUTPUT DATA \_ \_ BUFFERF \_ INCOMPLETE** nel membro **dwStatus** della struttura [**output DATA \_ \_ \_ BUFFER DMO.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnali digitali](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
