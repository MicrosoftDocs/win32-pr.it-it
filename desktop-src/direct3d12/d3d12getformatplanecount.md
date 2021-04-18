---
title: Funzione D3D12GetFormatPlaneCount (D3dx12. h)
description: Ottiene il numero di piani per il formato DXGI specificato per la scheda virtuale specificata (ID3D12Device).
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- D3D12GetFormatPlaneCount (funzione)
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322178"
---
# <a name="d3d12getformatplanecount-function"></a><span data-ttu-id="f7ad7-104">D3D12GetFormatPlaneCount (funzione)</span><span class="sxs-lookup"><span data-stu-id="f7ad7-104">D3D12GetFormatPlaneCount function</span></span>

<span data-ttu-id="f7ad7-105">Ottiene il numero di piani per il formato DXGI specificato per la scheda virtuale specificata ( **ID3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="f7ad7-105">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ad7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7ad7-106">Syntax</span></span>


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a><span data-ttu-id="f7ad7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7ad7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7ad7-108">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7ad7-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7ad7-109">Tipo: **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span><span class="sxs-lookup"><span data-stu-id="f7ad7-109">Type: **[**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span></span>

<span data-ttu-id="f7ad7-110">Scheda virtuale ( [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) per cui ottenere il conteggio del piano.</span><span class="sxs-lookup"><span data-stu-id="f7ad7-110">The virtual adapter (an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) for which to get the plane count.</span></span>

</dd> <dt>

<span data-ttu-id="f7ad7-111">*Formato*</span><span class="sxs-lookup"><span data-stu-id="f7ad7-111">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="f7ad7-112">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f7ad7-112">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f7ad7-113">[**\_ Formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) per il quale ottenere il conteggio del piano.</span><span class="sxs-lookup"><span data-stu-id="f7ad7-113">The [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) for which to get the plane count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7ad7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7ad7-114">Return value</span></span>

<span data-ttu-id="f7ad7-115">Tipo: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f7ad7-115">Type: **UINT8**</span></span>

<span data-ttu-id="f7ad7-116">Il numero di piani per il formato specificato nella scheda virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="f7ad7-116">The plane count for the specified format on the specified virtual adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7ad7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7ad7-117">Requirements</span></span>



| <span data-ttu-id="f7ad7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7ad7-118">Requirement</span></span> | <span data-ttu-id="f7ad7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f7ad7-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ad7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7ad7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f7ad7-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7ad7-121"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="f7ad7-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="f7ad7-122">Library</span></span><br/> | <dl> <span data-ttu-id="f7ad7-123"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7ad7-123"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7ad7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f7ad7-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="f7ad7-125"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7ad7-125"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7ad7-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7ad7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ad7-127">**\_Informazioni sul \_ formato dei dati della funzionalità \_ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="f7ad7-127">**D3D12\_FEATURE\_DATA\_FORMAT\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[<span data-ttu-id="f7ad7-128">**CheckFeatureSupport**</span><span class="sxs-lookup"><span data-stu-id="f7ad7-128">**CheckFeatureSupport**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[<span data-ttu-id="f7ad7-129">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="f7ad7-129">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

