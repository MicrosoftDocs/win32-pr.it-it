---
title: Metodo ID3DX11Effect GetConstantBufferByIndex (D3dx11effect. h)
description: Ottenere un buffer costante in base all'indice.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Metodo GetConstantBufferByIndex Direct3D 11
- Metodo GetConstantBufferByIndex Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetConstantBufferByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982424"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a><span data-ttu-id="c0bb2-106">Metodo ID3DX11Effect:: GetConstantBufferByIndex</span><span class="sxs-lookup"><span data-stu-id="c0bb2-106">ID3DX11Effect::GetConstantBufferByIndex method</span></span>

<span data-ttu-id="c0bb2-107">Ottenere un buffer costante in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="c0bb2-107">Get a constant buffer by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0bb2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0bb2-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="c0bb2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0bb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0bb2-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c0bb2-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c0bb2-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0bb2-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c0bb2-112">Indice a base zero.</span><span class="sxs-lookup"><span data-stu-id="c0bb2-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0bb2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0bb2-113">Return value</span></span>

<span data-ttu-id="c0bb2-114">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0bb2-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="c0bb2-115">Puntatore a un [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c0bb2-115">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c0bb2-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0bb2-116">Remarks</span></span>

<span data-ttu-id="c0bb2-117">Un effetto che contiene una variabile che verrà letta/scritta da un'applicazione richiede almeno un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="c0bb2-117">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="c0bb2-118">Per ottenere prestazioni ottimali, un effetto dovrebbe organizzare le variabili in uno o più buffer costanti in base alla relativa frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c0bb2-118">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="c0bb2-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c0bb2-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c0bb2-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c0bb2-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c0bb2-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c0bb2-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0bb2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0bb2-122">Requirements</span></span>



| <span data-ttu-id="c0bb2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0bb2-123">Requirement</span></span> | <span data-ttu-id="c0bb2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c0bb2-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0bb2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0bb2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c0bb2-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0bb2-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c0bb2-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c0bb2-127">Library</span></span><br/> | <dl> <span data-ttu-id="c0bb2-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c0bb2-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0bb2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0bb2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0bb2-130">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="c0bb2-130">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

