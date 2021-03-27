---
title: Metodo ID3DX11EffectVectorVariable SetIntVector (D3dx11effect. h)
description: Impostare un vettore a quattro componenti contenente dati Integer.
ms.assetid: d0546da4-c3b4-4e97-9aa9-d3b7022e22c5
keywords:
- Metodo SetIntVector Direct3D 11
- Metodo SetIntVector Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- Interfaccia ID3DX11EffectVectorVariable Direct3D 11, metodo SetIntVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6141185459dbe7aad494312210b4517fe4f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235031"
---
# <a name="id3dx11effectvectorvariablesetintvector-method"></a><span data-ttu-id="60082-106">Metodo ID3DX11EffectVectorVariable:: SetIntVector</span><span class="sxs-lookup"><span data-stu-id="60082-106">ID3DX11EffectVectorVariable::SetIntVector method</span></span>

<span data-ttu-id="60082-107">Impostare un vettore a quattro componenti contenente dati Integer.</span><span class="sxs-lookup"><span data-stu-id="60082-107">Set a four-component vector that contains integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="60082-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60082-108">Syntax</span></span>


```C++
HRESULT SetIntVector(
   int *pData
);
```



## <a name="parameters"></a><span data-ttu-id="60082-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="60082-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60082-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="60082-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="60082-111">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="60082-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="60082-112">Puntatore al primo componente.</span><span class="sxs-lookup"><span data-stu-id="60082-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60082-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60082-113">Return value</span></span>

<span data-ttu-id="60082-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60082-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60082-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="60082-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="60082-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="60082-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="60082-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="60082-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="60082-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="60082-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="60082-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="60082-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60082-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60082-120">Requirements</span></span>



| <span data-ttu-id="60082-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="60082-121">Requirement</span></span> | <span data-ttu-id="60082-122">Valore</span><span class="sxs-lookup"><span data-stu-id="60082-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60082-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60082-123">Header</span></span><br/>  | <dl> <span data-ttu-id="60082-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="60082-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="60082-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="60082-125">Library</span></span><br/> | <dl> <span data-ttu-id="60082-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="60082-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60082-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60082-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60082-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="60082-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

