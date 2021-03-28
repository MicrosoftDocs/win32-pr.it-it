---
title: Metodo ID3DX11Effect CloneEffect (D3dx11effect. h)
description: Crea una copia di un'interfaccia effetto.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Metodo CloneEffect Direct3D 11
- Metodo CloneEffect Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo CloneEffect
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982603"
---
# <a name="id3dx11effectcloneeffect-method"></a><span data-ttu-id="e3a12-106">Metodo ID3DX11Effect:: CloneEffect</span><span class="sxs-lookup"><span data-stu-id="e3a12-106">ID3DX11Effect::CloneEffect method</span></span>

<span data-ttu-id="e3a12-107">Crea una copia di un'interfaccia effetto.</span><span class="sxs-lookup"><span data-stu-id="e3a12-107">Creates a copy of an effect interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a12-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3a12-108">Syntax</span></span>


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a><span data-ttu-id="e3a12-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3a12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a12-110">*Flag*</span><span class="sxs-lookup"><span data-stu-id="e3a12-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a12-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3a12-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e3a12-112">Flag che influiscono sulla creazione dell'effetto clonato.</span><span class="sxs-lookup"><span data-stu-id="e3a12-112">Flags affecting the creation of the cloned effect.</span></span> <span data-ttu-id="e3a12-113">Può essere 0 o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e3a12-113">Can be 0 or one of the following values.</span></span>



| <span data-ttu-id="e3a12-114">Flag</span><span class="sxs-lookup"><span data-stu-id="e3a12-114">Flag</span></span>                                    | <span data-ttu-id="e3a12-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3a12-115">Description</span></span>                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a12-116">\_Clone effetto \_ D3DX11 \_ forza non \_ singolo</span><span class="sxs-lookup"><span data-stu-id="e3a12-116">D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE</span></span> | <span data-ttu-id="e3a12-117">Ignora tutti i qualificatori "single" in cBuffers.</span><span class="sxs-lookup"><span data-stu-id="e3a12-117">Ignore all "single" qualifiers on cbuffers.</span></span> <span data-ttu-id="e3a12-118">Tutti i cBuffers avranno i propri [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)creati nell'effetto clonato.</span><span class="sxs-lookup"><span data-stu-id="e3a12-118">All cbuffers will have their own [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s created in the cloned effect.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e3a12-119">*ppClonedEffect*</span><span class="sxs-lookup"><span data-stu-id="e3a12-119">*ppClonedEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a12-120">Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e3a12-120">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="e3a12-121">Puntatore a un puntatore [**ID3DX11Effect**](id3dx11effect.md) che verrà impostato sulla copia dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="e3a12-121">Pointer to an [**ID3DX11Effect**](id3dx11effect.md) pointer that will be set to the copy of the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a12-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3a12-122">Return value</span></span>

<span data-ttu-id="e3a12-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3a12-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3a12-124">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e3a12-124">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a12-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3a12-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e3a12-126">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e3a12-126">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e3a12-127">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e3a12-127">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e3a12-128">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e3a12-128">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3a12-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3a12-129">Requirements</span></span>



| <span data-ttu-id="e3a12-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a12-130">Requirement</span></span> | <span data-ttu-id="e3a12-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e3a12-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a12-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3a12-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e3a12-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a12-133"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e3a12-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3a12-134">Library</span></span><br/> | <dl> <span data-ttu-id="e3a12-135"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="e3a12-135"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a12-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3a12-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a12-137">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="e3a12-137">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

