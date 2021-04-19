---
description: Ottiene un puntatore al flusso DWORD della funzione.
ms.assetid: a051b51a-185c-4a9e-a8b9-4096615e2634
title: 'Metodo ID3DXTextureShader:: GetFunction (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetFunction
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80e504e65e4c8437247b2935794025e1b693433a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323356"
---
# <a name="id3dxtextureshadergetfunction-method"></a><span data-ttu-id="665f6-103">Metodo ID3DXTextureShader:: GetFunction</span><span class="sxs-lookup"><span data-stu-id="665f6-103">ID3DXTextureShader::GetFunction method</span></span>

<span data-ttu-id="665f6-104">Ottiene un puntatore al flusso DWORD della funzione.</span><span class="sxs-lookup"><span data-stu-id="665f6-104">Gets a pointer to the function DWORD stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="665f6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="665f6-105">Syntax</span></span>


```C++
HRESULT GetFunction(
  [in] LPD3DXBUFFER *ppFunction
);
```



## <a name="parameters"></a><span data-ttu-id="665f6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="665f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="665f6-107">*ppFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="665f6-107">*ppFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="665f6-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="665f6-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="665f6-109">Puntatore al flusso DWORD della funzione.</span><span class="sxs-lookup"><span data-stu-id="665f6-109">A pointer to the function DWORD stream.</span></span> <span data-ttu-id="665f6-110">Vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="665f6-110">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="665f6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="665f6-111">Return value</span></span>

<span data-ttu-id="665f6-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="665f6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="665f6-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="665f6-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="665f6-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="665f6-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="665f6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="665f6-115">Requirements</span></span>



| <span data-ttu-id="665f6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="665f6-116">Requirement</span></span> | <span data-ttu-id="665f6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="665f6-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="665f6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="665f6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="665f6-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="665f6-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="665f6-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="665f6-120">Library</span></span><br/> | <dl> <span data-ttu-id="665f6-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="665f6-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="665f6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="665f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="665f6-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="665f6-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




