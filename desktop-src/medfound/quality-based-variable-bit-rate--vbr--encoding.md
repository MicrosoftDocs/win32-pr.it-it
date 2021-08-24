---
description: Quality-Based di velocità in bit variabile
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Quality-Based di velocità in bit variabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19c2cd63d5bc6f777f702827e999cd9d2ae2a272194f4b776205c1581376256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722201"
---
# <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based di velocità in bit variabile

A differenza di [CBR (Constant Bit Rate Encoding),](constant-bit-rate-encoding.md) in cui il codificatore cerca di mantenere una particolare velocità in bit del supporto codificato, nella modalità VBR (Variable Bit Rate), il codificatore cerca di ottenere la migliore qualità possibile del supporto codificato. La differenza principale tra CBR e VBR è la dimensione della finestra del buffer usata. I flussi con codifica VBR hanno in genere finestre buffer di grandi dimensioni rispetto ai flussi con codifica CBR.

La qualità del contenuto codificato è determinata dalla quantità di dati persi quando il contenuto viene compresso. Molti fattori influiscono sulla perdita di dati nel processo di compressione; ma in generale, più complessi sono i dati originali e maggiore è il rapporto di compressione, maggiore sarà il dettaglio nel processo di compressione.

In modalità VBR basata sulla qualità non si definisce una velocità in bit o una finestra del buffer che il codificatore deve seguire. Si specifica invece un livello di qualità per un flusso multimediale digitale anziché una velocità in bit. Il codificatore comprime il contenuto in modo che tutti i campioni siano di qualità comparabile; ciò garantisce che la qualità sia coerente per tutta la durata della riproduzione, indipendentemente dal buffer necessario per il flusso risultante.

La codifica VBR basata sulla qualità tende a creare flussi compressi di grandi dimensioni. In generale, questo tipo di codifica è particolarmente adatto per la riproduzione locale o le connessioni di rete a larghezza di banda elevata (o per il download e la riproduzione). Ad esempio, è possibile scrivere un'applicazione per copiare i brani da CD a file ASF in un computer. L'uso della codifica VBR basata sulla qualità garantisce che tutti i brani copiati siano della stessa qualità. In questi casi, la qualità coerente offrirà un'esperienza utente migliore.

Lo svantaggio della codifica VBR basata sulla qualità è che non è possibile conoscere le dimensioni o i requisiti di larghezza di banda dei supporti codificati prima della sessione di codifica, perché il codificatore usa un singolo passaggio di codifica. Ciò può rendere i file con codifica VBR basati sulla qualità inappropriati in circostanze in cui la memoria o la larghezza di banda sono limitate, ad esempio la riproduzione di contenuto su lettori multimediali portatili o lo streaming su una rete a larghezza di banda ridotta.

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a>Configurazione del codificatore per la Quality-Based VBR

La configurazione del codificatore viene impostata tramite i valori delle proprietà. Queste proprietà sono definite in wmcodecdsp.h. Le proprietà di configurazione devono essere impostate sul codificatore prima di negoziare il tipo di supporto di output. Per informazioni su come impostare le proprietà nel codificatore, vedere [Configurazione del codificatore](configuring-the-encoder.md).

L'elenco seguente mostra le proprietà che è necessario impostare per questo tipo di codifica:

-   Specificare la modalità di codifica VBR impostando la **proprietà MFPKEY \_ VBRENABLED** su VARIANT \_ TRUE.
-   Impostare **MFPKEY \_ PASSESUSED** su 1 perché questa modalità VBR usa un solo passaggio di codifica.
-   Impostare il livello di qualità desiderato (da 0 a 100) impostando la **proprietà MFPKEY \_ DESIRED \_ VBRQUALITY.** VbR basato sulla qualità non codifica il contenuto in parametri di buffer predefiniti. Questo livello di qualità che verrà mantenuto per l'intero flusso, indipendentemente dal numero di bit che ne derivano.
-   Per i flussi video, impostare la velocità in bit media su un valore diverso da zero nell'attributo [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) sul tipo di supporto di output del codificatore. La velocità in bit accurata viene aggiornata al termine della sessione di codifica.

Nell'esempio di codice seguente viene illustrata l'implementazione per SetEncodingProperties. Questa funzione imposta le proprietà di codifica a livello di flusso per CBR e VBR.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di codifica ASF](asf-encoding-types.md)
</dt> </dl>

 

 



