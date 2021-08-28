---
title: Negoziazione del formato video nel plug-in DSP video di esempio
description: Negoziazione del formato video nel plug-in DSP video di esempio
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- Windows Media Player plug-in, DSP video
- plug-in, DSP video
- plug-in di elaborazione del segnale digitale, negoziazione del formato video
- plug-in DSP, negoziazione del formato video
- plug-in DSP video, negoziazione del formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90154f3fe7824fb9af563cb662fdcb2847339bc6061d79b3e92cab9c6e36e44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761821"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>Negoziazione del formato video nel plug-in DSP video di esempio

Prima Windows Media Player inserisce un plug-in DSP video nella catena di segnali, il lettore deve determinare se il plug-in è in grado di elaborare il video riprodotto. Il processo tramite il quale il plug-in e il lettore comunicano sui formati video supportati è detto negoziazione del formato.

## <a name="providing-the-supported-input-and-output-types"></a>Specifica dei tipi di input e output supportati

Se il plug-in DSP funge da oggetto multimediale DirectX (DMO), player esegue una query sul plug-in sui formati supportati effettuando una sequenza di chiamate a **IMediaObject::GetInputType** e **IMediaObject::GetOutputType.**

Se il plug-in DSP funge da Media Foundation Transform (MFT), player esegue una query sul plug-in sui formati supportati effettuando una sequenza di chiamate a **IMFTransform::GetInputAvailableType** e **IMFTransform::GetOutputAvailableType.**

Il plug-in video di esempio generato dalla procedura guidata Windows Media Player plug-in archivia l'elenco dei formati video supportati come matrice di GUID. Il codice seguente è dal file CPP principale:


```C++
static const GUID*    k_guidValidSubtypes[] = {
    &MEDIASUBTYPE_NV12,
    &MEDIASUBTYPE_YV12,
    &MEDIASUBTYPE_YUY2,
    &MEDIASUBTYPE_UYVY,
    &MEDIASUBTYPE_RGB32,
    &MEDIASUBTYPE_RGB24,
    &MEDIASUBTYPE RGB555,
    &MEDIASUBTYPE RGB565
};

```



Il lettore può chiamare **IMediaObject::GetInputType** e **IMediaObject::GetOutputType** in qualsiasi ordine, quindi il codice del plug-in deve prevedere questo aspetto. Analogamente, player può chiamare **IMFTransform::GetInputAvailableType** e **IMFTransform::GetOutputAvailableType** in qualsiasi ordine. Le implementazioni di esempio **di GetOutputType** e **GetOutputAvailableType** verificano se il tipo di input è già stato definito. In caso contrario, il plug-in risponde che supporta solo quel tipo. In caso contrario, il plug-in restituisce il tipo che corrisponde all'indice fornito, come illustrato nel codice seguente:


```C++
// If input type has been defined, then use that as output type.
if (GUID_NULL != m_mtInput.majortype)
{
    hr = ::MoCopyMediaType( pmt, &m_mtInput );
}
else // Otherwise use default for this plug-in.
{
    ::ZeroMemory( pmt, sizeof( DMO_MEDIA_TYPE ) );
    pmt->majortype = MEDIATYPE_Video;
    pmt->subtype = *k_guidValidSubtypes[dwTypeIndex];     
}

```



## <a name="setting-the-input-and-output-types"></a>Impostazione dei tipi di input e output

Se il plug-in DSP funge da DMO, Windows Media Player imposta il tipo di supporto chiamando **IMediaObject::SetInputType** e **IMediaObject::SetOutputType**, passando a ogni funzione un puntatore a una struttura **MEDIA \_ \_ TYPE di DMO** che rappresenta il tipo di supporto richiesto.

Se il plug-in DSP funge da MFT, Windows Media Player imposta il tipo di supporto chiamando **IMFTransform::SetInputType** e **IMFTransform::SetOutputType**, passando a ogni funzione un puntatore a un'interfaccia **IMFMediaType** che rappresenta il tipo di supporto richiesto.

Non esiste alcuna garanzia che il lettore chiami i metodi di negoziazione del formato in un ordine particolare, quindi il codice plug-in deve gestire qualsiasi caso. Ad esempio, se il lettore chiama **SetOutputType** prima di **chiamare SetInputType**, è una linea di azione valida per il plug-in rifiutare il tipo di supporto di output proposto. Il codice seguente dell'implementazione di esempio **di IMediaObject::SetOutputType** illustra quanto segue:


```C++
if( GUID_NULL != m_mtInput.majortype )
{
    // Validate that the output media type matches our requirements 
    // and matches our input type (if set).
    hr = ValidateMediaType(pmt, &m_mtInput);
}
else
{
    hr = DMO_E_TYPE_NOT_ACCEPTED;
}

```



Le implementazioni plug-in di esempio **di SetInputType** e **SetOutputType** chiamano la funzione personalizzata **denominata ValidateMediaType.** Questa funzione plug-in esegue una serie di test sul tipo di supporto proposto progettato per garantire che il tipo di supporto sia ben formato e supportato dal plug-in. **ValidateMediaType** esegue i test seguenti:

-   Verifica che i membri **majortype** **e formattype** contengano i valori corretti.
-   Verifica che il membro **del sottotipo** corrisponda a uno dei formati supportati.
-   Verifica che le informazioni nelle strutture **BITMAPINFOHEADER** e **VIDEOINFOHEADER** o **VIDEOINFOHEADER2** contengano valori validi.
-   Verifica se i tipi di supporti di input e output corrispondono perché il plug-in non converte i formati dall'input all'output.

Se il tipo di supporto proposto supera i test di convalida, viene archiviato in una variabile membro: **m \_ mtInput** per il tipo di supporto di input, **m \_ mtOutput** per il tipo di supporto di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP video**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




