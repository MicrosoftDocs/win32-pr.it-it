---
title: Funzioni helper DirectML
description: Alcuni elenchi di codice delle funzioni di supporto DirectML essenziali.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 7c223ac8d5649c385b4a6f2ccf38e53be6456049
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548827"
---
# <a name="directml-helper-functions"></a><span data-ttu-id="231e8-103">Funzioni helper DirectML</span><span class="sxs-lookup"><span data-stu-id="231e8-103">DirectML helper functions</span></span>

## <a name="dmlcalcbuffertensorsize"></a><span data-ttu-id="231e8-104">DMLCalcBufferTensorSize</span><span class="sxs-lookup"><span data-stu-id="231e8-104">DMLCalcBufferTensorSize</span></span>

<span data-ttu-id="231e8-105">Questa funzione helper calcola il numero minimo di byte necessari per archiviare un tensore del buffer con il tipo, le dimensioni e gli stride specificati.</span><span class="sxs-lookup"><span data-stu-id="231e8-105">This helper function calculates the minimum number of bytes required to store a buffer tensor with the specified type, sizes, and strides.</span></span> <span data-ttu-id="231e8-106">La formula può essere espressa come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="231e8-106">The formula can be expressed as the following.</span></span>

```cpp
IndexOfLastElement = dot(Sizes - 1, Strides);
MinimumImpliedSizeInBytes = roundup((IndexOfLastElement + 1) * ElementSizeInBytes, 4)
```

<span data-ttu-id="231e8-107">In altre parole, la dimensione minima di un tensore è l'indice dell'elemento One-Past-the-end, moltiplicato per le dimensioni dell'elemento (ad esempio, 2 byte per un tensore **FLOAT16** ).</span><span class="sxs-lookup"><span data-stu-id="231e8-107">In other words, the minimum size of a tensor is the index of the one-past-the-end element, multiplied by the element size (for example, 2 bytes for a **FLOAT16** tensor).</span></span> <span data-ttu-id="231e8-108">Inoltre, DirectML richiede che tutti i buffer associati abbiano una dimensione totale con allineamento **DWORD** e, di conseguenza, la dimensione minima implicita in byte deve essere arrotondata al limite di 4 byte più vicino.</span><span class="sxs-lookup"><span data-stu-id="231e8-108">Additionally, DirectML requires that all bound buffers must have a total size that is **DWORD**-aligned, and hence the minimum implied size in bytes must be rounded up to the nearest 4-byte boundary.</span></span>

```cppwinrt
inline UINT64 DMLCalcBufferTensorSize(
    DML_TENSOR_DATA_TYPE dataType,
    UINT dimensionCount,
    _In_reads_(dimensionCount) const UINT* sizes,
    _In_reads_opt_(dimensionCount) const UINT* strides
    )
{
    UINT elementSizeInBytes = 0;
    switch (dataType)
    {
    case DML_TENSOR_DATA_TYPE_FLOAT32:
    case DML_TENSOR_DATA_TYPE_UINT32:
    case DML_TENSOR_DATA_TYPE_INT32:
        elementSizeInBytes = 4;
        break;

    case DML_TENSOR_DATA_TYPE_FLOAT16:
    case DML_TENSOR_DATA_TYPE_UINT16:
    case DML_TENSOR_DATA_TYPE_INT16:
        elementSizeInBytes = 2;
        break;

    case DML_TENSOR_DATA_TYPE_UINT8:
    case DML_TENSOR_DATA_TYPE_INT8:
        elementSizeInBytes = 1;
        break;

    default:
        return 0; // Invalid data type
    }

    UINT64 minimumImpliedSizeInBytes = 0;
    if (!strides)
    {
        minimumImpliedSizeInBytes = sizes[0];
        for (UINT i = 1; i < dimensionCount; ++i)
        {
            minimumImpliedSizeInBytes *= sizes[i];
        }
        minimumImpliedSizeInBytes *= elementSizeInBytes;
    }
    else
    {
        UINT indexOfLastElement = 0;
        for (UINT i = 0; i < dimensionCount; ++i)
        {
            indexOfLastElement += (sizes[i] - 1) * strides[i];
        }

        minimumImpliedSizeInBytes = (indexOfLastElement + 1) * elementSizeInBytes;
    }

    // Round up to the nearest 4 bytes.
    minimumImpliedSizeInBytes = (minimumImpliedSizeInBytes + 3) & ~3ui64;

    return minimumImpliedSizeInBytes;
}
```

## <a name="calculatestrides"></a><span data-ttu-id="231e8-109">CalculateStrides</span><span class="sxs-lookup"><span data-stu-id="231e8-109">CalculateStrides</span></span>

<span data-ttu-id="231e8-110">Questa funzione helper calcola gli stride per i tensori 4D con layout NCHW o NHWC e la trasmissione facoltativa.</span><span class="sxs-lookup"><span data-stu-id="231e8-110">This helper function calculates strides for 4D tensors with either NCHW or NHWC layout, and optional broadcasting.</span></span>

```cppwinrt
enum class Layout
{
    NCHW,
    NHWC
};

// Given dimension sizes (in NCHW order), calculates the strides to achieve a desired layout.
std::array<uint32_t, 4> CalculateStrides(
        Layout layout, 
        std::array<uint32_t, 4> sizes, 
        std::array<bool, 4> broadcast)
{
    enum DML_ORDER { N, C, H, W };

    uint32_t n = broadcast[N] ? 1 : sizes[N];
    uint32_t c = broadcast[C] ? 1 : sizes[C];
    uint32_t h = broadcast[H] ? 1 : sizes[H];
    uint32_t w = broadcast[W] ? 1 : sizes[W];

    uint32_t nStride = 0, cStride = 0, hStride = 0, wStride = 0;

    switch (layout)
    {
    case Layout::NCHW:
        nStride = broadcast[N] ? 0 : c * h * w;
        cStride = broadcast[C] ? 0 : h * w;
        hStride = broadcast[H] ? 0 : w;
        wStride = broadcast[W] ? 0 : 1;
        break;

    case Layout::NHWC:
        nStride = broadcast[N] ? 0 : h * w * c;
        hStride = broadcast[H] ? 0 : w * c;
        wStride = broadcast[W] ? 0 : c;
        cStride = broadcast[C] ? 0 : 1;
        break;
    }

    return { nStride, cStride, hStride, wStride };
}
```
