---
description: Formato flusso
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Formato flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01ed1ac4501a2d8f081c12fef75baf15aaebd442fc182a116db1038c2a73523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903991"
---
# <a name="stream-format"></a>Formato flusso

Sia il driver MSDV che il driver UVC possono eseguire l'output di due formati DV: audio-video interleaved o solo video. L'audio-video interfoliato è il formato originale del dispositivo. Il formato solo video contiene gli stessi dati, ma gli esempi sono contrassegnati come senza dati audio. Il formato solo video è disponibile principalmente per la compatibilità con le applicazioni che usano Video per Windows. Per altre informazioni, vedere [Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).

**MSDV Driver**

Il driver MSDV ha due pin di output. Il primo pin di output invia dati interleaved e il secondo pin di output invia dati solo video. È possibile collegare un solo pin di output alla volta. Per selezionare un formato, connettere il pin di output appropriato. È possibile usare [**l'interfaccia IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sul pin di output per trovare il formato.

**UVC Driver**

A differenza del driver MSDV, il driver UVC offre entrambi i formati dallo stesso pin. Il formato predefinito è solo video. Per selezionare il formato, usare **l'interfaccia IAMStreamConfig** sul pin di output. Chiamare il **metodo GetStreamCaps** per enumerare i tipi di supporti sul pin di output. Per ogni tipo di supporto, se il tipo principale corrisponde al formato desiderato, chiamare **SetFormat** e passare tale tipo di supporto.



| Formato                      | Tipo principale             |
|-----------------------------|------------------------|
| Audio e video interleaved | MEDIATYPE \_ Interleaved |
| Solo video                  | MEDIATYPE \_ Video       |



 

La funzione seguente imposta il formato in base al GUID di tipo principale.


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



Il driver MSDV supporta anche **IAMStreamConfig,** quindi è possibile scrivere codice che funziona per entrambi i tipi di dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di un camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



