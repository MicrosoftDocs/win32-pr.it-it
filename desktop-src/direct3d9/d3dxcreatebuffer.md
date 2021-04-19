---
description: Crea un oggetto buffer.
ms.assetid: 6f44fe84-3e0b-4fb8-821a-c997944fed37
title: Funzione D3DXCreateBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc54813ea9947d263febcbe843702124c68ba747
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323423"
---
# <a name="d3dxcreatebuffer-function"></a><span data-ttu-id="5b02d-103">D3DXCreateBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="5b02d-103">D3DXCreateBuffer function</span></span>

<span data-ttu-id="5b02d-104">Crea un oggetto buffer.</span><span class="sxs-lookup"><span data-stu-id="5b02d-104">Creates a buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b02d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b02d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBuffer(
  _In_  DWORD        NumBytes,
  _Out_ LPD3DXBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="5b02d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b02d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b02d-107">*NumBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b02d-107">*NumBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b02d-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b02d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b02d-109">Dimensioni del buffer da creare, in byte.</span><span class="sxs-lookup"><span data-stu-id="5b02d-109">Size of the buffer to create, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5b02d-110">*ppBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5b02d-110">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b02d-111">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b02d-111">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5b02d-112">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che rappresenta l'oggetto buffer creato.</span><span class="sxs-lookup"><span data-stu-id="5b02d-112">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, representing the created buffer object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b02d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b02d-113">Return value</span></span>

<span data-ttu-id="5b02d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b02d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b02d-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b02d-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5b02d-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="5b02d-116">If the function fails, the return value can be one of the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b02d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b02d-117">Requirements</span></span>



| <span data-ttu-id="5b02d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b02d-118">Requirement</span></span> | <span data-ttu-id="5b02d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5b02d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b02d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b02d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5b02d-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b02d-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5b02d-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b02d-122">Library</span></span><br/> | <dl> <span data-ttu-id="5b02d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b02d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5b02d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b02d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b02d-125">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="5b02d-125">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
