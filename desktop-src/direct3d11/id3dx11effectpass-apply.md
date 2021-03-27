---
title: Metodo Apply ID3DX11EffectPass (D3dx11effect. h)
description: Impostare lo stato contenuto in un passaggio al dispositivo.
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Applicare il metodo Direct3D 11
- Apply Method Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo Apply
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a061609953e164524e16722222a5ecea81f275b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982250"
---
# <a name="id3dx11effectpassapply-method"></a><span data-ttu-id="9435e-106">Metodo ID3DX11EffectPass:: Apply</span><span class="sxs-lookup"><span data-stu-id="9435e-106">ID3DX11EffectPass::Apply method</span></span>

<span data-ttu-id="9435e-107">Impostare lo stato contenuto in un passaggio al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9435e-107">Set the state contained in a pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9435e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9435e-108">Syntax</span></span>


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="9435e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9435e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9435e-110">*Flag*</span><span class="sxs-lookup"><span data-stu-id="9435e-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="9435e-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9435e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9435e-112">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="9435e-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="9435e-113">*pContext*</span><span class="sxs-lookup"><span data-stu-id="9435e-113">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="9435e-114">Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="9435e-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="9435e-115">[**Sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a cui applicare il passaggio.</span><span class="sxs-lookup"><span data-stu-id="9435e-115">The [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) to apply the pass to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9435e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9435e-116">Return value</span></span>

<span data-ttu-id="9435e-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9435e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9435e-118">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9435e-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9435e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="9435e-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9435e-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="9435e-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9435e-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="9435e-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9435e-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9435e-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9435e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9435e-123">Requirements</span></span>



| <span data-ttu-id="9435e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9435e-124">Requirement</span></span> | <span data-ttu-id="9435e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9435e-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9435e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9435e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9435e-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9435e-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9435e-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="9435e-128">Library</span></span><br/> | <dl> <span data-ttu-id="9435e-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="9435e-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9435e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9435e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9435e-131">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="9435e-131">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

