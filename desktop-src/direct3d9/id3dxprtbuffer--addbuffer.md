---
description: Aggiunge un altro buffer a ID3DXPRTBuffer e archivia i risultati in ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'Metodo ID3DXPRTBuffer:: AddBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323707"
---
# <a name="id3dxprtbufferaddbuffer-method"></a><span data-ttu-id="ecd4f-103">Metodo ID3DXPRTBuffer:: AddBuffer</span><span class="sxs-lookup"><span data-stu-id="ecd4f-103">ID3DXPRTBuffer::AddBuffer method</span></span>

<span data-ttu-id="ecd4f-104">Aggiunge un altro buffer a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) e archivia i risultati in **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="ecd4f-104">Adds another buffer to the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and stores the results in **ID3DXPRTBuffer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd4f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecd4f-105">Syntax</span></span>


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ecd4f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecd4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecd4f-107">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecd4f-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd4f-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="ecd4f-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="ecd4f-109">Puntatore a un buffer contenente i membri da aggiungere ai rispettivi membri del buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd4f-109">Pointer to a buffer that contains members to be added to the respective members of the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecd4f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecd4f-110">Return value</span></span>

<span data-ttu-id="ecd4f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ecd4f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ecd4f-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ecd4f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ecd4f-113">Se il metodo ha esito negativo, verrà restituito il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="ecd4f-113">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecd4f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecd4f-114">Remarks</span></span>

<span data-ttu-id="ecd4f-115">pBuffer e [**ID3DXPRTBuffer**](id3dxprtbuffer.md) devono avere lo stesso numero di campioni, coefficienti e canali dei colori; altrimenti il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ecd4f-115">pBuffer and [**ID3DXPRTBuffer**](id3dxprtbuffer.md) must have the same number of samples, coefficients, and color channels; the method will fail otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd4f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecd4f-116">Requirements</span></span>



| <span data-ttu-id="ecd4f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecd4f-117">Requirement</span></span> | <span data-ttu-id="ecd4f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ecd4f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd4f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecd4f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ecd4f-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecd4f-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ecd4f-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="ecd4f-121">Library</span></span><br/> | <dl> <span data-ttu-id="ecd4f-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecd4f-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ecd4f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecd4f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd4f-124">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="ecd4f-124">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




