---
description: Formato flusso
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Formato flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316299"
---
# <a name="stream-format"></a>Formato flusso

Sia MSDV che il driver UVC possono restituire due formati DV: audio-video interleaved o solo video. Audio-video con interfoliazione è il formato originale dal dispositivo. Il formato solo video contiene gli stessi dati, ma gli esempi sono contrassegnati come privi di dati audio. Il formato solo video è disponibile principalmente per la compatibilità con le applicazioni che utilizzano video per Windows. Per ulteriori informazioni, vedere la pagina relativa ai [file AVI DV](type-1-vs--type-2-dv-avi-files.md)di tipo 1 e 2.

**Driver MSDV**

Il driver MSDV ha due pin di output. Il primo pin di output invia dati con interfoliazione e il secondo pin di output invia dati di solo video. È possibile connettere solo un pin di output alla volta. Per selezionare un formato, connettere il pin di output appropriato. Per trovare il formato, è possibile usare l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sul pin di output.

**Driver UVC**

Diversamente dal driver MSDV, il driver UVC fornisce entrambi i formati dallo stesso pin. Il formato predefinito è solo video. Per selezionare il formato, usare l'interfaccia **IAMStreamConfig** sul pin di output. Chiamare il metodo **GetStreamCaps** per enumerare i tipi di supporto sul pin di output. Per ogni tipo di supporto, se il tipo principale corrisponde al formato desiderato, chiamare **Seformatt** e passare il tipo di supporto.



| Formato                      | Tipo principale             |
|-----------------------------|------------------------|
| Audio e video con interfoliazione | MEDIATYPE con \_ interfoliazione |
| Solo video                  | Video di MEDIATYPE \_       |



 

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



Il driver MSDV supporta anche **IAMStreamConfig**, quindi è possibile scrivere codice che funziona per entrambi i tipi di dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



