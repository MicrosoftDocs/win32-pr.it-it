---
description: Ottenere un puntatore alla memoria buffer mesh per modificarne il contenuto.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: Metodo ID3DX10MeshBuffer::Map (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4a71aaaffe7ed11429efa67b6065f94ecd154d0
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335355"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="c025e-103">Metodo ID3DX10MeshBuffer::Map</span><span class="sxs-lookup"><span data-stu-id="c025e-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="c025e-104">Ottenere un puntatore alla memoria buffer mesh per modificarne il contenuto.</span><span class="sxs-lookup"><span data-stu-id="c025e-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="c025e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c025e-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="c025e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c025e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c025e-107">*ppData* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c025e-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c025e-108">Tipo: **\* \* void**</span><span class="sxs-lookup"><span data-stu-id="c025e-108">Type: **void\*\***</span></span>

<span data-ttu-id="c025e-109">Puntatore ai dati del buffer.</span><span class="sxs-lookup"><span data-stu-id="c025e-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="c025e-110">*pSize* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c025e-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c025e-111">Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c025e-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c025e-112">Dimensione del buffer in byte.</span><span class="sxs-lookup"><span data-stu-id="c025e-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c025e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c025e-113">Return value</span></span>

<span data-ttu-id="c025e-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c025e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c025e-115">Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="c025e-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c025e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c025e-116">Remarks</span></span>



 <span data-ttu-id="c025e-117">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="c025e-117">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="c025e-118">Map() in Direct3D 10 è analogo alla risorsa Map() in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c025e-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="c025e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c025e-119">Requirements</span></span>



| <span data-ttu-id="c025e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c025e-120">Requirement</span></span> | <span data-ttu-id="c025e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c025e-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c025e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c025e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c025e-123"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="c025e-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c025e-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="c025e-124">Library</span></span><br/> | <dl> <span data-ttu-id="c025e-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c025e-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c025e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c025e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c025e-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="c025e-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="c025e-128">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="c025e-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
