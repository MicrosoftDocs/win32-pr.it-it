---
title: Metodo ID3DX11Effect ottimizzato (D3dx11effect. h)
description: Testare un effetto per verificare se i metadati della reflection sono stati rimossi dalla memoria.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Metodo di ottimizzazione Direct3D 11
- Metodo optimized Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo di ottimizzazione
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355539"
---
# <a name="id3dx11effectisoptimized-method"></a><span data-ttu-id="3a0b2-106">Metodo ID3DX11Effect:: optimized</span><span class="sxs-lookup"><span data-stu-id="3a0b2-106">ID3DX11Effect::IsOptimized method</span></span>

<span data-ttu-id="3a0b2-107">Testare un effetto per verificare se i metadati della reflection sono stati rimossi dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="3a0b2-107">Test an effect to see if the reflection metadata has been removed from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0b2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a0b2-108">Syntax</span></span>


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a><span data-ttu-id="3a0b2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a0b2-109">Parameters</span></span>

<span data-ttu-id="3a0b2-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3a0b2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a0b2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a0b2-111">Return value</span></span>

<span data-ttu-id="3a0b2-112">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3a0b2-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3a0b2-113">**True** se l'effetto è ottimizzato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3a0b2-113">**TRUE** if the effect is optimized; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a0b2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a0b2-114">Remarks</span></span>

<span data-ttu-id="3a0b2-115">Un effetto usa uno spazio di memoria in due modi diversi: per archiviare le informazioni richieste dal runtime per eseguire un effetto e per archiviare i metadati necessari per riportare le informazioni a un'applicazione usando l'API.</span><span class="sxs-lookup"><span data-stu-id="3a0b2-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="3a0b2-116">È possibile ridurre al minimo la quantità di memoria necessaria per un effetto chiamando [**ID3DX11Effect:: Optimize**](id3dx11effect-optimize.md) che rimuove i metadati della reflection dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="3a0b2-116">You can minimize the amount of memory required by an effect by calling [**ID3DX11Effect::Optimize**](id3dx11effect-optimize.md) which removes the reflection metadata from memory.</span></span> <span data-ttu-id="3a0b2-117">Naturalmente, i metodi API per leggere le variabili non funzioneranno più dopo la rimozione dei dati di Reflection.</span><span class="sxs-lookup"><span data-stu-id="3a0b2-117">Of course, API methods to read variables will no longer work once reflection data has been removed.</span></span>

> [!Note]  
> <span data-ttu-id="3a0b2-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="3a0b2-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3a0b2-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3a0b2-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3a0b2-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3a0b2-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a0b2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a0b2-121">Requirements</span></span>



| <span data-ttu-id="3a0b2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a0b2-122">Requirement</span></span> | <span data-ttu-id="3a0b2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3a0b2-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0b2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a0b2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3a0b2-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a0b2-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3a0b2-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="3a0b2-126">Library</span></span><br/> | <dl> <span data-ttu-id="3a0b2-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="3a0b2-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0b2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a0b2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0b2-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="3a0b2-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

