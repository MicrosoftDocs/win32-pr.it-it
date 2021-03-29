---
title: Metodo ID3DX11EffectConstantBuffer SetConstantBuffer (D3dx11effect. h)
description: Impostare un buffer di costanti.
ms.assetid: 288e029a-e69a-4f58-be3f-8f9900c0e1dd
keywords:
- Metodo SetConstantBuffer Direct3D 11
- Metodo SetConstantBuffer Direct3D 11, interfaccia ID3DX11EffectConstantBuffer
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11, metodo SetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12249d9830ced43c3a56a2c8cf51942e66f6494e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235175"
---
# <a name="id3dx11effectconstantbuffersetconstantbuffer-method"></a><span data-ttu-id="55ba5-106">Metodo ID3DX11EffectConstantBuffer:: SetConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="55ba5-106">ID3DX11EffectConstantBuffer::SetConstantBuffer method</span></span>

<span data-ttu-id="55ba5-107">Impostare un buffer di costanti.</span><span class="sxs-lookup"><span data-stu-id="55ba5-107">Set a constant-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ba5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55ba5-108">Syntax</span></span>


```C++
HRESULT SetConstantBuffer(
   ID3D11Buffer *pConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="55ba5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="55ba5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ba5-110">*pConstantBuffer*</span><span class="sxs-lookup"><span data-stu-id="55ba5-110">*pConstantBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="55ba5-111">Tipo: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***</span><span class="sxs-lookup"><span data-stu-id="55ba5-111">Type: **[**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***</span></span>

<span data-ttu-id="55ba5-112">Puntatore a un'interfaccia del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="55ba5-112">A pointer to a constant-buffer interface.</span></span> <span data-ttu-id="55ba5-113">Vedere [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span><span class="sxs-lookup"><span data-stu-id="55ba5-113">See [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ba5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55ba5-114">Return value</span></span>

<span data-ttu-id="55ba5-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55ba5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55ba5-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="55ba5-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55ba5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="55ba5-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="55ba5-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="55ba5-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="55ba5-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="55ba5-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="55ba5-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="55ba5-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="55ba5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55ba5-121">Requirements</span></span>



| <span data-ttu-id="55ba5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="55ba5-122">Requirement</span></span> | <span data-ttu-id="55ba5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="55ba5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ba5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55ba5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="55ba5-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="55ba5-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="55ba5-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="55ba5-126">Library</span></span><br/> | <dl> <span data-ttu-id="55ba5-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="55ba5-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55ba5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55ba5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ba5-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="55ba5-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





