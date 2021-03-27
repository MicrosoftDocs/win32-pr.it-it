---
title: Metodo ID3DX11EffectPass IsValid (D3dx11effect. h)
description: Testare un passaggio per verificare se contiene una sintassi valida.
ms.assetid: 3c6ddcef-1303-4161-889c-c3ca271b6ad0
keywords:
- Metodo IsValid-Direct3D 11
- Metodo IsValid, Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50db900d3cea82197fb56ce3a57a5a548220ca1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982244"
---
# <a name="id3dx11effectpassisvalid-method"></a><span data-ttu-id="da9b6-106">Metodo ID3DX11EffectPass:: IsValid</span><span class="sxs-lookup"><span data-stu-id="da9b6-106">ID3DX11EffectPass::IsValid method</span></span>

<span data-ttu-id="da9b6-107">Testare un passaggio per verificare se contiene una sintassi valida.</span><span class="sxs-lookup"><span data-stu-id="da9b6-107">Test a pass to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="da9b6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da9b6-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="da9b6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="da9b6-109">Parameters</span></span>

<span data-ttu-id="da9b6-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="da9b6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da9b6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da9b6-111">Return value</span></span>

<span data-ttu-id="da9b6-112">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="da9b6-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="da9b6-113">**True** se la sintassi del codice è valida. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="da9b6-113">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="da9b6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="da9b6-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="da9b6-115">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="da9b6-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="da9b6-116">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="da9b6-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="da9b6-117">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="da9b6-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="da9b6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da9b6-118">Requirements</span></span>



| <span data-ttu-id="da9b6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="da9b6-119">Requirement</span></span> | <span data-ttu-id="da9b6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="da9b6-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da9b6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da9b6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="da9b6-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="da9b6-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="da9b6-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="da9b6-123">Library</span></span><br/> | <dl> <span data-ttu-id="da9b6-124"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="da9b6-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da9b6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da9b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9b6-126">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="da9b6-126">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

