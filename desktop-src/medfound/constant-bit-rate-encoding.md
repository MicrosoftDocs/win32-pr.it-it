---
description: Codifica della velocità in bit costante
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Codifica della velocità in bit costante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966404"
---
# <a name="constant-bit-rate-encoding"></a>Codifica della velocità in bit costante

Nella codifica della velocità in bit costante (CBR), il codificatore conosce la velocità in bit degli esempi di supporti di output e la finestra del buffer (parametri bucket persi) prima dell'inizio della sessione di codifica. Il codificatore usa lo stesso numero di bit per codificare ogni secondo di esempio per tutta la durata del file per ottenere la velocità in bit di destinazione per un flusso. Questo limita la variazione delle dimensioni degli esempi di flusso. Inoltre, durante la sessione di codifica la velocità in bit non corrisponde esattamente al valore specificato ma rimane vicina alla velocità in bit di destinazione.

La codifica con velocità in bit costante risulta utile se si vuole conoscere la velocità in bit o la durata approssimativa di un file senza analizzare tutto il file. Ciò è necessario negli scenari di streaming live, in cui il contenuto multimediale deve essere trasmesso in streaming a una velocità in bit prevedibile con un uso uniforme della larghezza di banda.

Lo svantaggio della codifica CBR è che la qualità del contenuto codificato non sarà costante. Poiché alcuni contenuti sono più difficili da comprimere, le parti di un flusso CBR saranno di qualità inferiore rispetto ad altri. Un film tipico, ad esempio, presenta alcune scene piuttosto statiche e alcune scene che sono piene di azioni. Se si codifica un film usando CBR, le scene che sono statiche e pertanto semplici da codificare in modo efficiente saranno di qualità superiore rispetto alle scene di azione, che richiederebbero dimensioni di campionamento più elevate per mantenere la stessa qualità.

In generale, le variazioni nella qualità di un file CBR sono più pronunciate a velocità in bit inferiori. A una velocità in bit superiore, la qualità di un file con codifica CBR sarà comunque diversa, ma i problemi di qualità saranno meno evidenti per l'utente. Quando si usa la codifica CBR, è consigliabile impostare la larghezza di banda massima come consentito dallo scenario di recapito.

-   [Impostazioni di configurazione CBR](#cbr-configuration-settings)
-   [Impostazioni bucket a perdita](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a>Impostazioni di configurazione CBR

È necessario configurare un codificatore specificando il tipo di codifica e le varie impostazioni specifiche del flusso prima della sessione di codifica.

**Per configurare il codificatore per la codifica CBR**

1.  Specificare la modalità di codifica CBR.

    Per impostazione predefinita, il codificatore è configurato per usare la codifica CBR. La configurazione del codificatore viene impostata tramite i valori delle proprietà. Queste proprietà sono definite in wmcodecdsp. h. È possibile specificare in modo esplicito questa modalità impostando la proprietà [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su Variant \_ false. Per informazioni su come impostare le proprietà nei codificatori, vedere [configurazione del codificatore](configuring-the-encoder.md).

2.  Scegliere la velocità in bit per la codifica.

    Per la codifica CBR, è necessario essere a conoscenza della velocità in bit in cui si desidera codificare il flusso prima che inizi la sessione di codifica. È necessario impostare la velocità in bit durante la configurazione del codificatore. A tale scopo, durante l'esecuzione della negoziazione del tipo di supporto, controllare l'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (per i flussi audio) o l'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) (per i flussi video) dei tipi di supporti di output disponibili e scegliere un tipo di supporto di output con la velocità in bit media più vicina alla velocità in bit di destinazione che si desidera ottenere. Per altre informazioni, vedere [negoziazione del tipo di supporto sul codificatore](media-type-negotiation-on-the-encoder.md).

Nell'esempio di codice riportato di seguito viene illustrata l'implementazione di SetEncodingProperties. Questa funzione imposta le proprietà di codifica a livello di flusso per CBR e VBR.


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a>Impostazioni bucket a perdita

Per la codifica CBR, la media e i valori massimi dei bucket a perdita per il flusso sono gli stessi. Per ulteriori informazioni su questi parametri, vedere [il modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md).

Per codificare in modo CBR i flussi audio, è necessario impostare i valori dei bucket persi dopo aver negoziato il tipo di supporto di output nel codificatore. Il codificatore calcola la finestra del buffer internamente in base alla velocità in bit media impostata sul tipo di supporto di output.

Per impostare i valori dei bucket persi, creare una matrice di valori DWORD in grado di impostare i valori seguenti nella proprietà [**\_ \_ \_ LEAKYBUCKET ASFSTREAMSINK con correzione MFPKEY**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) nell'archivio delle proprietà del sink multimediale. Per ulteriori informazioni, vedere [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).

-   Velocità in bit media: ottenere la velocità in bit media dal tipo di supporto di output selezionato durante la negoziazione del tipo di supporto. Usare l'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) .
-   Buffer Window: eseguire una query sul codificatore per l'interfaccia [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) e quindi chiamare [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib).
-   Dimensioni iniziali del buffer: impostare su 0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di codifica ASF](asf-encoding-types.md)
</dt> <dt>

[Esercitazione: codifica Windows Media da 1 passaggio](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Esercitazione: scrittura di un file WMA usando la codifica CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
