---
title: Funzione MemcpySubresource (D3dx12. h)
description: Copia una sottorisorsa riga per riga.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- MemcpySubresource (funzione)
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323089"
---
# <a name="memcpysubresource-function"></a><span data-ttu-id="fbb87-104">MemcpySubresource (funzione)</span><span class="sxs-lookup"><span data-stu-id="fbb87-104">MemcpySubresource function</span></span>

<span data-ttu-id="fbb87-105">Copia una sottorisorsa riga per riga.</span><span class="sxs-lookup"><span data-stu-id="fbb87-105">Copies a subresource row by row.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb87-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbb87-106">Syntax</span></span>


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a><span data-ttu-id="fbb87-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbb87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb87-108">*pDest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbb87-108">*pDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb87-109">Tipo: **const [**D3D12 \_ MEMCPY \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***</span><span class="sxs-lookup"><span data-stu-id="fbb87-109">Type: **const [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest)\***</span></span>

<span data-ttu-id="fbb87-110">Puntatore a una struttura [**\_ \_ dest MEMCPY D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) che descrive la destinazione dell'operazione di copia della memoria.</span><span class="sxs-lookup"><span data-stu-id="fbb87-110">A pointer to a [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) structure that describes the destination of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="fbb87-111">*pSrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbb87-111">*pSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb87-112">Tipo: **const \* [**D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)**</span><span class="sxs-lookup"><span data-stu-id="fbb87-112">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="fbb87-113">Puntatore a una struttura [**di \_ \_ dati della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) che descrive l'origine dell'operazione di copia della memoria.</span><span class="sxs-lookup"><span data-stu-id="fbb87-113">A pointer to a [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structure that describes the source of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="fbb87-114">*RowSizeInBytes*</span><span class="sxs-lookup"><span data-stu-id="fbb87-114">*RowSizeInBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb87-115">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fbb87-115">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fbb87-116">Dimensione, in byte, di ogni riga.</span><span class="sxs-lookup"><span data-stu-id="fbb87-116">The size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="fbb87-117">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="fbb87-117">*NumRows*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb87-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fbb87-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fbb87-119">Numero di righe.</span><span class="sxs-lookup"><span data-stu-id="fbb87-119">The number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="fbb87-120">*NumSlices*</span><span class="sxs-lookup"><span data-stu-id="fbb87-120">*NumSlices*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb87-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fbb87-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fbb87-122">Numero di sezioni.</span><span class="sxs-lookup"><span data-stu-id="fbb87-122">The number of slices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb87-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbb87-123">Return value</span></span>

<span data-ttu-id="fbb87-124">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fbb87-124">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb87-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbb87-125">Remarks</span></span>

<span data-ttu-id="fbb87-126">Prendere in considerazione anche i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="fbb87-126">Also consider the following methods:</span></span>

-   [<span data-ttu-id="fbb87-127">**ID3D12Resource::WriteToSubresource**</span><span class="sxs-lookup"><span data-stu-id="fbb87-127">**ID3D12Resource::WriteToSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [<span data-ttu-id="fbb87-128">**ID3D12Resource::ReadFromSubresource**</span><span class="sxs-lookup"><span data-stu-id="fbb87-128">**ID3D12Resource::ReadFromSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [<span data-ttu-id="fbb87-129">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="fbb87-129">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a><span data-ttu-id="fbb87-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbb87-130">Requirements</span></span>



| <span data-ttu-id="fbb87-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbb87-131">Requirement</span></span> | <span data-ttu-id="fbb87-132">Valore</span><span class="sxs-lookup"><span data-stu-id="fbb87-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb87-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbb87-133">Header</span></span><br/>  | <dl> <span data-ttu-id="fbb87-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbb87-134"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="fbb87-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="fbb87-135">Library</span></span><br/> | <dl> <span data-ttu-id="fbb87-136"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbb87-136"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="fbb87-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fbb87-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="fbb87-138"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbb87-138"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbb87-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbb87-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb87-140">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="fbb87-140">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="fbb87-141">Sottorisorse</span><span class="sxs-lookup"><span data-stu-id="fbb87-141">Subresources</span></span>](subresources.md)
</dt> </dl>

 

