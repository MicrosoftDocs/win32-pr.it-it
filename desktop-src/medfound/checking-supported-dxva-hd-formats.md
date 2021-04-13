---
description: .
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Controllo dei formati DXVA-HD supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7560d574cee5fca21ab8de78b01b87af1de5a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484124"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="305cc-103">Controllo dei formati DXVA-HD supportati</span><span class="sxs-lookup"><span data-stu-id="305cc-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="305cc-104">Verifica dei formati di input supportati</span><span class="sxs-lookup"><span data-stu-id="305cc-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="305cc-105">Per ottenere un elenco dei formati di input supportati dal dispositivo Microsoft DirectX Video Acceleration High Definition (DXVA-HD), eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="305cc-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="305cc-106">Chiamare [**IDXVAHD \_ Device:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) per ottenere le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="305cc-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="305cc-107">Verificare il membro **InputFormatCount** della struttura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="305cc-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="305cc-108">Questo membro fornisce il numero di formati di input supportati.</span><span class="sxs-lookup"><span data-stu-id="305cc-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="305cc-109">Allocare una matrice di valori **D3DFORMAT** di dimensioni **InputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="305cc-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="305cc-110">Passare questa matrice al metodo [**\_ Device:: GetVideoProcessorInputFormats di IDXVAHD**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) .</span><span class="sxs-lookup"><span data-stu-id="305cc-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="305cc-111">I metodi riempiono la matrice con un elenco di formati di input.</span><span class="sxs-lookup"><span data-stu-id="305cc-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="305cc-112">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="305cc-112">The following code shows these steps:</span></span>


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



## <a name="checking-supported-output-formats"></a><span data-ttu-id="305cc-113">Controllo dei formati di output supportati</span><span class="sxs-lookup"><span data-stu-id="305cc-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="305cc-114">Per ottenere un elenco dei formati di output supportati dal dispositivo DXVA-HD, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="305cc-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="305cc-115">Chiamare [**IDXVAHD \_ Device:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) per ottenere le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="305cc-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="305cc-116">Verificare il membro **OutputFormatCount** della struttura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="305cc-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="305cc-117">Questo membro fornisce il numero di formati di input supportati.</span><span class="sxs-lookup"><span data-stu-id="305cc-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="305cc-118">Allocare una matrice di valori **D3DFORMAT** di dimensioni **OutputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="305cc-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="305cc-119">Passare questa matrice al metodo [**\_ Device:: GetVideoProcessorOutputFormats di IDXVAHD**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) .</span><span class="sxs-lookup"><span data-stu-id="305cc-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="305cc-120">I metodi riempiono la matrice con un elenco di formati di output.</span><span class="sxs-lookup"><span data-stu-id="305cc-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="305cc-121">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="305cc-121">The following code shows these steps:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="305cc-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="305cc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="305cc-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="305cc-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



