---
title: Negoziazione del formato video nel plug-in DSP video di esempio
description: Negoziazione del formato video nel plug-in DSP video di esempio
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- Plug-in di Windows Media Player, video DSP
- plug-in, video DSP
- plug-in per l'elaborazione di segnali digitali, negoziazione del formato video
- Plug-in DSP, negoziazione del formato video
- plug-in di video DSP, negoziazione del formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287a38fbfcf11f1b9d74087a91c5825b22f1243
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330247"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>Negoziazione del formato video nel plug-in DSP video di esempio

Prima che Windows Media Player inserisca un plug-in di DSP video nella catena di segnali, il lettore deve determinare se il plug-in è in grado di elaborare il video riprodotto. Il processo mediante il quale il plug-in e il lettore comunicano sui formati video supportati è denominato negoziazione del formato.

## <a name="providing-the-supported-input-and-output-types"></a>Fornire i tipi di input e output supportati

Se il plug-in DSP funge da oggetto DMO (DirectX Media Object), il lettore esegue una query sul plug-in sui formati supportati eseguendo una sequenza di chiamate a **IMediaObject:: GetInputType** e **IMediaObject:: GetOutputType**.

Se il plug-in DSP funge da trasformazione Media Foundation (MFT), il lettore esegue una query sul plug-in sui formati supportati eseguendo una sequenza di chiamate a **IMFTransform:: GetInputAvailableType** e **IMFTransform:: GetOutputAvailableType**.

Il plug-in video di esempio generato dalla procedura guidata per il plug-in di Windows Media Player archivia l'elenco dei formati video supportati come una matrice di GUID. Il codice seguente viene dal file Main. cpp:


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



Il lettore può chiamare **IMediaObject:: GetInputType** e **IMediaObject:: GetOutputType** in qualsiasi ordine, quindi il codice del plug-in deve prevedere questa operazione. Analogamente, il lettore può chiamare **IMFTransform:: GetInputAvailableType** e **IMFTransform:: GetOutputAvailableType** in qualsiasi ordine. Le implementazioni di esempio di **GetOutputType** e **GetOutputAvailableType** verificano se il tipo di input è già stato definito. In caso contrario, il plug-in risponde che supporta solo quel tipo. In caso contrario, il plug-in restituisce il tipo che corrisponde all'indice fornito, come illustrato nel codice seguente:


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



## <a name="setting-the-input-and-output-types"></a>Impostazione dei tipi di input e di output

Se il plug-in DSP funge da DMO, Windows Media Player imposta il tipo di supporto chiamando **IMediaObject:: SetInputType** e **IMediaObject:: SetOutputType**, passando a ogni funzione un puntatore a una struttura del **\_ \_ tipo di supporto DMO** che rappresenta il tipo di supporto richiesto.

Se il plug-in DSP funge da MFT, Windows Media Player imposta il tipo di supporto chiamando **IMFTransform:: SetInputType** e **IMFTransform:: SetOutputType**, passando a ogni funzione un puntatore a un'interfaccia **IMFMediaType** che rappresenta il tipo di supporto richiesto.

Non vi è alcuna garanzia che il lettore chiamerà i metodi di negoziazione del formato in un ordine particolare, quindi il codice del plug-in deve gestire qualsiasi caso. Ad esempio, se il giocatore chiama **SetOutputType** prima di chiamare **SetInputType**, è una valida azione per il plug-in per rifiutare il tipo di supporto di output proposto. Il codice seguente dell'implementazione di esempio di **IMediaObject:: SetOutputType** dimostra quanto segue:


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



Le implementazioni di plug-in di esempio di **SetInputType** e **SetOutputType** chiamano la funzione personalizzata denominata **ValidateMediaType**. Questa funzione plug-in esegue una serie di test sul tipo di supporto proposto progettato per garantire che il tipo di supporto sia ben formato e supportato dal plug-in. **ValidateMediaType** esegue i test seguenti:

-   Verifica che i membri **majortype** e **formatType** contengano i valori corretti.
-   Verifica che il membro del **sottotipo** corrisponda a uno dei formati supportati.
-   Verifica che le informazioni nelle strutture **BITMAPINFOHEADER** e **VIDEOINFOHEADER** o **VIDEOINFOHEADER2** contengano valori validi.
-   Verifica se i tipi di supporto di input e di output corrispondono perché il plug-in non converte i formati dall'input all'output.

Se il tipo di supporto proposto supera i test di convalida, viene archiviato in una variabile membro: **m \_ mtInput** per il tipo di supporto di input, **m \_ mtOutput** per il tipo di supporto di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in video DSP**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




