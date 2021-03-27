---
title: Metodo ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessView (D3dx11effect. h)
description: Ottenere una visualizzazione di accesso non ordinato.
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- Metodo GetUnorderedAccessView Direct3D 11
- Metodo GetUnorderedAccessView Direct3D 11, interfaccia ID3DX11EffectUnorderedAccessViewVariable
- Interfaccia ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, metodo GetUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7743d15c2380ff4e38bdcae1d38bbd8905cbccda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996185"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a><span data-ttu-id="800ca-106">Metodo ID3DX11EffectUnorderedAccessViewVariable:: GetUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="800ca-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessView method</span></span>

<span data-ttu-id="800ca-107">Ottenere una visualizzazione di accesso non ordinato.</span><span class="sxs-lookup"><span data-stu-id="800ca-107">Get an unordered-access-view.</span></span>

## <a name="syntax"></a><span data-ttu-id="800ca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="800ca-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="800ca-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="800ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="800ca-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="800ca-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="800ca-111">Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="800ca-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="800ca-112">Puntatore a un puntatore [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) che verrà impostato al ritorno.</span><span class="sxs-lookup"><span data-stu-id="800ca-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="800ca-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="800ca-113">Return value</span></span>

<span data-ttu-id="800ca-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="800ca-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="800ca-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="800ca-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="800ca-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="800ca-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="800ca-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="800ca-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="800ca-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="800ca-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="800ca-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="800ca-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="800ca-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="800ca-120">Requirements</span></span>



| <span data-ttu-id="800ca-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="800ca-121">Requirement</span></span> | <span data-ttu-id="800ca-122">Valore</span><span class="sxs-lookup"><span data-stu-id="800ca-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800ca-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="800ca-123">Header</span></span><br/>  | <dl> <span data-ttu-id="800ca-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="800ca-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="800ca-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="800ca-125">Library</span></span><br/> | <dl> <span data-ttu-id="800ca-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="800ca-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="800ca-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="800ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="800ca-128">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="800ca-128">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





