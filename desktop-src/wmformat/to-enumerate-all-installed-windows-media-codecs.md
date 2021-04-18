---
title: Per enumerare tutti i codec Windows Media installati
description: Per enumerare tutti i codec Windows Media installati
ms.assetid: 651c8624-0b66-4d0e-a25f-6c4b1a94e849
keywords:
- flussi, enumerazione dei codec Windows Media installati
- codec, enumerazioni
- flussi, indici di codec
- codec, indici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db9a35913dde13f563ee57d54ee5e7de87d82cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298783"
---
# <a name="to-enumerate-all-installed-windows-media-codecs"></a>Per enumerare tutti i codec Windows Media installati

Le interfacce di informazioni del codec utilizzano tutti gli indici codec per identificare i singoli codec. I codec sono indicizzati in modo indipendente per l'audio e per i video. All'interno di un tipo di codec, gli indici variano da 0 a uno inferiore al numero di codec di quel tipo.

Nell'esempio di codice seguente viene illustrato come ottenere l'indice associato a ciascun codec. Per compilare il codice nell'applicazione, includere STDIO. h.


```C++
HRESULT GetCodecNames(IWMCodecInfo3* pCodecInfo)
{
    HRESULT hr = S_OK;
    DWORD   cCodecs  = 0;
    WCHAR*  pwszCodecName  = NULL;
    DWORD   cchCodecName     = 0;
    
    // Retrieve the number of supported audio codecs on the system.
    hr = pCodecInfo->GetCodecInfoCount(WMMEDIATYPE_Audio, &cCodecs);

    if(SUCCEEDED(hr))
        printf("Number of audio codecs: %d\n\n", cCodecs);
    else
    {
        printf("Could not get the count of audio codecs.\n");
        return hr;
    }

    // Loop through all the audio codecs.
    for(DWORD dwCodecIndex = 0; dwCodecIndex < cCodecs; dwCodecIndex++)
    {
        // Get the codec name:
        // First, get the size of the name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Audio, 
                                      dwCodecIndex, 
                                      NULL, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            printf("Could not get the size of the codec name.\n");
            return hr;
        }

        // Allocate a string of the appropriate size.
        pwszCodecName = new WCHAR[cchCodecName];
        if(pwszCodecName == NULL)
        {
            printf("Could not allocate memory.\n");
            return E_OUTOFMEMORY;
        }

        // Retrieve the codec name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Audio, 
                                      dwCodecIndex, 
                                      pwszCodecName, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            delete[] pwszCodecName;
            printf("Could not get the codec name.\n");
            return hr;
        }

        // Print the codec name.
        printf("%d %S\n", dwCodecIndex, pwszCodecName);

        // Clean up for the next iteration.
        delete[] pwszCodecName;
        pwszCodecName = NULL;
        cchCodecName  = 0;
    }

    // Retrieve the number of supported video codecs on the system.
    hr = pCodecInfo->GetCodecInfoCount(WMMEDIATYPE_Video, &cCodecs);

    if(SUCCEEDED(hr))
        printf("\n\nNumber of video codecs: %d.\n\n", cCodecs);
    else
    {
        printf("Could not get the count of video codecs.\n");
        return hr;
    }

    // Loop through all the video codecs.
    for(dwCodecIndex = 0; dwCodecIndex < cCodecs; dwCodecIndex++)
    {
        // Get the codec name:
        // First, get the size of the name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Video, 
                                      dwCodecIndex, 
                                      NULL, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            printf("Could not get the size of the codec name.\n");
            return hr;
        }

        // Allocate a string of the appropriate size.
        pwszCodecName = new WCHAR[cchCodecName];
        if(pwszCodecName == NULL)
        {
            printf("Could not allocate memory.\n");
            return E_OUTOFMEMORY;
        }

        // Retrieve the codec name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Video, 
                                      dwCodecIndex, 
                                      pwszCodecName, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            printf("Could not get the codec name.\n");
            return hr;
        }

        // Print the codec name.
        printf("%d %S\n", dwCodecIndex, pwszCodecName);

        delete[] pwszCodecName;
        pwszCodecName = NULL;
        cchCodecName  = 0;
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero delle informazioni di configurazione dei flussi dai codec**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




