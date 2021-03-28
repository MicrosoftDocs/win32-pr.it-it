---
title: Metodo ID3DX11EffectVariable IsValid (D3dx11effect. h)
description: Confrontare il tipo di dati con i dati archiviati.
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- Metodo IsValid-Direct3D 11
- Metodo IsValid, Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5136005e675a6f5e54cc3863ef2d80ffadfb7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996137"
---
# <a name="id3dx11effectvariableisvalid-method"></a><span data-ttu-id="5e9cf-106">Metodo ID3DX11EffectVariable:: IsValid</span><span class="sxs-lookup"><span data-stu-id="5e9cf-106">ID3DX11EffectVariable::IsValid method</span></span>

<span data-ttu-id="5e9cf-107">Confrontare il tipo di dati con i dati archiviati.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-107">Compare the data type with the data stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e9cf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e9cf-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="5e9cf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e9cf-109">Parameters</span></span>

<span data-ttu-id="5e9cf-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e9cf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e9cf-111">Return value</span></span>

<span data-ttu-id="5e9cf-112">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5e9cf-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5e9cf-113">**True** se la sintassi è valida. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-113">**TRUE** if the syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e9cf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e9cf-114">Remarks</span></span>

<span data-ttu-id="5e9cf-115">Questo metodo verifica che il tipo di dati corrisponda ai dati archiviati dopo il cast di un'interfaccia a un'altra (usando uno dei metodi As).</span><span class="sxs-lookup"><span data-stu-id="5e9cf-115">This method checks that the data type matches the data stored after casting one interface to another (using any of the As methods).</span></span>

> [!Note]  
> <span data-ttu-id="5e9cf-116">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5e9cf-117">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5e9cf-118">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5e9cf-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e9cf-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e9cf-119">Requirements</span></span>



| <span data-ttu-id="5e9cf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e9cf-120">Requirement</span></span> | <span data-ttu-id="5e9cf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5e9cf-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e9cf-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e9cf-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5e9cf-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e9cf-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5e9cf-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e9cf-124">Library</span></span><br/> | <dl> <span data-ttu-id="5e9cf-125"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="5e9cf-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e9cf-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e9cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9cf-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="5e9cf-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

