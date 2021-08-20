---
description: Controllo dei formati DXVA-HD supportati
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Controllo dei formati DXVA-HD supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b28586148bb96a918c8a230a25ff1477af73e0604d3b62e11e644e8276b7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035409"
---
# <a name="checking-supported-dxva-hd-formats"></a>Controllo dei formati DXVA-HD supportati

## <a name="checking-supported-input-formats"></a>Controllo dei formati di input supportati

Per ottenere un elenco dei formati di input supportati dal dispositivo DXVA-HD (Microsoft DirectX Video Acceleration High Definition), eseguire le operazioni seguenti:

1.  Chiamare [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) per ottenere le funzionalità del dispositivo.
2.  Controllare il **membro InputFormatCount** della struttura [**\_ VPDEVCAPS DXVAHD.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Questo membro fornisce il numero di formati di input supportati.
3.  Allocare una matrice di **valori D3DFORMAT** di dimensioni **InputFormatCount**.
4.  Passare questa matrice al [**metodo IDXVAHD \_ Device::GetVideoProcessorInputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) I metodi riempiono la matrice con un elenco di formati di input.

Il codice seguente illustra questi passaggi:


```C++
// Checks whether a DXVA-HD device supports a specified input format.

HRESULT CheckInputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[ caps.InputFormatCount ];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorInputFormats(
        caps.InputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.InputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.InputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="checking-supported-output-formats"></a>Controllo dei formati di output supportati

Per ottenere un elenco dei formati di output supportati dal dispositivo DXVA-HD, eseguire le operazioni seguenti:

1.  Chiamare [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) per ottenere le funzionalità del dispositivo.
2.  Controllare il **membro OutputFormatCount** della [**struttura \_ VPDEVCAPS DXVAHD.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Questo membro fornisce il numero di formati di input supportati.
3.  Allocare una matrice di **valori D3DFORMAT** di dimensioni **OutputFormatCount**.
4.  Passare questa matrice al [**metodo IDXVAHD \_ Device::GetVideoProcessorOutputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) I metodi riempiono la matrice con un elenco di formati di output.

Il codice seguente illustra questi passaggi:


```C++
// Checks whether a DXVA-HD device supports a specified output format.

HRESULT CheckOutputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[caps.OutputFormatCount];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorOutputFormats(
        caps.OutputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.OutputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.OutputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



