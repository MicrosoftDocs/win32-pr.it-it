---
title: Metodo Optimize ID3DX11Effect (D3dx11effect. h)
description: Ridurre al minimo la quantità di memoria necessaria per un effetto.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Metodo Optimize Direct3D 11
- Metodo Optimize Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, Metodo Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996089"
---
# <a name="id3dx11effectoptimize-method"></a><span data-ttu-id="307f9-106">Metodo ID3DX11Effect:: Optimize</span><span class="sxs-lookup"><span data-stu-id="307f9-106">ID3DX11Effect::Optimize method</span></span>

<span data-ttu-id="307f9-107">Ridurre al minimo la quantità di memoria necessaria per un effetto.</span><span class="sxs-lookup"><span data-stu-id="307f9-107">Minimize the amount of memory required for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="307f9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="307f9-108">Syntax</span></span>


```C++
HRESULT Optimize();
```



## <a name="parameters"></a><span data-ttu-id="307f9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="307f9-109">Parameters</span></span>

<span data-ttu-id="307f9-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="307f9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="307f9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="307f9-111">Return value</span></span>

<span data-ttu-id="307f9-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="307f9-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="307f9-113">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="307f9-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="307f9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="307f9-114">Remarks</span></span>

<span data-ttu-id="307f9-115">Un effetto usa uno spazio di memoria in due modi diversi: per archiviare le informazioni richieste dal runtime per eseguire un effetto e per archiviare i metadati necessari per riportare le informazioni a un'applicazione usando l'API.</span><span class="sxs-lookup"><span data-stu-id="307f9-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="307f9-116">È possibile ridurre al minimo la quantità di memoria necessaria per un effetto chiamando **ID3DX11Effect:: Optimize** che rimuove i metadati della reflection dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="307f9-116">You can minimize the amount of memory required by an effect by calling **ID3DX11Effect::Optimize** which removes the reflection metadata from memory.</span></span> <span data-ttu-id="307f9-117">I metodi API per leggere le variabili non funzioneranno più dopo la rimozione dei dati di Reflection.</span><span class="sxs-lookup"><span data-stu-id="307f9-117">API methods to read variables will no longer work once reflection data has been removed.</span></span>

<span data-ttu-id="307f9-118">I metodi seguenti avranno esito negativo dopo la chiamata di optimize su un effetto.</span><span class="sxs-lookup"><span data-stu-id="307f9-118">The following methods will fail after Optimize has been called on an effect.</span></span>

-   [<span data-ttu-id="307f9-119">**ID3DX11Effect::GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="307f9-119">**ID3DX11Effect::GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md)
-   [<span data-ttu-id="307f9-120">**ID3DX11Effect::GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="307f9-120">**ID3DX11Effect::GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)
-   [<span data-ttu-id="307f9-121">**ID3DX11Effect:: getdesc**</span><span class="sxs-lookup"><span data-stu-id="307f9-121">**ID3DX11Effect::GetDesc**</span></span>](id3dx11effect-getdesc.md)
-   [<span data-ttu-id="307f9-122">**ID3DX11Effect:: GetDevice**</span><span class="sxs-lookup"><span data-stu-id="307f9-122">**ID3DX11Effect::GetDevice**</span></span>](id3dx11effect-getdevice.md)
-   [<span data-ttu-id="307f9-123">**ID3DX11Effect::GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="307f9-123">**ID3DX11Effect::GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)
-   [<span data-ttu-id="307f9-124">**ID3DX11Effect::GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="307f9-124">**ID3DX11Effect::GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)
-   [<span data-ttu-id="307f9-125">**ID3DX11Effect::GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="307f9-125">**ID3DX11Effect::GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)
-   [<span data-ttu-id="307f9-126">**ID3DX11Effect::GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="307f9-126">**ID3DX11Effect::GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)
-   [<span data-ttu-id="307f9-127">**ID3DX11Effect::GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="307f9-127">**ID3DX11Effect::GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> <span data-ttu-id="307f9-128">I riferimenti recuperati con questi metodi prima di chiamare **ID3DX11Effect:: Optimize** sono ancora validi dopo la chiamata a **ID3DX11Effect:: Optimize** .</span><span class="sxs-lookup"><span data-stu-id="307f9-128">References retrieved with these methods before calling **ID3DX11Effect::Optimize** are still valid after **ID3DX11Effect::Optimize** is called.</span></span> <span data-ttu-id="307f9-129">Ciò consente all'applicazione di ottenere tutte le variabili, le tecniche e le passate che utilizzeranno, chiamare optimize e quindi usare l'effetto.</span><span class="sxs-lookup"><span data-stu-id="307f9-129">This allows the application to get all the variables, techniques, and passes it will use, call Optimize, and then use the effect.</span></span>

 

> [!Note]  
> <span data-ttu-id="307f9-130">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="307f9-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="307f9-131">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="307f9-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="307f9-132">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="307f9-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="307f9-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="307f9-133">Requirements</span></span>



| <span data-ttu-id="307f9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="307f9-134">Requirement</span></span> | <span data-ttu-id="307f9-135">Valore</span><span class="sxs-lookup"><span data-stu-id="307f9-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307f9-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="307f9-136">Header</span></span><br/>  | <dl> <span data-ttu-id="307f9-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="307f9-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="307f9-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="307f9-138">Library</span></span><br/> | <dl> <span data-ttu-id="307f9-139"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="307f9-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="307f9-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="307f9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="307f9-141">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="307f9-141">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





