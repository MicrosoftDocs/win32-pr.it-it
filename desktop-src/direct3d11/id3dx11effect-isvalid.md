---
title: Metodo ID3DX11Effect IsValid (D3dx11effect. h)
description: Testare un effetto per verificare se contiene una sintassi valida. | Metodo ID3DX11Effect IsValid (D3dx11effect. h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- Metodo IsValid-Direct3D 11
- Metodo IsValid, Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo IsValid
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88aef9e3864fc77380b3459860178c8537a6a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996092"
---
# <a name="id3dx11effectisvalid-method"></a><span data-ttu-id="11627-107">Metodo ID3DX11Effect:: IsValid</span><span class="sxs-lookup"><span data-stu-id="11627-107">ID3DX11Effect::IsValid method</span></span>

<span data-ttu-id="11627-108">Testare un effetto per verificare se contiene una sintassi valida.</span><span class="sxs-lookup"><span data-stu-id="11627-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="11627-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11627-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="11627-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="11627-110">Parameters</span></span>

<span data-ttu-id="11627-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="11627-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11627-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11627-112">Return value</span></span>

<span data-ttu-id="11627-113">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="11627-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="11627-114">**True** se la sintassi del codice è valida. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="11627-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="11627-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="11627-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="11627-116">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="11627-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="11627-117">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="11627-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="11627-118">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="11627-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11627-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11627-119">Requirements</span></span>



| <span data-ttu-id="11627-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="11627-120">Requirement</span></span> | <span data-ttu-id="11627-121">Valore</span><span class="sxs-lookup"><span data-stu-id="11627-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11627-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11627-122">Header</span></span><br/>  | <dl> <span data-ttu-id="11627-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="11627-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="11627-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="11627-124">Library</span></span><br/> | <dl> <span data-ttu-id="11627-125"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="11627-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11627-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11627-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11627-127">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="11627-127">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

