---
description: Moltiplica ogni valore nel buffer per un valore costante.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'Metodo ID3DXPRTBuffer:: ScaleBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05bdd066f4b7c33ad06f089551f16f0489608c83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323697"
---
# <a name="id3dxprtbufferscalebuffer-method"></a><span data-ttu-id="55b0d-103">Metodo ID3DXPRTBuffer:: ScaleBuffer</span><span class="sxs-lookup"><span data-stu-id="55b0d-103">ID3DXPRTBuffer::ScaleBuffer method</span></span>

<span data-ttu-id="55b0d-104">Moltiplica ogni valore nel buffer per un valore costante.</span><span class="sxs-lookup"><span data-stu-id="55b0d-104">Multiplies every value in the buffer by a constant value.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b0d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55b0d-105">Syntax</span></span>


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="55b0d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="55b0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b0d-107">*Ridimensiona* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55b0d-107">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b0d-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55b0d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55b0d-109">Valore costante utilizzato per ridimensionare il buffer.</span><span class="sxs-lookup"><span data-stu-id="55b0d-109">Constant value used to scale the buffer.</span></span> <span data-ttu-id="55b0d-110">Ogni valore nel buffer viene sostituito dal prodotto di questo valore e dal valore del buffer originale.</span><span class="sxs-lookup"><span data-stu-id="55b0d-110">Every value in the buffer is replaced by the product of this value and the original buffer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b0d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55b0d-111">Return value</span></span>

<span data-ttu-id="55b0d-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55b0d-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55b0d-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55b0d-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="55b0d-114">Se il metodo ha esito negativo, verrà restituito il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="55b0d-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b0d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55b0d-115">Requirements</span></span>



| <span data-ttu-id="55b0d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b0d-116">Requirement</span></span> | <span data-ttu-id="55b0d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="55b0d-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b0d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55b0d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="55b0d-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b0d-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="55b0d-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="55b0d-120">Library</span></span><br/> | <dl> <span data-ttu-id="55b0d-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55b0d-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="55b0d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55b0d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b0d-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="55b0d-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
