---
title: Metodo ID3DX11EffectInterfaceVariable GetClassInstance (D3dx11effect. h)
description: Ottenere un'istanza della classe.
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- Metodo GetClassInstance Direct3D 11
- Metodo GetClassInstance Direct3D 11, interfaccia ID3DX11EffectInterfaceVariable
- Interfaccia ID3DX11EffectInterfaceVariable Direct3D 11, metodo GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f729da6ee84d76dd37a40a7946438e367c1a4cbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969419"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a><span data-ttu-id="08bed-106">Metodo ID3DX11EffectInterfaceVariable:: GetClassInstance</span><span class="sxs-lookup"><span data-stu-id="08bed-106">ID3DX11EffectInterfaceVariable::GetClassInstance method</span></span>

<span data-ttu-id="08bed-107">Ottenere un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="08bed-107">Get a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="08bed-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08bed-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="08bed-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="08bed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08bed-110">*ppEffectClassInstance*</span><span class="sxs-lookup"><span data-stu-id="08bed-110">*ppEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="08bed-111">Tipo: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="08bed-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span></span>

<span data-ttu-id="08bed-112">Puntatore a un puntatore [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) che verrà impostato sull'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="08bed-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) pointer that will be set to the class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08bed-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08bed-113">Return value</span></span>

<span data-ttu-id="08bed-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08bed-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08bed-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="08bed-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="08bed-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="08bed-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="08bed-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="08bed-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="08bed-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="08bed-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="08bed-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="08bed-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08bed-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08bed-120">Requirements</span></span>



| <span data-ttu-id="08bed-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="08bed-121">Requirement</span></span> | <span data-ttu-id="08bed-122">Valore</span><span class="sxs-lookup"><span data-stu-id="08bed-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08bed-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08bed-123">Header</span></span><br/>  | <dl> <span data-ttu-id="08bed-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="08bed-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="08bed-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="08bed-125">Library</span></span><br/> | <dl> <span data-ttu-id="08bed-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="08bed-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08bed-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08bed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bed-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="08bed-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





