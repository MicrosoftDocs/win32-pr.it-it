---
title: Metodo ID3DX11EffectClassInstanceVariable GetClassInstance (D3dx11effect. h)
description: Ottiene un'istanza della classe.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Metodo GetClassInstance Direct3D 11
- Metodo GetClassInstance Direct3D 11, interfaccia ID3DX11EffectClassInstanceVariable
- Interfaccia ID3DX11EffectClassInstanceVariable Direct3D 11, metodo GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dae96d42a0088adc683ca93d7e3215c12912a87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356039"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a><span data-ttu-id="bbf49-106">Metodo ID3DX11EffectClassInstanceVariable:: GetClassInstance</span><span class="sxs-lookup"><span data-stu-id="bbf49-106">ID3DX11EffectClassInstanceVariable::GetClassInstance method</span></span>

<span data-ttu-id="bbf49-107">Ottiene un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="bbf49-107">Gets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf49-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbf49-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="bbf49-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbf49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf49-110">*ppClassInstance*</span><span class="sxs-lookup"><span data-stu-id="bbf49-110">*ppClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf49-111">Tipo: **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span><span class="sxs-lookup"><span data-stu-id="bbf49-111">Type: **[**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span></span>

<span data-ttu-id="bbf49-112">Puntatore a un puntatore [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) che verrà impostato sull'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="bbf49-112">Pointer to an [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointer that will be set to class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf49-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbf49-113">Return value</span></span>

<span data-ttu-id="bbf49-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bbf49-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bbf49-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bbf49-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf49-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbf49-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bbf49-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="bbf49-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bbf49-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="bbf49-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bbf49-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bbf49-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bbf49-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbf49-120">Requirements</span></span>



| <span data-ttu-id="bbf49-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbf49-121">Requirement</span></span> | <span data-ttu-id="bbf49-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bbf49-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf49-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbf49-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bbf49-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf49-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bbf49-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="bbf49-125">Library</span></span><br/> | <dl> <span data-ttu-id="bbf49-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="bbf49-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf49-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbf49-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf49-128">ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="bbf49-128">ID3DX11EffectClassInstanceVariable</span></span>](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





