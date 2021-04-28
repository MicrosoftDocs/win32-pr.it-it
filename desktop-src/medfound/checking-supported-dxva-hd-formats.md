---
description: Controllo dei formati DXVA-HD supportati
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Controllo dei formati DXVA-HD supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07d47043ed200d256e2bef8fa2c9ab6717f3b82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090009"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="ed49e-103">Controllo dei formati DXVA-HD supportati</span><span class="sxs-lookup"><span data-stu-id="ed49e-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="ed49e-104">Controllo dei formati di input supportati</span><span class="sxs-lookup"><span data-stu-id="ed49e-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="ed49e-105">Per ottenere un elenco dei formati di input supportati dal dispositivo Microsoft DirectX Video Acceleration High Definition (DXVA-HD), seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="ed49e-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="ed49e-106">Chiamare [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) per ottenere le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed49e-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="ed49e-107">Controllare il **membro InputFormatCount** della [**struttura DXVAHD \_ VPDEVCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)</span><span class="sxs-lookup"><span data-stu-id="ed49e-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="ed49e-108">Questo membro fornisce il numero di formati di input supportati.</span><span class="sxs-lookup"><span data-stu-id="ed49e-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="ed49e-109">Allocare una matrice di **valori D3DFORMAT** di dimensioni **InputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="ed49e-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="ed49e-110">Passare questa matrice al [**metodo IDXVAHD \_ Device::GetVideoProcessorInputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats)</span><span class="sxs-lookup"><span data-stu-id="ed49e-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="ed49e-111">I metodi riempiono la matrice con un elenco di formati di input.</span><span class="sxs-lookup"><span data-stu-id="ed49e-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="ed49e-112">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="ed49e-112">The following code shows these steps:</span></span>


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



## <a name="checking-supported-output-formats"></a><span data-ttu-id="ed49e-113">Controllo dei formati di output supportati</span><span class="sxs-lookup"><span data-stu-id="ed49e-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="ed49e-114">Per ottenere un elenco dei formati di output supportati dal dispositivo DXVA-HD, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="ed49e-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="ed49e-115">Chiamare [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) per ottenere le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed49e-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="ed49e-116">Controllare il **membro OutputFormatCount** della [**struttura DXVAHD \_ VPDEVCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)</span><span class="sxs-lookup"><span data-stu-id="ed49e-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="ed49e-117">Questo membro fornisce il numero di formati di input supportati.</span><span class="sxs-lookup"><span data-stu-id="ed49e-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="ed49e-118">Allocare una matrice di **valori D3DFORMAT** di dimensioni **OutputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="ed49e-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="ed49e-119">Passare questa matrice al [**metodo IDXVAHD \_ Device::GetVideoProcessorOutputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats)</span><span class="sxs-lookup"><span data-stu-id="ed49e-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="ed49e-120">I metodi riempiono la matrice con un elenco di formati di output.</span><span class="sxs-lookup"><span data-stu-id="ed49e-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="ed49e-121">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="ed49e-121">The following code shows these steps:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ed49e-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed49e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed49e-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ed49e-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



