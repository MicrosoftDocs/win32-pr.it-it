---
title: Metodo ID3DX11Effect GetConstantBufferByName (D3dx11effect. h)
description: Ottenere un buffer costante in base al nome.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Metodo GetConstantBufferByName Direct3D 11
- Metodo GetConstantBufferByName Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetConstantBufferByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886314"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a><span data-ttu-id="3bd44-106">Metodo ID3DX11Effect:: GetConstantBufferByName</span><span class="sxs-lookup"><span data-stu-id="3bd44-106">ID3DX11Effect::GetConstantBufferByName method</span></span>

<span data-ttu-id="3bd44-107">Ottenere un buffer costante in base al nome.</span><span class="sxs-lookup"><span data-stu-id="3bd44-107">Get a constant buffer by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd44-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3bd44-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="3bd44-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3bd44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd44-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="3bd44-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="3bd44-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3bd44-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3bd44-112">Nome del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="3bd44-112">The constant-buffer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd44-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3bd44-113">Return value</span></span>

<span data-ttu-id="3bd44-114">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3bd44-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="3bd44-115">Puntatore al buffer costante indicato dal nome.</span><span class="sxs-lookup"><span data-stu-id="3bd44-115">A pointer to the constant buffer indicated by the Name.</span></span> <span data-ttu-id="3bd44-116">Vedere [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3bd44-116">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd44-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bd44-117">Remarks</span></span>

<span data-ttu-id="3bd44-118">Un effetto che contiene una variabile che verrà letta/scritta da un'applicazione richiede almeno un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="3bd44-118">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="3bd44-119">Per ottenere prestazioni ottimali, un effetto dovrebbe organizzare le variabili in uno o più buffer costanti in base alla relativa frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3bd44-119">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="3bd44-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="3bd44-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3bd44-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3bd44-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3bd44-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3bd44-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3bd44-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bd44-123">Requirements</span></span>



| <span data-ttu-id="3bd44-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bd44-124">Requirement</span></span> | <span data-ttu-id="3bd44-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3bd44-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd44-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3bd44-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3bd44-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bd44-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3bd44-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="3bd44-128">Library</span></span><br/> | <dl> <span data-ttu-id="3bd44-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="3bd44-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bd44-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bd44-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd44-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="3bd44-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

