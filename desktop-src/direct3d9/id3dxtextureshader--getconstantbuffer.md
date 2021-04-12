---
description: Ottenere un puntatore alla tabella delle costanti.
ms.assetid: 5d836d99-783f-41e1-b7bf-d874d09a4892
title: 'Metodo ID3DXTextureShader:: GetConstantBuffer (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c83a723dde56fc80f643d7209c56fc05ad6cce5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354499"
---
# <a name="id3dxtextureshadergetconstantbuffer-method"></a><span data-ttu-id="debbb-103">Metodo ID3DXTextureShader:: GetConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="debbb-103">ID3DXTextureShader::GetConstantBuffer method</span></span>

<span data-ttu-id="debbb-104">Ottenere un puntatore alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="debbb-104">Get a pointer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="debbb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="debbb-105">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
  [out] LPD3DXBUFFER *ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="debbb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="debbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="debbb-107">*ppConstantBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="debbb-107">*ppConstantBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="debbb-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="debbb-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="debbb-109">Puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che contiene le costanti.</span><span class="sxs-lookup"><span data-stu-id="debbb-109">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains the constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="debbb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="debbb-110">Return value</span></span>

<span data-ttu-id="debbb-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="debbb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="debbb-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="debbb-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="debbb-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="debbb-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="debbb-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="debbb-114">Requirements</span></span>



| <span data-ttu-id="debbb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="debbb-115">Requirement</span></span> | <span data-ttu-id="debbb-116">Valore</span><span class="sxs-lookup"><span data-stu-id="debbb-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="debbb-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="debbb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="debbb-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="debbb-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="debbb-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="debbb-119">Library</span></span><br/> | <dl> <span data-ttu-id="debbb-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="debbb-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="debbb-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="debbb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="debbb-122">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="debbb-122">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




