---
title: Funzione GetRequiredIntermediateSize (D3dx12. h)
description: Restituisce le dimensioni richieste di un buffer da utilizzare per il caricamento dei dati.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- GetRequiredIntermediateSize (funzione)
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323127"
---
# <a name="getrequiredintermediatesize-function"></a><span data-ttu-id="d6931-104">GetRequiredIntermediateSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="d6931-104">GetRequiredIntermediateSize function</span></span>

<span data-ttu-id="d6931-105">Restituisce le dimensioni richieste di un buffer da utilizzare per il caricamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="d6931-105">Returns the required size of a buffer to be used for data upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6931-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6931-106">Syntax</span></span>


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a><span data-ttu-id="d6931-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6931-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6931-108">*pDestinationResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6931-108">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6931-109">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="d6931-109">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="d6931-110">Puntatore all'interfaccia [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) che rappresenta la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d6931-110">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="d6931-111">*FirstSubresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6931-111">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6931-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6931-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d6931-113">Indice della prima sottorisorsa nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6931-113">The index of the first subresource in the resource.</span></span> <span data-ttu-id="d6931-114">L'intervallo di valori validi è compreso tra 0 e D3D12 le \_ \_ sottorisorse di req.</span><span class="sxs-lookup"><span data-stu-id="d6931-114">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="d6931-115">*NumSubresources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6931-115">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6931-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6931-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d6931-117">Numero di sottorisorse nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6931-117">The number of subresources in the resource.</span></span> <span data-ttu-id="d6931-118">L'intervallo di valori validi è compreso tra 0 e (D3D12 \_ req Resources \_ - *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="d6931-118">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6931-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6931-119">Return value</span></span>

<span data-ttu-id="d6931-120">Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6931-120">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d6931-121">Dimensioni del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="d6931-121">The size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6931-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6931-122">Requirements</span></span>



| <span data-ttu-id="d6931-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6931-123">Requirement</span></span> | <span data-ttu-id="d6931-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d6931-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6931-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6931-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d6931-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6931-126"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d6931-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="d6931-127">Library</span></span><br/> | <dl> <span data-ttu-id="d6931-128"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6931-128"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6931-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d6931-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6931-130"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6931-130"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6931-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6931-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6931-132">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="d6931-132">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

