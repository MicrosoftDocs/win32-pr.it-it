---
title: Metodo GetBool ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Ottenere una variabile booleana.
ms.assetid: 9d2789af-c59f-4d2d-87c6-9f36286e8a15
keywords:
- Metodo GetBool Direct3D 11
- Metodo GetBool Direct3D 11, interfaccia ID3DX11EffectScalarVariable
- Interfaccia ID3DX11EffectScalarVariable Direct3D 11, Metodo GetBool
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 754dd8856876ca441e83267250dcfad4f4011c69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762322"
---
# <a name="id3dx11effectscalarvariablegetbool-method"></a><span data-ttu-id="0a027-106">Metodo ID3DX11EffectScalarVariable:: GetBool</span><span class="sxs-lookup"><span data-stu-id="0a027-106">ID3DX11EffectScalarVariable::GetBool method</span></span>

<span data-ttu-id="0a027-107">Ottenere una variabile booleana.</span><span class="sxs-lookup"><span data-stu-id="0a027-107">Get a boolean variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a027-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a027-108">Syntax</span></span>


```C++
HRESULT GetBool(
   BOOL *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="0a027-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a027-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a027-110">*pValue*</span><span class="sxs-lookup"><span data-stu-id="0a027-110">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="0a027-111">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="0a027-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="0a027-112">Puntatore alla variabile.</span><span class="sxs-lookup"><span data-stu-id="0a027-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a027-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a027-113">Return value</span></span>

<span data-ttu-id="0a027-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a027-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a027-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0a027-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a027-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a027-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0a027-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="0a027-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0a027-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="0a027-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0a027-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0a027-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a027-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a027-120">Requirements</span></span>



| <span data-ttu-id="0a027-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a027-121">Requirement</span></span> | <span data-ttu-id="0a027-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0a027-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a027-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a027-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0a027-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a027-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0a027-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a027-125">Library</span></span><br/> | <dl> <span data-ttu-id="0a027-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="0a027-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a027-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a027-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a027-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="0a027-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

