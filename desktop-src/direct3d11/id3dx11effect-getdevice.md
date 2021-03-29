---
title: Metodo GetDevice ID3DX11Effect (D3dx11effect. h)
description: Ottenere il dispositivo che ha creato l'effetto.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Metodo GetDevice Direct3D 11
- Metodo GetDevice Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetDevice
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235150"
---
# <a name="id3dx11effectgetdevice-method"></a><span data-ttu-id="c73bf-106">Metodo ID3DX11Effect:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="c73bf-106">ID3DX11Effect::GetDevice method</span></span>

<span data-ttu-id="c73bf-107">Ottenere il dispositivo che ha creato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="c73bf-107">Get the device that created the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="c73bf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c73bf-108">Syntax</span></span>


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="c73bf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c73bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c73bf-110">*ppDevice*</span><span class="sxs-lookup"><span data-stu-id="c73bf-110">*ppDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c73bf-111">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span><span class="sxs-lookup"><span data-stu-id="c73bf-111">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span></span>

<span data-ttu-id="c73bf-112">Puntatore a un [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span><span class="sxs-lookup"><span data-stu-id="c73bf-112">A pointer to an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c73bf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c73bf-113">Return value</span></span>

<span data-ttu-id="c73bf-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c73bf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c73bf-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c73bf-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c73bf-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c73bf-116">Remarks</span></span>

<span data-ttu-id="c73bf-117">Viene creato un effetto per un dispositivo specifico, chiamando una funzione come [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="c73bf-117">An effect is created for a specific device, by calling a function such as [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

> [!Note]  
> <span data-ttu-id="c73bf-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c73bf-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c73bf-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c73bf-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c73bf-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c73bf-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c73bf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c73bf-121">Requirements</span></span>



| <span data-ttu-id="c73bf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c73bf-122">Requirement</span></span> | <span data-ttu-id="c73bf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c73bf-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c73bf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c73bf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c73bf-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c73bf-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c73bf-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c73bf-126">Library</span></span><br/> | <dl> <span data-ttu-id="c73bf-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c73bf-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c73bf-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c73bf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c73bf-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="c73bf-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





