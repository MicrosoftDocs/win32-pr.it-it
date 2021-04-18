---
description: Recupera le informazioni su un file di immagine specificato in memoria.
ms.assetid: 6363aaf1-abfc-49df-9b99-be8a1c3540e1
title: Funzione D3DXGetImageInfoFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2bad56cb2aa769be80a6b031b1783d8717bc485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322664"
---
# <a name="d3dxgetimageinfofromfileinmemory-function"></a><span data-ttu-id="9d378-103">D3DXGetImageInfoFromFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="9d378-103">D3DXGetImageInfoFromFileInMemory function</span></span>

<span data-ttu-id="9d378-104">Recupera le informazioni su un file di immagine specificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="9d378-104">Retrieves information about a given image file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d378-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d378-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFileInMemory(
  _In_ LPCVOID        pSrcData,
  _In_ UINT           SrcDataSize,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9d378-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d378-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d378-107">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d378-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d378-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d378-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d378-109">Puntatore VOID al file di origine in memoria.</span><span class="sxs-lookup"><span data-stu-id="9d378-109">VOID pointer to the source file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="9d378-110">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d378-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d378-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d378-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d378-112">Dimensioni in byte del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="9d378-112">Size of file in memory, in bytes.</span></span> <span data-ttu-id="9d378-113">.</span><span class="sxs-lookup"><span data-stu-id="9d378-113">.</span></span>

</dd> <dt>

<span data-ttu-id="9d378-114">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d378-114">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d378-115">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d378-115">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="9d378-116">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) che deve essere riempita con la descrizione dei dati nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="9d378-116">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d378-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d378-117">Return value</span></span>

<span data-ttu-id="9d378-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d378-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d378-119">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9d378-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9d378-120">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="9d378-120">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="9d378-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d378-121">Requirements</span></span>



| <span data-ttu-id="9d378-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d378-122">Requirement</span></span> | <span data-ttu-id="9d378-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9d378-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d378-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d378-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9d378-125"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d378-125"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9d378-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="9d378-126">Library</span></span><br/> | <dl> <span data-ttu-id="9d378-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d378-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9d378-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d378-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d378-129">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="9d378-129">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="9d378-130">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="9d378-130">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="9d378-131">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="9d378-131">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
