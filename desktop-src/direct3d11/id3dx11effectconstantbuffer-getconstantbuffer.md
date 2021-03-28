---
title: Metodo ID3DX11EffectConstantBuffer GetConstantBuffer (D3dx11effect. h)
description: Ottenere un buffer costante.
ms.assetid: 857b3dc2-41ae-4a52-904a-9ca8f0afeb9e
keywords:
- Metodo GetConstantBuffer Direct3D 11
- Metodo GetConstantBuffer Direct3D 11, interfaccia ID3DX11EffectConstantBuffer
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11, metodo GetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041ca2fea028cb86d0959313bae73c320e6e5a36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058693"
---
# <a name="id3dx11effectconstantbuffergetconstantbuffer-method"></a><span data-ttu-id="1af4b-106">Metodo ID3DX11EffectConstantBuffer:: GetConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="1af4b-106">ID3DX11EffectConstantBuffer::GetConstantBuffer method</span></span>

<span data-ttu-id="1af4b-107">Ottenere un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="1af4b-107">Get a constant-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af4b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1af4b-108">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
   ID3D11Buffer **ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="1af4b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1af4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af4b-110">*ppConstantBuffer*</span><span class="sxs-lookup"><span data-stu-id="1af4b-110">*ppConstantBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="1af4b-111">Tipo: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="1af4b-111">Type: **[**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span></span>

<span data-ttu-id="1af4b-112">Indirizzo di un puntatore a un'interfaccia del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="1af4b-112">The address of a pointer to a constant-buffer interface.</span></span> <span data-ttu-id="1af4b-113">Vedere [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span><span class="sxs-lookup"><span data-stu-id="1af4b-113">See [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af4b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1af4b-114">Return value</span></span>

<span data-ttu-id="1af4b-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1af4b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1af4b-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1af4b-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1af4b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1af4b-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1af4b-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="1af4b-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1af4b-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="1af4b-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1af4b-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1af4b-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1af4b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1af4b-121">Requirements</span></span>



| <span data-ttu-id="1af4b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af4b-122">Requirement</span></span> | <span data-ttu-id="1af4b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1af4b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1af4b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1af4b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1af4b-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1af4b-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1af4b-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="1af4b-126">Library</span></span><br/> | <dl> <span data-ttu-id="1af4b-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="1af4b-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af4b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1af4b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af4b-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="1af4b-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





