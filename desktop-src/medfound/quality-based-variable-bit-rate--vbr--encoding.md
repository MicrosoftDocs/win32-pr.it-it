---
description: Codifica della velocità in bit della variabile Quality-Based
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Codifica della velocità in bit della variabile Quality-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309024"
---
# <a name="quality-based-variable-bit-rate-encoding"></a>Codifica della velocità in bit della variabile Quality-Based

Diversamente dalla [codifica della velocità in bit costante](constant-bit-rate-encoding.md) (CBR), in cui il codificatore tenta di mantenere una particolare velocità in bit del supporto codificato, nella modalità velocità in bit variabile (VBR), il codificatore tenta di ottenere la migliore qualità possibile del supporto codificato. La differenza principale tra CBR e VBR è la dimensione della finestra del buffer utilizzata. I flussi con codifica VBR hanno in genere finestre di buffer di grandi dimensioni rispetto a flussi con codifica CBR.

La qualità del contenuto codificato è determinata dalla quantità di dati persi quando il contenuto è compresso. Molti fattori influiscono sulla perdita di dati nel processo di compressione. Tuttavia, in generale, più complessi sono i dati originali e maggiore è il rapporto di compressione, più dettagli vengono persi nel processo di compressione.

In modalità VBR basata sulla qualità non si definisce una velocità in bit o una finestra del buffer che il codificatore deve seguire. Si specifica invece un livello di qualità per un flusso multimediale digitale anziché una velocità in bit. Il codificatore comprime il contenuto in modo che tutti gli esempi siano di qualità paragonabile; Ciò garantisce che la qualità sia coerente durante la durata della riproduzione, indipendentemente dai requisiti del buffer del flusso risultante.

La codifica VBR basata sulla qualità tende a creare flussi compressi di grandi dimensioni. In generale, questo tipo di codifica è particolarmente adatto per la riproduzione locale o per le connessioni di rete a larghezza di banda elevata (o per il download e la riproduzione). È ad esempio possibile scrivere un'applicazione per copiare canzoni da CD a file ASF in un computer. L'uso della codifica VBR basata sulla qualità garantisce che tutti i brani copiati abbiano la stessa qualità. In questi casi, la qualità coerente offrirà un'esperienza utente migliore.

Lo svantaggio della codifica VBR basata sulla qualità è che non esiste alcun modo per comprendere i requisiti di larghezza di banda o di larghezza di banda del supporto codificato prima della sessione di codifica, perché il codificatore usa un singolo passaggio di codifica. In questo modo, i file con codifica VBR basati sulla qualità non sono appropriati per le situazioni in cui la memoria o la larghezza di banda sono limitate, ad esempio la riproduzione di contenuti su lettori multimediali portatili o lo streaming su una rete a larghezza di banda ridotta.

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a>Configurazione del codificatore per la codifica Quality-Based VBR

La configurazione del codificatore viene impostata tramite i valori delle proprietà. Queste proprietà sono definite in wmcodecdsp. h. Prima di negoziare il tipo di supporto di output, è necessario impostare le proprietà di configurazione nel codificatore. Per informazioni su come impostare le proprietà nel codificatore, vedere [configurazione del codificatore](configuring-the-encoder.md).

Nell'elenco seguente vengono illustrate le proprietà che è necessario impostare per questo tipo di codifica:

-   Specificare la modalità di codifica VBR impostando la proprietà **MFPKEY \_ VBRENABLED** su Variant \_ true.
-   Impostare **MFPKEY \_ PASSESUSED** su 1 perché questa modalità VBR usa un passaggio di codifica.
-   Impostare il livello di qualità desiderato, da 0 a 100, impostando la proprietà **MFPKEY \_ desired \_ VBRQUALITY** . Il VBR basato sulla qualità non codifica il contenuto per i parametri del buffer predefiniti. Questo livello di qualità che verrà mantenuto per l'intero flusso, indipendentemente dai requisiti di velocità in bit che risultano.
-   Per i flussi video, impostare la velocità in bit media su un valore diverso da zero nell'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) nel tipo di supporto di output del codificatore. La velocità in bit accurata viene aggiornata dopo il completamento della sessione di codifica.

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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di codifica ASF](asf-encoding-types.md)
</dt> </dl>

 

 



