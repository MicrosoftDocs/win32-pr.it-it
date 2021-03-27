---
title: Metodo ID3DX11EffectGroup IsValid (D3dx11effect. h)
description: Testare un effetto per verificare se contiene una sintassi valida. | Metodo ID3DX11EffectGroup IsValid (D3dx11effect. h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- Metodo IsValid-Direct3D 11
- Metodo IsValid, Direct3D 11, interfaccia ID3DX11EffectGroup
- Interfaccia ID3DX11EffectGroup Direct3D 11, metodo IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d1fd110a0f35f8a288517d72b69a6f5ad9f0ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982283"
---
# <a name="id3dx11effectgroupisvalid-method"></a><span data-ttu-id="740c9-107">Metodo ID3DX11EffectGroup:: IsValid</span><span class="sxs-lookup"><span data-stu-id="740c9-107">ID3DX11EffectGroup::IsValid method</span></span>

<span data-ttu-id="740c9-108">Testare un effetto per verificare se contiene una sintassi valida.</span><span class="sxs-lookup"><span data-stu-id="740c9-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="740c9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="740c9-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="740c9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="740c9-110">Parameters</span></span>

<span data-ttu-id="740c9-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="740c9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="740c9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="740c9-112">Return value</span></span>

<span data-ttu-id="740c9-113">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="740c9-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="740c9-114">**True** se la sintassi del codice è valida. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="740c9-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="740c9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="740c9-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="740c9-116">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="740c9-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="740c9-117">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="740c9-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="740c9-118">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="740c9-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="740c9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="740c9-119">Requirements</span></span>



| <span data-ttu-id="740c9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="740c9-120">Requirement</span></span> | <span data-ttu-id="740c9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="740c9-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="740c9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="740c9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="740c9-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="740c9-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="740c9-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="740c9-124">Library</span></span><br/> | <dl> <span data-ttu-id="740c9-125"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="740c9-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="740c9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="740c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="740c9-127">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="740c9-127">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

