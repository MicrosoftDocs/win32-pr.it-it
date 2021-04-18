---
description: Modifica il numero di campioni contenuti nel buffer.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: 'Metodo ID3DXPRTBuffer:: Resize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c54044ffc9e166131faa16c9b438b497c658ef25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323038"
---
# <a name="id3dxprtbufferresize-method"></a><span data-ttu-id="5a139-103">Metodo ID3DXPRTBuffer:: Resize</span><span class="sxs-lookup"><span data-stu-id="5a139-103">ID3DXPRTBuffer::Resize method</span></span>

<span data-ttu-id="5a139-104">Modifica il numero di campioni contenuti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="5a139-104">Changes the number of samples contained in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a139-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a139-105">Syntax</span></span>


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a><span data-ttu-id="5a139-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a139-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a139-107">*NewSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a139-107">*NewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a139-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a139-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a139-109">Numero di campioni da contenere nel buffer.</span><span class="sxs-lookup"><span data-stu-id="5a139-109">Number of samples to be contained in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a139-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a139-110">Return value</span></span>

<span data-ttu-id="5a139-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a139-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a139-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a139-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5a139-113">Se il metodo ha esito negativo, verrà restituito il valore seguente, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="5a139-113">If the method fails, the following value will be returned, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a139-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a139-114">Requirements</span></span>



| <span data-ttu-id="5a139-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a139-115">Requirement</span></span> | <span data-ttu-id="5a139-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5a139-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a139-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a139-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5a139-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a139-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5a139-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a139-119">Library</span></span><br/> | <dl> <span data-ttu-id="5a139-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a139-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a139-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a139-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a139-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="5a139-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
