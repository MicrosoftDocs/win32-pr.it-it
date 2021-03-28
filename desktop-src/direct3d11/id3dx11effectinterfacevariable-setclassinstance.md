---
title: Metodo ID3DX11EffectInterfaceVariable SetClassInstance (D3dx11effect. h)
description: Imposta un'istanza della classe.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Metodo SetClassInstance Direct3D 11
- Metodo SetClassInstance Direct3D 11, interfaccia ID3DX11EffectInterfaceVariable
- Interfaccia ID3DX11EffectInterfaceVariable Direct3D 11, metodo SetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982274"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a><span data-ttu-id="f23ef-106">Metodo ID3DX11EffectInterfaceVariable:: SetClassInstance</span><span class="sxs-lookup"><span data-stu-id="f23ef-106">ID3DX11EffectInterfaceVariable::SetClassInstance method</span></span>

<span data-ttu-id="f23ef-107">Imposta un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="f23ef-107">Sets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f23ef-108">Syntax</span></span>


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="f23ef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f23ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f23ef-110">*pEffectClassInstance*</span><span class="sxs-lookup"><span data-stu-id="f23ef-110">*pEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f23ef-111">Tipo: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="f23ef-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="f23ef-112">Puntatore a un'interfaccia [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) .</span><span class="sxs-lookup"><span data-stu-id="f23ef-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f23ef-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f23ef-113">Return value</span></span>

<span data-ttu-id="f23ef-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f23ef-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f23ef-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f23ef-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f23ef-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f23ef-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f23ef-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="f23ef-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f23ef-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f23ef-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f23ef-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f23ef-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f23ef-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f23ef-120">Requirements</span></span>



| <span data-ttu-id="f23ef-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f23ef-121">Requirement</span></span> | <span data-ttu-id="f23ef-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f23ef-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f23ef-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f23ef-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f23ef-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f23ef-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f23ef-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f23ef-125">Library</span></span><br/> | <dl> <span data-ttu-id="f23ef-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="f23ef-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23ef-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f23ef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23ef-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="f23ef-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





