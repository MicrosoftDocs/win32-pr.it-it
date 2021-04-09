---
description: Utilizzo degli esempi di supporti
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Utilizzo degli esempi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968856"
---
# <a name="working-with-media-samples"></a>Utilizzo degli esempi di supporti

In questo argomento viene descritto come utilizzare l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) per modificare gli oggetti di esempio multimediali. Per una panoramica generale degli esempi di supporti, vedere [esempi di supporti](media-samples.md).

Per creare un nuovo esempio di supporto, chiamare la funzione [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) . Inizialmente, l'elenco di buffer dell'esempio è vuoto. Per aggiungere un buffer alla fine dell'elenco, chiamare [**IMFSample:: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Il codice seguente illustra come creare un esempio e aggiungervi un buffer.


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



Il metodo consigliato per ottenere i buffer dall'esempio consiste nel chiamare [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). Questo metodo restituisce un singolo buffer Continguous.

Per scorrere i buffer nell'elenco, iniziare chiamando [**IMFSample:: GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount). Questo metodo restituisce il numero di buffer. Chiamare quindi [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) e specificare l'indice del buffer da recuperare. I buffer sono indicizzati da zero.

Nel codice seguente viene illustrato come scorrere i buffer in un esempio.


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



Gli esempi hanno un timestamp e una durata. Il timestamp indica quando deve essere eseguito il rendering dei dati nell'esempio rispetto al clock di presentazione. La durata è l'intervallo di tempo per cui è necessario eseguire il rendering dei dati. In genere, il componente che genera i dati imposta il timestamp e la durata iniziali. Questi valori potrebbero essere modificati dalla sessione multimediale. Per impostare il timestamp, chiamare [**IMFSample:: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Per impostare la durata, chiamare [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Gli esempi possono includere anche attributi, che contengono informazioni aggiuntive sull'esempio. Per un elenco di attributi di esempio, vedere [esempi di attributi](sample-attributes.md). Per impostare e recuperare gli attributi, usare l' [**interfaccia IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), che eredita da [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[Buffer multimediali](media-buffers.md)
</dt> </dl>

 

 



